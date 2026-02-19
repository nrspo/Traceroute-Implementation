# Traceroute Implementation in Python 3.13

This project is a traceroute tool created from a raw socket ping implementation in Python 3.13. For simplicity, the project does not strictly adhere to the official RFC 1739 specification.

## Project Specifications
### Update the __validateIcmpReplyPacketWithOriginalPingData() function
- Validate received sequence number, packet identifier, and raw data.
- Set the valid data variable in the IcmpPacket_EchoReply class based on the outcome of the data comparison.
- Create getter methods to more easily track validation of data points

### Update the printResultToConsole() function
- Identify valid responses and report error details
- Report min, max, and average RTTs and packet loss rate
- Modify ping functionality to parse error codes (type 0, 3, 11) and display the corresponding error results

### Implement traceroute functionality
- update the __sendIcmpTraceRoute() function to handle sending ICMP echo requests with increasing TTL values and processing the responses to trace the route to the destination
    - Check the hops, RTTs, types, codes, and IP addresses.
    - Must show type 3 and type 11 error messages.

## Sources Cited
- Oregon State University CS372 Icmp_Helper_Library skeleton code.