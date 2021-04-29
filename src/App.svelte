<script>
  import HeadingText from "./HeadingText.svelte";
  import ProjectCard from "./ProjectCard.svelte";

  let values = [
    {
      src: "/dating-smartphone-man.svg",
      alt: "Smarphone man icon",
      title: 'Modern & <span class="italic">User-Friendly</span>',
      description: `Membangun aplikasi dengan mengikuti teknik <span class="italic">software development</span> terbaru untuk mengoptimalkan pengalaman pengguna.`,
    },
    {
      src: "/laptop-smiley-1.svg",
      alt: "Laptop smiley icon",
      title: '<span class="italic">Highly Customizable</span>',
      description: `Merancang aplikasi khusus sesuai dengan kebutuhan klien.`,
    },
  ];

  let projects = [
    {
      name: "You NU",
      src: "/younu-feature-graphic.png",
      description: `<span class="font-bold text-green-700">You NU</span> adalah aplikasi
              Android milik koperasi Muslimat NU yang melayani transaksi jual beli online anggota
              koperasi di Jawa Timur dan pengelolaan aktivitas koperasi lainnya.`,
      href:
        "https://play.google.com/store/apps/details?id=com.komplit.ecomm.jatim",
    },
    {
      name: "Koins",
      src: "/koins-feature-graphic.png",
      description: `<span class="font-bold text-green-700">Koins</span> adalah aplikasi 
              pengelolaan berita dan simpanan anggota koperasi Koins.`,
    },
  ];
  let otherProjectsCount = 4;

  let tools = [
    {
      name: "Laravel",
      src: "/icon-laravel.svg",
    },
    {
      name: "CodeIgniter",
      src: "/icon-codeigniter.svg",
    },
    {
      name: "Android",
      src: "/icon-android.svg",
    },
    {
      name: "Flutter",
      src: "/icon-flutter.svg",
    },
    {
      name: "React.JS",
      src: "/icon-react.svg",
    },
    {
      name: "Firebase",
      src: "/icon-firebase.svg",
    },
    {
      name: "Express.JS",
      src: "/icon-express.svg",
    },
    {
      name: "Mongo DB",
      src: "/icon-mongodb.svg",
    },
    {
      name: "MySQL",
      src: "/icon-mysql.svg",
    },
    {
      name: "Jenkins",
      src: "/icon-jenkins.svg",
    },
    {
      name: "Docker",
      src: "/icon-docker.svg",
    },
    {
      name: "Digital Ocean",
      src: "/icon-digitalocean.svg",
    },
  ];
  let tools1 = [...tools].splice(0, 6);
  let tools2 = [...tools].splice(6);
</script>

<main>
  <div class="pb-24 pt-24">
    <div class="flex justify-center">
      <img class="w-36 h-36" alt="KomplitApp" src="komplit-logo.png" />
    </div>
    <h1 class="text-5xl text-purple-800 font-thin text-center mb-12">
      KomplitApp
    </h1>
    <HeadingText title="Tentang Kami" />
    <div class="max-w-md mx-auto">
      <p class="text-sm mb-24 text-center">
        <span class="text-purple-800">KomplitApp</span> adalah tim pengembang
        perangkat lunak (<span class="italic">software</span>) yang
        mengembangkan berbagai aplikasi untuk Komunitas, Perusahaan, Lembaga dan
        Institusi. Kami berpengalaman membangun aplikasi berbasis Android dan
        web sejak tahun 2019.
      </p>
    </div>

    <div class="bg-purple-500 pt-12 pb-12 mb-12">
      <HeadingText title={'<span class="italic">Value</span> Kami'} isPrimary />
      <div class="grid grid-cols-2 mt-8">
        {#each values as { src, alt, title, description }}
          <div class="flex flex-col items-center">
            <img
              {src}
              {alt}
              class="w-24 h-24 mb-4 transform transition-transform hover:rotate-12"
            />
            <p class="text-md text-center text-black font-medium tracking-wide">
              {@html title}
            </p>
            <p
              class="text-sm text-center text-gray-800 mt-2 tracking-wide font-light"
            >
              {@html description}
            </p>
          </div>
        {/each}
      </div>
    </div>

    <HeadingText title="Portofolio Kami" />
    <div class="pl-12 pr-12 grid md:grid-cols-3 sm:grid-cols-2 gap-1 mb-24">
      {#each projects as { name, src, description, href }}
        <ProjectCard {name} {src} {description} {href} />
      {/each}
      <div
        class="rounded-xl flex flex-col hover:shadow-lg shadow-none bg-purple-200"
      >
        <div class="p-6 flex flex-grow flex-col justify-center items-center">
          <p class="text-6xl">+{otherProjectsCount}</p>
          <p class="text-sm">proyek lainnya yang bersifat privat</p>
        </div>
      </div>
    </div>

    <HeadingText title={'<span class="italic">Tools</span> Kami'} />
    <div class="grid grid-cols-12 mb-24 mt-8">
      <div />
      <div />
      <div />
      {#each tools1 as { name, src }}
        <div class="flex flex-col items-center has-tooltip">
          <img class="w-12 h-12" alt={`${name}`} {src} />
          <span
            class="tooltip rounded shadow-lg p-1 bg-purple-500 text-white text-xs -mt-8"
            >{name}</span
          >
        </div>
      {/each}
    </div>
    <div class="grid grid-cols-12 mb-24 mt-4">
      <div />
      <div />
      <div />
      {#each tools2 as { name, src }}
        <div class="flex flex-col items-center has-tooltip">
          <img class="w-12 h-12" alt={`${name}`} {src} />
          <span
            class="tooltip rounded shadow-lg p-1 bg-purple-500 text-white text-xs -mt-8"
            >{name}</span
          >
        </div>
      {/each}
    </div>

    <div class="pr-12">
      <p class="text-xs text-right">© 2021 KomplitApp</p>
      <p class="text-xs text-right">
        Wonderful icons by <a href="https://streamlineicons.com" target="_blank"
          >Streamline</a
        >
        and <a href="https://devicon.dev/" target="_blank">Devicon</a>
      </p>
    </div>
  </div>
</main>

<style>
  .tooltip {
    visibility: hidden;
    position: absolute;
  }
  .has-tooltip:hover .tooltip {
    visibility: visible;
    z-index: 100;
  }

  ::-moz-selection {
    /* Code for Firefox */
    /* purple-800 */
    color: #5c21b6;
    /* purple-200 */
    background: #ddd6fe;
  }

  ::selection {
    color: #5c21b6;
    background: #ddd6fe;
  }
</style>
