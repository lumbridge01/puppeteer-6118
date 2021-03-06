<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [puppeteer](./puppeteer.md) &gt; [Browser](./puppeteer.browser.md) &gt; [waitForTarget](./puppeteer.browser.waitfortarget.md)

## Browser.waitForTarget() method

Searches for a target in all browser contexts.

<b>Signature:</b>

```typescript
waitForTarget(predicate: (x: Target) => boolean, options?: WaitForTargetOptions): Promise<Target>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  predicate | (x: [Target](./puppeteer.target.md)<!-- -->) =&gt; boolean | A function to be run for every target. |
|  options | [WaitForTargetOptions](./puppeteer.waitfortargetoptions.md) |  |

<b>Returns:</b>

Promise&lt;[Target](./puppeteer.target.md)<!-- -->&gt;

The first target found that matches the `predicate` function.

## Example

An example of finding a target for a page opened via `window.open`<!-- -->:

```js
await page.evaluate(() => window.open('https://www.example.com/'));
const newWindowTarget = await browser.waitForTarget(target => target.url() === 'https://www.example.com/');

```

