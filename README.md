# zod-course-summary

1️⃣ مقدمة

Zod هي مكتبة TypeScript للتحقق من صحة البيانات (schema validation) بطريقة قوية وسهلة.
تستخدم لإنشاء schemas تحدد شكل البيانات وقواعدها، ومفيدة جدًا في مشاريع Node.js، Next.js، أو أي مشروع TypeScript.


```ts
import { z } from "zod";

const userSchema = z.object({
  name: z.string(),
  age: z.number().min(0),
});
