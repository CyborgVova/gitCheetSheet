﻿# gitCheetSheet

- **Диаграмма с простыми командами для работы с git.**

 ```mermaid
    graph LR;
    untracked -- "git add" --> staged/tracked;
    staged/tracked -- "git restore --staged" --> untracked;
    staged/tracked -- "git commit"--> fixed/tracked;
    staged/tracked --> modified;
    modified -- "git add" --> staged/tracked;
    fixed/tracked --> modified;
    modified -- "git restore" --> unmodified;
    unmodified -- "git add" --> staged/tracked;
    fixed/tracked -- "git push" --> X[Remote repository];
```
