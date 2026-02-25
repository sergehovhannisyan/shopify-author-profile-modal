# Shopify Author Profile Modal 🚀

Clean and interactive modal for displaying author biographies on Shopify product pages.

## Setup Metafields
1. Create a Metafield (Reference) `custom.author_reference`.
2. Ensure the referenced object has:
   - `full_name` (Text)
   - `photo` (File/Image)
   - `biography` (Rich text)

## Installation
1. Add `product-author-modal.liquid` to your **Snippets**.
2. Render it in `sections/main-product.liquid`:

```liquid
{%- when 'author_profile' -%}
  {% render 'product-author-modal', 
     block: block, 
     author: product.metafields.custom.author_reference.value 
  %}