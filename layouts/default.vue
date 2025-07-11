<template>
	<div>
		<header class="bg-gray-100 dark:bg-gray-800 shadow-sm">
			<UContainer>
				<div class="flex items-center justify-between h-16">
					<div class="flex items-center">
						<NuxtLink to="/" class="text-xl font-bold"> Advokat </NuxtLink>
					</div>
					<nav class="hidden md:flex items-center space-x-4">
						<NuxtLink
							to="/services"
							class="text-gray-700 dark:text-gray-300 hover:text-primary"
							>Услуги</NuxtLink
						>
						<NuxtLink
							to="/about"
							class="text-gray-700 dark:text-gray-300 hover:text-primary"
							>О компании</NuxtLink
						>
						<NuxtLink
							to="/cases"
							class="text-gray-700 dark:text-gray-300 hover:text-primary"
							>Кейсы</NuxtLink
						>
						<NuxtLink
							to="/blog"
							class="text-gray-700 dark:text-gray-300 hover:text-primary"
							>Блог</NuxtLink
						>
						<NuxtLink
							to="/contacts"
							class="text-gray-700 dark:text-gray-300 hover:text-primary"
							>Контакты</NuxtLink
						>
					</nav>
					<div class="flex items-center">
						<UButton color="primary" variant="solid">Бесплатная консультация</UButton>
					</div>
				</div>
			</UContainer>
		</header>

		<main>
			<UContainer>
				<slot />
			</UContainer>
		</main>

		<footer class="bg-gray-100 dark:bg-gray-800 mt-12">
			<UContainer class="py-8">
				<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
					<div>
						<h3 class="text-lg font-semibold">Advokat</h3>
						<p class="text-sm text-gray-600 dark:text-gray-400 mt-2">
							Ваша надежная юридическая поддержка.
						</p>
					</div>
					<div>
						<h3 class="text-lg font-semibold">Навигация</h3>
						<ul class="mt-4 space-y-2">
							<li>
								<NuxtLink to="/services" class="text-sm hover:text-primary"
									>Услуги</NuxtLink
								>
							</li>
							<li>
								<NuxtLink to="/about" class="text-sm hover:text-primary"
									>О компании</NuxtLink
								>
							</li>
							<li>
								<NuxtLink to="/cases" class="text-sm hover:text-primary"
									>Кейсы</NuxtLink
								>
							</li>
							<li>
								<NuxtLink to="/blog" class="text-sm hover:text-primary"
									>Блог</NuxtLink
								>
							</li>
						</ul>
					</div>
					<div>
						<h3 class="text-lg font-semibold">Контакты</h3>
						<address class="not-italic mt-4 space-y-2 text-sm">
							<p>г. Москва, ул. Примерная, д.1, оф. 101</p>
							<p>
								<a href="tel:+74951234567" class="hover:text-primary"
									>+7 (495) 123-45-67</a
								>
							</p>
							<p>
								<a href="mailto:info@advokat.com" class="hover:text-primary"
									>info@advokat.com</a
								>
							</p>
						</address>
					</div>
				</div>
				<div
					class="mt-8 border-t border-gray-200 dark:border-gray-700 pt-4 text-center text-sm text-gray-500 dark:text-gray-400"
				>
					<p>&copy; {{ new Date().getFullYear() }} Advokat. Все права защищены.</p>
				</div>
			</UContainer>
		</footer>
	</div>
</template>
