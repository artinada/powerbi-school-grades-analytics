## Architecture / Star Schema

<p align="center">
  <img src="https://github.com/artinada/powerbi-school-grades-analytics/blob/main/powerbi/screenshots/data-model.png?raw=true" alt="Star Schema Image"/>
</p>


### Data Model

The project uses a Star Schema approach:

Fact table:
- grades

Dimension tables:
- students
- classes
- teachers
- subjects
- periods
- calendar

Relationships:
- One-to-Many
- Single direction filtering
