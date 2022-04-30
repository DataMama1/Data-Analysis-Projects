-- LOOKING FOR THE MOST POPULAR BAOTS IN THE LAST SEVEN DAYS
  select top (10) *
  from [ForPractise].[dbo].[BoatSales$]
  order by [Number of views last 7 days] desc

-- LOOKING FOR THE MOST POPULAR BOAT TYPE IN THE LAST 7 DAYS
  with BoatType as (select top (10) *
  from [ForPractise].[dbo].[BoatSales$])
  select distinct([Boat Type]), count(*) from BoatType
  group by [Boat Type]

-- CHECKING IF PRICE DETERMINES THE POPULARITY OF A BOAT
 select  Price, Eur_Price, [Number of views last 7 days]
  from [ForPractise].[dbo].[BoatSales$]
  order by  Eur_Price desc

  
  -- LOOKING FOR THE CHARCTERISTICS OF THE MOST POPULAR BOATS
  
  select top (100) Price, Eur_Price, [Number of views last 7 days]
  from [ForPractise].[dbo].[BoatSales$]
  order by [Number of views last 7 days]  desc

  
  -- CHECKING THE FEATURES OF THE MOST VIEWED BOAT
  
with BoatCte as (
select top (150) *
  from [dbo].[BoatSales$])
  select distinct([Boat Type]), Count(*) as Ty from BoatCte
  group by [Boat Type]
  
 
  with BoatCte as (
select top (150) *
  from [dbo].[BoatSales$])
  select distinct(Type), count(*) from BoatCte
  group by Type

  with BoatCte as (
select top (150) *
  from [dbo].[BoatSales$])
  select * from BoatCte 
  order by [Number of views last 7 days] desc

  with BoatCte as (
select top (150) *
  from [dbo].[BoatSales$])
  select distinct(Material), Count(*) as Ty from BoatCte
  group by Material

