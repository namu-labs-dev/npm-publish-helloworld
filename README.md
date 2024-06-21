# npm 배포 helloworld

* build 

```bash
# npm run clean                  dist 경로 삭제
# npm run build:generate-types   tsc를 이용하여 index.d.ts 생성(emitDeclarationOnly 옵션이 활성화되어 있어 .d.ts 파일만 생성된다.)
# npm run build:js               src/index.ts를 기준으로 js, cjs 생성
$ npm run build
```

* npm publish

publish 하기전에 package.json에서 version을 올렸는지 확인할 것

```bash
$ publish:npm
```

### usage

* install

```bash
$ npm i @namulabsdev/helloworld 
```

* test.js

```javascript
const {a, b} = require('@namulabsdev/helloworld');

a(1234)
b(1234)
```

```bash
$ node test.js
```

* test.mjs

```javascript
import { a, b } from '@namulabsdev/helloworld';

a(1234)
b(1234)
```

```bash
$ node test.mjs
```

* test.cjs

```javascript
const {a, b} = require('@namulabsdev/helloworld');

a(1234)
b(1234)
```

```bash
$ node test.cjs
```

* test.ts

```typescript
import { a, b } from '@namulabsdev/helloworld';

a(12345)
b(12345)
```

```bash
$ ts-node test.ts
```