---
title: Tombstone-Lifetime atributo
description: O número de dias antes que um objeto excluído seja removido dos serviços de diretório.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Esquema de Tombstone-Lifetime do atributo AD
- Esquema de AD do atributo tombstoneLifetime
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c96d440b82f488e7968f787ae52d9f431350bee6050bd50b385f5751f51e76a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644946"
---
# <a name="tombstone-lifetime-attribute"></a>Tombstone-Lifetime atributo

O número de dias antes que um objeto excluído seja removido dos serviços de diretório. Isso ajuda a remover objetos de servidores replicados e a impedir que as restaurações reintroduzam um objeto excluído. Esse valor está no objeto de serviço de diretório na NIC de configuração.



| Entrada | Valor |
|-------------------|-----------------------------------------------------------|
| CN                | Tombstone-Lifetime                                        |
| LDAP-Display-Name | tombstoneLifetime                                         |
| Tamanho              | 4 bytes. O padrão é 60 dias quando nenhum valor é inserido. |
| Privilégio de atualização  | \-                                                        |
| Frequência de atualização  | \-                                                        |
| Attribute-Id      | 1.2.840.113556.1.2.54                                     |
| System-ID-GUID    | 16c3a860-1273-11d0-a060-00aa006c33ed                      |
| Syntax            | [**Enumeração**](s-enumeration.md)                      |



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
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| É de valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| É de valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| É de valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Tem valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Tem valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Tem valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Tem valor único       | Verdadeiro                                             |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



 

 





