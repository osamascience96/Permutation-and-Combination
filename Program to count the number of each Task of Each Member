Module Module1

    Dim StaffNum As Integer 'holds the record of the staff
    Dim TaskNum As Integer 'holds the current task of the specific staff number
    Dim TaskGrid(5, 12) As Integer 'TaskGrid Array that holds the record of all the 60 tasks 
    Dim NewStaffTask As Boolean 'new staff task flag that indicates the need for the new task 
    Dim Completed As Integer ' holds the record for the loop to the finished tasks
    Dim randomNumGen As New Random ' Init the object for random class


    Sub Main()
        'Call InitlizeTaskGrid
        InitlizeTaskGrid()
        Completed = 0 'init the variable 
        'Loop unitl the completed reaches the value of 60 
        While Completed <> 60
            NewStaffTask = False 'newstafftask must be false in order to avoid init redundancy to grid
            ' iterate until the NewStaffTask is False
            While NewStaffTask = False
                Randomize()
                StaffNum = randomNumGen.Next(1, 5) ' generates the number from 1 to 5 for the staff number 
                TaskNum = randomNumGen.Next(1, 12) ' generates the number from 1 to 12 for the task number 
                ' if the TaskGrid[n, n] is equal to false then
                If TaskGrid(StaffNum, TaskNum) = False Then
                    TaskGrid(StaffNum, TaskNum) = True
                    NewStaffTask = True

                    'Write the name code of that was mentioned in the last question

                    ' Display the data in the same order as it was stored in the array
                    Console.Write(StaffNum)
                    Console.Write("-->")
                    Console.Write(TaskNum)
                End If
            End While
            Console.WriteLine()
            Completed = Completed + 1
            Console.WriteLine(Completed)
        End While

        ' Display the tasks completed by the staff
        Console.WriteLine("Staff Task Count ", Completed)
    End Sub

    'Making Procedure that initlizes the Grid
    Sub InitlizeTaskGrid()
        Dim i As Integer
        Dim j As Integer

        For i = 1 To 5
            For j = 1 To 12
                ' init the taskgrid index all to 0
                TaskGrid(i, j) = False
            Next
        Next
    End Sub

End Module
