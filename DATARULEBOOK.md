# Style Guide for IGIS Data Lab Database

* author -- Sang Il Bae
* version -- 1.0.0
* created -- 2022.06.03
* last edit -- 2022.06.03

## Introduction

<p>

This document provides coding convention for IGIS Data Lab Database. This style is meant to prevent ugly database from spawning.

</p>


#### Database Name

<p>

Database name should be as written as such. 

* Start with IGIS if the data is realated to IGIS
* End with 3 letter keywords
  * ex. IGISDFS: IGIS D-Lab Fund Service
  * ex. IGISGEO: IGIS Asset's geographical features

* Else follow
* [4 letter words for source] + [3 letter keywords]
  * ex. WSFNIDX: WiseFn Index Information
  * ex. BLBGMAC: Bloomberg Macro Data
  * ex. REIKMAC: Reuter Eikon Macro Data 

</p>


#### Table Name and Table Column Name.

<p>

Table name should be written like so.

* All capital letters
* "_" to substitute " " (blank spaces)
  * ex LENDER_BENEFICIARY

</p>

