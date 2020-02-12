# Unique textbox

This is a [custom element](https://docs.kontent.ai/tutorials/develop-apps/integrate/integrating-your-own-content-editing-features) for [Kentico Kontent](https://kontent.ai) that allows you toensure that the entered value is unique across all instances of the element.

![Screenshot of custom element](UniqueTextbox.gif)

## Setup

1. Deploy the code to a secure public host
    * See [deploying section](#Deploying) for a really quick option
1. Follow the instructions in the [Kentico Kontent documentation](https://docs.kontent.ai/tutorials/develop-apps/integrate/integrating-your-own-content-editing-features#a-3--displaying-a-custom-element-in-kentico-kontent) to add the element to a content model.
    * The `Hosted code URL` is where you deployed to in step 1
    * Pass the necessary parameters as directing in the [JSON Parameters configuration](#json-parameters) section of this readme.

## Deploying

Netlify has made this easy. If you click the deploy button below, it will guide you through the process of deploying it to Netlify and leave you with a copy of the repository in your GitHub account as well.

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/hzik/kontent-custom-element-unique-textbox)

## JSON Parameters

The `codename` should be set to the codename of the custom element. If you use the same codename across multiple content types, it will ensure uniqueness across all types.

```Json
{
    "codename": "unique_element",
    "previewApiKey": "[your-preview-api-key]"
}
```

## Saved Value

The value is saved as a string representing the entered text.
