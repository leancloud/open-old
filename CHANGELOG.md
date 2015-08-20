<a name="0.0.1"></a>
## 0.0.1 (2015-08-20)


### Bug Fixes

* `last_modified_at` not format correctly ([8e94869](https://github.com/leancloud/open/commit/8e94869))
* add base path ([5d4adc3](https://github.com/leancloud/open/commit/5d4adc3))
* **authors:** wrong default author name ([420dc64](https://github.com/leancloud/open/commit/420dc64))
* **grunt:** `grunt-html-smoosher` cannot be installed ([36e6318](https://github.com/leancloud/open/commit/36e6318))
* **package:** missing deps ([3831133](https://github.com/leancloud/open/commit/3831133))
* **post:** blockquote ([17cc298](https://github.com/leancloud/open/commit/17cc298))
* **post:** correct times symbol ([87ca1b9](https://github.com/leancloud/open/commit/87ca1b9))
* **post:** many typography fixes for post "余光中：怎样改进英式中文？——论中文的常态与变态" ([90a1777](https://github.com/leancloud/open/commit/90a1777))
* **script:** wrong GA code ([c1138bd](https://github.com/leancloud/open/commit/c1138bd))
* **style:** avoid _italic_ ([a95575a](https://github.com/leancloud/open/commit/a95575a))
* **style:** fix `text-align: justified;` for posts in Chinese ([b0334c8](https://github.com/leancloud/open/commit/b0334c8))
* **style:** reset header text align for justified text ([0721af5](https://github.com/leancloud/open/commit/0721af5))
* **style:** title hyphens fix ([00f2973](https://github.com/leancloud/open/commit/00f2973))
* **style:** wrong heading padding fix ([399d99a](https://github.com/leancloud/open/commit/399d99a))
* **tempalte:** wrong Twitter user handle for Twitter Cards ([83d83ff](https://github.com/leancloud/open/commit/83d83ff))
* **template:** apply markdownify for post description ([0e2c847](https://github.com/leancloud/open/commit/0e2c847))
* **template:** avoid “layout not found” error introduced since Jekyll 2.2.0 ([5a3b6be](https://github.com/leancloud/open/commit/5a3b6be))
* **template:** correct error page title ([93c212d](https://github.com/leancloud/open/commit/93c212d))
* **travis:** build error ([14338d8](https://github.com/leancloud/open/commit/14338d8))
* cht -> chs ([06da656](https://github.com/leancloud/open/commit/06da656))
* ci error ([b682143](https://github.com/leancloud/open/commit/b682143))
* **travis:** celluloid release was pulled (yanked) ([eaee434](https://github.com/leancloud/open/commit/eaee434))

### Features

* **template:** /avoscloud.com/leancloud.cn/ ([e624189](https://github.com/leancloud/open/commit/e624189))
* basic file structure ([02726fd](https://github.com/leancloud/open/commit/02726fd))
* thinner footer ([c9704ca](https://github.com/leancloud/open/commit/c9704ca))
* **docs:** update guide ([c39b94b](https://github.com/leancloud/open/commit/c39b94b))
* boost Jekyll performance up to 30%, yay. ([7ab9d1e](https://github.com/leancloud/open/commit/7ab9d1e))
* more string replaced ([8cf0779](https://github.com/leancloud/open/commit/8cf0779))
* smaller base font size ([757b831](https://github.com/leancloud/open/commit/757b831))
* update `favicon.ico` ([9181a0c](https://github.com/leancloud/open/commit/9181a0c))
* **style:** heading tweaks ([e4bd678](https://github.com/leancloud/open/commit/e4bd678))
* update to latest AMSF ([ed60121](https://github.com/leancloud/open/commit/ed60121))
* **grunt:** simplify banner ([8d9f345](https://github.com/leancloud/open/commit/8d9f345))
* **post:** add modified date ([bf56df9](https://github.com/leancloud/open/commit/bf56df9))
* **post:** update company name guide ([c26cd45](https://github.com/leancloud/open/commit/c26cd45))
* **script:** vanity variables ([b2ac56b](https://github.com/leancloud/open/commit/b2ac56b))
* **style:** dynamic text color for `code` and `pre` ([1e15e6b](https://github.com/leancloud/open/commit/1e15e6b))
* **template:** /AVOS Cloud/LeanCloud/, /avoscloud/leancloud/ ([3fa0817](https://github.com/leancloud/open/commit/3fa0817))
* **template:** add `lang` YAML front-matter data ([de37618](https://github.com/leancloud/open/commit/de37618))
* **template:** enable alternative title size ([3cfc365](https://github.com/leancloud/open/commit/3cfc365))
* **template:** hide placeholder posts from Atom feed ([56cf51f](https://github.com/leancloud/open/commit/56cf51f))
* **template:** remove `amsf` option, add `clean_homepage` and `credits` options ([ac07b75](https://github.com/leancloud/open/commit/ac07b75))
* **theme:** update template for new AMSF structure ([b0529ee](https://github.com/leancloud/open/commit/b0529ee))


### BREAKING CHANGES

* Now you can define `lang` tag for your post, simply add `lang` to your post front-matter data, for example:
```
lang: ar
```
then define your own styles in `custom.less`:
```css
[lang=ar] {
direction: rtl;
}
```
* Please note that templates should be updated for new options


