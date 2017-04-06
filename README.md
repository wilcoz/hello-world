# hello-world
blaat

Select replace(convert(varchar,t.CreationTime,111), '/', ' ') Datum
, convert(time(0),T.CreationTime) as Tijd
, t.ExpiringTime, Status = case when t.ProcessingState = 1 then 'Waiting'
								when t.ProcessingState = 5 then 'Released'
								Else 'Unkown'
							End
, t.Pages from cxPOST_rs_TP_dt t

