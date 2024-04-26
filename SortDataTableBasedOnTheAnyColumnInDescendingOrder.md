## Sort DataTable Based On The Any Column In Descending Order

###  Apply the dataview for sort the data
  // Sort DataTable based on the "Number" column in descending order
  
        DataView dv = dtKeywords.DefaultView;
        dv.Sort = "Number DESC";
        DataTable sortedDt = dv.ToTable();

### Store it an array
 string[] arr = new string[sortedDt.Rows.Count]; // Declare string array

        for (int i = 0; i < sortedDt.Rows.Count; i++)
        {
            arr[i] = sortedDt.Rows[i]["Keyword"].ToString(); // Assign DataTable values to array
        }

### Output
 // Printing array elements
        foreach (string item in arr)
        {
            Console.WriteLine(item);
        }

## For only print single highest value 

 if (sortedDt.Rows.Count > 0)
        {
            string keyword = sortedDt.Rows[0]["Keyword"].ToString();
            int number = Convert.ToInt32(sortedDt.Rows[0]["Number"]);
            Console.WriteLine($"{keyword} - {number}"); // Print highest value
        }

