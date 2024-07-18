# How It Started
Yesterday, I read a blog post by Reza Rad on merge types in Power BI, and it got me thinking. This is a concept I always ended up confusing in my college days. It struck me that creating a Power BI report to demonstrate the different join types while merging queries could be much more effective. Users could easily understand it by clicking through the join types and seeing the results instead of just Watching You Tube . To enhance its utility, I also want to include the ability to add, modify, or delete records in the two tables so that my users can see in real-time how these changes affect the merged tables.

# Working -: What And How
For demonstrating the solution, I made use of 2 simple tables: Table A consists of Customer ID and Customer Name, Table B consists of Customer ID and Email. We will be merging both of these tables using the Customer ID column. In the report, you can see Table A is on the left side, Table B is on the right side and the resultant merged table is on the bottom. We also have a slicer on the top to choose the Join Type, and just under it, we have a description for the Join Type as well as a Venn Diagram. For both Table A and Table B, we have a IsJoined column which denotes whether the corresponding row is present in the Merged table for the selected Join Type.

# Screenshot
![Screenshot 2024-07-18 134134](https://github.com/user-attachments/assets/754f676c-da6e-4c8e-8019-1a8d16bc9946)
![Screenshot 2024-07-18 134533](https://github.com/user-attachments/assets/4a2226e7-f12b-4daa-88be-0ab1f091900b)
![Screenshot 2024-07-18 134640](https://github.com/user-attachments/assets/c96be9e4-9954-4711-869b-9de3828c32a2)

### Now, if you are reading this, most probably you are interested in learning how this was done. To be honest, this report ended up being a little more tricky than I thought it would be and it has some hidden tips and tricks.

– Table A and Table B data is entered through Power BI. So you can add more records and see how the merged table would look like for the changed data. For eg, what happens when I have duplicate customer ids and how will it affect my merged table?

– How does the slicer have images under it? – Chiclet slicer

– How did I make the Venn Diagram to change based on the filter selection? – Use Synoptic Designer to create the Venn diagram, and then link it to your dataset using a DAX measure that will highlight the appropriate area.

– How does the IsJoined column show whether the source table’s record is present in the merged table? – DAX Measure

– How do I display the right results in the Merged table? – A combination of using Power Query and DAX measures.

### I know I have answered the questions only on a high level, but if there is enough interest in knowing more about this, please let me know



