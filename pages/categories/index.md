---
title: Categories
queries:
   - categories: categories.sql
---

Click on an item to see more detail


```sql categories_with_link
select *, '/categories/' || category as link
from ${categories}
```


<Tabs>
    <Tab label="Category 1">

        <Details title="Data Table">

            <DataTable data={categories_with_link} link=link search=true rowShading=true emptySet=pass align=center wrapTitles=true compact=true showLinkCol=false totalRow=true>
                <Column id=category />
            </DataTable>

        </Details>
    </Tab>
</Tabs>


{#each categories_with_link as row}
<a href={row.link}></a>
{/each}