# Troubleshooting

Common issues and resolutions for the **Private 5G Network Infrastructure**.

## Radio Issues

### 1. Radio Unit Offline

**Symptom:** Radio unit shows offline in console.

**Resolution:**
- Check power connection
- Verify backhaul network connectivity
- Check for hardware faults
- Review radio unit logs
- Contact AWS support if persistent

### 2. Poor Coverage

**Symptom:** Devices have weak signal in certain areas.

**Resolution:**
- Review site survey and radio placement
- Check for physical obstructions
- Consider additional radio units
- Adjust antenna orientation
- Review interference sources

### 3. Radio Interference

**Symptom:** Intermittent connectivity, high error rates.

**Resolution:**
- Scan for interfering signals
- Adjust channel/frequency if possible
- Check for nearby equipment interference
- Review spectrum allocation

## Device Issues

### 4. Device Cannot Connect

**Symptom:** Device fails to attach to network.

**Resolution:**
- Verify SIM is activated
- Check device is in coverage area
- Verify device supports frequency band
- Check SIM is properly inserted
- Review device APN settings

### 5. Device Authentication Failure

**Symptom:** Device rejected during authentication.

**Resolution:**
- Verify SIM credentials are correct
- Check SIM is not blocked
- Review network access policies
- Check device certificate validity

### 6. Slow Data Speeds

**Symptom:** Throughput lower than expected.

**Resolution:**
- Check signal strength (RSRP/RSRQ)
- Review network slice QoS settings
- Check for network congestion
- Verify device capabilities
- Test with different device

## Network Issues

### 7. High Latency

**Symptom:** Application latency exceeds requirements.

**Resolution:**
- Check backhaul network latency
- Review network slice configuration
- Consider edge compute (Wavelength)
- Optimize application placement
- Check for congestion

### 8. Network Slice Not Working

**Symptom:** QoS policies not being applied.

**Resolution:**
- Verify slice configuration
- Check device is assigned to slice
- Review QoS flow rules
- Check slice capacity limits

## Integration Issues

### 9. IoT Core Connection Failure

**Symptom:** Devices cannot reach IoT Core.

**Resolution:**
- Verify VPC connectivity
- Check security group rules
- Review IoT Core policies
- Test with AWS CLI from VPC

### 10. Wavelength Latency High

**Symptom:** Edge compute not reducing latency.

**Resolution:**
- Verify traffic is routing to Wavelength
- Check application is deployed to edge
- Review network path
- Consider carrier zone placement

> For architecture details, see `ARCHITECTURE.md`.
