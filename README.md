# CSVParser
Delphi Simple CSV Parser. Load CSV Data and start processing it.

# Usage :
Add csvparser.pas on delphi IDE library

```
uses CSVParser;

var ParseCsv: TCSVParser;
begin
  ParseCsv := TCSVParser.Create;
  try
    ParseCsv.SetDataFile := 'your\directory\example.csv';
    ParseCsv.Open;

    while not ParseCsv.Eof do
    begin
      Memo1.Lines.Add(ParseCsv.Fields[5]); //or ParseCsv.FieldByName['column_name']
      ParseCsv.Next;
    end;
    
  finally
    ParseCsv.Free;
  end;
end;
```
And Enjoy....

Available properties and methods :
* property SetDataFile - Set csv directori file
* property SetDelimiter - For ddefault ','
* property Fields - result string from Index of column
* property FieldByName - result string from Name of column
and others read source

Semoga Bermanfaat :kissing_closed_eyes:

Hope Useful :kissing_closed_eyes:
