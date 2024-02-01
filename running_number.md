Text(
      Today(),"yyyymmdd") & 
      CountIf(
              'Document Id_1',
              Not(IsBlank(Title)))+1 & "-" & 
      LookUp(
            'Project Database',
            DataCardValue61.Selected.Value = 'Project Name', 
            ID
            )
    )
