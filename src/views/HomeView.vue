<script setup>
import { useRouter } from 'vue-router';
import AppButton from '@/components/ui/AppButton.vue';

const router = useRouter();
</script>

<template>
  <div class="home-page">
    <section class="hero-section">
      <div class="hero-content">
        <span class="hero-badge">WELCOME TO GATHERLY</span>
        <h1 class="hero-title">Discover & Manage Amazing Events Together</h1>
        <p class="hero-description">
          Gatherly adalah platform serba ada untuk menemukan workshop, seminar, meetup, dan kompetisi terbaik. Daftar acara favoritmu atau kelola acaramu sendiri dengan mudah.
        </p>
        <div class="hero-actions">
          <AppButton variant="primary" @click="router.push('/browse/events')">
            Explore Events &rarr;
          </AppButton>
          <AppButton variant="secondary" @click="router.push('/dashboard')">
            Organizer Dashboard
          </AppButton>
        </div>
      </div>
    </section>

    <section class="features-section">
      <div class="feature-card">
        <div class="feature-icon">🔍</div>
        <h3>Cari & Temukan</h3>
        <p>Jelajahi berbagai kategori acara menarik dan amankan kuota kepersertaanmu secara langsung.</p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">🎟️</div>
        <h3>Tiket Digital</h3>
        <p>Akses tanda terima dan tiket digital resmi kapan saja melalui menu riwayat acara kamu.</p>
      </div>

      <div class="feature-card">
        <div class="feature-icon">📊</div>
        <h3>Manajemen Panitia</h3>
        <p>Buat acara baru, pantau kuota pendaftar, dan kelola status publikasi acara dengan cepat.</p>
      </div>
    </section>
  </div>
</template>

<style scoped>
.home-page {
  padding-bottom: var(--space-12, 48px);
}

.hero-section {
  background: var(--bg-light, #fdfdfd);
  border: 1px solid var(--border-color, #e4e4e7);
  border-radius: var(--space-4, 16px);
  padding: var(--space-12, 48px) var(--space-8, 32px);
  text-align: center;
  margin-bottom: var(--space-12, 48px);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.03);
}

.hero-content {
  max-width: 720px;
  margin: 0 auto;
}

.hero-badge {
  display: inline-block;
  background: rgba(102, 68, 255, 0.1);
  color: var(--primary, #6644ff);
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  padding: 6px 16px;
  border-radius: 50px;
  margin-bottom: var(--space-4, 16px);
}

.hero-title {
  font-size: 2.5rem;
  color: var(--text-main, #1c1948);
  margin-bottom: var(--space-4, 16px);
  line-height: 1.25;
}

.hero-description {
  font-size: 1.1rem;
  color: var(--text-muted, #666666);
  line-height: 1.6;
  margin-bottom: var(--space-8, 32px);
}

.hero-actions {
  display: flex;
  justify-content: center;
  gap: var(--space-4, 16px);
  flex-wrap: wrap;
}

.features-section {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: var(--space-6, 24px);
}

.feature-card {
  background: white;
  border: 1px solid var(--border-color, #e4e4e7);
  border-radius: var(--space-4, 16px);
  padding: var(--space-6, 24px);
  text-align: center;
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

.feature-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
}

.feature-icon {
  font-size: 2.5rem;
  margin-bottom: var(--space-3, 12px);
}

.feature-card h3 {
  font-size: 1.25rem;
  color: var(--text-main, #1c1948);
  margin-bottom: var(--space-2, 8px);
}

.feature-card p {
  font-size: 0.95rem;
  color: var(--text-muted, #666666);
  line-height: 1.5;
  margin: 0;
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 1.8rem;
  }
}
</style>