<script setup lang="ts">
import KExperienceItem from "~/components/KExperienceItem.vue";


const items = [{
  link: 'https://www.tennisbear.net/bear/board-game',
  title: 'ボドゲベア',
  date: '2024 ー 現在',
  skills: ['HTML', 'CSS', 'Javascript', 'Vue.js', 'Nuxt', 'Kotlin', 'Spring Boot', 'PostgreSQL', 'Node.js', 'Puppeteer(スクレイピング)', 'AWS'],
  texts: [
    'Vue.jsおよびNuxt.jsを使用してWebサイトを構築し、サーバーサイドにはKotlinを用いたSpring Bootフレームワークを採用しています。ボードゲームイベントの管理をよりスムーズに行えるよう、直感的なUI/UXの提供を目指して開発を進めています。',
    'ユーザー体験を最適化するために、ユーザーインタビューを実施し、デザイナーとの密接な連携を図りながら、実際に自らイベントのホストや参加者として関わることで、ユーザー目線に立った改善を日々行っています。このアプローチにより、継続的なフィードバックを反映し、使いやすさと機能性の向上に努めています。'
  ]
}, {
  link: 'https://www.tennisbear.net',
  title: 'テニスベア',
  date: '2020 ー 2024',
  skills: ['HTML', 'CSS', 'Javascript', 'Vue.js', 'Nuxt', 'Kotlin', 'Spring Boot', 'PostgreSQL', 'Node.js', 'Puppeteer(スクレイピング)', 'AWS', 'Flutter', 'Dart', 'Stripe'],
  texts: [
    '基本的には「ボドゲベア」と同様の開発環境で構築を行っています。また、「テニスベア」ではiOSおよびAndroid向けのアプリ開発も手がけており、クロスプラットフォームでのユーザー体験を最適化するための技術的な対応を進めています。'
  ]
}, {
  link: null,
  title: 'ソフトバンク株式会社 - 社内ナレッジ検索システム',
  date: '2017 ー 2020',
  skills: ['HTML', 'CSS', 'Javascript', 'JQuery', 'Java', 'Spring Boot', 'MySQL', 'Elasticsearch', 'Solr', 'Linux'],
  texts: [
    '社内ナレッジ検索システムの開発に従事していました。Javaを用いたSpring Bootフレームワークを採用し、MySQLをデータベースとして使用していました。また、検索エンジンにはElasticsearchおよびSolrを採用し、大量のデータを高速に検索できるように設計していました。',
    'また、社内の情報共有を目的としたシステムであるため、セキュリティにも配慮し、アクセス権限の設定やログの記録など、セキュリティに関する機能の実装も行っていました。'
  ]
},{
  link: 'https://www.ricoh.co.jp/sales/about',
  title: 'リコージャパン株式会社 - 営業職',
  date: '2014 ー 2017',
  skills: ['営業', '提案', '交渉', '顧客対応'],
  texts: [
    'リコージャパン株式会社にて、法人向けの営業職として勤務していました。主にオフィス機器の提案営業を行っており、顧客との信頼関係を築くことを重視していました。',
    'また、リコージャパン株式会社では、新規顧客の開拓や既存顧客のフォローアップなど、幅広い業務を経験し、営業スキルを磨くことができました。'
  ]
}]
</script>

<template>
  <div class="text-gray-300">
    <h2 class="text-3xl flex items-center px-8 py-4">
      <UIcon name="i-ic-baseline-work-history" class="text-cyan-500 mr-2"/>
      <span>これまでの経歴</span>
    </h2>
    <KExperienceItem v-for="item in items" :title="item.title" :date="item.date" :skills="item.skills"
                     :texts="item.texts" :link="item.link" class="py-4 px-8"/>
  </div>
</template>