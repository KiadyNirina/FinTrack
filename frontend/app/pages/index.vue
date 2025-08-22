<template>
    <div class="min-h-screen bg-gray-50">
      <!-- Navbar -->
      <UHeader
        :links="[
          { label: 'Accueil', to: '/' },
          { label: 'Fonctionnalités', to: '#features' },
          { label: 'À propos', to: '#about' }
        ]"
        :logo="{ alt: 'FinTrack', class: 'text-2xl font-bold text-emerald-600' }"
      >
        <template #right>
          <UButton label="Connexion" to="/login" variant="ghost" />
          <UButton label="Essayer gratuitement" to="/register" color="emerald" />
        </template>
      </UHeader>
  
      <!-- Hero Section -->
      <section class="container mx-auto px-6 py-16 text-center">
        <h1 class="text-4xl md:text-6xl font-extrabold text-gray-800 mb-6">
          Prends le contrôle de <span class="text-emerald-600">tes finances</span>
        </h1>
        <p class="text-xl text-gray-600 mb-10 max-w-3xl mx-auto">
          FinTrack t’aide à suivre tes revenus, dépenses et budgets en toute simplicité. 
          Pas de banque, pas de paperasse — juste une vision claire de ta santé financière.
        </p>
        <div class="flex flex-col sm:flex-row justify-center gap-4">
          <UButton
            label="Créer un compte gratuit"
            size="xl"
            color="emerald"
            to="/register"
            class="px-8"
          />
          <UButton
            label="Voir une démo"
            size="xl"
            variant="ghost"
            color="gray"
            @click="alert('Bientôt disponible !')"
          />
        </div>
      </section>
  
      <!-- Features -->
      <section id="features" class="bg-white py-20">
        <div class="container mx-auto px-6">
          <h2 class="text-3xl font-bold text-center text-gray-800 mb-12">
            Fonctionnalités clés
          </h2>
          <div class="grid md:grid-cols-3 gap-10">
            <UCard>
              <template #header>
                <UIcon name="i-heroicons-currency-dollar" class="text-4xl text-emerald-500 mb-4" />
                <h3 class="text-xl font-semibold">Suivi des dépenses</h3>
              </template>
              <p class="text-gray-600">
                Enregistre tes achats, catégorise-les automatiquement et visualise où part ton argent.
              </p>
            </UCard>
  
            <UCard>
              <template #header>
                <UIcon name="i-heroicons-chart-bar" class="text-4xl text-emerald-500 mb-4" />
                <h3 class="text-xl font-semibold">Tableau de bord intelligent</h3>
              </template>
              <p class="text-gray-600">
                Graphiques clairs, résumés mensuels et alertes quand tu dépasses ton budget.
              </p>
            </UCard>
  
            <UCard>
              <template #header>
                <UIcon name="i-heroicons-lock-closed" class="text-4xl text-emerald-500 mb-4" />
                <h3 class="text-xl font-semibold">Sécurisé & Privé</h3>
              </template>
              <p class="text-gray-600">
                Tes données sont chiffrées et stockées dans Supabase. Tu restes seul maître de ton compte.
              </p>
            </UCard>
          </div>
        </div>
      </section>
  
      <!-- CTA Section -->
      <section id="about" class="bg-emerald-600 text-white py-20">
        <div class="container mx-auto px-6 text-center">
          <h2 class="text-3xl md:text-4xl font-bold mb-6">
            Prêt à transformer ta relation avec l’argent ?
          </h2>
          <p class="text-xl mb-10 opacity-90">
            Rejoins des milliers d'utilisateurs qui ont déjà repris le contrôle de leurs finances.
          </p>
          <UButton
            label="Commence maintenant — Gratuit à vie"
            size="xl"
            color="white"
            to="/register"
            class="px-10"
          />
        </div>
      </section>
  
      <!-- Footer -->
      <footer class="bg-gray-800 text-gray-300 py-12">
        <div class="container mx-auto px-6 text-center">
          <div class="flex justify-center mb-4">
            <UIcon name="i-logos-nuxt-icon" class="text-3xl" />
            <span class="ml-2 text-xl font-bold text-white">FinTrack</span>
          </div>
          <p class="mb-4">© 2025 FinTrack. Tous droits réservés.</p>
          <p class="text-sm">Construit avec ❤️ et Nuxt 4.</p>
        </div>
      </footer>
    </div>
</template>
  
<script setup>
  useHead({
    title: 'FinTrack – Gère tes finances simplement',
    meta: [
      { name: 'description', content: 'Application de suivi financier simple et puissante, basée sur Nuxt et Supabase.' }
    ]
  })
</script>
  
<style>
  .page-enter-active, .page-leave-active {
    transition: all 0.3s;
  }
  .page-enter-from, .page-leave-to {
    opacity: 0;
    transform: translateY(10px);
  }
</style>