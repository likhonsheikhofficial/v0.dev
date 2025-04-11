# v0.dev

<div align="center">
  <img src="https://registry.npmmirror.com/@lobehub/icons-static-png/1.44.0/files/dark/v0.png" alt="v0.dev Logo" width="180" />
  <h3>AI-powered web application development</h3>
  <p>Build stunning web applications with the power of AI</p>
  
  <div>
    <a href="https://v0.dev">Try v0.dev</a> •
    <a href="#features">Features</a> •
    <a href="#how-it-works">How It Works</a> •
    <a href="#getting-started">Getting Started</a> •
    <a href="#examples">Examples</a>
  </div>
</div>

<br />

## 🌟 Highlight: Use v0 System Prompts with Any AI Model

**Get the full v0 system prompts directly from our repository!**

You can now use the same system prompts that power v0.dev with any compatible AI model. This allows you to experiment with v0-like capabilities in your preferred environment:

```bash
# Direct link to v0 system prompts
https://raw.githubusercontent.com/likhonsheikhofficial/v0.dev/refs/heads/main/System/Prompts/v0.txt
```

### Example Usage with Different Models

#### Python (Together API)
```python
from together import Together

# Initialize the client
client = Together()

# Get v0 system prompt
import requests
v0_prompt = requests.get("https://raw.githubusercontent.com/likhonsheikhofficial/v0.dev/refs/heads/main/System/Prompts/v0.txt").text

# Create completion with v0 system prompt
response = client.chat.completions.create(
    model="deepseek-ai/DeepSeek-R1-Distill-Llama-70B-free",
    messages=[
        {"role": "system", "content": v0_prompt},
        {"role": "user", "content": "Create a simple product card with an image, title, price, and add to cart button"}
    ]
)
print(response.choices[0].message.content)
```

#### TypeScript (OpenAI API)
```typescript
import { OpenAI } from 'openai';
import fetch from 'node-fetch';

async function generateUIWithV0Prompt() {
  // Initialize the client
  const openai = new OpenAI({
    apiKey: process.env.OPENAI_API_KEY,
  });

  // Get v0 system prompt
  const response = await fetch('https://raw.githubusercontent.com/likhonsheikhofficial/v0.dev/refs/heads/main/System/Prompts/v0.txt');
  const v0Prompt = await response.text();

  // Create completion with v0 system prompt
  const completion = await openai.chat.completions.create({
    model: "gpt-4",
    messages: [
      { role: "system", content: v0Prompt },
      { role: "user", content: "Create a login form with email and password fields" }
    ],
  });

  console.log(completion.choices[0].message.content);
}

generateUIWithV0Prompt();
```

#### cURL
```bash
# First, save the v0 prompt to a file
curl -s https://raw.githubusercontent.com/likhonsheikhofficial/v0.dev/refs/heads/main/System/Prompts/v0.txt > v0_prompt.txt

# Then use it in your API call
curl https://api.together.xyz/v1/chat/completions \
  -H "Authorization: Bearer $TOGETHER_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "mistralai/Mixtral-8x7B-Instruct-v0.1",
    "messages": [
      {"role": "system", "content": "'$(cat v0_prompt.txt)'"},
      {"role": "user", "content": "Design a simple navigation bar with logo, links, and dark mode toggle"}
    ]
  }'
```

Simply copy the contents from the link above and use it as a system prompt with your favorite AI model to unlock similar web development capabilities!

## What is v0.dev?

v0 by Vercel is a generative AI tool that revolutionizes web development by transforming natural language descriptions and design mockups into production-ready code. Whether you're a seasoned developer or just getting started, v0.dev helps you build beautiful, responsive, and functional web applications with ease.

![v0.dev CRM Example](assets/Simple-CRM-with-React-v0-by-Vercel-11-23-2024_01_53_PM-1536x747.png)

## Features

- 🚀 **Text-to-App Generation** - Describe your app in plain language and get code instantly
- 🎨 **Design-to-Code** - Upload mockups and designs and convert them to working code
- 🧩 **Framework Support** - Works with React, Vue, Svelte, and HTML with CSS
- 📱 **Responsive Design** - All generated designs work seamlessly across devices
- 🔄 **Figma Integration** - Seamless workflow between design and development
- ⚡ **Rapid Prototyping** - Quickly iterate on ideas and bring them to life

## How It Works

v0.dev utilizes a chat-based interface similar to ChatGPT, making it intuitive and easy to use:

1. **Describe or Upload** - Explain what you want to build or upload a design mockup
2. **Generate Options** - The AI engine creates initial versions of your application
3. **Customize** - Refine the output using natural language instructions
4. **Export Code** - Get clean, production-ready code to integrate into your project

![v0.dev Workflow](assets/Page-design-from-file-v0-by-Vercel-1024x576.gif)

## Getting Started

```bash
# No installation needed!
# Just visit v0.dev to get started
```

Visit [v0.dev](https://v0.dev) and start building with AI right away! No complex setup required.

## Tips for Effective Use

- **Start Simple**: Begin with basic components before attempting complex designs
- **Be Specific**: Provide clear, detailed descriptions for better results
- **Iterate**: Use feedback cycles to refine your generated designs
- **Combine Components**: Build complex applications by combining simpler components

## Examples

Here are some examples of what you can build with v0.dev:

- E-commerce product pages
- Admin dashboards
- Landing pages
- Contact forms
- Data visualization interfaces
- And much more!

## Modes

v0.dev supports both light and dark themes for your development experience:

<div align="center">
  <img src="assets/ent-light-small.avif" alt="Light Mode" width="400" />
  <img src="assets/ent-dark-small.avif" alt="Dark Mode" width="400" />
</div>

## Community

Have questions or want to share your creations? Join our community:

- Open an [issue](https://github.com/likhonsheikhofficial/v0.dev/issues) for questions
- Check out community examples in the [examples folder](https://github.com/likhonsheikhofficial/v0.dev/tree/main/examples)
- Follow [Guillermo Rauch](https://twitter.com/rauchg) for updates

## Limitations

While v0.dev is powerful, it's important to be aware of its limitations:

- Complex interactions may require manual refinement
- Generated code might need optimization for production use
- Accessibility compliance should be verified manually

## License

This repository contains v0.dev examples and documentation. Refer to [Vercel's terms](https://vercel.com/terms) for actual v0.dev usage terms.

---

<div align="center">
  <p>Created with ❤️ by the community</p>
  <p>
    <a href="https://twitter.com/vercel">Twitter</a> •
    <a href="https://vercel.com/blog">Blog</a> •
    <a href="https://vercel.com">Vercel</a>
  </p>
</div>
