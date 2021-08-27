---
title: Atributo ms-FRS-Hub-Member
description: O atributo ms-FRS-Hub-Member é usado para registrar as configurações de topologia NTFRS preferenciais.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo ms-FRS-Hub-Member
- Esquema do AD do atributo msFRS-Hub-Member
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f2cc1014b081ac13183144fca34c2087539de0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885705"
---
# <a name="ms-frs-hub-member-attribute"></a>Atributo ms-FRS-Hub-Member

O **atributo ms-FRS-Hub-Member** é usado para registrar as configurações de topologia NTFRS preferenciais. Quando um membro FRS é adicionado ou excluído de um conjunto de réplicas, esses atributos são referenciados e os ajustes apropriados são feitos nas conexões entre o restante dos membros FRS no conjunto de réplicas.



| Entrada | Valor |
|-------------------|--------------------------------------------------------------------|
| CN                | ms-FRS-Hub-Member                                                  |
| Ldap-Display-Name | msFRS-Hub-Member                                                   |
| Tamanho              | \-                                                                 |
| Privilégio de atualização  | Administrador de domínio                                               |
| Frequência de atualização  | Quando o conjunto de réplicas é criado ou a topologia preferencial muda. |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| System-Id-Guid    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)                            |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| ID do link                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Tem valor único       | True                                                      |
| É indexado             | Falso                                                     |
| No Catálogo Global      | Falso                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes usadas em        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| ID do link                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Tem valor único       | True                                                      |
| É indexado             | Falso                                                     |
| No Catálogo Global      | Falso                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes usadas em        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| ID do link                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Tem valor único       | True                                                      |
| É indexado             | Falso                                                     |
| No Catálogo Global      | Falso                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes usadas em        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| ID do link                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Tem valor único       | True                                                      |
| É indexado             | Falso                                                     |
| No Catálogo Global      | Falso                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes usadas em        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| ID do link                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Tem valor único       | True                                                      |
| É indexado             | Falso                                                     |
| No Catálogo Global      | Falso                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes usadas em        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a>Comentários

Esse é o nome diferenciado totalmente qualificado de um [**objeto NTFRS-Member.**](c-ntfrsmember.md) O nome diferenciado está no formato "CN=*&lt; computerGuid &gt;*, CN= *<Dfs Link Name>* , CN= , *<Dfs Root name>* CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."

 

 





