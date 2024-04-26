## Get data from datagrid in window application

```
foreach (DataGridViewRow row in gridKeywords.Rows)
{
    bool isBlank = true;
    DataRow dRow = dtKeywords.NewRow();
    foreach (DataGridViewCell cell in row.Cells)
    {
        if (cell.Value != null)
         if (cell.Value.ToString().Length > 0)
            {
                dRow[cell.ColumnIndex] = cell.Value;
                isBlank = false;
            }
            else
                isBlank = true;
    }
    if (!isBlank)
    {
        dtKeywords.Rows.Add(dRow);
    }
}
```
