<template>
  <footer class="footer d-flex justify-content-between mt-auto py-2 px-3 bg-light user-select-none">
    <div class="footer-copyrights text-muted my-auto d-none d-lg-block col-4">
      {{ $t("footer.trademark") }}<br />
      {{ $t("footer.copyright") }}
    </div>
    <div class="flex-fill text-center text-muted">
      <img src="../assets/brand.png" alt="XIV ToDo branding" />
      <br />
      <router-link to="/">
        <small>{{ $t("page.about") }}</small>
      </router-link>
      ·
      <router-link to="/help">
        <small>{{ $t("page.help") }}</small>
      </router-link>
      ·
      <router-link to="/privacy">
        <small>{{ $t("page.privacy") }}</small>
      </router-link>
      ·
      <a href="https://forms.gle/2t5nLB28xDyi3Tn6A" target="_blank" rel="noopener noreferrer">
        <small>{{ $t("page.contact") }}</small>
      </a>
      ·
      <a href="https://github.com/bourgeoisor/xivtodo" target="_blank" rel="noopener noreferrer">
        <small>{{ $t("page.github") }}</small>
      </a>
      ·
      <a href="https://twitter.com/XIVToDo" target="_blank" rel="noopener noreferrer">
        <small>{{ $t("page.twitter") }}</small>
      </a>
      <br />
      <a href="https://ko-fi.com/olivi_eh" target="_blank" rel="noopener noreferrer">
        <small>{{ $t("page.donate") }} <i class="bi bi-balloon-heart"></i></small>
      </a>
    </div>
    <div class="footer-copyrights text-muted text-end my-auto d-none d-lg-block col-4">
      {{ $t("footer.buildVersion", { buildNum: buildNum }) }}<br />
      {{ $t("footer.buildDate", { buildDate: buildDate }) }}
    </div>
  </footer>
</template>

<style lang="scss">
footer {
  a,
  a:focus {
    color: #6c757d;
  }

  a:hover {
    color: #222222;
  }
}

.night footer {
  background-color: #212529 !important;
  border-top: 1px solid #333333;

  a,
  a:focus {
    color: #6c757d;
  }

  a:hover {
    color: #eeeeee;
  }
}

.footer-copyrights {
  font-size: 0.6rem;
}

footer a {
  text-decoration: none;
}

footer img {
  height: 22px;
  margin-bottom: 5px;
  margin-top: 5px;
  filter: brightness(70%) grayscale(100%);
  -webkit-filter: brightness(70%) grayscale(100%);
}

footer img:hover {
  filter: brightness(100%) grayscale(0%);
  -webkit-filter: brightness(100%) grayscale(0%);
}
</style>

<script>
export default {
  Name: "TheFooter",
  data() {
    return {
      buildNum: process.env.VUE_APP_BUILD_NUM,
      buildDate: process.env.VUE_APP_BUILD_DATE,
    };
  },
};
</script>
