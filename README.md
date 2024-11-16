# monorepo-template

I have several React+Next.js projects; I have some code that I’d like to share among these projects. For example, I bought a website template, which I’d like to reuse across different websites. Also, I have some util functions (such as Google Analytics tracking) that I’d like to reuse.

This article shows the minimum setup to meet the requirements above. https://monorepo.tools/ unfortunately does not meet what I need because it assumes that people want the heavy duty distributed solution. But I don’t want that; I just want to reuse code locally.

## Deploy locally

```
git clone git@github.com:junhe/monorepo-template.git
cd monorepo-template/packages/project1
npm install
npm run dev
```

Open http://localhost:3000/. You should see the following, which are code and image from shared/.

![image](https://github.com/user-attachments/assets/df9ee1c5-4ee6-4a45-a13d-d641e20f6c56)


## Deploy to Vercel
Go to https://vercel.com/, follow the usual steps to deploy. Everything should be straightforward; but make sure the settings are as follows. Root directory should be `packages/project1`.

![image](https://github.com/user-attachments/assets/ba612ba7-9439-4374-9b5e-1051414a4b72)

https://everything-is-an-experiment.com/2024/11/personal-monorepo-setup-with-vercel/ has a bit more info.

