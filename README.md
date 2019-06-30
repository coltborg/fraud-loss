# 💳 fraud-loss

## 🤔 Thought process

Using [Vue.js CLI](https://cli.vuejs.org/) is the best way to get a Vue.js app up and running.

I enjoy using [Tailwind CSS](https://tailwindcss.com/) for application development—especially prototyping—because I can make small adjustments while in development and then using templates and components to replicate patterns easily as needed.

I have heard good things about [ChartJS](https://www.chartjs.org/) in the past. It's not as robust as something like [D3](https://d3js.org/), but it has enough options and uses canvas well.

One disappointing choice I made was to use the Vue.js wrapper for chartJS, [vue-chartjs](https://vue-chartjs.org/). It doesn't give you enough control over the canvas or even access to the `ctx` from the chart. It was a good lesson to learn, it was quick to get a chart up and running, but difficult to make fine tuned adjustments.

## 🚀 Deployment

I have this git repo on Github, which [Netlify](https://www.netlify.com/) can have access to and will deploy the `built` app on to a custom domain any time a new commit is pushed to the `master` branch of the repo.

## 🔧 Project setup

Install project dependencies

```
npm install
```

Compiles and hot-reloads for development

```
npm run serve
```

Compiles and minifies for production (this is the command used by Netlify)

```
npm run build
```

Lints and fixes files

```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
