# DesignParkingLotSystem
low-level architecture for a backend system of a smart parking lot
# 1. Database Model
#
Table vehicles {<br>
  vehicle_id integer [primary key]<br>
  licenceplate varchar<br>
  vehicletype_id integer<br>
  entrytime timestamp<br>
  exittime timestamp<br>
  created_at timestamp<br>
}<br>
#<br>
Table parkingspots {<br>
  parkingspot_id integer [primary key]<br>
  floor_id integer<br>
  spot_number varchar<br>
  size integer<br>
  is_available bool<br>
  created_at timestamp<br>
}<br>
#<br>
Table floors {<br>
  floor_id integer [primary key]<br>
  floortitle varchar<br>
  created_at timestamp<br>
}<br>
#<br>
Table vehicletypes {<br>
  vehicletype_id integer [primary key]<br>
  vehicletype_name varchar<br>
  created_at timestamp<br>
}<br>
#<br>
Table payments {<br>
  payment_id integer [primary key]<br>
  vehicle_id integer<br>
  parkingspot_id integer<br>
  amount integer<br>
  is_paid bool<br>
  created_at timestamp<br>
}<br>
<img src='./parkingSlot_DatabaseModel.PNG'/>
