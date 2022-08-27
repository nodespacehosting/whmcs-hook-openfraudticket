# WHMCS Hook - Open Fraud Ticket
If you want to open a ticket for a client who places an order and they do not pass fraud check, this hook will help you out. 

Just upload it to `/your/path/to/whmcs/includes/hooks/` and then modify the variables at the top:

```
    $adminuser = 'api'; // This should be the username of an admin account that exists.
    $fraud_ticket_department_id = '3'; // This should be a department ID.
    $add_ticket_note = true; // Do you want a note added to the ticket? If not, set to false.
    $ticket_note_to_admins = "Please carefully review order ID $order_id. If client doesn't reply, cancel the order.";
    $ticket_subject = "Your order was marked as fraud"; 
    $ticket_priority = "High"; // "High", "Medium", "Low"
    $ticket_message = "
Hello,

We detected some unusual activity when you placed your order and we marked it as fraud.

Possible reasons for this include:
- You ordered using a proxy or VPN service or you're using another hosting provider's network as a VPN.
- You provided false or incorrect details such as name, address, or phone number.
- The name on your payment method doesn't match the name you provided us.

Things you can try doing:
- Disable your proxy or VPN and place your order again.
- Provide your real information.
- Have the person who owns the payment method you're trying to use place the order under their name.

If none of the suggestions work or apply, please **not** place any additional orders. One of our staff will help you soon.

Thank you!";
```
`$ticket_message` can contain markdown formatting if you want to format it. 

# License
 Copyright (C) 2022 Xinsto, LLC dba NodeSpace Hosting. All rights reserved.
 Author: Travis Newton <travis.newton@nodespace.net>
 Web: https://www.nodespace.net
 Version: 1.0.0
 
 This program is free software: you can redistribute it and/or modify it
 under the terms of the GNU General Public License as published by the
 Free Software Foundation, either version 3 of the License, or (at your
 option) any later version.
 
 This program is distributed in the hope that it will be useful, but WITHOUT
 ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
 FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
 
 You should have received a copy of the GNU General Public License along with
 this program. If not, see <https://www.gnu.org/licenses/>.


