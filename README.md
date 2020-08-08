# gas-clasp-starter

[howdy39](https://github.com/howdy39) さん作成の Google Apps Script by [google/clasp](https://github.com/google/clasp) スターターテンプレートを自分用に fork したものです。
GitHub Actions 対応にしようかと思い fork しましたが、過剰かな？って感じなんで、当面このまま使用します。
対応させる場合は、[momumomu/clasp_ci_sample](https://github.com/momumomu/clasp_ci_sample) を参考にすると良さげ。

## howdy39 さんの記事

+ [(Japanese) Google Apps Script をローカル環境で快適に開発するためのテンプレートを作りました](https://qiita.com/howdy39/items/0e799a9bfc1d3bccf6e5)
+ [Google Apps Script のデプロイを Circle CI から行う](https://qiita.com/howdy39/items/2c21251331e011d04512)

## momumomu さんの記事

[Google Apps Script(GAS)をclasp&GitHub Actionsでお手軽CI管理する](https://undersooon.hatenablog.com/entry/2019/12/25/200636)

## Tech Stack

- [google/clasp](https://github.com/google/clasp)
- [webpack](https://webpack.js.org/)
- [TypeScript](http://www.typescriptlang.org/)
- [ESLint](https://github.com/eslint/eslint)
- [Prettier](https://prettier.io/)
- [Jest](https://facebook.github.io/jest/)

## Prerequisites

- [Node.js](https://nodejs.org/)
- [google/clasp](https://github.com/google/clasp)

## Getting Started

### Clone the repository

```bash
git clone --depth=1 https://github.com/tyamadadd/gas-clasp-starter.git <project_name>
cd <project_name>
rm -Rf .git
```

windows の場合、最後のディレクトリ削除は、適当に読み換えてください。

### Install dependencies

```bash
npm install
```

初回、メモリ不足で実行できませんでした。
不足した場合、端末を再起動後、再度試行してみてください。

### VScode 利用の場合

[EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig) を利用すると、エディタの設定をそのまま利用できます。

### Configuration

#### Open `.clasp.json`, change scriptId

What is scriptId ? <https://github.com/google/clasp#scriptid-required>

```json
{
  "scriptId": <your_script_id>,
  "rootDir": "dist"
}
```

#### Open `src/appsscript.json`, change timeZone (optional)

[Apps Script Manifests](https://developers.google.com/apps-script/concepts/manifests)

```json
{
  "timeZone": "Asia/Tokyo", ## Change timeZone
  "dependencies": {
  },
  "exceptionLogging": "STACKDRIVER"
}
```

### Development and build project

```bash
npm run build
```

### Push

```bash
clasp push
```

## Advanced

### Using Es6 with Apps Script

[Using Es6 with Apps Script](http://ramblings.mcpher.com/Home/excelquirks/gassnips/es6shim)

## Others

### howdy39/gas-clasp-library

[howdy39/gas-clasp-library](https://github.com/howdy39/gas-clasp-library) is sample project made with [Google Apps Script Libraries](https://developers.google.com/apps-script/guides/libraries).  
also, `gas-clasp-library` use circle CI.

### takanakahiko/sao-clasp

[takanakahiko/sao-clasp](https://github.com/takanakahiko/sao-clasp) was made based on gas-clasp-starter and [SAO](https://github.com/saojs/sao).

## License

This software is released under the MIT License, see LICENSE.txt.
