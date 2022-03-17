<script>
  import { fly } from "svelte/transition";
  import { onMount } from "svelte";

  let show = false;

  onMount(() => {
    show = true;
  });

  const twitterURL = "https://twitter.com/hammad2506";
  const linkedInURL = "https://www.linkedin.com/in/hammad-balkhi-629088b6/";
  const mediumURL = "https://medium.com/@hammad2506";
</script>

{#if show}
  <main in:fly={{ y: 200, duration: 500 }}>
    <p class="title">hello i'm Hammad 👋</p>
    <p>developer 💻. web3 🌐. crypto 🪙. fitness 🏋. sports ⚽. CompSci @ YorkU.</p>
    <div class="contact-card">
      <div class="pic">
        <img src="me.png" alt="My Pic" />
      </div>
      <div class="contact-info">
        <a href={twitterURL} target="_blank" class="link-item">💬 DM on Twitter</a>
        <a href={linkedInURL} target="_blank" class="link-item">🤝 Connect on LinkedIn</a>
        <a href={mediumURL} target="_blank" class="link-item">📖 Follow on Medium</a>
      </div>
    </div>
    <p style="font-size: 14px; text-align: center">"The urgency of today. The consistency of tomorrow. The patience of a dacade-long time horizion."</p>
    <div class="bio">
      <p class="subtitle">More <span style="font-size: 0.8em; margin-left: 6px"> 👤</span></p>
      <p>• Developer Full-Time (Web2 + Web3) 🌐</p>
      <p>• Focus on Data Viz 📊</p>
      <p>• Aspiring Indie Hacker ⚡️</p>
      <p>• Senior Software Developer @ GEOTAB 💻</p>
    </div>
    <div class="other">
      <p class="subtitle">Recommended readings <span style="font-size: 0.8em; margin-left: 6px"> 📘</span></p>
      <li><a href="https://fs.blog/the-buffett-formula/" target="_blank">The Buffet Formula</a></li>
      <li><a href="https://jamesclear.com/first-principles" target="_blank">First Principles</a></li>
      <li><a href="https://fs.blog/mental-models/" target="_blank">Mental Models (Charlie Munger's interdisciplinary thinking)</a></li>
    </div>
  </main>
{/if}

<style lang="scss">
  :global(body) {
    background: snow;
  }

  main {
    color: #101011;
    padding: 0 1em;
    max-width: 680px;
    margin: 0 auto;
  }

  .title {
    font-size: 2.8em;
    font-weight: 500;
    margin-bottom: 0;
  }

  .subtitle {
    font-size: 2em;
    font-weight: 500;
    margin-bottom: 0;
  }

  .contact-card {
    display: flex;
    margin: 2em 0;

    .pic {
      flex-grow: 0;
      width: 180px;
      height: 180px;
      border-radius: 50%;
      margin-right: 24px;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 50%;
      }
    }

    .contact-info {
      flex-grow: 1;
      display: flex;
      flex-direction: column;
    }
  }

  .bio {
    margin: 1em 0;

    p {
      margin: 6px 0;

      &:first-child {
        margin-bottom: 0.4em;
      }
    }
  }

  .other {
    margin: 1em 0;

    p {
      margin-bottom: 0.4em;
    }

    li {
      margin: 6px 0;
    }
  }

  .link-item {
    padding: 0.6em;
    margin: 4px 0;
    background: #f3f5f8;
    color: skyblue;
    font-weight: 500;
    font-size: 1.2em;

    &:hover {
      color: rgb(46, 160, 206);
    }
  }
</style>
