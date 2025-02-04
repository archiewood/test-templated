---
sidebar: hide
queries:
   - categories: categories.sql
---

<LastRefreshed/>

# {params.category}

```sql categories_filtered
select * from ${categories}
where category = '${params.category}'
```

<DataTable data={categories_filtered}/>


<BigValue data={categories_filtered} value=category/>


```sql test
select * from orders limit 100
```

<BigValue
   data={test}
   value=first_name
/>

<BigValue
   data={test}
   value=last_name
/>

<Dropdown data={test} name=test_dropdown value=first_name/>



The name is {inputs.test_dropdown.value}.

