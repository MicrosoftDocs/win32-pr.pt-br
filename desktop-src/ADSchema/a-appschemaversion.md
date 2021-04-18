---
title: Aplicativo-esquema-versão do atributo
description: Esse atributo armazena a versão do esquema do repositório de classe. Ele é usado para fornecer o comportamento correto entre alterações de esquema.
ms.assetid: e8c2ab2b-1b7f-4d4f-b9ea-4116a8e30277
ms.tgt_platform: multiple
keywords:
- App-esquema-Version atributo AD Schema
- Esquema de AD do atributo appSchemaVersion
topic_type:
- apiref
api_name:
- App-Schema-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09265299a676ef6b9d319153c7efdbe3929ee883
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105771721"
---
# <a name="app-schema-version-attribute"></a>Aplicativo-esquema-versão do atributo

Esse atributo armazena a versão do esquema do repositório de classe. Ele é usado para fornecer o comportamento correto entre alterações de esquema.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Versão de esquema de aplicativo                   |
| LDAP-Display-Name | appSchemaVersion                     |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.848               |
| System-ID-GUID    | 96a7dd65-9118-11d1-aebc-0000f80367c1 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------|
| ID do link                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Falso                                          |
| É de valor único       | True                                           |
| É indexado             | Falso                                          |
| No catálogo global      | Falso                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                   |
| Range-Lower            | \-                                             |
| Range-Upper            | \-                                             |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Classes usadas em        | [**Armazenamento de classe**](c-classstore.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Armazenamento de classe**](c-classstore.md)<br/> [**Ponto de conexão de serviço**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Armazenamento de classe**](c-classstore.md)<br/> [**Ponto de conexão de serviço**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Armazenamento de classe**](c-classstore.md)<br/> [**Ponto de conexão de serviço**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Armazenamento de classe**](c-classstore.md)<br/> [**Ponto de conexão de serviço**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| Classes usadas em        | [**Versão do aplicativo**](c-applicationversion.md)<br/> [**Armazenamento de classe**](c-classstore.md)<br/> [**Ponto de conexão de serviço**](c-serviceconnectionpoint.md)<br/> |



 

 





