---
layout: page
---

<script setup>
import {
  VPTeamPage,
  VPTeamPageTitle,
  VPTeamMembers,
  VPTeamPageSection
} from 'vitepress/theme'


const sponsors = [
  {
    avatar: '../images/sponsors/hetzner.webp',
    name: 'Hetzner',
    title: 'Server, cloud, hosting, and data center solutions',
    links: [
      { icon: 'expedia', link: 'http://htznr.li/CoolifyXHetzner' }
    ]
  },
  {
    avatar: '../images/sponsors/logto.webp',
    name: 'Logto',
    title: 'The better identity infrastructure for developers',
    links: [
      { icon: 'expedia', link: 'https://logto.io/?ref=coolify' }
    ]
  },
  {
    avatar: '../images/sponsors/tolgee.webp',
    name: 'Tolgee',
    title: 'The open source localization platform',
    links: [
      { icon: 'expedia', link: 'https://tolgee.io/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/bc.webp',
    name: 'Best Consultant',
    title: 'Your trusted technology consulting partner',
    links: [
      { icon: 'expedia', link: 'https://bc.direct/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/quant.webp',
    name: 'QuantCDN',
    title: 'Enterprise-grade content delivery network',
    links: [
      { icon: 'expedia', link: 'https://www.quantcdn.io/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/arcjet.webp',
    name: 'Arcjet',
    title: 'Advanced web security and performance solutions',
    links: [
      { icon: 'expedia', link: 'https://arcjet.com/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/supaguide.webp',
    name: 'SupaGuide',
    title: 'Your comprehensive guide to Supabase',
    links: [
      { icon: 'expedia', link: 'https://supa.guide/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/stream.webp',
    name: 'Stream',
    title: 'APIs and SDKs to Build In-App Chat, Video, & Feeds Faster.',
    links: [
      { icon: 'expedia', link: 'https://getstream.io/?utm_source=opensource&utm_medium=referral&utm_content=&utm_campaign=coolifyq12025' }
    ]
  },
  {
    avatar: '../images/sponsors/goldenvm.webp',
    name: 'GoldenVM',
    title: 'Premium virtual machine hosting solutions',
    links: [
      { icon: 'expedia', link: 'https://billing.goldenvm.com/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/tigris.webp',
    name: 'Tigris',
    title: 'Modern developer data platform',
    links: [
      { icon: 'expedia', link: 'https://www.tigrisdata.com/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/cloudify.webp',
    name: 'Cloudify',
    title: 'Cloud hosting solutions',
    links: [
      { icon: 'expedia', link: 'https://cloudify.ro/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/trieve.webp',
    name: 'Trieve',
    title: 'AI-powered search and analytics',
    links: [
      { icon: 'expedia', link: 'https://trieve.ai/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/blacksmith.webp',
    name: 'Blacksmith',
    title: 'Infrastructure automation platform',
    links: [
      { icon: 'expedia', link: 'https://blacksmith.sh/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/comit.webp',
    name: 'Comit International',
    title: 'New York Times award–winning contractor!',
    links: [
      { icon: 'expedia', link: 'https://comit.international/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/branddev.webp',
    name: 'Brand.dev',
    title: 'The #1 Brand API for B2B software startups',
    links: [
      { icon: 'expedia', link: 'https://brand.dev/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/syntax.webp',
    name: 'Syntax.fm',
    title: 'Podcast for web developers',
    links: [
      { icon: 'expedia', link: 'https://syntax.fm?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/jobscollider.webp',
    name: 'Jobs Collider',
    title: '30,000+ remote jobs for developers',
    links: [
      { icon: 'expedia', link: 'https://jobscollider.com/remote-jobs?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/hostinger.webp',
    name: 'Hostinger',
    title: 'Web hosting and VPS solutions',
    links: [
      { icon: 'expedia', link: 'https://www.hostinger.com/vps/coolify-hosting?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/glueops.webp',
    name: 'GlueOps',
    title: 'DevOps automation and infrastructure management',
    links: [
      { icon: 'expedia', link: 'https://www.glueops.dev/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/ubicloud.webp',
    name: 'Ubicloud',
    title: 'Open source cloud infrastructure platform',
    links: [
      { icon: 'expedia', link: 'https://www.ubicloud.com/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/pfglabs.webp',
    name: 'Pfglabs',
    title: 'Build Real Projects with Golang',
    links: [
      { icon: 'expedia', link: 'https://pfglabs.com/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/juxtdigital.webp',
    name: 'JuxtDigital',
    title: 'Digital transformation and web solutions',
    links: [
      { icon: 'expedia', link: 'https://juxtdigital.com/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/saasykit.webp',
    name: 'SaasyKit',
    title: 'Complete SaaS starter kit for developers',
    links: [
      { icon: 'expedia', link: 'https://saasykit.com/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/massivegrid.webp',
    name: 'MassiveGrid',
    title: 'Enterprise cloud hosting solutions',
    links: [
      { icon: 'expedia', link: 'https://massivegrid.com/?ref=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/americancloud.webp',
    name: 'American Cloud',
    title: 'US-based cloud infrastructure services',
    links: [
      { icon: 'expedia', link: 'https://americancloud.com/?utm_source=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/algora.webp',
    name: 'Algora',
    title: 'Open source contribution platform',
    links: [
      { icon: 'expedia', link: 'https://algora.io/?utm_source=coolify.io' }
    ]
  },
  {
    avatar: '../images/sponsors/liquidweb.webp',
    name: 'LiquidWeb',
    title: 'Premium managed hosting solutions',
    links: [
      { icon: 'expedia', link: 'https://liquidweb.com/?utm_source=coolify.io' }
    ]
  },
  {
    avatar: '../images/team/coollabs.webp',
    name: 'You Company?',
    title: 'Will Your Company Be Next?'
  }
]
</script>

<VPTeamPage>
  <VPTeamPageTitle>
    <template #title>
      Coolify Sponsors
    </template>
    <template #lead>
      We have amazing sponsors who support the development of Coolify.
    </template>
  </VPTeamPageTitle>
<VPTeamMembers size="small" :members="sponsors" />
</VPTeamPage>
