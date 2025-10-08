### Criterion for Bubble Growth Diagram

```mermaid
graph TD
    A[Hot Wall Temperature $T_w$] -->|Conducts Heat| B(Thermal Layer)
    B --> C{Nucleation Site / Cavity $R_c$}
    C -->|Vaporizes Liquid| D[Vapor Bubble Radius $R$]

    style A fill:#ff9999,stroke:#333
    style D fill:#ddddff,stroke:#333

    subgraph Liquid
        E[Bulk Liquid Temperature $T_\infty$]
        B -- Heat Transfer --> E
    end

    subgraph Criterion for Growth
        P[Pressure in Bubble $P_b$] -->|Must be >| L[Liquid Pressure $P_\infty$]
        P -->|Needed to Overcome| S[Surface Tension $2\sigma/R$]
        T[Temperature in Bubble $T_b$] -->|Must be >| K[Saturation Temp $T_{sat}$]
        T -->|Relates $\Delta P$ and $\Delta T$| P
    end

    A -- Must be High Enough --> T
    C -- Sets Initial R --> S
    D -- Growth --> G[Bubble Detaches]

    linkStyle 0 stroke-width:2px,stroke:red;
    linkStyle 1 stroke-width:2px,stroke:red;
    linkStyle 2 stroke-width:2px,stroke:blue;
    linkStyle 3 stroke-width:2px,stroke:blue;# Boiling-diagram
