# Cost Analysis (₹)

This document provides cost estimates for the **Private 5G Network Infrastructure** in **Indian Rupees (₹)**.

## Production Environment

At production scale (enterprise campus deployment), the architecture typically costs:

| Service | Monthly Cost (₹) | Notes |
|---------|------------------|-------|
| **AWS Private 5G** | ₹150,000–250,000 | Network subscription |
| **Radio Units** | ₹50,000–100,000 | Per radio unit lease |
| **SIM Management** | ₹10,000–20,000 | Device provisioning |
| **IoT Core** | ₹15,000–30,000 | Device connectivity |
| **Wavelength** | ₹40,000–80,000 | Edge compute (optional) |
| **CloudWatch** | ₹5,000–10,000 | Network monitoring |
| **Total** | **₹270,000–490,000** | ~$3,375–6,125/month |

## Hardware Costs (One-Time)

| Component | Cost (₹) | Notes |
|-----------|----------|-------|
| Radio Unit | ₹8,00,000–15,00,000 | Per unit |
| SIM Cards | ₹500–1,000 | Per device |
| Installation | ₹5,00,000–10,00,000 | Professional services |

## Per-Device Costs

| Device Type | Monthly Cost (₹) | Notes |
|-------------|------------------|-------|
| IoT Sensor | ₹200–500 | Low bandwidth |
| Mobile Device | ₹500–1,000 | Standard usage |
| AGV/Robot | ₹1,000–2,000 | High bandwidth |
| AR/VR Device | ₹2,000–4,000 | Ultra-low latency |

## Cost Optimization Strategies

- **Network slicing** – Optimize QoS per use case
- **Device density planning** – Right-size radio coverage
- **Shared spectrum** – Use CBRS where available
- **Edge compute placement** – Reduce backhaul costs
- **Traffic optimization** – Local breakout for internal traffic

## Related Documentation

See the project README for architecture details.md` for installation guide.
