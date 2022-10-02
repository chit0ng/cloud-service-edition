  <div class="px-4 sm:px-6 lg:px-8 bg-slate-100" as="template">
      <div class="sm:flex sm:items-center">
  <div class="sm:flex-auto">
    <h1 class="text-xl font-semibold text-gray-900">{{title}}</h1>
    <p class="mt-2 text-sm text-gray-700">
      {{ description }}
    </p>
  </div>
    </div>
    <div class="mt-2 flex flex-col">
      <div class="-my-2 -mx-4 overflow-x-auto sm:-mx-6 lg:-mx-8">
        <div class="inline-block min-w-full py-2 align-middle md:px-6 lg:px-8">
          <table class="min-w-full divide-y divide-gray-300">
            <thead>
              <tr>
                <th scope="col" class="py-3.5 pl-4 pr-3 text-left text-sm font-semibold text-gray-900 sm:pl-6 md:pl-0">
                  SeverName
                </th>
                <th scope="col" class="py-3.5 px-3 text-left text-sm font-semibold text-gray-900">IP Address</th>
                <th scope="col" class="py-3.5 px-3 text-left text-sm font-semibold text-gray-900">Status</th>
                <th scope="col" class="py-3.5 px-3 text-left text-sm font-semibold text-gray-900">Provider</th>
              </tr>
            </thead>
            <tbody class="divide-y divide-gray-200">
              <tr v-for="item in list" :key="item.servername">
                <td class="whitespace-nowrap py-4 pl-4 pr-3 text-sm font-medium text-gray-900 sm:pl-6 md:pl-0">
                  {{
                    item.servername
                  }}
                </td>
                <td class="whitespace-nowrap py-4 px-3 text-sm text-gray-500">{{ item.ipaddress }}</td>
                <td class="whitespace-nowrap py-4 px-3 text-sm text-gray-500">{{ item.status }}</td>
                <td class="whitespace-nowrap py-4 px-3 text-sm text-gray-500">{{ item.provider }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
