# How to hide the sort icon in WPF DataGrid (SfDataGrid)?

How to hide the sort icon in WPF DataGrid (SfDataGrid)?

# About the sample

In [WPF DataGrid](https://www.syncfusion.com/wpf-ui-controls/datagrid) (SfDataGrid), you can hide the sort icon by changing the fill color for PART_SortButtonPresenter in GridHeaderCellControl.

```Xaml
<Grid x:Name="PART_SortButtonPresenter" 
Grid.Column="1" 
SnapsToDevicePixels="True"> 
    <Grid.ColumnDefinitions> 
        <ColumnDefinition Width="0" MinWidth="{Binding Path=SortDirection, Mode=OneWay, RelativeSource={RelativeSource TemplatedParent}, Converter={StaticResource sortDirectionToWidthConverter}}" /> 
        <ColumnDefinition Width="*" /> 
    </Grid.ColumnDefinitions> 
 
    <Path Width="8.938" 
Height="8.138" 
HorizontalAlignment="Center" 
VerticalAlignment="Center" 
Data="F1M753.644,-13.0589L753.736,-12.9639 753.557,-12.7816 732.137,8.63641 732.137,29.7119 756.445,5.40851 764.094,-2.24384 764.275,-2.42352 771.834,5.1286 796.137,29.4372 796.137,8.36163 774.722,-13.0589 764.181,-23.5967 753.644,-13.0589z" 
Fill="Transparent" 
SnapsToDevicePixels="True" 
Stretch="Fill" 
Visibility="{Binding Path=SortDirection, 
            RelativeSource={RelativeSource TemplatedParent}, 
            ConverterParameter=Ascending, 
            Converter={StaticResource sortDirectionToVisibilityConverter}}"> 
        <Path.RenderTransform> 
            <TransformGroup> 
                <TransformGroup.Children> 
                    <RotateTransform Angle="0" /> 
                    <ScaleTransform ScaleX="1" ScaleY="1" /> 
                </TransformGroup.Children> 
            </TransformGroup> 
        </Path.RenderTransform> 
    </Path> 
 
    <Path Width="8.938" 
Height="8.138" 
HorizontalAlignment="Center" 
VerticalAlignment="Center" 
Data="F1M181.297,177.841L181.205,177.746 181.385,177.563 202.804,156.146 202.804,135.07 178.497,159.373 170.847,167.026 170.666,167.205 163.107,159.653 138.804,135.345 138.804,156.42 160.219,177.841 170.76,188.379 181.297,177.841z" 
Fill="Transparent" 
SnapsToDevicePixels="True" 
Stretch="Fill" 
Visibility="{Binding Path=SortDirection, 
            RelativeSource={RelativeSource TemplatedParent}, 
            ConverterParameter=Decending, 
            Converter={StaticResource sortDirectionToVisibilityConverter}}"> 
        <Path.RenderTransform> 
            <TransformGroup> 
                <TransformGroup.Children> 
                    <RotateTransform Angle="0" /> 
                    <ScaleTransform ScaleX="1" ScaleY="1" /> 
                </TransformGroup.Children> 
            </TransformGroup> 
        </Path.RenderTransform> 
    </Path> 
 
    <TextBlock Grid.Column="1" 
    Margin="0,-4,0,0" 
    VerticalAlignment="Center" 
    FontSize="10" 
    Foreground="{TemplateBinding Foreground}" 
    SnapsToDevicePixels="True" 
    Text="{TemplateBinding SortNumber}" 
    Visibility="{TemplateBinding SortNumberVisibility}" /> 
 
</Grid>
```

KB article - [How to hide the sort icon in WPF DataGrid (SfDataGrid)?](https://www.syncfusion.com/kb/12133/how-to-hide-the-sort-icon-in-wpf-datagrid-sfdatagrid)

## Requirements to run the demo
 Visual Studio 2015 and above versions
