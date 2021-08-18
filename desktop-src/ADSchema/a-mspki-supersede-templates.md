---
title: MS-PKI-precedência-atributo-templates
description: Especifica os nomes dos modelos de certificado que são substituídos pelo modelo atual.
ms.assetid: 4e247932-1c50-4bfb-b723-52b7c36a8571
ms.tgt_platform: multiple
keywords:
- MS-PKI-precedência-templates atributo AD Schema
- msPKI-esquema de atributos do atributo de substituição-modelos
topic_type:
- apiref
api_name:
- ms-PKI-Supersede-Templates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12fbda25794dfe75e7f75fce4c2796cabca00e26697f7321f9edec46276e874a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803056"
---
# <a name="ms-pki-supersede-templates-attribute"></a>MS-PKI-precedência-atributo-templates

Especifica os nomes dos modelos de certificado que são substituídos pelo modelo atual.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------------------------------|
| CN                | MS-PKI-precedência-modelos                                                                        |
| LDAP-Display-Name | msPKI-substituir-modelos                                                                         |
| Tamanho              | 64 bytes                                                                                          |
| Privilégio de atualização  | Administrador de domínio                                                                              |
| Frequência de atualização  | Quando o modelo de certificado (MS-PKI-Certificate-template) é editado, criado ou clonado. |
| Attribute-Id      | 1.2.840.113556.1.4.1437                                                                           |
| System-ID-GUID    | 9de8ae7d-7a5b-421d-b5e4-061f79dfd5d7                                                              |
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
| Tem valor único       | Falso                                                                   |
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
| Tem valor único       | Falso                                                                   |
| É indexado             | Falso                                                                   |
| No Catálogo Global      | Falso                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Classes usadas em        | [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> |



 

 





