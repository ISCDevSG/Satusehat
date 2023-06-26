# Satusehat
ISC Dev SG Satusehat

Link to documentation:  
[ISC Internal: https://intersystemscorporation-my.sharepoint.com/personal/kalau_intersystems_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fkalau%5Fintersystems%5Fcom%2FDocuments%2FDocuments%2FGeneralMaterials%2FProject%2FSATUSEHAT&ga=1]   
https://satusehat-kemkes-go-id.translate.goog/platform/docs/id/playbook/?_x_tr_sl=id&_x_tr_tl=en&_x_tr_hl=en  
https://www.postman.com/satusehat/workspace/satusehat-public/overview  

ISC internal link to TrakCare data fields https://usconfluence.iscinternal.com/display/THE/Satu+Sehat+%28One+Health%29+-+Guidelines+for+Variables+and+Meta+Data+in+EMR+Implementation

This tool can be used to generate OpenAPI spec from POSTMAN collection (exported as JSON):
https://kevinswiber.github.io/postman2openapi/

Transactions to implement with BitHealth (*12 May 2023*):

1-Registration of organization: one time upload and more to be added when growing  
2-Location  
3-Practitioner  

A sample production is added, in this production, we have -Kate @ISC (*17 May 2023*)<br>
1- BS for intake a csv file "sampleOrganizationData"<br>
2- BP for transfrom the csv into fhie bundle<br>
3- Bo for sending things to SATUSEHAT development environment<br>

A sample production_v1 is added, in this production, we have -Kate @ISC (*18 May 2023*)<br>
1- BS for intake a csv file "sampleOrganizationDatav1"<br>
   *add the Method, id fields to the csv file<br>
   *add POST, GET, and PUT method for the Orgainztion resource<br>
2- BP for transfrom the csv into fhie bundle<br>
3- Bo for sending things to SATUSEHAT development environment<br>

A sample production_v2 is added, in this production, we have -Kate @ISC (*26 May 2023*)<br>
--Organization-GET POST PUT<br>
--Location-GET POST PUT<br>
--Practitioner-GET<br>
--Patient-GET<br>
--Encounter-(still working on it)<br>
Sample data .csv is uploaded<br>
lookup table is added<br>

__Questions__:
- how can codesets be downloaded
- what is the expected medication coding process (hospitals send using codes from DTO web site? or can POST their own)
- how to handle Encounter (keep internal state or passthrough anything that is sent from EMR)
- what data to be persisted in the FHIR repository
-   inbound 
-   received
on a per-transaction basis.
- how to trigger budnles (_TBD_)
- how to handle errors: 40x and 20x with text (consent) (_TBD_)
- how to handle consent
