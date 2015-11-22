## Fast and Highly affordable DataGrid Component for FLEX and AIR project! ##

This datagrid only refresh the viewable region, so the refresh and scrolling speed is fast. You can export spreadsheet content to binary Excel file. If you use the AIR project, your users can save desktop AIR without installed MS-Excel.

### [Visit our website on mechan project (http://www.mechansp.com)](http://www.mechansp.com/) ###

### Export grid content to Excel file ###

[FLEX Sample](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridDemo/MecGridDemo.html) [AIR Sample](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridAirDemo/MecGridAIRDemo.air)

### MecGrid Features ###

1. SpreadSheet style column and row index.

2. MouseWheel scroll.

3. Hierarchical data (Tree grid).

4. Cell Border Style (top, left, right, bottom with thickness and color adjust).

5. {dataProvider} binding support for compatibility.

6. FixeRows and Columns each.

7. Various CellRenderer (StatusBar for dashboard, Text, CheckBox).

8. Separate merge option for fixed range and normal range.

9. Merge option (MERGE\_FREE, MERGE\_PREV, MERGE\_NONE).

10. Large Data Support.

11. (version 1.0.3) OLAP Pivoting Support.
> (version 1.1.3) OLAP Drill to Detail Support.

12. (version 1.0.5)
  * Support Cell Calculation (Sample Calculator format)
    1. arithmatic calculation (eg, = C1+D1)
    1. Flex Math function (eg, = min(C1, D1) + max(C1, D1)   = sin(20))
    1. mixed arithmatic and math calculation (eg, = C1 + (min(C1, D1) / max(C1, D1)) )
  * Support Column FormatString
    1. (#,### for 1000 seperator)
    1. ($#,### for $1,000)
    1. (#,###.## for specify float position)
  * Cell level fontstyle Support

13. (version 1.0.6) _Simple setting by Design Wizard_.

14. (version 1.0.7) Multi-column sorting.

15. (version 1.0.8) Freeze row and column.

16. (version 1.0.9) ResourseXML property ([Sample sourcecode](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridResourceXML/srcview/index.html))

17. (version 1.1.0) Grand Total and Sub Total Support. ([Sample](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridSubTotal/MecGridSubTotal.html))

18. MecGridWizard Style Definition Support

19. (version 1.1.2) Drag and Drop Support. ([Sample](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridDragDrop/MecGridDragDrop.html))
  * Column Moving
  * Row Moving (In row selection mode), Cell Copying (In cell selection mode)

20. (version 1.1.3) Filtering Support. ([Sample](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridFiltering/MecGridFiltering.html))
  * Numeric Operation Filtering
  * CheckBox filtering

21. (version 1.1.6) (AIR Only) Export microsoft excel file.
  * Creat Excel File with binary format (Not in html export)
  * No need to install microsoft excel on client PC. (BIFF Format)
  * (For FLEX) Create BinaryArray with excel binary data.
  * [Adobe AIR Demo Center](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridAirDemo/MecGridAIRDemo.air)    |    [Download Adobe AIR Framework](http://www.adobe.com/go/EN_US-H-GET-AIR)

22. (version 1.1.6 fix) Fix Dynamic Rows and Column Adding Features.
  * [Sample Demo](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridDynamicColumn/MecGridDynamicColumn.html)

23. (version 1.1.7) Excel File Export Features.
```
    // How to create excel file and export to excel sheet.
    try
    {
        var exp:MecExporter = new MecExporter();
            
        // add MecGrid with sheetname
        exp.AddDataGrid(mgrid, "");
        // exporting to binary data
        var ebt:ByteArray = exp.Export2BiffExcel();
          
        // If you use flex with web server, you can use base64 encoded text file.
            var b64encoder:Base64Encoder = new Base64Encoder();    
            b64encoder.encodeBytes(ebt);
            
        // If you use AIR
            var f:File = new File("c:\\mecgrid_excel_file.xls");
            var fs:FileStream = new FileStream();
            fs.open(f, FileMode.WRITE);
            fs.writeBytes(ebt);
            fs.close();
    }
    catch (e:Error)
    {
        Alert.show(e.message);
    }
```

---


### MecGrid Demo ###
(_Click images to experience the features_)

| **MecGrid Wizard** |
|:-------------------|
| [![](http://flexspreadsheet.googlecode.com/svn/trunk/images/mecgrid_wizard.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/mecgridwizard/MecGridWizard.html) |
| _Compare with viewsource_ : [Resource with XML](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridResourceXML/MecGridResourceXML.html)  [Resource with Encripted String](http://flexspreadsheet.googlecode.com/svn/trunk/sample03/MecGridTemplate.html)|

| **MecGrid DemoCenter** [(For AIR DemoCenter)](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridAirDemo/MecGridAIRDemo.air) |
|:---------------------------------------------------------------------------------------------------------------------------------|
| [![](http://flexspreadsheet.googlecode.com/svn/trunk/flex_datagrid_democenter.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridDemo/MecGridDemo.html) |

| **Flex OLAP Support** | **Large Data** |
|:----------------------|:---------------|
| [![](http://flexspreadsheet.googlecode.com/svn/trunk/images/flex_datagrid_olap.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/olap_analysis/MecGridForOLAP.html) | [![](http://flexspreadsheet.googlecode.com/svn/trunk/images/flex_datagrid_largedata.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/sample01/MecGridSample.html) |
| **Drag and Drop**     | **Filtering**  |
| [![](http://flexspreadsheet.googlecode.com/svn/trunk/images/flex_datagrid_dragdrop.jpg)](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridDragDrop/MecGridDragDrop.html) | [![](http://flexspreadsheet.googlecode.com/svn/trunk/flex_datagrid_filtering.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/MecGridFiltering/MecGridFiltering.html) |
| **Dynamic Styling**   | **User Formula and Text Styling** |
| [![](http://flexspreadsheet.googlecode.com/svn/trunk/images/flex_datagrid_sample02.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/sample01/MecGridCellBorder.html) | [![](http://flexspreadsheet.googlecode.com/svn/trunk/images/flex_datagrid_style.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/sample02/bin/MecCustomFormula.html) |
| **Multi Sorting**     | **Tree** (_Click on Load DataProvider Button_) |
| [![](http://flexspreadsheet.googlecode.com/svn/trunk/images/flex_datagrid_sorting.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/sample04/MecGridSorting.html) | [![](http://flexspreadsheet.googlecode.com/svn/trunk/images/flex_datagrid_treegrid.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/sample01/MecGridSample.html) |
| **Freeze Column and Row** | **MineSweep Game** |
| [![](http://flexspreadsheet.googlecode.com/svn/trunk/images/flex_datagrid_freezecell.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/sample05/MecGridFrozen.html) | [![](http://flexspreadsheet.googlecode.com/svn/trunk/images/flex_datagrid_minesweep.gif)](http://flexspreadsheet.googlecode.com/svn/trunk/MineSweep/MineSweep.html) |


## API Document ##
[API Documentation](http://flexspreadsheet.googlecode.com/svn/trunk/document/index.html)

Send comment to mechan93@gmail.com.

## Sample code to draw MecGrid ##
```
<MecGrid:MecGrid id="mgrid" bottom="40" right="10" top="60" left="10" dataProvider="{myDataCollection}">
    <MecGrid:ResourceString>
eNrF1c2O2jAQB/BjpT6F5Vy6oio4HyxVyEq7rHrqpepqr8jFQ2IpsVl7YNkH6fvWxHwotEbpgfaS
ZMx48v8hRX73c/pVWrx7T8hUr1BqRRa6tgWdULKUWxBGv7oq3lf+txElDZgS5n5HQdPuwvzQu27U
b93zw9h2qq3c/JUBLmwFgAX94taghsWutdECCspcFDQAGwluz5MvZqfhCFvktSxVA8oNGJ+t+PcV
NKPDVulj2d3zsSKKN+5Nrpi7gYIjX0qo3SYfBQQlG2nljxraACAk8rZwad0mqQRs2yx8jfpVCqza
vv1TyvxMfFtBN/Eu1ak6JGWuZalNw9GikaosKCWV+4fAFPR7Gyj3Ny/6k4J1FAu9VmjeeiFYADHu
ILIOIv1LxMznyff3MCPuMiT2M8T/wuDC5LtLOH3SSf+CrFf4JBB+MgmHZ6Ne6aOPURR9iqKT4tnl
QW1sziySb2uOYMiH+5uwKT0zxb1MacD0Ob6mKVbiaHq4YMrOTEkvUxYyja5pSszJNLtgGp+Z0l6m
8X8xpVgdTY8XTLcdE9+UvUy3ARPLkiug7jdgeAmkcJ/R4GEwGzzekCFJ88D6/kwaHg+l6bA9jn8B
CJF0Hw==
    </MecGrid:ResourceString>
</MecGrid:MecGrid>
```

```
<MecGrid:MecGrid id="mgrid" bottom="40" right="10" top="60" left="10" dataProvider="{myDataCollection}">
    <MecGrid:ResourceXML>
        <mx:XML xmlns="">
            <List>
              <option cols="8" fixedrows="2" fixedcols="0" merge_option="4" merge_option_fixedcolumn="0" merge_option_fixedrow="2" showspreadsheet="F" selectionmode="18" treeview="T" treeColumn="0" textalignment="6" textalignment_fixed="5"/>
              <columns>
                <column name="col_0" datafield="selected" visible="T" editable="F" colindex="0" autowidth="T" width="41" datatype="0" textalign="5" textalign_fixed="10" formatstring="" header="Select;Select"/>
                <column name="col_1" datafield="country" visible="T" editable="F" colindex="1" autowidth="T" width="61" datatype="5" textalign="4" textalign_fixed="10" formatstring="" header="Country;Country"/>
                <column name="col_2" datafield="city" visible="T" editable="F" colindex="2" autowidth="T" width="61" datatype="5" textalign="4" textalign_fixed="10" formatstring="" header="City;City"/>
                <column name="col_3" datafield="qt1" visible="T" editable="F" colindex="3" autowidth="T" width="88" datatype="5" textalign="10" textalign_fixed="10" formatstring="#,###.##" header="Visitors;1st Quater (A)"/>
                <column name="col_4" datafield="qt2" visible="T" editable="F" colindex="4" autowidth="T" width="92" datatype="5" textalign="10" textalign_fixed="10" formatstring="#,###.##" header="Visitors;2nd Quater (B)"/>
                <column name="col_5" datafield="qt3" visible="T" editable="F" colindex="5" autowidth="T" width="90" datatype="5" textalign="10" textalign_fixed="10" formatstring="#,###.##" header="Visitors;3rd Quater (C)"/>
                <column name="col_6" datafield="qt4" visible="T" editable="F" colindex="6" autowidth="T" width="90" datatype="5" textalign="10" textalign_fixed="10" formatstring="#,###.##" header="Visitors;4th Quater (D)"/>
                <column name="col_7" datafield="avg" visible="T" editable="F" colindex="7" autowidth="T" width="153" datatype="5" textalign="10" textalign_fixed="10" formatstring="#,###.##" header="Average = (A+B+C+D) / 4;Average = (A+B+C+D) / 4"/>
              </columns>
            </List>    
        </mx:XML>
    </MecGrid:ResourceXML>
</MecGrid:MecGrid>
```


---


For Job offer & Request Component Development (FLEX, Java, MS.NET), please send email to mechan93 at gmail.


---
