# 🏈 NFL Contract Analysis (2014–2024)

This project explores over a decade of NFL player contract data, analyzing trends in salaries, positions, and teams using SQL Server and Power BI. It’s a real-world demonstration of how data analytics can uncover insights in the world of sports.

## 📊 Project Goals

- Identify the top earners in the NFL since 2014
- Compare total contract value by position**
- Visualize **average contract durations across teams and positions
- Show how **teams invest differently based on roles

# 🔧 Tools & Technologies

- SQL Server Management Studio (SSMS) – Data extraction, transformation, ranking, and filtering
- Power BI Desktop** – Interactive dashboards and visual analysis
- Excel / Google Sheets – Initial data formatting and structure cleanup

## 🗂️ Dataset Fields Used

- `PlayerName`
- `TeamName`
- `Position`
- `ContractValue`
- `LengthOfContractInYears`
- `AverageAnnualSalary`
- `CurrentYear`

## 🖼️ Dashboards & Visuals (Included in /images)

- Top Earners in NFL since 2014 (Pie & Bar Charts)
- Highest Contract Value by Position (Line Chart)
- Team Comparisons (Stacked Bar by Position)
- Average Contract Duration by Team and Position

# ⚙️ SQL Highlights

```sql
RANK() OVER (
PARTITION BY contractyear, teamname, position
ORDER BY contractvalue DESC
) AS rank
