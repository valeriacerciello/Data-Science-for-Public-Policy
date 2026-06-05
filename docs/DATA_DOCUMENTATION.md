# Data Documentation


### 1. Referenda Results (`referenda_results.csv`)
- **Source URL**: https://wab.sg.ch/archive/2023
- **Access Date**: 7-07-2024
- **Description**: This file contains data on results of referenda in canton St. Gallen
- **Original Name**: 'all_votes.csv'
- **Data Structure**: 23886 entries, 26 columns
- **Variables Description**:
        - id: Unique identifier for each referendum.
        - title_de_CH: Title of the referendum in German (Switzerland).
        - title_fr_CH, title_it_CH, title_rm_CH: Titles of the referendum in French, Italian, and Romansh (Switzerland), respectively (all null values).
        - short_title_de_CH, short_title_fr_CH, short_title_it_CH, short_title_rm_CH: Short titles in respective languages (all null values).
        - date: Date of the referendum.
        - shortcode: Short code for the referendum.
        - domain: Category of the referendum.
        - status: Status of the referendum.
        - answer: Answer options for the referendum.
        - type: Type of the referendum.
        - ballot_answer: Specific ballot answers.
        - district: District where the referendum took place (some null values).
        - name: Name of the entity/municipality (some null values).
        - entity_id: Numerical ID for the entity.
        - counted: Boolean indicating if the votes have been counted.
        - yeas: Number of affirmative votes.
        - nays: Number of negative votes.
        - invalid: Number of invalid votes.
        - empty: Number of empty votes.
        - eligible_voters: Number of eligible voters.
        - expats: Number of expatriates (all null values).
- **Data Cleaning**:
        - The following columns have been removed because contained only null values
        'title_fr_CH', 'title_it_CH', 'title_rm_CH', 'short_title_de_CH', 
        'short_title_fr_CH', 'short_title_it_CH', 'short_title_rm_CH', 'expats'
        - The 'date' column has been converted to datetime format
        - Rows with missing 'district' and 'name' values have been removed
        - Data have been filtered for the date range between 2015 and 2024
        - Data relative to municipalities of Hemberg, Oberhelfenschwil and Neckertal before 2023 have been combined in the municipality of Neckertal


### 2. Party Strength Left (`party_strength_left.xlsx`)
- **Source URL**: https://stada2.sg.ch
- **Access Date**: 10-07-2024
- **Description**: This file contains data on party strength of SP, the main swiss left-wing party, determined as a percentage of the votes of the party in the total vote of all parties. Data for National Elections between 2007 and 2023 are stored, for each of canton St. Gallen municipalities.  
- **Original Name**: 'stada2.xlsx'
- **Data Structure**: 92 entries, 7 columns
- **Variables Description**:
        - BFS_NR: Integer, representing a unique identifier for each entry.
        - GEBIET_NAME: Object (string), representing the name of the region or area.
        - 2023: Object (string), representing party strength in the year 2023.
        - 2019: Object (string), representing party strength in the year 2019.
        - 2015: Object (string), representing party strength in the year 2015.
        - 2011: Object (string), representing party strength in the year 2011.
        - 2007: Object (string), representing party strength in the year 2007.
- **Data Cleaning**:
        - The xlsx file has been converted to csv format using an online tool
        - Only data relative to elections of 2015, 2019, and 2023 have been selected
        - The following data points have been removed because they do not represent cantons:
        'Gesamtschweiz', 'Grossregion Ostschweiz', 'Kanton Glarus', 'Kanton Schaffhausen', 'Kanton Appenzell a.Rh.', 'Kanton Appenzell i.Rh.', 'Kanton St.Gallen', 'Kanton Graubünden', 'Kanton Thurgau', 'Wahlkreis St.Gallen', 'Wahlkreis Rorschach', 'Wahlkreis Rheintal', 'Wahlkreis Werdenberg', 'Wahlkreis Sarganserland', 'Wahlkreis See-Gaster', 'Wahlkreis Toggenburg', 'Wahlkreis Wil'
        - Year columns have been converted to numeric type


### 3. Party Strength Right (`party_strength_right.xlsx`)
- **Source URL**: https://stada2.sg.ch
- **Access Date**: 10-07-2024
- **Description**: This file contains data on party strength of SVP, the main swiss right-wing party, determined as a percentage of the votes of the party in the total vote of all parties. Data for National Elections between 2007 and 2023 are stored, for each of canton St. Gallen municipalities.  
- **Original Name**: 'stada2.xlsx'
- **Data Structure**: 92 entries, 7 columns
- **Variables Description**:
        - BFS_NR: Integer, representing a unique identifier for each entry.
        - GEBIET_NAME: Object (string), representing the name of the region or area.
        - 2023: Object (string), representing party strength in the year 2023.
        - 2019: Object (string), representing party strength in the year 2019.
        - 2015: Object (string), representing party strength in the year 2015.
        - 2011: Object (string), representing party strength in the year 2011.
        - 2007: Object (string), representing party strength in the year 2007.
- **Data Cleaning**:
        - The xlsx file has been converted to csv format using an online tool
        - Only data relative to elections of 2015, 2019, and 2023 have been selected
        - The following data points have been removed because they do not represent cantons:
        'Gesamtschweiz', 'Grossregion Ostschweiz', 'Kanton Glarus', 'Kanton Schaffhausen', 'Kanton Appenzell a.Rh.', 'Kanton Appenzell i.Rh.', 'Kanton St.Gallen', 'Kanton Graubünden', 'Kanton Thurgau', 'Wahlkreis St.Gallen', 'Wahlkreis Rorschach', 'Wahlkreis Rheintal', 'Wahlkreis Werdenberg', 'Wahlkreis Sarganserland', 'Wahlkreis See-Gaster', 'Wahlkreis Toggenburg', 'Wahlkreis Wil'
        - Year columns have been converted to numeric type


### 4. Share Over 64 (`share_over_64.xlsx`)
- **Source URL**: https://stada2.sg.ch
- **Access Date**: 10-07-2024
- **Description**: This dataset outlines the percentage share of the population over 64 years old relatively to the population aged 20-64 (old-age dependency ratio) by municipality from 1981 to 2022.
- **Original Name**: 'stada2.xlsx'
- **Data Structure**: 92 entries, 44 columns
- **Variables Description**:
        - BFS_NR: Integer, representing a unique identifier for each entry.
        - GEBIET_NAME: Object (string), representing the name of the region or area.
        - 2022 - 2010: Float64, representing the share of the population over 64 years old from 2022 to 2010.
        - 2009 - 1981: Object (string), representing the share of the population over 64 years old from 2009 to 1981. Some of these entries contain ***, indicating missing or unavailable data.
- **Data Cleaning**:
        - The xlsx file has been converted to csv format using an online tool
        - Only data related to the year 2019 have been selected
        - The following data points have been removed because they do not represent cantons:
        'Gesamtschweiz', 'Grossregion Ostschweiz', 'Kanton Glarus', 'Kanton Schaffhausen', 'Kanton Appenzell a.Rh.', 'Kanton Appenzell i.Rh.', 'Kanton St.Gallen', 'Kanton Graubünden', 'Kanton Thurgau', 'Wahlkreis St.Gallen', 'Wahlkreis Rorschach', 'Wahlkreis Rheintal', 'Wahlkreis Werdenberg', 'Wahlkreis Sarganserland', 'Wahlkreis See-Gaster', 'Wahlkreis Toggenburg', 'Wahlkreis Wil'
        - Year column has been converted to numeric type

### 5. Share Under 20 (`share_under_20.xlsx`)
- **Source URL**: https://stada2.sg.ch
- **Access Date**: 10-07-2024
- **Description**: This dataset outlines the percentage share of the population under 20 years old relatively to the population aged 20-64 (youth dependency ratio) by municipality from 1981 to 2022.
- **Original Name**: 'stada2.xlsx'
- **Data Structure**: 92 entries, 44 columns
- **Variables Description**:
        - BFS_NR: Integer, representing a unique identifier for each entry.
        - GEBIET_NAME: Object (string), representing the name of the region or area.
        - 2022 - 2010: Float64, representing the share of the population under 20 years old from 2022 to 2010.
        - 2009 - 1981: Object (string), representing the share of the population under 20 years old from 2009 to 1981. Some of these entries contain ***, indicating missing or unavailable data.
- **Data Cleaning**:
        - The xlsx file has been converted to csv format using an online tool
        - Only data related to the year 2019 have been selected
        - The following data points have been removed because they do not represent cantons:
        'Gesamtschweiz', 'Grossregion Ostschweiz', 'Kanton Glarus', 'Kanton Schaffhausen', 'Kanton Appenzell a.Rh.', 'Kanton Appenzell i.Rh.', 'Kanton St.Gallen', 'Kanton Graubünden', 'Kanton Thurgau', 'Wahlkreis St.Gallen', 'Wahlkreis Rorschach', 'Wahlkreis Rheintal', 'Wahlkreis Werdenberg', 'Wahlkreis Sarganserland', 'Wahlkreis See-Gaster', 'Wahlkreis Toggenburg', 'Wahlkreis Wil'
        - Year column has been converted to numeric type