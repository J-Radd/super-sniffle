# super-sniffle
{
  "id": "card_9CUH5DBY1jTgQ0",
  "object": "card",
  ...
  "account": "acct_1032D82eZvKYlo2C",
  "available_payout_methods": ["standard", "instant"],
}
const stripe = require('stripe')('sk_test_51HmuxwJtofXoPBKRajCQr5ivlqKmbMz5uDKBWXXyRQl27rsr2zbEdAkJgVt1VVBbI80gT4ir68E7dcsvchVOqPJE00zubKlhIv');

const payout = await stripe.payouts.create({
  amount: 1000,
  currency: 'cad',
  method: 'instant',
}, {
  stripeAccount: '{{CONNECTED_STRIPE_ACCOUNT_ID}}',
});
