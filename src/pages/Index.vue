<template>
  <Layout>
    <div class="hero container-inner mx-auto flex flex-col sm:flex-row justify-between py-16">
      <div class="text-4xl font-bold w-full sm:w-3/5 text-center sm:text-left">
        <div class="leading-tight">Gridsome Auth0 Starter</div>
        <div class="text-green-700 leading-tight">using <a target=_new href="https://auth0.com">Auth0</a> for user authentication</div>
      </div>
      <div class="mt-8 sm:mt-0">
        <g-image src="../../static/auth0.svg" width=200 alt="hero" class="mx-auto sm:mx-0" />
      </div>
    </div> <!-- end hero -->

    <div class="container-inner mx-auto">
      <p class="text-lg sm:text-xl">This Gridsome Auth0 Hubpsot starter is a fork from this <a href="https://github.com/drehimself/gridsome-portfolio-starter">Gridsome Portfolio Starter</a>. Feel free to use it for your own site or projects! Lorem, ipsum dolor sit amet consectetur adipisicing elit. Minima, repellat. Dolores iure, quas perspiciatis rerum quaerat atque eum repellat autem.</p>

      <div class="flex justify-between items-center py-6">
        <div class="w-full sm:w-1/2 px-8 py-8 sm:py-0">
          <g-image src="../../static/mind_map.svg" alt="browser" />
        </div>
        <div class="w-1/2 px-8 hidden sm:flex justify-end">
          <g-image src="../../static/code_review.svg" alt="mobile" />
        </div>
      </div>
    </div>

    <div class="overflow-x-hidden">
      <div class="projects container-inner mx-auto text-xl border-t border-gray-500 border-b py-16 mb-16 relative">
        <h2 class="font-bold mb-6" id="projects">Here are some projects I've worked on:</h2>

        <div class="absolute right-0" style="top: 50px; transform: translate(100%) rotate(180deg)">
          <svg width="170px" height="170px"><use xlink:href="#dots-triangle" /></svg>
        </div>

        <ul class="text-lg sm:text-xl space-y-6">
          <li class="checkmark">
            <div>Project One</div>
            <div class="text-lg text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui ab nam animi iure nemo exercitationem a, eius non culpa itaque!</div>
          </li>
          <li class="checkmark">
            <div>Project Two</div>
            <div class="text-lg text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui ab nam animi iure nemo exercitationem a, eius non culpa itaque!</div>
          </li>
          <li class="checkmark">
            <div>Project Three</div>
            <div class="text-lg text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui ab nam animi iure nemo exercitationem a, eius non culpa itaque!</div>
          </li>
          <li class="checkmark">
            <div>Project Four</div>
            <div class="text-lg text-gray-600">Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui ab nam animi iure nemo exercitationem a, eius non culpa itaque!</div>
          </li>

        </ul>
      </div> <!-- end projects -->
    </div>

    <div class="overflow-x-hidden border-gray-200 border-b">
      <div class="get-to-know-me container-inner mx-auto text-xl pb-16 relative">
        <h2 class="font-bold mb-6" id="about">Get to know me:</h2>

        <div class="absolute left-0" style="top: 50px; transform: translateX(-100%)">
          <svg width="170px" height="170px"><use xlink:href="#dots-triangle" /></svg>
        </div>

        <div class="flex flex-col sm:flex-row justify-between items-center mb-16">
          <div><g-image src="../../static/avatar.jpg" alt="avatar" class="w-32 h-32 rounded-full mb-8 lg:mb-0" /></div>
          <div class="flex-1 text-lg sm:text-xl ml-6">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Eum quae architecto minus molestias iusto ducimus fuga quo quia libero dignissimos, fugiat modi assumenda debitis laboriosam.</div>
        </div>

      </div> <!-- end get-to-know me -->
    </div>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Home'
  }
}
</script>

