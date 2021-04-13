---
title: Atributo de fornecedor
description: Esse atributo identifica o fornecedor de um aplicativo.
ms.assetid: af376e9a-ae30-49f5-baff-c888e83688b0
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo de fornecedor
- Esquema de AD do atributo de fornecedor
topic_type:
- apiref
api_name:
- Vendor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39aed7d01c04750e1613615fe0d5f1e21303c291
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499944"
---
# <a name="vendor-attribute"></a>Atributo de fornecedor

Esse atributo identifica o fornecedor de um aplicativo.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Fornecedor                                      |
| LDAP-Display-Name | fornecedor                                      |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.255                      |
| System-ID-GUID    | 281416df-1968-11d0-a28f-00aa003049e2        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 512                                                              |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                       |
| Range-Upper            | 512                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                              |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Ponto de conexão de serviço**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                       |
| Range-Upper            | 512                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                              |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Ponto de conexão de serviço**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                       |
| Range-Upper            | 512                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                              |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Ponto de conexão de serviço**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                       |
| Range-Upper            | 512                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                              |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Ponto de conexão de serviço**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                   |
| É de valor único       | True                                                                                                                                                                                                    |
| É indexado             | Falso                                                                                                                                                                                                   |
| No catálogo global      | Falso                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                       |
| Range-Upper            | 512                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                              |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Registro de pacote**](c-packageregistration.md)<br/> [**Ponto de conexão de serviço**](c-serviceconnectionpoint.md)<br/> |



 

 





