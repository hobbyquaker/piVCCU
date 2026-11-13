# piVCCU drivers for openccu-lite

This is a fork of [Alexander Reinert's piVCCU](https://github.com/alexreinert/piVCCU). Its branch `lite` is what
[openccu-lite](https://github.com/hobbyquaker/openccu-lite) builds its radio module drivers from: the kernel modules in
`kernel/` (such as `generic_raw_uart`, `hb_rf_eth` and `eq3_char_loop`) and `detect_radio_module`. The piVCCU
container itself, its packages and installers are not used.

## Thank you, Alex

Alex's drivers are what connects openccu-lite to its radio modules. He wrote them and has maintained them for years,
together with the HB-RF-ETH, HB-RF-USB and HB-RF-USB-2 boards they support, and OpenCCU (and RaspberryMatic before it)
builds on them as well. Thank you for that work, and for sharing it.

If openccu-lite is useful to you, please consider supporting Alex: [GitHub Sponsors](https://github.com/sponsors/alexreinert),
[Ko-fi](https://ko-fi.com/alexreinert), [PayPal](https://www.paypal.com/donate/?cmd=_s-xclick&hosted_button_id=4PW43VJ2DZ7R2)
or his [Amazon wishlist](https://www.amazon.de/gp/registry/wishlist/3NNUQIQO20AAP/ref=nav_wishlist_lists_1).

## What `lite` carries

The fork is meant to stay as close to Alex's `master` as possible; `lite` is his `master` plus a few commits on top:

- **The changes OpenCCU builds with**, cherry-picked from [OpenCCU/piVCCU](https://github.com/OpenCCU/piVCCU)
  (`git cherry-pick -x`, so each names its source commit): building as a buildroot package, compiler warnings, and the
  `hb_rf_eth` reconnect fixes.
- **Our own fixes**, which are offered to Alex as pull requests and stay here until his `master` has them.

## Comparison with upstream

- [Everything `lite` has on top of Alex's `master`](https://github.com/alexreinert/piVCCU/compare/master...openccu-lite:piVCCU:lite)
- openccu-lite's [daily overview](https://hobbyquaker.github.io/openccu-lite/en.html) also says whether Alex's `master` has
  commits `lite` has not taken yet.

## Branches and tags

| Branch | Holds |
| --- | --- |
| `lite` | what openccu-lite builds (the default branch) |
| `master` | a copy of Alex's `master`, the base for pull requests to him |
| others | the branches of pull requests to Alex's piVCCU |

Every openccu-lite release tags the `lite` commit it was built from with its own version, for example `v2.0.0-beta.3`,
and openccu-lite pins that tag.

## Issues and licence

- Problems with openccu-lite: [openccu-lite's issues](https://github.com/hobbyquaker/openccu-lite/issues). Problems in
  the drivers themselves: [piVCCU's issues](https://github.com/alexreinert/piVCCU/issues).
- The licence is unchanged: see [LICENSE](LICENSE). piVCCU's own documentation is
  [Alex's README](https://github.com/alexreinert/piVCCU/blob/master/README.md).
