<template>
  <main>
    <!--
    <section v-if="posts" class="w-full max-w-5xl mx-auto">
      <h1 class="title">integration</h1>
      <posts post-type="integration" :amount="100" />
    </section>
    -->
    <section class="integration-main-section main-section">
      <div class="container">
        <div class="row h100 justify-content-center align-items-center">
          <div class="col-md-12" data-aos="fade-up">
            <img src="assets/img/main-integration.svg" />
            <div class="title-block text-center">
              <h1>30+ Integrations for streamlined processes</h1>
              <h4>Integrate DocuX with systems and tools you already use.</h4>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="integration-details my-120">
      <div class="container">
        <div class="row">
          <div class="col-md-3">
            <div class="integration-filter-bar">
              <h3 class="mb-32">
                <a href="javascript:;" data-filter=".item" class="trigger-filter unique">All integrations</a>
              </h3>
              <h3 class="mb-32"><a href="javascript:;" data-filter=".premium" class="trigger-filter">Premium</a></h3>
              <h3>For Teams</h3>
              <ul>
                <li><a href="javascript:;" data-filter=".sales" class="trigger-filter">Sales teams</a></li>
                <li><a href="javascript:;" data-filter=".marketing" class="trigger-filter">Marketing teams</a></li>
                <li><a href="javascript:;" data-filter=".finance" class="trigger-filter">Finance teams</a></li>
                <li><a href="javascript:;" data-filter=".legal" class="trigger-filter">Legal teams</a></li>
              </ul>
              <h3>Category</h3>
              <ul>
                <li><a href="javascript:;" data-filter=".crm" class="trigger-filter">CRM</a></li>
                <li><a href="javascript:;" data-filter=".storage" class="trigger-filter">Storage</a></li>
                <li><a href="javascript:;" data-filter=".productivity" class="trigger-filter">Productivity</a></li>
                <li><a href="javascript:;" data-filter=".marketing" class="trigger-filter">Marketing</a></li>
                <li><a href="javascript:;" data-filter=".finance" class="trigger-filter">Finance</a></li>
                <li><a href="javascript:;" data-filter=".security" class="trigger-filter">Security</a></li>
              </ul>
              <!-- <a href="javascript:;" data-filter=".item" class="trigger-filter
                        unique">Clear Filter</a> -->
            </div>
          </div>
          <div class="col-md-9">
            <Integrations />
          </div>
        </div>
      </div>
    </section>
    <section class="footer-cta mt-64">
      <div class="container">
        <div class="row justify-content-center align-items-end">
          <div class="col-md-4">
            <img src="assets/img/newsletter.png" class="newsletter-img" data-aos="fade-right" />
          </div>
          <div class="col-md-5" data-aos="fade-left" data-aos-id="super-duper">
            <h2 class="f-36 f-600">Let’s get you started!</h2>
            <form class="cta-form left pb-60">
              <div class="input-group">
                <input type="email" class="cta-email" placeholder="Your email" />
                <button type="submit" class="cta-btn" data-text="Try for FREE"><span>Try for FREE</span></button>
              </div>
              <ul class="benifits">
                <li>&#10003; Instant access</li>
                <li>&#10003; No credit card required</li>
              </ul>
            </form>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, error }) {
    let posts
    try {
      posts = await $content('integration').fetch()
    } catch (e) {
      error({ message: 'Blog posts not found' })
    }
    return { posts }
  },
}
</script>
