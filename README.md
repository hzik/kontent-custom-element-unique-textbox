# Unique textbox

This custom element check whether your entered value is unique across all items in your project in specified element:

![Screenshot of custom element](UniqueTextbox.gif)

## Configuration

```json
{
    "codename": "unique_element",
    "request_repeater": "https://x2jp66x1y92.execute-api.eu-central-1.amazonaws.com/default/requestRepeater"
}
```

You need to specify both `codename` parameter for the element code name you want to check for unique values and you need to link your repeater in the `request_repeater` parameter.

To set up `request_repeater` above, please follow [Working with sensitive data in custom elements](https://docs.kontent.ai/tutorials/develop-apps/integrate/working-with-sensitive-data-in-custom-elements).
In **Step 2: Configuring your Lambda function**, use the following keys and values in the **Environment variables** section:
  - `BEARER_TOKEN`: `<Preview Delivery API key>`
  - `HOST`: `preview-delivery.kontent.ai`
  - `PATH`: `/<Project ID>/items`


## Setup

1. Deploy the code to a secure public host
    * See [deploying section](#Deploying) for a really quick option
1. Follow the instructions in the [Kentico Kontent documentation](https://docs.kontent.ai/tutorials/develop-apps/integrate/integrating-your-own-content-editing-features#a-3--displaying-a-custom-element-in-kentico-kontent) to add the element to a content model.
    * The `Hosted code URL` is where you deployed to in step 1
    * Pass the necessary parameters as directing in the [JSON Parameters configuration](#json-parameters) section of this readme.

## Deploying

Netlify has made this easy. If you click the deploy button below, it will guide you through the process of deploying it to Netlify and leave you with a copy of the repository in your GitHub account as well.

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/hzik/kontent-custom-element-unique-textbox)


