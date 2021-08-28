---
title: Atributo de localização
description: A localização do usuário, como o número do escritório.
ms.assetid: 3ee97a61-6dce-4f41-b03a-a475706f3cbd
ms.tgt_platform: multiple
keywords:
- Atributo de local esquema do AD
- atributo de local esquema do AD
topic_type:
- apiref
api_name:
- Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7e8080ffa24c9b2a147e6e3ec76f586a92fba3456aa1f80d2875c1292940232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705766"
---
# <a name="location-attribute-ad-schema"></a>Atributo Location (esquema do AD)

A localização do usuário, como o número do escritório.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Localização                                    |
| LDAP-Display-Name | local                                    |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.222                      |
| System-ID-GUID    | 09dcb79f-165f-11d0-a064-00aa006c33ed        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                            |
| É de valor único       | Verdadeiro                                                                                                                                                             |
| É indexado             | Verdadeiro                                                                                                                                                             |
| No catálogo global      | Verdadeiro                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                |
| Range-Upper            | 1024                                                                                                                                                             |
| Search-Flags           | 0x00000001                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                       |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Fila de impressão**](c-printqueue.md)<br/> [**Site**](c-site.md)<br/> [**Sub-rede**](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| É de valor único       | Verdadeiro                                                                                                                                                                                               |
| É indexado             | Verdadeiro                                                                                                                                                                                               |
| No catálogo global      | Verdadeiro                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Fila de impressão**](c-printqueue.md)<br/> [**espaço**](c-room.md)<br/> [**Site**](c-site.md)<br/> [**Sub-rede**](c-subnet.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------|
| ID do link                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| É de valor único       | Verdadeiro                                                                    |
| É indexado             | Verdadeiro                                                                    |
| No catálogo global      | Verdadeiro                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                            |
| Range-Lower            | 0                                                                       |
| Range-Upper            | 1024                                                                    |
| Search-Flags           | 0x00000001                                                              |
| System-Flags           | 0x00000010                                                              |
| Classes usadas em        | [**Site**](c-site.md)<br/> [**Sub-rede**](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| É de valor único       | Verdadeiro                                                                                                                                                                                               |
| É indexado             | Verdadeiro                                                                                                                                                                                               |
| No catálogo global      | Verdadeiro                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Fila de impressão**](c-printqueue.md)<br/> [**espaço**](c-room.md)<br/> [**Site**](c-site.md)<br/> [**Sub-rede**](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| É de valor único       | Verdadeiro                                                                                                                                                                                               |
| É indexado             | Verdadeiro                                                                                                                                                                                               |
| No catálogo global      | Verdadeiro                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Fila de impressão**](c-printqueue.md)<br/> [**espaço**](c-room.md)<br/> [**Site**](c-site.md)<br/> [**Sub-rede**](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| É de valor único       | Verdadeiro                                                                                                                                                                                               |
| É indexado             | Verdadeiro                                                                                                                                                                                               |
| No catálogo global      | Verdadeiro                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Fila de impressão**](c-printqueue.md)<br/> [**espaço**](c-room.md)<br/> [**Site**](c-site.md)<br/> [**Sub-rede**](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| É de valor único       | Verdadeiro                                                                                                                                                                                               |
| É indexado             | Verdadeiro                                                                                                                                                                                               |
| No catálogo global      | Verdadeiro                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Fila de impressão**](c-printqueue.md)<br/> [**espaço**](c-room.md)<br/> [**Site**](c-site.md)<br/> [**Redes**](c-subnet.md)<br/> |



 

 





