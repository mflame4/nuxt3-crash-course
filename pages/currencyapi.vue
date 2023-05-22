<template>
  <div>
    <h2>Currency Conversion API</h2>
    <p>
      The perfect tool to handle your exchange rate conversions. Our API helps
      you with current and historical foreign exchanges rates. Stop worrying
      about uptime & outdated data.
    </p>
    <div class="max-w-2xl mx-auto">
      <div class="flex flex-col">
        <div class="overflow-x-auto shadow-md sm:rounded-lg">
          <div class="inline-block min-w-full align-middle">
            <div class="overflow-hidden">
              <table
                class="min-w-full divide-y divide-gray-200 table-fixed dark:divide-gray-700"
              >
                <thead class="bg-gray-100 dark:bg-gray-700">
                  <tr>
                    <th scope="col" class="p-4"></th>
                    <th
                      scope="col"
                      class="py-3 px-6 text-xs font-medium tracking-wider text-left text-gray-700 uppercase dark:text-gray-400"
                    >
                      Currency Name
                    </th>
                    <th
                      scope="col"
                      class="py-3 px-6 text-xs font-medium tracking-wider text-left text-gray-700 uppercase dark:text-gray-400"
                    >
                      Currency Symbol
                    </th>
                    <th
                      scope="col"
                      class="py-3 px-6 text-xs font-medium tracking-wider text-left text-gray-700 uppercase dark:text-gray-400"
                    >
                      Currency Code
                    </th>
                  </tr>
                </thead>
                <tbody
                  class="bg-white divide-y divide-gray-200 dark:bg-gray-800 dark:divide-gray-700"
                >
                  <tr
                    class="hover:bg-gray-100 dark:hover:bg-gray-700"
                    v-for="currency in currencies"
                    :key="currency.symbol"
                  >
                    <td class="p-4 w-4"></td>
                    <td
                      class="py-4 px-6 text-sm font-medium text-gray-900 whitespace-nowrap dark:text-white"
                    >
                      {{ currency.name }}
                    </td>
                    <td
                      class="py-4 px-6 text-sm font-medium text-gray-500 whitespace-nowrap dark:text-white"
                    >
                      {{ currency.symbol }}
                    </td>
                    <td
                      class="py-4 px-6 text-sm font-medium text-gray-900 whitespace-nowrap dark:text-white"
                    >
                      {{ currency.code }}
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
h2 {
  margin-bottom: 20px;
  font-size: 36px;
}
p {
  margin: 20px 0;
}
</style>

<script setup>
const { data } = await useFetch(
  "/api/currency/UAH%2CEUR%2CGBP%2CCAD%2CJPY%2CUSD%2CAUD"
);
const currencies = data;
</script>
