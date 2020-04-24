# Bloom-Economy-Plugin

Economy/Tax System by Fisher
* The market: Accessed by /market, gives a value to each survival item obtainable relative to a diamond upon the initiation of the plugin by a quadratic formula (#More information in Magic.pdf)
* The Tax system: Forces players to participate in the economy. Seen by “/tax”, which gives the time the next tax is due/the amount you owe. The tax is separated into 5 different types.
A. Life tax, the only tax which is applied to everyone without exception. Value of 1000.
B. Death tax, a tax forced onto players who have died with the exception of witches. Value of 2000
C. Income tax, contrary to what it sounds like, it only affects one if at the time of the payment, they have items
in their income box. Value of income box over 3.
D. Transaction fees, they aren’t taxes but still apply in the same way. Value of the sum of all the transactions
you’ve sent multiplied by 0.1.
E. Receivers fee, this fee heavily depends on the transaction system and will be explained in a following part.
Value varies.
Players have two chances to pay of their taxes per 6 hour session. Once they fail to pay twice in a row, they are announced as witches and their location is given by “/witch”, and for two hours they can be hunted, and once killed, the killer receives 8 diamond blocks and the witch hunt on the victim ends, decreasing their due date to 12 hours.
* The deposit box: Accessed by typing “/dep” players open their deposit box where they deposit the items they are willing to give away in exchange for transactions with other players or so as to have their taxes payed. To see the value of one’s deposit value type “/bal”.
* The income box: Accessed by typing “/inc”, shows the items you’ve received through transactions.
* The transaction system: Used by typing “/send RECEIVER_PLAYER amount_in_value“It took quite a while to figure out, but a solution was found. The trouble was the if a player had, as an example, only nether stars, and had to pay for something very cheap, like a piece of wood, I didn’t know what to do. How do we create half an item? Well, I decided on the following, that which could be payed out with whole items would be payed, and for the remainder, we find the largest item that the sending player has in their deposit box and we assign a dividing factor to it of x, which would make its price smaller. Then we send a copy of that WHOLE item to the receiver, however, we also append the receiver fee to the receiver so as to compensate for their unfair gain. As in our example, suppose the sender sends a value of 5 to the receiver, however, the sender’s deposit box is filed up with diamonds, which are generally more than just 5 in value. So we add a dividing factor to one of those diamonds, decreasing its worth, and we send a whole diamond to the receiver, as well as the receiver fee of the diamond's market value minus that value divided by the dividing factor. And just like that, an economy functions based of items.
TLDR: Tax/economy system which took way to long to make.
