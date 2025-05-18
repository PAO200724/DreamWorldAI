# Prisma 设置

## 安装 Prisma

```bash
yarn add prisma --dev
```

## 初始化 Prisma

```bash
npx prisma init
```

## 连接数据库

```bash
npx prisma migrate dev
```

## 运行 Prisma Client

```bash
npx prisma generate
```

## 示例代码

```typescript
import { PrismaClient } from '@prisma/client';

const prisma = new PrismaClient();

async function main() {
  const users = await prisma.user.findMany();
  console.log(users);
}

main();