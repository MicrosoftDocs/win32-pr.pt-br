---
title: atributo ms-PKI-RA-Policies
description: Contém a lista de OIDs de política necessária de autoridades de registro que assinam a solicitação de registro.
ms.assetid: ebbdf95e-05c8-4b54-b7a5-4bb81d425225
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-PKI-RA-Policies
- atributo msPKI-RA-Policies do AD Schema
topic_type:
- apiref
api_name:
- ms-PKI-RA-Policies
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b948dac7a95ae8b46972ace4d1ab46260b476da
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919597"
---
# <a name="ms-pki-ra-policies-attribute"></a>atributo ms-PKI-RA-Policies

Contém a lista de OIDs de política necessária de autoridades de registro que assinam a solicitação de registro.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------------------------------|
| CN                | MS-PKI-RA-Policies                                                                                |
| LDAP-Display-Name | msPKI-RA-Policies                                                                                 |
| Tamanho              | 64 bytes vezes o número de entradas.                                                             |
| Privilégio de atualização  | Administrador de domínio                                                                              |
| Frequência de atualização  | Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado. |
| Attribute-Id      | 1.2.840.113556.1.4.1438                                                                           |
| System-ID-GUID    | d546ae22-0951-4d47-817e-1c9f96faad46                                                              |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                                       |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------|
| ID do link                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| É de valor único       | Falso                                                                   |
| É indexado             | Falso                                                                   |
| No catálogo global      | Falso                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Classes usadas em        | [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------|
| ID do link                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| É de valor único       | Falso                                                                   |
| É indexado             | Falso                                                                   |
| No catálogo global      | Falso                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Classes usadas em        | [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------|
| ID do link                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| É de valor único       | Falso                                                                   |
| É indexado             | Falso                                                                   |
| No catálogo global      | Falso                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Classes usadas em        | [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------|
| ID do link                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| É de valor único       | Falso                                                                   |
| É indexado             | Falso                                                                   |
| No catálogo global      | Falso                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Classes usadas em        | [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------|
| ID do link                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| É de valor único       | Falso                                                                   |
| É indexado             | Falso                                                                   |
| No catálogo global      | Falso                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Classes usadas em        | [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> |



 

 





