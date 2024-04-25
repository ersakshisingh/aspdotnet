## Get highest number from datatable single column
### steps
1. Assign Columns in DataTable
2. Fill DataTable with data
3. Apply Method Syntax Linq Query and get single value

### Assign Columns in DataTable
```
DataTable dtKeywords = new DataTable();
            dtKeywords.Columns.Add("Keyword", typeof(string)); // Add DataColumn for keyword
            dtKeywords.Columns.Add("Number", typeof(int)); // Add DataColumn for number
```
### Data Insert
```
dtKeywords.Rows.Add("A", 20);
            dtKeywords.Rows.Add("B", 2);
            dtKeywords.Rows.Add("C", 52);
            dtKeywords.Rows.Add("D", 32);
```
### Apply Method Syntax Linq Query and get single value

```
  string mostAgedPerson = dtKeywords.Select("", "Number ASC").Last()["Number"].ToString();
```

### output
```
 Console.WriteLine(mostAgedPerson);
```
