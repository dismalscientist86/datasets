# Datasets
This is a complication of datasets that I hope can be useful to students, professors, and others for research, data visualization, etc. I am an applied microeconomist, and this is reflected in what is included below. Most of the datasets are publicly available, but some aren't and require data agreements. If you have any changes, additions, or comments, please let me know.
 \- [Todd Jones](https://www.toddrjones.com/)

<!-- 
<details>
<summary>Details</summary>

- [Link](https://www.bls.gov/tus/)


</details> 
-->

### Contents

Skip to: [Time use](#time-use), [Names](#names), [Crime](#crime), [Family](#family), [Injury and death](#injury-and-death), [Crashes and traffic](#crashes-and-traffic), [Sports](#sports), [Education](#education), [Inflation data](#inflation-data), [Health](#health), [Temperature](#temperature), [Census and Genealogy](#census-and-genealogy), [Real estate](#real-estate), [Labor and working](#labor-and-working)

---

### Time Use

- [American Time Use Survey (ATUS)](https://www.bls.gov/tus/) - 24-hour US time diaries
  - Years: 2003-present; Access: Public; There is also an IPUMS [version](https://www.atusdata.org/atus/)
  - Includes minute-by-minute information on which  of hundreds of activities the person is doing. For most activities, there is also information on where and with whom the activity occurred.
  - The ATUS is a sample of the Current Population Survey (CPS), to which it can be linked.
  - Sample paper: [Parental and Student Time Use Around the Academic Year](https://www.sciencedirect.com/science/article/pii/S0167268124001598)
- [Multinational Time Use Study](https://www.mtusdata.org/mtus/) - Time diaries from a number of countries
  - Years: varies. Access: Requires IPUMS data agreement.

---

### Crime

- [National Incident-based Reporting System (NIBRS)](https://www.icpsr.umich.edu/sites/icpsr/view/studies/118281/versions/V11) - Individual-level crime data covering much of the US
  - Years: 1991-present. This version was standardized and compiled by Jacob Kaplan.
  - Includes information like offender age, sex, and race; victim age, sex, and race; type of offense; time of offense; location of offense; and relationship between victim and offender.
  - The geography is police agency, so the individual crimes are not geocoded.
    - [Useful crosswalk to get more information about the police agencies](https://www.icpsr.umich.edu/web/ICPSR/studies/35158/versions/V2)
  - Sample paper: [School and Crime](https://www.toddrjones.com/papers/School_Crime_most_recent.pdf)
- [National Crime Victimization Survey (NCVS)](https://www.icpsr.umich.edu/sites/nacjd/view/collections/95) - Self-reported victimization data
  - Years: 1992-present. This version is from ICPSR.
- City-level crime data - many cities have individual-level, geocoded crime data. A small number of examples:
  - [New York City](https://www.nyc.gov/site/nypd/stats/crime-statistics/citywide-crime-stats.page)
  - [Chicago](https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2/about_data)
  - [Los Angeles](https://data.lacity.org/Public-Safety/Crime-Data-from-2020-to-2024/2nrs-mtv8/about_data)
  - [Seattle](https://data.seattle.gov/Public-Safety/SPD-Crime-Data-2008-Present/tazs-3rd5/about_data)
- 911 calls - many cities have data on 911 calls. A small number of examples:
  - [New York](https://data.cityofnewyork.us/Public-Safety/NYPD-Calls-for-Service-Year-to-Date-/n2zq-pubd/about_data)
  - [Los Angeles](https://data.lacity.org/Public-Safety/LAPD-Calls-for-Service-2024-to-Present/xjgu-z4ju/about_data)
  - [Seattle](https://www.seattle.gov/police/information-and-data/data/public-data-sets)
- [Stanford Open Policing Project](https://openpolicing.stanford.edu/) - Data on millions of police traffic stops across locations

---

### US Censuses and Economic History

- [1850-1880 and 1900-1950 individual-level full count US Censuses](https://usa.ipums.org/usa/)
  - This version is from IPUMS, which requires an agreement.
    - IPUMS also has samples of some of the later Censuses
  - Information varies by year, but includes fields like age, sex, race, occupation, household structure, etc. Sometimes earnings and years of education.
  - It does not include name or address.
- [OpenCensus](https://opencensus.us/)
   - A project that is initially working to make the 1940 Census publicly available, so it includes name, address, etc.
- Individual-level links between Censuses
    - [Census Tree](https://www.censustree.org/) - The largest set of links and good coverage for women. It uses information from the world's largest family tree, [FamilySearch](https://www.familysearch.org/en/united-states/), to create the links. 
    - [IPUMS](https://usa.ipums.org/usa/) has its own links
    - Another option is the [Census Linking Project](https://censuslinkingproject.org/) 
- [Census Place Project](https://www.icpsr.umich.edu/sites/icpsr/view/studies/179401/versions/V2.1) - Census links to standardized and geocoded place names.
- [CenSoc](https://censoc.berkeley.edu/) - Links between the 1940 Census and death records.

---

### Household Surveys 

- [American Community Survey (ACS)](https://usa.ipums.org/usa/) - Like a more-detailed version of the US Census, but only a sample of the population participates
  - Repeated cross-section. You can access it, e.g., via IPUMS (above link) or the [tidycensus](https://walker-data.com/tidycensus/) R package (requires a Census API key).
  - Depending on the geography, you can get a large number of variables like demographics, income, travel time to work, college major, industry, home value, and primary heating source.
- [Current Population Survey (CPS)](https://cps.ipums.org/cps/) - Large US labor force survey
  - Years: 1962-present. This version is via IPUMS.
  - A person participates every month for four months, takes eight months off, then does four more months.
  - A subset of the CPS participates in the ATUS (see above).
- [Panel Study of Income Dynamics (PSID)](https://psidonline.isr.umich.edu/) - long-running panel household survey
- [National Longitudinal Study of Youth (NLSY79 and NLSY97)](https://www.bls.gov/nls/cohorts.htm) - detailed, long-running panel surveys
  - NLSY79 follows people born 1957-64, with the first interview in 1979
  - NLSY97 follows people born 1980-84, with the first interview in 1997
  
---

### Names

- [SSA baby names](https://www.ssa.gov/oact/babynames/limits.html) – Frequencies of baby names by year from the Social Security Administration
  - Years: 1880–present; Access: Public
  - Data presented separately by male and female and by state. Minimum 5 names.
  - Fun [article](https://nameberry.com/blog/most-popular-names-how-the-list-was-born) about the origins of these data.
- [England and Wales names](https://www.ons.gov.uk/releases/babynamesinenglandandwales2025#data) - Baby names from the Office of National Statistics
  - Years: 1996-present
  - Minimum 3 names.
- [US Census names](https://www.census.gov/topics/population/genealogy/data.html) - Most commonly-occurring first and last names in the US
  - Years: 1990, 2000, 2010, 2020. Access: Public
- [Facebook Name List](https://web.archive.org/web/20220119175817/http://sites.google.com/site/facebooknamelist/namelist) - How often names are male and female
  - Access: Public

 ---
 
### Injury and death

- [NCHS Multiple Cause of Death](https://www.nber.org/research/data/mortality-data-vital-statistics-nchs-multiple-cause-death-data) - Individual-level US mortality data
  - Years: 1959-present. Only years before 2005 have geographical information.
  - This version is cleaned by the NBER.
- [CDC Mortality Data](https://wonder.cdc.gov/deaths-by-underlying-cause.html) - County-level mortality data
  - Years: 1969-present. Requires agreement.
  - Depending on the year, splits by age, race, sex, and cause of death.
- [National Electronic Injury Surveillance System](https://www.cpsc.gov/Research--Statistics/NEISS-Injury-Data) - Individual-level data on injuries involving consumer products.
  - Sample paper: [Smartphones and child injuries](https://www.sciencedirect.com/science/article/pii/S0047272717301810)

---

### Crashes and traffic

- [Fatal Accident Reporting System (FARS)](https://www.nhtsa.gov/research-data/fatality-analysis-reporting-system-fars) - Individual-level data on virtually the universe of US fatal car crashes
  - Years: 1975-present. Includes drive and passenger demographics, car characteristics, location, and other circumstances regarding the crash.
- State-level crash data - some states (and cities) have individual-level, geocoded car crash data. A small number of examples:
  - [California](https://data.ca.gov/@california-highway-patrol/ccrs)
  - [Massachusetts](https://massdot-impact-crashes-vhb.opendata.arcgis.com/) and then search for "Crashes"
- [UTD19](https://utd19.ethz.ch/) - Traffic data from 20k+ stations across 40 cities
  - Years: 2017-2019. Access: public. 

---

### Education

- [IPEDS](https://nces.ed.gov/ipeds/) - Data on college enrollments, faculty/staff, expenditures, incoming test scores, graduation, etc.
- [SEDA](https://edopportunity.org/opportunity/data/downloads/) - K-12 district-, county-, and state-level test scores, by race and gender
  - Years: 2009-2019
- [Common Core of Data](https://nces.ed.gov/ccd/ccddata.asp) - K-12 school- and district-level data 
- You can access a lot of different datasets, such as IPEDS and CCD, using Urban Institute's [educationdata](https://educationdata.urban.org/documentation/), including R and Stata packages.
- [NERD$](https://edunomicslab.org/nerds/) - K-12 nationwide per pupil spending by school, nationwide
- [HERI](https://heri.ucla.edu/heri-data-archive/) - Detailed college freshman, senior, and faculty surveys
  - Years vary.  Some of data is publicly available; rest requires agreement.
- [Data on where colleges graduates go after graduating](https://www.openicpsr.org/openicpsr/project/170381/version/V3/view)
  - Years: 2010-2018. From [Grads on the Go: Measuring College-Specific Labor Markets for Graduates](https://onlinelibrary.wiley.com/doi/full/10.1002/pam.22553)
- [PISA](https://nces.ed.gov/surveys/pisa/datafiles.asp) - Data allowing cross-county comparisons on educational progress
- [Median earnings four years after graduation by university-major](https://www.theheagroup.com/blog/earnings-test-data)
  - Graduates from 2017-18 and 2018-19. Access: public. A university-major is only included if there are at least 16 graduates.
  - From the Department of Education; this version is made available by the HEA Group.

<!-- [University enrollments](https://borealisdata.ca/dataset.xhtml?persistentId=doi:10.5683/SP3/P0D1KE&version=1.0) -->

---

### Family
*Births, Marriages, and Divorces*

- [NVSS Natality data](https://www.nber.org/research/data/vital-statistics-natality-birth-data) - Individual-level data on births
  - Years: 1968-present. Provided by NBER. Only years before 2005 have geographical information.
- [National Survey of Family Growth](https://www.cdc.gov/nchs/nsfg/index.htm) - Survey on things like pregnancy, infertility, births, and marriage
- [CDC and SSA Birthdates](https://github.com/fivethirtyeight/data/tree/master/births) - Counts of birth by calendar day
  - Years: 1994-2003 (CDC) and 2000-2014 (Social Security Administration)
  - From FiveThirtyEight. See [Some People Are Too Superstitious To Have A Baby On Friday The 13th](https://web.archive.org/web/20160516152410/http://fivethirtyeight.com/features/some-people-are-too-superstitious-to-have-a-baby-on-friday-the-13th/)
- [Marriages and Divorces in Texas](https://www.dshs.texas.gov/vital-statistics/marriage-divorce-records/marriage-divorce-indexes) - Individual-level data on marriages and divorces
   - Years vary. Some of the years are missing data.
   - Both files have names and dates. The divorce file has number of children and date of marriage.
- [Marriages in England and Wales](https://www.ons.gov.uk/peoplepopulationandcommunity/birthsdeathsandmarriages/marriagecohabitationandcivilpartnerships/datasets/marriagesinenglandandwales2013) - Counts of marriages by day
  - Years: 1999-present for the data with day of marriage. 

--- 

### Temperature

- [PRISM](https://prism.oregonstate.edu/) - Gridded weather data, including temperature and precipitation
  - Years: 1981-present (daily), 1895-present (monthly)
- [NOAA](https://www.ncdc.noaa.gov/cdo-web/datatools/findstation) - Weather station data
- [Open-Meteo](https://open-meteo.com/) - weather API
  - Some of data goes back to 1940. Forecast data from 2021. Free version of API is rate limited (300k/month)

---
 
### Sports

- MLB
  - Pitch-level data from Baseball Savant's [Statcast](https://baseballsavant.mlb.com/statcast_search). You can get the location of the pitch, the distance a batted ball was estimated to travel, etc.
  - [Cot's salary data](https://legacy.baseballprospectus.com/compensation/cots/)
  - [Lahman Baseball Database](https://sabr.org/lahman-database/) - Season-level player statistics, 1871-present
- NBA
  - [Box score data](https://www.kaggle.com/datasets/eoinamoore/historical-nba-data-and-player-box-scores), 1947-present, from Kaggle
  - [Play-by-play data](https://www.kaggle.com/datasets/szymonjwiak/nba-play-by-play-data-1997-2023), 1997-present, from Kaggle
- NFL
  - [nflverse](https://github.com/nflverse) - R package that you can use to get lots of data, including play-by-play

---

### Health

- [National Health and Nutrition Examination Survey (NHANES)](https://www.cdc.gov/nchs/nhanes/index.html) - National survey for adults and children with various health-related questions

---

### Real estate

- [Prices paid dataset](https://www.gov.uk/government/statistical-data-sets/price-paid-data-downloads) - All residential property sales in England and Wales (that are sold for value and registered)
  - Years: 2018-present. Has address and price paid.
- [Larson and Contat (2022)](https://www.fhfa.gov/PolicyProgramsResearch/Research/Pages/wp2101.aspx) - Tract-level home price indices
  - Years: 1989-2021

---

### Inflation data

- [CPI-U](https://fred.stlouisfed.org/series/CPIAUCNS#) - you can use this to adjust for inflation
  - To use, click on "Edit Graph" and adjust the frequency to "Annual" with "Average aggregation" method. 

---

### Labor and working

- CPS, ACS, PSID - see above
- [O*NET](https://www.onetcenter.org/database.html) - Data on occupational tasks
- [Anthropic Economic Index](https://huggingface.co/datasets/Anthropic/EconomicIndex?st_source=ai_overview) - AI exposure by job and by geography

---

### Religion

- [2020 US Religion Census](https://www.usreligioncensus.org/node/1639) - Estimates of the number of adherents by faith at the county and state level
- [Pew's Religious Landscape Study (RLS)](https://www.icpsr.umich.edu/sites/icpsr/view/studies/221062/versions/V1) - large survey about religion
- [LDS Hymn Stats](https://hymnstats.joeystanley.com/overview.html) - the hymns sung at over 100,000 (non-representative) Latter-day Saint Sacrament Meetings
  - The microdata is not available, but counts by hymn are, overall and separately by before and since June 2024



---

  Disclaimer: This site may contain errors and in no way do we guarantee the accuracy of the referenced data. In no event will we be liable for any loss or damage.
