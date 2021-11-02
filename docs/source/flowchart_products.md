# content/products

This flowchart represents the high-level interaction of components under the `products` folder.

Note that colors are used to highlight components which interact with other folders under the `content` repository.

> ***NOTE***: Since the colors have only visual effects when presented in individual flowcharts, they are very useful when analyzing multiple flowcharts together.

<div class="mermaid" style="width=100%;">
flowchart TD
    subgraph products
    60[products] --> |identified by| 61[product_name]
        61[product_name] --> |defined at| 62[product.yml]
        61[product_name] --> |contains| 63[overlays]
        61[product_name] --> |contains| 64[profiles]
            64[profiles] --> |written at| 65[profile_name.profile]
                65[profile_name.profile] --> |refers to| 66([rules])
                65[profile_name.profile] --> |may override| 67[variables]
        61[product_name] --> |contains| 68[transforms]
        61[product_name] --> |may have| 69[kickstart]
        61[product_name] --> |may have| 70[checks]
            70[checks] --> |instructed using| 71([OVAL + XCCDF])
                71([OVAL + XCCDF]) --> |written at| 72[check_name.xml]
    end
    style 60 fill: #F0E68C,stroke:#333,stroke-width:4px
    style 64 fill: #F4A460,stroke:#333,stroke-width:4px
    style 66 fill: #FFD700,stroke:#333,stroke-width:4px
    style 67 fill: #FFA500,stroke:#333,stroke-width:4px
    style 71 fill: #1E90FF,stroke:#333,stroke-width:4px
    style 71 fill: #D3D3D3,stroke:#333
    style 72 fill: #1E90FF,stroke:#333,stroke-width:4px
</div>
<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
