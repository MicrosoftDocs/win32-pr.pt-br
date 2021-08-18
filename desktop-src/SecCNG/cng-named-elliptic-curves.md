---
description: A partir do Windows 10, o CNG fornece suporte para as seguintes curvas elípticas nomeadas (ANSI X9.62, X9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: Curvas elípticas nomeadas CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691f1211b56abc41d622d20857653723be37681014a9bf72b91c1384c8f4b8cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908247"
---
# <a name="cng-named-elliptic-curves"></a>Curvas elípticas nomeadas em CNG

A partir do Windows 10, o CNG fornece suporte para as seguintes curvas elípticas nomeadas (ANSI X9.62, X9.63, FIPS 186-2).

<dl> <dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ECC \_ CURVE \_ 25519**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------|
| Nome              | curve25519                                                  |
| Standard          | [Curva 25519](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| Tamanho da chave (bits)   | 255                                                         |
| Capacidade para TLS       |                                                             |
| Identificador de objeto | Nenhum                                                        |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP160R1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP160r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 160                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.1                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP160T1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP160t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 160                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.2                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP192R1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP192r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 192                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.3                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP192T1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP192t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 192                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.4                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP224R1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP224r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 224                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.5                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP224T1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP224t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 224                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.6                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP256R1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP256r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 256                                                                                                               |
| Capacidade para TLS       | Sim                                                                                                               |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.7                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP256T1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP256t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 256                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.8                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP320R1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP320r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 320                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.9                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP32 0T1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP320t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 320                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.10                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP384R1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP384r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 384                                                                                                               |
| Capacidade para TLS       | Sim                                                                                                               |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.11                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP384T1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP384t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 384                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.12                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP512R1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP512r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 512                                                                                                               |
| Capacidade para TLS       | Sim                                                                                                               |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.13                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP512T1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nome              | brainpoolP512t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamanho da chave (bits)   | 512                                                                                                               |
| Capacidade para TLS       | Não                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.14                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ ECC \_ CURVE \_ EC192WAPI**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|----------------------------------------------------------------|
| Nome              | ec192wapi                                                      |
| Standard          | Chinês nacional padrão para LANs sem fio (GB 15629.11-2003) |
| Tamanho da chave (bits)   | 192                                                            |
| Compatível com TLS       | Não                                                             |
| Identificador de objeto | 1.2.156.11235.1.1.2.1                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**\_NISTP192 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nome              | nistP192                                                                                                                     |
| Standard          | [Curvas elípticas recomendadas para uso do governo federal](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Tamanho da chave (bits)   | 192                                                                                                                          |
| Compatível com TLS       | Sim                                                                                                                          |
| Identificador de objeto | 1.2.840.10045.3.1.1                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ \_ \_ NISTP224 de curva ECC**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nome              | nistP224                                                                                                                     |
| Standard          | [Curvas elípticas recomendadas para uso do governo federal](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Tamanho da chave (bits)   | 224                                                                                                                          |
| Compatível com TLS       | Sim                                                                                                                          |
| Identificador de objeto | 1.3.132.0.33                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**\_NISTP256 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nome              | nistP256                                                                                                                     |
| Standard          | [Curvas elípticas recomendadas para uso do governo federal](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Tamanho da chave (bits)   | 256                                                                                                                          |
| Compatível com TLS       | Sim                                                                                                                          |
| Identificador de objeto | 1.2.840.10045.3.1.7                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ \_ \_ NISTP384 de curva ECC**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nome              | nistP384                                                                                                                     |
| Standard          | [Curvas elípticas recomendadas para uso do governo federal](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Tamanho da chave (bits)   | 384                                                                                                                          |
| Compatível com TLS       | Sim                                                                                                                          |
| Identificador de objeto | 1.3.132.0.34                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**\_NISTP521 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nome              | nistP521                                                                                                                     |
| Standard          | [Curvas elípticas recomendadas para uso do governo federal](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Tamanho da chave (bits)   | 521                                                                                                                          |
| Compatível com TLS       | Sim                                                                                                                          |
| Identificador de objeto | 1.3.132.0.35                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ \_ \_ NUMSP256T1 de curva ECC**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nome              | numsP256t1                                                                                                                              |
| Standard          | [Especificação de seleção de curva e parâmetros de curva com suporte no ECCLib MSR](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Tamanho da chave (bits)   | 256                                                                                                                                     |
| Compatível com TLS       | Não                                                                                                                                      |
| Identificador de objeto | Nenhum                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ \_ \_ NUMSP384T1 de curva ECC**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nome              | numsP384t1                                                                                                                              |
| Standard          | [Especificação de seleção de curva e parâmetros de curva com suporte no ECCLib MSR](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Tamanho da chave (bits)   | 384                                                                                                                                     |
| Compatível com TLS       | Não                                                                                                                                      |
| Identificador de objeto | Nenhum                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**\_NUMSP512T1 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nome              | numsP512t1                                                                                                                              |
| Standard          | [Especificação de seleção de curva e parâmetros de curva com suporte no ECCLib MSR](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Tamanho da chave (bits)   | 512                                                                                                                                     |
| Compatível com TLS       | Não                                                                                                                                      |
| Identificador de objeto | Nenhum                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ \_ \_ SECP160K1 de curva ECC**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP160k1                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 160                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.3.132.0.9                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 de curva ECC**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP160r1                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 160                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.3.132.0.8                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ \_ SECP160R1 de curva ECC**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP160r2                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 160                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.3.132.0.30                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**\_SECP192K1 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP192k1                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 192                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.3.132.0.31                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ \_ \_ SECP192R1 de curva ECC**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP192r1                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 192                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.2.840.10045.3.1.1                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**\_SECP224K1 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP224k1                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 224                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.3.132.0.32                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**\_SECP224R1 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP224r1                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 224                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.3.132.0.33                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**\_SECP256K1 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP256k1                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 256                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.3.132.0.10                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**\_SECP256R1 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP256r1                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 256                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.2.840.10045.3.1.7                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ \_ \_ SECP384R1 de curva ECC**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP384r1                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 384                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.3.132.0.34                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**\_SECP521R1 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| Nome              | secP521r1                                                                       |
| Standard          | [Parâmetros de domínio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamanho da chave (bits)   | 521                                                                             |
| Compatível com TLS       | Sim                                                                             |
| Identificador de objeto | 1.3.132.0.35                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**\_WTLS12 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|--------------|
| Nome              | wtls12       |
| Standard          | WTLS         |
| Tamanho da chave (bits)   | 224          |
| Compatível com TLS       | Não           |
| Identificador de objeto | 1.3.132.0.33 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**\_WTLS7 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|--------------|
| Nome              | wtls7        |
| Standard          | WTLS         |
| Tamanho da chave (bits)   | 160          |
| Compatível com TLS       | Não           |
| Identificador de objeto | 1.3.132.0.30 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ \_ \_ WTLS9 de curva ECC**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------|
| Nome              | wtls9         |
| Standard          | WTLS          |
| Tamanho da chave (bits)   | 160           |
| Compatível com TLS       | Não            |
| Identificador de objeto | 2.23.43.1.4.9 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**\_X962P192V1 de \_ curva de ECC BCRYPT \_**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------|
| Nome              | x962P192v1          |
| Standard          | ANSI X9.62          |
| Tamanho da chave (bits)   | 192                 |
| Capacidade para TLS       | Não                  |
| Identificador de objeto | 1.2.840.10045.3.1.1 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ CURVA ECC \_ \_ X962P192V2**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------|
| Nome              | x962P192v2          |
| Standard          | ANSI X9.62          |
| Tamanho da chave (bits)   | 192                 |
| Capacidade para TLS       | Não                  |
| Identificador de objeto | 1.2.840.10045.3.1.2 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P192V3**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------|
| Nome              | x962P192v3          |
| Standard          | ANSI X9.62          |
| Tamanho da chave (bits)   | 192                 |
| Capacidade para TLS       | Não                  |
| Identificador de objeto | 1.2.840.10045.3.1.3 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ CURVA ECC \_ \_ X962P239V1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------|
| Nome              | x962P239v1          |
| Standard          | ANSI X9.62          |
| Tamanho da chave (bits)   | 239                 |
| Capacidade para TLS       | Não                  |
| Identificador de objeto | 1.2.840.10045.3.1.4 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ CURVA ECC \_ \_ X962P239V2**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------|
| Nome              | x962P239v2          |
| Standard          | ANSI X9.62          |
| Tamanho da chave (bits)   | 239                 |
| Capacidade para TLS       | Não                  |
| Identificador de objeto | 1.2.840.10045.3.1.5 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ CURVA ECC \_ \_ X962P239V3**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------|
| Nome              | x962P239v3          |
| Standard          | ANSI X9.62          |
| Tamanho da chave (bits)   | 239                 |
| Capacidade para TLS       | Não                  |
| Identificador de objeto | 1.2.840.10045.3.1.6 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P256V1**</dt> <dd> <dl> <dt> 

| Requisito | Valor |
|-------------------|---------------------|
| Nome              | x962P256v1          |
| Standard          | ANSI X9.62          |
| Tamanho da chave (bits)   | 256                 |
| Capacidade para TLS       | Não                  |
| Identificador de objeto | 1.2.840.10045.3.1.7 |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Para usar uma curva nomeada, chame [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) usando o ALGORITMO **\_ \_ ECDSA BCRYPT** ou o **ALGORITMO \_ ECDH \_ BCRYPT** como a ID do algoritmo. Em seguida, [**chame BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) e delimita a propriedade **BCRYPT \_ ECC \_ CURVE \_ NAME** como uma das curvas acima ou quaisquer curvas nomeadas registradas no computador, conforme mostrado pelo `certutil -displayEccCurve` comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




