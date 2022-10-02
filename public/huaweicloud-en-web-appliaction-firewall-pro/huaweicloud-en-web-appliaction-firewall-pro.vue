<div class="bg-white shadow overflow-hidden sm:rounded-lg">
  <div class="px-4 py-5 sm:px-6">
    <h3 class="text-lg leading-6 font-medium text-gray-900">{{title}}</h3>
    <p class="mt-1 max-w-2xl text-sm text-gray-500">{{description}}</p>
  </div>
  <div class="border-t border-gray-200">
    <dl  v-for="item in list" :key="item.title">
      <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
          <dt class="text-sm font-medium text-gray-500">Provider</dt>
          <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">{{item.provider}}</dd>
        </div>
      <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-500">Service Name</dt>
        <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2"> {{item.name}}</dd>
      </div>
      <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-500">Region</dt>
        <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">{{item.region}}</dd>
      </div>
      <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-500">Edition</dt>
        <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">{{item.edition}}</dd>
      </div>
      <div class="bg-white px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-500">Price</dt>
     
        <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
        <ul role="list" class="border border-gray-200 rounded-md divide-y divide-gray-200" :key="i.month">
            <li class="pl-3 pr-4 py-3 flex items-center justify-between text-sm">
              <div class="w-0 flex-1 flex items-center">
                <span class="ml-2 flex-1 w-0 truncate"> {{item.price.month}} / Monthly </span>
              </div>
            </li>
            <li class="pl-3 pr-4 py-3 flex items-center justify-between text-sm">
              <div class="w-0 flex-1 flex items-center">
                <span class="ml-2 flex-1 w-0 truncate">  {{item.price.year}} / Yearly </span>
              </div>
            </li>
          </ul>
        </dd>
      </div>
      <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-500">Billing Mode</dt>
        <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">Yearly/Monthly</dd>
      </div>
      <div class="bg-white  px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-500">Features</dt>
        <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
          {{ item.features }}
        </dd>
      </div>
      <div class="bg-gray-50 px-4 py-5 sm:grid sm:grid-cols-3 sm:gap-4 sm:px-6">
        <dt class="text-sm font-medium text-gray-500">wiki URL</dt>
        <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:col-span-2">
          <ul role="list" class="border border-gray-200 rounded-md divide-y divide-gray-200">
            <li class="pl-3 pr-4 py-3 flex items-center justify-between text-sm">
              <div class="w-0 flex-1 flex items-center">
                <span class="ml-2 flex-1 w-0 truncate"> English </span>
              </div>
              <div class="ml-4 flex-shrink-0">
                <a :href="item.wiki.english" class="font-medium text-indigo-600 hover:text-indigo-500"> Link </a>
              </div>
            </li>
            <li class="pl-3 pr-4 py-3 flex items-center justify-between text-sm">
              <div class="w-0 flex-1 flex items-center">
                <span class="ml-2 flex-1 w-0 truncate"> Chinese </span>
              </div>
              <div class="ml-4 flex-shrink-0">
                <a :href="item.wiki.chinese" class="font-medium text-indigo-600 hover:text-indigo-500"> Link </a>
              </div>
            </li>
          </ul>
        </dd>
      </div>
    </dl>
  </div>
</div>