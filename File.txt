        #region handles name
        List<string> names = new List<string>();
        names.Add("Sophia");
        names.Add("Nicolas");
        names.Add("Zahirah");
        names.Add("Jeong");
        #endregion

        #region handles Nested List Marks
        List<List<int>> marks = new List<List<int>>(){};
        #endregion

        #region handles data for Sophia
        List<int> SophieMarks = new List<int>(){93, 87, 98, 95, 100};
        marks.Add(SophieMarks);
        #endregion

        #region handles data for Nicolas
        List<int> NicolasMarks = new List<int>(){80, 83, 82, 88, 85};
        marks.Add(NicolasMarks);
        #endregion

        #region handles data for Zahirah
        List<int> ZahirahMarks = new List<int>(){84, 96, 73, 85, 79};
        marks.Add(ZahirahMarks);
        #endregion

        #region handles data for Jeong
        List<int> JeongMarks = new List<int>(){90, 92, 98, 100, 97};
        marks.Add(JeongMarks);
        #endregion

        #region that actually calculates avg data for each student
        char ch;
        Console.WriteLine($"Student\t\tGrade");
        for (int i = 0; i < marks.Count; i++)
        {
            float sum = 0;
            for (int j = 0; j < marks[i].Count; j++)
            {
                sum += marks[i][j];
            }

            float average = sum / marks[i].Count;
            if(average > 90.0f)
            {
                ch = 'A';
                Console.WriteLine($"{names[i]}\t\t{average}"+ "  "+ch);
            }
            else
            {
                ch = 'B';
                Console.WriteLine($"{names[i]}\t\t{average}"+ "  "+ch);
            }
        }
        #endregion
