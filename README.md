# Ubercart Restrict Purchase

Limits who can buy each Ubercart product, by role. A club can sell some
items to full members only, or a shop can sell trade items to reseller
accounts only, while everyone can still see the product.

- **Per product.** Tick the roles allowed to buy the product on its edit
  form. With no roles ticked, anyone can buy it.
- **A message or a button instead of Add to cart.** Users who cannot buy the
  product see a message ("Only full members can purchase these items."), or
  a button such as "Log in to purchase" with the message below it. The
  button can link to the login page or a join page, and brings the user
  back to the product afterwards.
- **Prices can be hidden too**, on the product page.
- **Really blocks the purchase.** The add to cart itself is refused, so
  catalog buttons, Views "Add to cart" fields and `cart/add` links cannot be
  used to get round the restriction.

## Requirements

- Ubercart: Product (`uc_product`) and Cart (`uc_cart`).

## Installation

1. Install this module using the official Backdrop CMS instructions at
   https://docs.backdropcms.org/documentation/extend-with-modules.
2. Configure the message or button at *Store > Configuration > Products*, on
   the **Restrict purchase** tab.
3. Edit each product and tick the roles that may buy it, under *Product
   information*.

See [MANUAL.md](MANUAL.md) for the settings and their limits.

## Upgrading from Drupal 7

This module replaces Ubercart Price Visibility (`uc_price_visibility`) but
uses a different name and table, and there is no upgrade path: set the roles
on each product again. Note one change in behaviour: in the Drupal 7 module
a product with no roles ticked was hidden from everyone; here it can be
bought by anyone.

## Issues

Bugs and feature requests should be reported in the issue queue:
https://github.com/backdrop-contrib/uc_restrict_purchase/issues

## Security
Reviewed on 3 November 2026 for the kinds of vulnerability reported in the Drupal security advisories of 7 to 28 October 2026. Those advisories were for Drupal 10/11 and do not apply to Backdrop directly; this module was checked for the same classes of mistake.

Please report security issues privately to security@backdropcms.org, not in the issue queue.

## Current Maintainer(s)
- Steve Moorhouse (albanycomputers) (https://github.com/albanycomputers)
- Additional maintainers and contributors welcome.

---

## Credits
- Based on the Drupal 7 module [Ubercart Price Visibility](https://www.drupal.org/project/uc_price_visibility) by joelstein and fizk; its Drupal 7 upgrade was sponsored by Web Design 4 Traffic.
- Ported to Backdrop and extended by Steve Moorhouse - Zulip (DrAlbany)
- Assisted by AI.

- Current development is sponsored by [Albany Computer Services](https://www.albany-computers.co.uk), providers of computer support, [web design](https://www.albanywebdesign.co.uk), and [web hosting](https://www.albany-hosting.co.uk).

## License

This project is GPL v2 software. See the LICENSE.txt file in this directory
for complete text.
