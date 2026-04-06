# Zod Course Summary

## جدول المحتويات
1. [مقدمة](#مقدمة)
2. [تثبيت المكتبة](#تثبيت-المكتبة)
3. [إنشاء Schema](#إنشاء-schema)
4. [التحقق من البيانات](#التحقق-من-البيانات)
5. [أنواع متقدمة](#أنواع-متقدمة)
    - [Array](#array)
    - [Enum](#enum)
    - [Optional & Nullable](#optional--nullable)
    - [Union](#union)
    - [Preprocess](#preprocess)
6. [نصائح مهمة](#نصائح-مهمة)
7. [روابط مفيدة](#روابط-مفيدة)


## مقدمة
**Zod** هي مكتبة TypeScript للتحقق من صحة البيانات (schema validation) بطريقة قوية وسهلة.  
تستخدم لإنشاء **schemas** تحدد شكل البيانات وقواعدها، ومفيدة جدًا في مشاريع **Node.js** و **Next.js**.


## تثبيت المكتبة
```bash
npm install zod
# أو
yarn add zod


## إنشاء Schema
```ts
import { z } from "zod";

const userSchema = z.object({
  name: z.string(),
  age: z.number().min(0),
  email: z.string().email(),
});
