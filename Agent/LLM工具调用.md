
# Function Calling[[Agent/LLM工具调用|LL]]

## 是什么

Function Calling 本质上是模型与代码之间的**标准化接口**。
它的核心在于利用 **JSON Schema**（特别是 description 字段）让模型理解工具能力。当模型决定调用时，会通过 `finish_reason` 明确告知，并输出标准的 JSON 指令。
这里有个亮点是它支持**并行调用**，能一次性处理多个任务。最后由我的代码去执行真正的业务逻辑，把结果喂给模型，让它完成从‘数据’到‘人话’的翻译。”

## 背景      [[LLM工具调用#Function Calling|Function Caling]]
没有Function Calling前：
- LLM输出随机的自然语言说明我要调用哪个工具，程序只能用if/else来进行模糊匹配。
有了之后：
- LLM通过Function Calling 直接输出结构化的json，程序只需要按格式解析即可。






