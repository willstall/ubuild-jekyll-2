---
layout: blocks
title: Demo Page
date: 2022-07-16 04:00:00 +0000
page_sections:
- template: full-width-media-element
  block: media-1
  slug: ''
  image: ''
  caption: ''
- template: content-feature
  block: feature-1
  media_alignment: Right
  headline: Headline Here
  content: '<a href="http://localhost:3000/docs/getting-started/#main">Skip to content</a><a
    href="http://localhost:3000/"><img src="http://localhost:3000/images/tina-logo.svg"
    alt="Tina Docs Example" height="32"></a><a href="http://localhost:3000/docs/">Docs</a>New<a
    href="http://localhost:3000/docs/Test_Page/">Test Page</a>Docs<a href="http://localhost:3000/docs/getting-started/">Getting
    Started</a>Getting Started with Tina and MDXA Quick overview of how Tina and MDX
    works.Create componentsCreate any components you would like to use inside your
    MDX file, for example here is a callout using styled components<code>import styled
    from "styled-components"; import rem from "../utils/rem"; export const SubHeader
    = styled.h3` color: rgb(120, 120, 120); display: block; margin: 2em 0 0.75em;
    font-size: ${rem(24)}; font-weight: 600; `; export const Title = styled.h1` display:
    block; text-align: left; width: 100%; color: rgb(120, 120, 120); font-size: ${rem(42)};
    font-weight: bold; `; export const CalloutWrapper = styled.div` background: ${(props)
    =&gt; props.type || "rgba(255,250,240,1)"}; padding: ${rem(7)} ${rem(10)} ${rem(5)}
    ${rem(14)}; border-left: ${rem(4)} solid rgb(220, 220, 220); margin: ${rem(45)}
    0; border-radius: ${rem(3)}; &gt; p { margin: 0 0 ${rem(5)} 0; } ${SubHeader}
    + &amp;, ${Title} + &amp; { margin-top: ${rem(35)}; } `; const CalloutLabel =
    styled.strong` display: block; font-weight: 600; text-transform: uppercase; font-size:
    100%; margin-bottom: ${rem(7)}; `; const CalloutText = styled.p` color: ${(props)
    =&gt; props.textColor || "rgba(156,66,33,1)"}; font-weight: 500; font-size: 90%;
    `; const backgroundColor = { warning: "rgba(254,252,191,1)", error: "rgba(254,215,215,1)",
    default: "rgba(255,250,240,1)", }; const textColor = { warning: "rgba(116,66,16,1)",
    error: "rgba(116,42,42,1)", default: "rgba(156,66,33,1)", }; const label = { default:
    "Note", }; export default function Callout({ callout }) { return ( &lt;CalloutWrapper
    type={backgroundColor[callout.type]}&gt; &lt;CalloutLabel&gt;{label[callout.type]
    || callout.type}&lt;/CalloutLabel&gt; &lt;CalloutText textColor={textColor[callout.type]
    || textColor.default}&gt; {callout?.text} &lt;/CalloutText&gt; &lt;/CalloutWrapper&gt;
    ); }</code>Add your components to your schemaYour schema.ts found in the .tina
    directory needs the following things:You need to use the rich-text typeYou need
    to add the component to the schemaYou need to add what parts you want to be able
    to edit.Here is the schema.ts file with the Callout component added:<code>...
    { type: "rich-text", label: "Body", name: "body", templates: [ { name: "Callout",
    label: "Callout", fields:[ { name: "type", label: "Type", type: "string", options:
    ["default", "warning", "error"], }, { name: "text", label: "Text", type: "string",
    }, ] }, ], ], isBody: true, }, ...</code><a href="http://localhost:3000/docs/Test_Page">←<span
    class="Apple-converted-space"> </span>Test Page</a><br>'
  slug: ''
  media:
    image: ''
    alt_text: ''
published: false

---
