<script>
  import ProjectCard from "./ProjectCard.svelte";
</script>

<main>
  <div class="pl-12 pr-12 pb-24 pt-24">
    <h1 class="text-5xl text-purple-800 font-thin text-center mb-12">
      KomplitApp
    </h1>
    <h2 class="text-xl font-extralight mb-2 text-center">Tentang Kami</h2>
    <div class="max-w-md mx-auto">
      <p class="text-sm mb-24 text-center">
        <span class="text-purple-800">KomplitApp</span> adalah tim pengembang
        perangkat lunak (<span class="italic">software</span>) yang
        mengembangkan berbagai aplikasi untuk Komunitas, Perusahaan, Lembaga dan
        Institusi. Kami berpengalaman membangun aplikasi berbasis Android dan
        web sejak tahun 2019.
      </p>
    </div>

    <h2 class="text-xl font-extralight mb-2 text-center">Value Kami</h2>
    <div class="grid grid-cols-2 mb-24">
      <div class="flex flex-col items-center">
        <img
          src="/dating-smartphone-man.svg"
          alt="Smarphone man icon"
          class="w-24 h-24 mb-4 transform hover:rotate-12"
        />
        <p class="text-md text-center">
          Modern & <span class="italic">User-Friendly</span>
        </p>
        <p class="text-sm text-center text-gray-500">
          Membangun aplikasi dengan mengikuti teknik
          <span class="italic">software development</span>
          terbaru untuk mengoptimalkan pengalaman pengguna.
        </p>
      </div>
      <div class="flex flex-col items-center">
        <img
          src="/laptop-smiley-1.svg"
          alt="Laptop smiley icon"
          class="w-24 h-24 mb-4 transform hover:rotate-12"
        />
        <p class="text-md text-center italic">Highly Customizable</p>
        <p class="text-sm text-center text-gray-500">
          Merancang aplikasi khusus sesuai dengan kebutuhan client.
        </p>
      </div>
    </div>

    <h2 class="text-xl font-extralight mb-2 text-center">Portofolio Kami</h2>
    <div class="grid md:grid-cols-3 sm:grid-cols-2 gap-1 mb-24">
      <ProjectCard
        name="You NU"
        src="/younu-feature-graphic.png"
        description={`<span class="font-bold text-green-700">You NU</span> adalah aplikasi
              Android milik koperasi Muslimat NU yang melayani transaksi jual beli online anggota
              koperasi di Jawa Timur dan pengelolaan aktivitas koperasi lainnya.`}
        href="https://play.google.com/store/apps/details?id=com.komplit.ecommjatim"
      />
      <ProjectCard
        name="Koins"
        src="/younu-feature-graphic.png"
        description={`<span class="font-bold text-green-700">Koins</span> adalah aplikasi 
              pengelolaan berita dan simpanan anggota koperasi .`}
      />
      <div
        class="rounded-xl flex flex-col hover:shadow-lg shadow-none bg-purple-200"
      >
        <div class="p-6 flex flex-grow flex-col justify-center items-center">
          <p class="text-6xl">+4</p>
          <p class="text-md">proyek lainnya yang bersifat privat</p>
        </div>
      </div>
    </div>
    <p class="text-xs text-right">
      Wonderful icons by <a href="https://streamlineicons.com" target="_blank"
        >Streamline</a
      >
    </p>
  </div>
</main>

<style>
  /* h1 {
    color: #8f1d89;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  } */

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
