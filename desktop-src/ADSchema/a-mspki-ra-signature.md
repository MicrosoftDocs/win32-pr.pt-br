---
title: atributo ms-PKI-RA-Signature
description: Especifica o número de assinaturas de autoridade de registro de registro que são necessárias em uma solicitação de registro.
ms.assetid: da9d9357-6826-4511-b589-594c73114713
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-PKI-RA-Signature
- msPKI-RA-atributo de assinatura esquema do AD
topic_type:
- apiref
api_name:
- ms-PKI-RA-Signature
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870e10809d346fa8776da7a101bb406041be75822c62ded19f1c1f9823ffce7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761766"
---
# <a name="ms-pki-ra-signature-attribute"></a>atributo ms-PKI-RA-Signature

Especifica o número de assinaturas de autoridade de registro de registro que são necessárias em uma solicitação de registro.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------------------------------|
| CN                | MS-PKI-RA-Signature                                                                               |
| LDAP-Display-Name | msPKI-RA-Signature                                                                                |
| Tamanho              | 4 bytes                                                                                           |
| Privilégio de atualização  | Administrador de domínio                                                                              |
| Frequência de atualização  | Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado. |
| Attribute-Id      | 1.2.840.113556.1.4.1429                                                                           |
| System-ID-GUID    | fe17e04b-937d-4f7e-8e0e-9292c8d5683e                                                              |
| Syntax            | [**Enumeração**](s-enumeration.md)                                                              |



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
| É de valor único       | Verdadeiro                                                                    |
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
| É de valor único       | Verdadeiro                                                                    |
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
| É de valor único       | Verdadeiro                                                                    |
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
| Tem valor único       | Verdadeiro                                                                    |
| É indexado             | Falso                                                                   |
| No Catálogo Global      | Falso                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Classes usadas em        | [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------|
| ID do link                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| Tem valor único       | Verdadeiro                                                                    |
| É indexado             | Falso                                                                   |
| No Catálogo Global      | Falso                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Classes usadas em        | [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> |



 

 





