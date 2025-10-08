graph TD
    A[Hot Wall Temperature Tw] -->|Conducts Heat| B(Thermal Layer)
    B --> C{Nucleation Site / Cavity Rc}
    C -->|Vaporizes Liquid| D[Vapor Bubble Radius R]

    style A fill:#ff9999,stroke:#333
    style D fill:#ddddff,stroke:#333

    subgraph Liquid
        E[Bulk Liquid Temperature Tinf]
        B -- Heat Transfer --> E
    end

    subgraph Criterion for Growth
        P[Pressure in Bubble Pb] -->|Must be >| L[Liquid Pressure Pinf]
        P -->|Needed to Overcome| S[Surface Tension 2sigma/R]
        T[Temperature in Bubble Tb] -->|Must be >| K[Saturation Temp Tsat]
        T -->|Relates Delta P and Delta T| P
    end

    A -- Must be High Enough --> T
    C -- Sets Initial R --> S
    D -- Growth --> G[Bubble Detaches]

    linkStyle 0 stroke-width:2px,stroke:red;
    linkStyle 1 stroke-width:2px,stroke:red;
    linkStyle 2 stroke-width:2px,stroke:blue;
    linkStyle 3 stroke-width:2px,stroke:blue;
    linkStyle 1 stroke-width:2px,stroke:red;
    linkStyle 2 stroke-width:2px,stroke:blue;
    linkStyle 3 stroke-width:2px,stroke:blue;# Boiling-diagram
