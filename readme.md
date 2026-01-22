Are you tired to look for the most recent queries?

Are you tired to write the same function and code again and again?

I know that feeling...


# DSNP Query Box

![query_box](./query_box2.png)

Keep all DSNP queries one place. Let all the team members can access to the most recent updated queries and functions

#### 1. Queries we use for reports

[Check the query list](./query_list.csv)

#### 2. Helper Functions that can make your life easy

[Check HelperFunction](./cdst_snp_query_box/DsnpHelperFunction.py)

#### 3. Constant Values we use frequently

[Check Dsnp Values](./cdst_snp_query_box/DsnpVal.py)

#### 4. Also, there are frequently used transformations

[Check dsnp transforms](./cdst_snp_query_box/dsnp_transform/)

---
<br>


>How to use it?

1. clone or pull the repo
2. if you are on conda env, deactivate conda env in terminal `conda deactivate`
3. go under the repo `cdst_snp_query_box`
4. in your terminal and run `pip install cdst_snp_query_box=={version}`
5. it is ready to use the queries

<br>
> how to build
0. go the the folder, update version in setup.cfg
1. rm -rf dist
2. rm -rf build
3. python -m build
4. check build includes the right script
4. push to master
5. jenkins build

Example
```
from cdst_snp_query_box import DsnpHelperFunction, populDashQueries  

#use helper functions
DsnpHelperFunction.last_date_of_month("2023-01-29")
>> datetime.date(2023, 1, 31)

# use pull queries
pull_snp_member = populDashQueries.pull_ctm(medicare_number_list, start_date, end_date)
```