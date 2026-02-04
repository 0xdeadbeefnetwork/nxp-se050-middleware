● # NXP SE050 Plug & Trust Middleware

  Official NXP middleware for SE050/SE051 secure elements. Version 04.07.01.

  ## What's Included

  - **hostlib/** - Host library for SE05x communication
  - **sss/** - Secure Subsystem API abstraction layer
  - **demos/** - Example applications (SCP03, crypto operations, provisioning)
  - **binaries/** - Pre-built binaries for Raspbian, i.MX, K64F
  - **doc/** - API documentation and application notes
  - **ext/** - External dependencies (mbedTLS, OpenSSL wrappers)

  ## Application Notes (PDFs)

  | Document | Description |
  |----------|-------------|
  | AN12396 | SE05x Host Library API |
  | AN12398 | SE05x Examples & Demos |
  | AN12448 | SE05x SCP03 Secure Channel |
  | AN13013 | SE05x Integration Guide |
  | AN13030 | SE05x for Raspberry Pi |
  | AN13539 | SE05x Trust Provisioning |

  ## Quick Start (Raspberry Pi)

  ```bash
  # Use pre-built Raspbian binaries
  cd binaries/Raspbian/se05x/

  # Or build from source
  mkdir build && cd build
  cmake .. -DPTMW_SE05X=ON -DPTMW_Host=Raspbian
  make -j4

  SCP03 Authentication

  Default keys for SE050E dev kits (rotate for production!):
  - Key Version: 0x0B
  - ENC: D2DB63E7A0A5AED72A6460C4DFDCAF64
  - MAC: 738D5B798ED241B0B24768514BFBA95B

  License

  See LA_OPT_NXP_Software_License.txt

  Links

  - https://www.nxp.com/products/security-and-authentication/authentication/edgelock-se050-plug-trust-secure-element-family:SE050
  - https://www.nxp.com/docs/en/data-sheet/SE050-DATASHEET.pdf
