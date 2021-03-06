## content/shared

This flowchart represents the high-level interaction of components under the `utils`, `release_tools`, `ssg` and `Dockerfiles` folders.

Note that colors are used to highlight components which interact with other folders under the `content` repository.

> ***NOTE***: Since the colors have only visual effects when presented in individual flowcharts, they are very useful when analyzing multiple flowcharts together.

<div class="mermaid" style="width=100%;">
flowchart TD
    subgraph utils
    200[utils] --> |contains| 201(scrits)
    200[utils] --> |contains| 202(html templates)
    203[release_tools] --> |contains| 204(scripts)
    205[ssg] --> |contains| 206(python scripts)
    207[Dockerfiles]
    end
    style 201 fill: #A9A9A9,stroke:#333
    style 202 fill: #A9A9A9,stroke:#333
    style 204 fill: #A9A9A9,stroke:#333
    style 206 fill: #A9A9A9,stroke:#333
    style 207 fill: #CD5C5C,stroke:#333,stroke-width:4px
</div>
<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
