---
title: SPN-Mappings atributo
description: Esse atributo com vários valores contém uma lista de SPN (nomes de entidade de serviço) para mostrar a equivalência dos tipos de SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- SPN-Mappings atributo AD Schema
- Esquema do AD do atributo sPNMappings
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 451f8d3f98984f725915410e964e39a66905f29c1ccbcf9156b55d7ba51d3e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960045"
---
# <a name="spn-mappings-attribute"></a>SPN-Mappings atributo

Esse atributo com vários valores contém uma lista de SPN (nomes de entidade de serviço) para mostrar a equivalência dos tipos de SPN. O SPN é o nome que um cliente usa para identificar exclusivamente uma instância de um serviço. Se você instalar várias instâncias de um serviço em computadores em toda a floresta, cada instância deverá ter seu próprio SPN. Uma determinada instância de serviço poderá ter vários SPNs se houver vários nomes que os clientes possam usar para autenticação. Por exemplo, "ldap/..." Os SPNs podem ser mapeados para que sejam equivalentes a "host/..." Spns.



| Entrada | Valor |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | SPN-Mappings                                                                                                       |
| Ldap-Display-Name | sPNMappings                                                                                                        |
| Tamanho              | \-                                                                                                                 |
| Privilégio de atualização  | Esse valor é definido durante a instalação do produto. Ele pode ser modificado pelo administrador do sistema posteriormente. |
| Frequência de atualização  | \-                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1347                                                                                            |
| System-Id-Guid    | 2ab0e76c-7041-11d2-9905-0000f87a57d4                                                                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                        |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Tem valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Tem valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Tem valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No Catálogo Global      | Falso                                            |
| Descritor de segurança NT | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| É de valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| É de valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-serviço**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| ID do link                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| É de valor único       | Falso                                            |
| É indexado             | Falso                                            |
| No catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classes usadas em        | [**NTDS-serviço**](c-ntdsservice.md)<br/> |



 

 





