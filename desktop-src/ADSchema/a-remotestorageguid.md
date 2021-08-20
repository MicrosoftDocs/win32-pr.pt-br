---
title: atributo Remote-Armazenamento-GUID
description: Esse atributo contém o GUID de um objeto de armazenamento remoto.
ms.assetid: 9051666f-539c-4339-8652-3ebdab1af301
ms.tgt_platform: multiple
keywords:
- esquema do AD do atributo Armazenamento-GUID remoto
- Esquema de AD do atributo remoteStorageGUID
topic_type:
- apiref
api_name:
- Remote-Storage-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54b3f00137661f73356a8b0af41ca0f2882b0b0c6b0f5bfb210d185e7a1b3243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118423772"
---
# <a name="remote-storage-guid-attribute"></a>atributo Remote-Armazenamento-GUID

Esse atributo contém o GUID de um objeto de armazenamento remoto.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Armazenamento-GUID remoto                         |
| LDAP-Display-Name | remoteStorageGUID                           |
| Tamanho              | \-                                          |
| Privilégio de atualização  | \-                                          |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.809                      |
| System-ID-GUID    | 2a39c5b0-8960-11d1-aebc-0000f80367c1        |
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
|------------------------|--------------------------------------------------------------------------------|
| ID do link                | \-                                                                             |
| MAPI-Id                | \-                                                                             |
| System-Only            | Falso                                                                          |
| É de valor único       | Verdadeiro                                                                           |
| É indexado             | Falso                                                                          |
| No catálogo global      | Falso                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                   |
| Range-Lower            | \-                                                                             |
| Range-Upper            | \-                                                                             |
| Search-Flags           | 0x00000000                                                                     |
| System-Flags           | 0x00000010                                                                     |
| Classes usadas em        | [**ponto de serviço Armazenamento remoto**](c-remotestorageservicepoint.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------|
| ID do link                | \-                                                                             |
| MAPI-Id                | \-                                                                             |
| System-Only            | Falso                                                                          |
| É de valor único       | Verdadeiro                                                                           |
| É indexado             | Falso                                                                          |
| No catálogo global      | Falso                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                   |
| Range-Lower            | \-                                                                             |
| Range-Upper            | \-                                                                             |
| Search-Flags           | 0x00000000                                                                     |
| System-Flags           | 0x00000010                                                                     |
| Classes usadas em        | [**ponto de serviço Armazenamento remoto**](c-remotestorageservicepoint.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------|
| ID do link                | \-                                                                             |
| MAPI-Id                | \-                                                                             |
| System-Only            | Falso                                                                          |
| É de valor único       | Verdadeiro                                                                           |
| É indexado             | Falso                                                                          |
| No catálogo global      | Falso                                                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                   |
| Range-Lower            | \-                                                                             |
| Range-Upper            | \-                                                                             |
| Search-Flags           | 0x00000000                                                                     |
| System-Flags           | 0x00000010                                                                     |
| Classes usadas em        | [**ponto de serviço Armazenamento remoto**](c-remotestorageservicepoint.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------|
| ID do link                | \-                                                                             |
| MAPI-Id                | \-                                                                             |
| System-Only            | Falso                                                                          |
| Tem valor único       | Verdadeiro                                                                           |
| É indexado             | Falso                                                                          |
| No Catálogo Global      | Falso                                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                   |
| Range-Lower            | \-                                                                             |
| Range-Upper            | \-                                                                             |
| Search-Flags           | 0x00000000                                                                     |
| System-Flags           | 0x00000010                                                                     |
| Classes usadas em        | [**Remote-Armazenamento-Service-Point**](c-remotestorageservicepoint.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------|
| ID do link                | \-                                                                             |
| MAPI-Id                | \-                                                                             |
| System-Only            | Falso                                                                          |
| Tem valor único       | Verdadeiro                                                                           |
| É indexado             | Falso                                                                          |
| No Catálogo Global      | Falso                                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                   |
| Range-Lower            | \-                                                                             |
| Range-Upper            | \-                                                                             |
| Search-Flags           | 0x00000000                                                                     |
| System-Flags           | 0x00000010                                                                     |
| Classes usadas em        | [**Remote-Armazenamento-Service-Point**](c-remotestorageservicepoint.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------|
| ID do link                | \-                                                                             |
| MAPI-Id                | \-                                                                             |
| System-Only            | Falso                                                                          |
| Tem valor único       | Verdadeiro                                                                           |
| É indexado             | Falso                                                                          |
| No Catálogo Global      | Falso                                                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                   |
| Range-Lower            | \-                                                                             |
| Range-Upper            | \-                                                                             |
| Search-Flags           | 0x00000000                                                                     |
| System-Flags           | 0x00000010                                                                     |
| Classes usadas em        | [**Remote-Armazenamento-Service-Point**](c-remotestorageservicepoint.md)<br/> |



 

 





