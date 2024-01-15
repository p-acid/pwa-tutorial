# `next-pwa` 라이브러리와 함께하는 설정

1. 라이브러리 설치

```sh
yarn add next-pwa
```

2. `next.config.js` 수정

```js
const withPWA = require("next-pwa")({
  dest: "public",
});

/** @type {import('next').NextConfig} */
const nextConfig = {
  // next.js config
};

module.exports = withPWA(nextConfig);
```

> 린트 에러가 발생하는 경우 `.eslintrc.json` 파일 수정 필요
>
> ```json
> // .eslintrc.json
> {
>   "extends": ["next/babel", "next/core-web-vitals"]
> }
> ```

3. Manifest 및 아이콘 파일 추가

> - [PWA Manifest Generator](https://www.simicart.com/manifest-generator.html/)
> - [PWA Icon Generator](https://tools.crawlink.com/tools/pwa-icon-generator/)

- `app` 디렉토리 루트에 저장 `manifest.json` 파일 추가

4.
