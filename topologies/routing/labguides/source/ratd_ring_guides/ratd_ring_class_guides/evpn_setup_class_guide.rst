Prepare to Offer VPN Services to Customers via MP-BGP EVPN Control-Plane
==================================================================================

.. image:: ../../images/ratd_ring_images/ratd_ring_evpn.png
   :align: center

|

#. BGP Autonomous System 100 is leveraged by the Service Provider

   :Question: Do all nodes within the Service Provider need to run BGP? Why, or why not?

#. Enable BGP EVPN peering within the service provider

   - BGP Router-ID should be Loopback0 with a 32-bit value

   - Loopback0 IP address should be used for all BGP peerings

   - All PE nodes must be capable of advertising and receiving reachability information to/from all other PE nodes

   - A full mesh of peerings must not be used to accomplish this task

   - EOS8 should act as the peering point for all PE nodes

   - Disable any unnecessary BGP AFI/SAFI peerings
   
   - Use MPLS as the data-plane encapsulation / VPN label distribution