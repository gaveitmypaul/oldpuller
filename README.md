# oldpuller
banking transferhoyyea
const request: LinkTokenCreateRequest = {
  user: {
    client_user_id: 'user-id',
  },
  client_name: 'Plaid Test App',
  products: [Products.Auth, Products.Transactions],
  country_codes: [Products.Gb],
  language: 'en',
  webhook: 'https://sample-web-hook.com',
  account_filters: {
    depository: {
      account_subtypes: ['checking', 'savings'],
    },
  },
};
try {
  const response = await plaidClient.linkTokenCreate(request);
  const linkToken = response.data.link_token;
} catch (error) {
  // handle error
}
