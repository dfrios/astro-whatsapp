# Astro WhatsApp

Astro component to show a WhatsApp fixed floating icon in your website.

## ⚡ Instalation
Using `npm`:
```sh
npm install astro-whatsapp
```

Using `yarn`:
```sh
yarn add astro-whatsapp
```

Using `pnpm`:
```sh
pnpm add astro-whatsapp
```

## 💻 How to use it
Keep in mind that WhatsApp can be invoke in 2 different ways. They different URLs with different params and you must choose according to your needs:

### Using api.whatsapp.com
The `astro-whatsapp` component creates a link that fits this format:

```text
https://api.whatsapp.com/send?phone=MOBILE_NUMBER&text=MESSAGE
```

This is how you can use `astro-whatsapp`:

```html
<WhatsApp useApi={true}, mobile={123456789}, message="Message to send", classNames="" />
```

### Using wa.me
The `astro-whatsapp` component creates a link that fits this format:

```text
https://wa.me/MOBILE_NUMBER
```

This is how you can use `astro-whatsapp`:

```html
<WhatsApp useApi={false}, mobile={123456789}, classNames="" />
```

⚠️ Notice that you cannot attach any messages using wa.me

## 🧱 Parameters

| Name | Type | Mandatory | Description |
| ---- | :--: | :-------: | ----------- |
| useApi | boolean | Yes | Use it to choose the type of output URL. |
| mobile | number | Yes | The WhatsApp number to which the message will be sent. It must include the international prefix number, but never spaces or symbols like + - (). That's why this parameter is a number instead of a string. |
| message | string | No | The message will be sent.<br />If you set `useApi={true}`, `message` parameter is optional.<br />If you set `useApi={false}` **you cannot** use the `message` parameter |
| className | string | No | You can add your own classnames at the beginning of the component |