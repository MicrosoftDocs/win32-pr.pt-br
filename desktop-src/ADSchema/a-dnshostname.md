---
title: Atributo DNS-Host-Name
description: Nome do computador como registrado no DNS.
ms.assetid: ba655adb-cb70-47f2-820f-c5b0749d3e70
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo DNS-Host-Name
- Esquema do AD do atributo dNSHostName
topic_type:
- apiref
api_name:
- DNS-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241ea7144db7895e521c2844627d77b2f0ce54b5da518d180c87c6e9f834140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085956"
---
# <a name="dns-host-name-attribute"></a>Atributo DNS-Host-Name

Nome do computador como registrado no DNS.



| Entrada | Valor |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Nome do host DNS                                                               |
| Ldap-Display-Name | dNSHostName                                                                 |
| Tamanho              | Cada segmento pode ter 63 caracteres. O comprimento inteiro pode ter 255 caracteres. |
| Privilégio de atualização  | Administrador de domínio                                                        |
| Frequência de atualização  | Quando o computador é nomeado.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.619                                                      |
| System-Id-Guid    | 72e39547-7b18-11d1-adef-00c04fd8d5cd                                        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                 |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                      |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2.048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> [**Computador**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                      |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2.048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> [**Computador**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| Tem valor único       | Verdadeiro                                  |
| É indexado             | Falso                                 |
| No Catálogo Global      | Verdadeiro                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                          |
| Range-Lower            | 0                                     |
| Range-Upper            | 2.048                                  |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Classes usadas em        | [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                      |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2.048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> [**Computador**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                      |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2.048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> [**Computador**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                      |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2.048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> [**Computador**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                                                                      |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2.048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Classes usadas em        | [**Autoridade de Certificação**](c-certificationauthority.md)<br/> [**Computador**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



 

 





