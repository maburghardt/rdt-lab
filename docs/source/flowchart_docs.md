# CaC Flowchart Docs

<div class="mermaid" style="width=100%;">
flowchart TD
    subgraph docs
    180[docs] --> |about| 181[jinja_macros]
    180[docs] --> |contains| 182[manual]
        182[manual] --> |for| 183[developer]
            183[developer] --> |rendered at| 184(complianceascode.readthedocs.io)
        182[manual] --> |contains| 185[images]
        182[manual] --> |contains| 186[user_guide.adoc]
    180[docs] --> |about| 187[modules]
    180[docs] --> |about| 188[templates]
    180[docs] --> |contains| 189[readme_images]
    end
    style 181 fill: #FFA07A,stroke:#333,stroke-width:4px
    style 188 fill: #9370DB,stroke:#333,stroke-width:4px
    style 184 fill: #A9A9A9,stroke:#333
</div>

<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>


