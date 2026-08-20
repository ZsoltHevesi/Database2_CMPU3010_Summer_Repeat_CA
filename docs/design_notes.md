# Design Notes

## Schema modifications and justifications
I modified the schemas first by renaming the "**amounts**" attribute in payments to "**payment_amount**" as it seemed less vague than just "**amount**".

My second modification was to add the "**late_fees**" attribute to **rentals**, as it seemed practical in a rental business setting.

The constraints added were NOT NULL constraints to the **customer_id** references in **rentals** and **payments**.
This is because without it, a NULL customer_id means there are payments or rentals attributed to no one, which is not a valid business state.

## Dataset expansion
Using [Mockaroo.com](https://mockaroo.com/), I generated additional records for customers, payments and rentals, along with the "**late_fees**" attribute to rentals.
