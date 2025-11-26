# Runbook

Operational guide for deploying and managing the **Private 5G Network Infrastructure**.

## 1. Deployment

### Prerequisites

- AWS Private 5G service access approved
- Site survey completed
- Spectrum allocation confirmed
- Physical installation planned

### Deploy Steps

```bash
# Install dependencies
npm install

# Bootstrap CDK
cdk bootstrap

# Deploy network infrastructure
cdk deploy --context environment=prod
```

## 2. Network Setup

### Create Private 5G Network

1. Request network in AWS Console
2. Configure network settings (PLMN, TAC)
3. Order radio units
4. Plan coverage areas

### Radio Unit Installation

1. Mount radio units per site survey
2. Connect to power and backhaul
3. Activate in AWS Console
4. Verify coverage

## 3. Device Onboarding

### Provision SIM Cards

```bash
# Order SIMs via AWS Console or API
aws private-networks create-device-identifier \
  --network-arn arn:aws:private-networks:... \
  --device-identifier-type IMSI
```

### Activate Device

1. Insert SIM into device
2. Device authenticates to network
3. Verify connectivity
4. Assign to network slice

## 4. Network Slicing

### Create Network Slice

```yaml
# Example slice configuration
slice:
  name: "iot-sensors"
  sst: 1  # eMBB
  qos:
    5qi: 9  # Best effort
    bandwidth: 10Mbps
```

### Assign Devices to Slice

- Group devices by use case
- Apply QoS policies
- Monitor slice performance

## 5. Monitoring

### Key Metrics to Watch

- **Radio metrics**: RSRP, RSRQ, SINR
- **Network metrics**: Throughput, latency
- **Device metrics**: Connection status, data usage
- **Slice metrics**: QoS compliance

### Dashboards

Pre-configured dashboards for:

- Network coverage map
- Device connectivity
- Slice performance
- Capacity planning

## 6. Maintenance

### Regular Tasks

- Monitor radio unit health weekly
- Review device inventory monthly
- Update firmware as released
- Audit security policies quarterly

### Troubleshooting Device Issues

```bash
# Check device status
aws private-networks get-device-identifier \
  --device-identifier-arn arn:aws:...
```

### Teardown

```bash
cdk destroy --context environment=dev
```

> For troubleshooting common issues, see `docs/troubleshooting.md`.
