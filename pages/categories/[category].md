---
toc: false
sidebar: hide
---
<LastRefreshed/>

# {params.category}

```sql inventory_filtered
select * from orders
where category = '${params.category}'
```

{#if inventory_filtered.length === 0}

# No data found
## This Product must not exist in the inventory or is out of stock. 

{:else}
<DataTable data={inventory_filtered}/>
{/if}
