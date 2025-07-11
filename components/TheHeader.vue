<template>
	<header class="sticky top-0 z-50 bg-white/75 dark:bg-gray-900/75 backdrop-blur-lg shadow-sm">
		<UContainer>
			<div class="flex items-center justify-between h-16">
				<div class="flex items-center space-x-4">
					<NuxtLink to="/" class="text-xl font-bold"> Advokat </NuxtLink>
					<p class="hidden md:block text-sm text-gray-500">
						Юридическая поддержка с 2014 года
					</p>
				</div>

				<nav class="hidden lg:flex items-center space-x-6">
					<ULink
						to="/services"
						class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-primary"
						>Услуги</ULink
					>
					<ULink
						to="/about"
						class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-primary"
						>О компании</ULink
					>
					<ULink
						to="/cases"
						class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-primary"
						>Кейсы</ULink
					>
					<ULink
						to="/blog"
						class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-primary"
						>Блог</ULink
					>
					<ULink
						to="/contacts"
						class="text-sm font-medium text-gray-700 dark:text-gray-300 hover:text-primary"
						>Контакты</ULink
					>
				</nav>

				<div class="flex items-center space-x-4">
					<a
						href="tel:+74951234567"
						class="hidden sm:flex items-center space-x-2 text-sm font-semibold"
					>
						<UIcon name="i-heroicons-phone" class="w-5 h-5" />
						<span>+7 (495) 123-45-67</span>
					</a>
					<UButton color="primary" variant="solid">Бесплатная консультация</UButton>
					<ClientOnly>
						<ColorModeButton />
					</ClientOnly>
				</div>
			</div>
		</UContainer>
	</header>
</template>

<script setup lang="ts">
// This component follows the structure defined in the project rules.
// It includes a logo, slogan, navigation, contact info, and a primary CTA.
// The header is sticky for better user experience.
</script>
