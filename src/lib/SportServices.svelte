<script>
import {services, details} from "$lib/data/sport_services";
</script>
<div class="bg-white">
  <div aria-hidden="true" class="relative">
    <img src="{details.heroimage}" alt="" class="h-96 w-full object-cover object-center">
    <div class="absolute inset-0 bg-gradient-to-t from-white"></div>
  </div>

  <div class="relative mx-auto -mt-12 max-w-7xl px-4 pb-2 sm:px-6 lg:px-8">
    <div class="mx-auto max-w-2xl text-center lg:max-w-4xl">
      <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">{details.head}</h2>
      <p class="mt-4 text-gray-500">{details.subhead}</p>
    </div>
      {#each details.summary as pd }
      <p class="mt-6 text-lg leading-8 text-gray-600">{pd}</p>
      {/each}
    <dl class="hidden mx-auto mt-16 grid max-w-2xl grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 sm:gap-y-16 lg:max-w-none lg:grid-cols-3 lg:gap-x-8">
      {#each details.types as type}
      <div class="border-t border-gray-200 pt-4">
        <dt class="font-medium text-gray-900">{type.head}</dt>
        <dd class=" mt-2 text-sm text-gray-500">{type.detail}</dd>
      </div>
      {/each}
    </dl>
  </div>
</div>
<!-- Feature section -->
<div class="bg-white pb-24">
  <div class="mx-auto max-w-7xl px-6 lg:px-8">
    <div class="hidden mx-auto max-w-2xl sm:text-center">
      <h2 class="text-base font-semibold leading-7 text-indigo-600">{details.head}</h2>
       <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">{details.subhead}</p>
      {#each details.summary as pd }
      <p class="mt-6 text-lg leading-8 text-gray-600">{pd}</p>
      {/each}
    </div>
    <ul class="mx-auto mt-20 grid max-w-2xl grid-cols-1 gap-x-6 gap-y-20 sm:grid-cols-2 lg:max-w-4xl lg:gap-x-8 xl:max-w-none">
    {#each services as service, i}
      <li>
        <img class="aspect-[3/2] w-full rounded-2xl object-cover" src="{service.image}" alt="">
          <h3 class="mt-4 text-lg font-semibold leading-8 tracking-tight text-gray-900">{service.title}</h3>         
          <ul  class="mt-6 space-y-3 text-sm leading-6 text-gray-600">

              {#each service.points as point}
            <li class="flex gap-x-3">
              <svg class="h-6 w-5 flex-none text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                <path fill-rule="evenodd" d="M16.704 4.153a.75.75 0 01.143 1.052l-8 10.5a.75.75 0 01-1.127.075l-4.5-4.5a.75.75 0 011.06-1.06l3.894 3.893 7.48-9.817a.75.75 0 011.05-.143z" clip-rule="evenodd" />
              </svg>
              {point}
            </li>
              {/each}
              </ul>
   
      </li>
    {/each}
    </ul>
  </div>
</div>
