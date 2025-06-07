## Изменяемость

Изменяемость — это способность изменить своё значение и поведение.

В RTS существуют несколько разных состояний от полностью не изменяемого до полностью изменяемого. Для реализации этого используются флаги **~** (волнистая линия), **~~** (две волнистые линии) или их отсутсвие, которые указываются после имени структуры при их первом объявлении.

| Category     | Syntax         | Mutability            | Data Type               | Value Assigned | Initialization Behavior                                                          |
|--------------|----------------|-----------------------|-------------------------|----------------|----------------------------------------------------------------------------------|
| **Final**    | a              | 🔶 (Only first value) | ❌ (inferred from value) | ❌              | Type is inferred on first assignment; Value can be assigned once; Becomes const. |
|              | a: UInt        | 🔶 (Only first value) | ✅                       | ❌              | Value is cast to specified type; Value can be assigned once; Becomes const.      |
| **Сonst**    | a = 10         | ❌                     | ❌ (inferred from value) | ✅              | Type is inferred from value; Value and type are fixed.                           |
|              | a: UInt = -10  | ❌                     | ✅                       | ✅              | Value is cast to specified type; Value and type are fixed.                       |
| **Variable** | a~             | 🔶 (Only value)       | ❌ (inferred from value) | ❌              | Type is inferred from value; Value can be changed.                               |
|              | a~: UInt       | 🔶 (Only value)       | ✅                       | ❌              | Value is cast to specified type; Value can be changed.                           |
|              | a~ = 10        | 🔶 (Only value)       | ❌ (inferred from value) | ✅              | Type is inferred from value; Value can be changed.                               |
|              | a~: UInt = 10  | 🔶 (Only value)       | ✅                       | ✅              | Value is cast to specified type; Value can be changed.                           |
| **Dynamic**  | a~~            | ✅ (Type and value)    | ❌ (inferred from value) | ❌              | Type is inferred from value; Both type and value can be changed.                 |
|              | a~~: UInt      | ✅ (Type and value)    | ✅                       | ❌              | Value is cast to specified type; Both type and value can be changed.             |
|              | a~~ = 10       | ✅ (Type and value)    | ❌ (inferred from value) | ✅              | Type is inferred from value; Both type and value can be changed.                 |
|              | a~~: UInt = 10 | ✅ (Type and value)    | ✅                       | ✅              | Value is cast to specified type; Both type and value can be changed.             |