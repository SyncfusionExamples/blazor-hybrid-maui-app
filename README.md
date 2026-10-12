# Blazor Hybrid MAUI App

## Overview

This sample demonstrates how to create a .NET MAUI Blazor Hybrid application and integrate Syncfusion services into the application startup pipeline. The project uses Syncfusion [Blazor Components](https://www.syncfusion.com/blazor-components) within a .NET MAUI single-project structure, enabling developers to build cross-platform applications for Windows, Android, iOS, and Mac Catalyst.

The sample focuses on application bootstrap and service registration by configuring Syncfusion Blazor support in the MAUI host. It serves as a starting point for adding Syncfusion controls and building native-like cross-platform experiences with a shared Blazor UI layer.

## Key Features

- Uses Syncfusion [Blazor Charts](https://www.syncfusion.com/blazor-components/blazor-charts) to visualize monthly sales data.
- Renders a chart using the `SfChart` component with a categorical X-axis configured through `ChartPrimaryXAxis` and `ValueType.Category`.
- Binds chart data through the `ChartSeries.DataSource` property using a strongly typed `SalesInformation` collection.
- Maps chart fields using:
  - `XName="Month"` for category labels.
  - `YName="SalesValue"` for numeric values.
- Dynamically changes the chart visualization type using the `ChartSeries.Type` property.
- Uses the Syncfusion `SfDropDownList` component to provide chart type selection.
- Populates dropdown items from a strongly typed `SelectionTypes` collection.
- Configures dropdown value mapping through `DropDownListFieldSettings`.
- Handles user interaction through the `DropDownListEvents.ValueChange` event.
- Updates the displayed chart in the `ChangeType(ChangeEventArgs<ChartSeriesType, SelectionTypes> args)` event handler.
- Demonstrates switching between multiple chart series types:
  - Area
  - Bar
  - Line
  - Column
- Uses the `ChartSeriesType` enumeration to control chart rendering dynamically at runtime.
- Includes a sample monthly sales dataset represented by the `SalesInformation` model.
- Showcases data binding, event handling, and UI interaction between Syncfusion Chart and DropDownList components in a Blazor application.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone this repository.
2. Open `MAUI_Blazor_Windows/MAUI_Blazor_Windows.sln`.
3. Restore NuGet packages.
4. Ensure the `MAUI_Blazor_Windows` project is selected as the startup project.
5. Register your Syncfusion license key in `MauiProgram.cs`.
6. Build the solution.
7. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Clone the repository.
2. Open the repository folder in Visual Studio Code.
3. Navigate to the project directory:

```bash
cd MAUI_Blazor_Windows
```

4. Restore dependencies:

```bash
dotnet restore
```

5. Run the application:

```bash
dotnet run
```

## Project Structure

`MAUI_Blazor_Windows/Pages/Index.razor` - Main sample page that hosts the `SfChart` and `SfDropDownList` components, defines the sales data source, chart type collection, and runtime chart switching logic.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Official documentation: https://blazor.syncfusion.com/documentation/getting-started/maui-blazor-app

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.