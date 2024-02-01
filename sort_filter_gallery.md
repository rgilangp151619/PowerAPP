If(
    LookUp(
        Sharepoint Data 1,
        User().Email = Email,
        Role.Value = "Super User"
    ),
    SortByColumns(
        Filter(
            Sharepoint Data on Gallery,
            Title = SearchBox_3.Text || IsBlank(SearchBox_3.Text) || 'Requestor Email' = SearchBox_3.Text || IsBlank(SearchBox_3.Text),
            Project.Value = ComboBox1_6.Selected.Value || IsBlank(ComboBox1_6.Selected.Value),
            Status.Value = ComboBox1_7.Selected.Value || IsBlank(ComboBox1_7.Selected.Value),
            'Request Type'.Value = ComboBox1_8.Selected.Value || IsBlank(ComboBox1_8.Selected.Value),
            ComboBox1_9.Selected.Value = 'GA Site' || IsBlank(ComboBox1_9.Selected.Value)
        ),
        "RequestDate",
        SortOrder.Descending
    )
