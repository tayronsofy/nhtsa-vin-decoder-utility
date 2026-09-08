# NHTSA VIN Decoder Utility

A lightweight JavaScript / TypeScript helper to validate standard 17-character North American Vehicle Identification Numbers (VIN), calculate the mathematical check-digit, and query vehicle specifications from the official NHTSA vPIC public API.

## Features

- **17-Character Standard Validation:** Rejects malformed strings and invalid characters (I, O, Q).
- **Check-Digit Verification:** Implements standard ISO 3779 / US Federal check-digit weighting.
- **NHTSA vPIC Integration:** Normalizes public endpoints for Year, Make, Model, Body Class, Trim, and Engine Displacement.

## Quick Start

```bash
git clone [https://github.com/tayronsofy/nhtsa-vin-decoder-utility.git](https://github.com/tayronsofy/nhtsa-vin-decoder-utility.git)
cd nhtsa-vin-decoder-utility
npm install

import { decodeVIN } from './decoder.js';

const vehicle = await decodeVIN('1HGCR2F83HA000000');
console.log(vehicle);
// Output: { make: 'HONDA', model: 'Accord', year: 2017, trim: 'EX-L' }
