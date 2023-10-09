# @codegenius/verify-plugin

校验 `COMMIT_EDITMSG` 中的信息是否符合 **Angualr** 规范, 支持命令模式和 **API** 模式;

使用场景: 用于校验正在执行 `git commit` 时所提交的信息是否符合规范.

## 安装

``` bash
npm i @codegenius/verify-plugin -D
```

```javascript
import { defineConfig } from "code-genius";
import { gitCommitVerifyInstaller } from "@codegenius/verify-plugin";

export default defineConfig({
  plugins: [
    gitCommitVerifyInstaller(),
  ],
});
```

## 使用

### 命令模式

```bash
codeg verify
```

### API 模式

```typescript
import { gitCommitVerify } from "@codegenius/verify-plugin";

(async () => {
  await gitCommitVerify();
  console.log("Git 提交信息校验通过, 正在执行后续逻辑...");
})();
```
