# MPR Mapping  File Config Details

# BOB :-

|S.NO|  MPR Column    | -| DB Column |
|:--| :----------: |:--: |-----------: |
|1|Payment Gateway Transaction ID  | -|  acq id|
|2|Merchant Track Id | -| pgrefnum|
|3|Transaction Type  | -| sale PURCHASE and for refund REFUND|
|4|Transaction Amount | -| total amount|
|5|NET AMOUNT  | -|settlement amount (NetAmount -(TDX-GTS))|


# IDFC

|S.NO|  MPR Column    | -| DB Column |
|:--| :----------: |:--: |-----------: |
|1|BAT NBR transaction type | -|  For sale 15 and for refund 999|
|2|DOMESTIC AMT  | -|  Total Amt|
|3|TRAN_ID  | -|  AcqId|
|4|MERCHANT_TRACKID  | -|  PgRefNum|
|5|ACQUIRER_TDR_SC	  | -| TDR/surcharge|
|6|ACQUIRER_GST	  | -|  GST|
|7|Net Amount | -|  Settlement Amt|


# Axis
|S.NO|  MPR Column    | -| DB Column |
|:--| :----------: |:--: |-----------: |
|1|Txn Amount | -| Total amount
|2|COMMISSION | -| Acqr Tdr_Src
|3|GST | -| Acqr gst
|4|Payment Amount | -| Merchant Amount(Total amount - (acqr tdr_src + acqr gst))|
|5|MERCHANT TRANS REF | -| PgRef
|6|ORDER ID | -| ACQ_ID
# Lyra
|S.NO|  MPR Column    | -| DB Column |
|:--| :----------: |:--: |-----------: |
|1|UUID | -| Acq_Id|
|2|Bank_Ref_No | -| RRN|
|3|Order_Id | -| PgRefNum|
|4|Transaction_Type | -| Sale/Refund|
|5|Gross_Amount | -| TotalAmount|
|6|Commission_Fee | -| Acq_TDR|
|7|GST | -| Acq_GST|
|8|Payout_Amount | -| NetAmount|

-----------------------------
# PayU
-----------------------------
|S.NO|  MPR Column    | -| DB Column |
|:--| :----------: |:--: |-----------: |
|1|Amount  | - | Gross Amount/Total Amount|
|2|Transaction ID | - | Pg Reff.no|
|3|Bank Reference No | - | RRN|
|4|Net Amount | -|  Amount-(TDR+GST)|
|5|Payment Processing Fee | -| ACQUIRER_TDR_SC|
|6|Service Tax | -| AcquirerGST|
|7|PayU ID | -|  ACQ|
|8|Requested Action | -| capture(for sale)/refund|

## PayU Refund case 
|S.NO|  MPR Column    | -| DB Column |
|:--| :----------: |:--: |-----------: |
|1|Amount  | -| Gross Amount/Total Amount|
|2|Transaction ID | -| Pg Reff.no (Sale Txn Pg Reff No.)|
|3|Bank Reference No | -| RRN (update manually)|
|4|Net Amount | -|  Amount-(TDR+GST)|
|5|Payment Processing Fee | -| ACQUIRER_TDR_SC|
|6|Service Tax | -| AcquirerGST|
|7|PayU ID  | -|  ACQ|
|8|Requested Action | -| refund|



-----------------------------
# Paytm 
-----------------------------
transaction_id      ------  ACQ ID
order_id            ------  PG REF NUM
transaction_type    ------  ACQUIRING(Capture txn)
amount 		    ------  NETAMT
settled_amount      ------  NETAMT- (TDR+GST)
bank_transaction_id ------  RRN
acquiring_fee	    -----   TDR
acquiring_tax	    -----   GST

	Paytm Refund case 

transaction_id      ------  ACQ ID
order_id            ------  PG REF NUM
transaction_type    ------  REFUND (Refund txn)
amount 		    ------  NETAMT
settled_amount      ------  NETAMT- (TDR+GST)
bank_transaction_id ------  RRN
acquiring_fee	    -----   TDR
acquiring_tax	    -----   GST












 