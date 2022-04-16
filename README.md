select *
  from [ecommerce].[dbo].[olist_geolocation_dataset$] where geolocation_zip_code_prefix = 17970;

  update [ecommerce].[dbo].[olist_geolocation_dataset$]
		set geolocation_city= 'sao joao do pau dalho'
		where geolocation_zip_code_prefix = 17970;

		update [ecommerce].[dbo].[olist_geolocation_dataset$]
		set geolocation_city= 'lambari doeste'
		where geolocation_zip_code_prefix = 78278;
