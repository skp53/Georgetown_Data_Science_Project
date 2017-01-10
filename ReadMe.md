Georgetown University Professional Data Science Certification Program, Fall 2016, Cohort-7, Team Ship Happen.

Team Member-

1. Aaron Wright
2. Brian Fan
3. Kayla Hinrichs (Captain, Team Ship Happen)
4. Sudha Goel
5. Sushanta K Paul

To achieve this certification, we are working on Capstone Project to predict Marine incident using publicly available data from-
https://www.marad.dot.gov/resources/data-statistics/
 
Marine Information for Safety and Law Enforcement (MISLE)
Marine Casualty and Pollution Database, July 6, 2015

In this dataset we have three types of incident data - casualty, pollution and event. Our initial plan was we will work with all incident data and integrate with Marine AIS (Automatic Identification System) data
to show the location where most incident happen that Marine authority make their strategic plan based on prediction.

But due to time constraint and after lots of experimentation on ArcGIS, PostGIG, QGIS etc. and also after discussing with project coordinator (Tony Odeja) we narrowed down our project scope. 
But this not the end, we eager to continue these challenges after completion of this academic program. 

Entity Attributes

Table Name: MisleActivity

Column No.  Type          Column Name                         Length                               
 
 1 		int           activity_id                              4 
 2 		int           case_id                                  4 
 3 		varchar       incident_dt                             10 
 4 		varchar       dept_name                               80 
 5 		varchar       activity_type                           60 
 6 		varchar       activity_status                         60 
 7 		varchar       activity_status_subtype                 60 
 8		numeric       vessel_property_damage                  12   	
 9      numeric 	  cargo_property_damage                   12            
 10     numeric       facility_property_damage                12        
 11     numeric       other_property_damage                   12         

Table Name: MisleInjury

Column No.  Type          Column Name                         Length                               

  1			 int          activity_id                           4 
  2			 int          fk_d_vessel					 		4
  3			 int	      vessel_id						 		4
  4		 	 varchar	  vin									30 
  5	       	 varchar	  vessel_name							50
  6		 	 varchar	  vessel_service						30
  7		 	 varchar      vessel_class							50
  8		 	 varchar	  vessel_type							50
  9		 	 varchar	  vessel_subtype						50
 10          varchar	  flag_desc					      		30
 11 		 varchar	  vessel_activity_role_desc	  			50
 12		     int		  facility_id					 		4
 13          varchar	  facility_name							50
 14		     varchar	  facility_type_desc					40
 15    	     varchar 	  facility_activity_role_desc		  	50 
 16          varchar      relationship_type                     80 
 17          varchar      waterway_name                         50 
 18          varchar      accident_type                         60 
 19          varchar      casualty_type_desc                    30 
 20          numeric      latitude                              18 
 21          numeric      longitude                             18 

Table Name: MisleVessel

Column No.    Type        Column Name                         Length                               

 1            int         gk_d_vessel                              4
 2  		  int         vessel_id                                4
 3            varchar     vessel_name                             50
 4    	      int         managing_owner_id                        4
 5            varchar     managing_owner                         120
 6            varchar     gross_ton                               40
 7            varchar     net_ton                                 40
 8            varchar     length                                  40
 9            varchar     breadth                                 40
10            varchar     depth                                   40
11            varchar     itc_breadth                             40
12            varchar     itc_depth                               40
13            varchar     itc_gross_ton                           40
14            varchar     itc_length                              40
15            varchar     itc_net_ton                             40
16            varchar     draft_design                            40
17            varchar     draft_design_units                       2
18            varchar     dead_weight_ton                         40
19            varchar     deadweighttonnage_units                  2
20            char        flag_abbr                                2
21            varchar     hailing_port                            50
22            varchar     hailing_port_state                       2
23            varchar     hailing_port_province                   50
24            varchar     route_type                              50
25            varchar     classification_society                  80
26            varchar     cargo_authorization_type                30
27            varchar     documented_ind                          40
28            varchar     documented_status_type                  30
29            varchar     inspected_ind                           40
30            varchar     inspected_desc                          30
31            varchar     state_vessel_ind                        40
32            varchar     state_vessel_desc                       30
33            varchar     lloyds_ind                              40
34            varchar     lloyds_desc                             30
35            varchar     solas_ind                               40
36            varchar     solas_desc                              30
37            varchar     insp_subchapter_type                   255
38            varchar     vessel_class                            50
39            varchar     vessel_type                             50
40            varchar     vessel_subtype                          50
41            varchar     vessel_service                          30
42            varchar     max_passengers_allowed                  40
43            varchar     max_crew                                40
44            varchar     self_propelled_ind                      40
45            varchar     propulsion_type                         30
46            varchar     hull_material                           30
47            varchar     hull_design_type                        30
48            varchar     hull_double_bottom_type                 30
49            varchar     hull_double_side_type                   30
50            varchar     call_sign                               10
51            varchar     official_number                         10
52	          varchar	  primary_vin	                          30
53            varchar     hull_number                             30
54            varchar     rbs_hull_number                         30
55            varchar     imo_number                              30
56            varchar     vessel_age                              40
57            varchar     build_shipyard                          50
58            char        build_year                               4
59            varchar     hull_build_party_name                   80
60            varchar     completed_by_party_name                 80
61            varchar     horsepower_ahead                        40
62            varchar     horsepower_astern                       40
63            varchar     forebody_type_desc                      30
64            varchar     hull_configuration                      30
65            varchar     hull_shape                              30
66            char        filler                                   1
