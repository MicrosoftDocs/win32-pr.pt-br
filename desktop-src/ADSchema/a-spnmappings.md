---
title: SPN-Mappings atributo
description: Esse atributo de valores múltiplos contém uma lista de SPN (nomes de entidade de serviço) para mostrar a equivalência dos tipos SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- Esquema de SPN-Mappings do atributo AD
- Esquema de AD do atributo sPNMappings
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500032"
---
# <a name="spn-mappings-attribute"></a>SPN-Mappings atributo

Esse atributo de valores múltiplos contém uma lista de SPN (nomes de entidade de serviço) para mostrar a equivalência dos tipos SPN. O SPN é o nome que um cliente usa para identificar exclusivamente uma instância de um serviço. Se você instalar várias instâncias de um serviço em computadores em uma floresta, cada instância deverá ter seu próprio SPN. Uma determinada instância de serviço pode ter vários SPNs se houver vários nomes que os clientes podem usar para autenticação. Por exemplo, "LDAP/..." Os SPNs podem ser mapeados para que eles sejam equivalentes a "host/..." SPNs.



| Entrada | Valor |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | SPN-Mappings                                                                                                       |
| LDAP-Display-Name | sPNMappings                                                                                                        |
| Tamanho              | \-                                                                                                                 |
| Privilégio de atualização  | Esse valor é definido durante a instalação do produto. Ele pode ser modificado pelo administrador do sistema em um momento posterior. |
| Frequência de atualização  | \-                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1347                                                                                            |
| System-ID-GUID    | 2ab0e76c-7041-11d2-9905-0000f87a57d4                                                                               |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                                                        |



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
| É de valor único       | Falso                                            |
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



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



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



 

 





