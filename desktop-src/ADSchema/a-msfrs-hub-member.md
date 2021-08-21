---
title: MS-FRS-Hub-atributo de membro
description: O atributo ms-FRS-Hub-member é usado para registrar as configurações de topologia de NTFRS preferenciais.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- MS-FRS-Hub-member atributo AD Schema
- msFRS-Hub-membro atributo AD Schema
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa08d1eb3cbb8086149192e6ecd5fa3880f01e6cfa1800468d2825c243b211e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803304"
---
# <a name="ms-frs-hub-member-attribute"></a>MS-FRS-Hub-atributo de membro

O atributo **MS-FRS-Hub-member** é usado para registrar as configurações de topologia de NTFRS preferenciais. Quando um membro do FRS é adicionado ou excluído a um conjunto de réplicas, esses atributos são chamados e os ajustes apropriados são feitos nas conexões entre o restante dos membros do FRS no conjunto de réplicas.



| Entrada | Valor |
|-------------------|--------------------------------------------------------------------|
| CN                | MS-FRS-Hub-member                                                  |
| LDAP-Display-Name | msFRS-Hub-membro                                                   |
| Tamanho              | \-                                                                 |
| Privilégio de atualização  | Administrador de domínio                                               |
| Frequência de atualização  | Quando o conjunto de réplicas é criado ou a topologia preferida é alterada. |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| System-ID-GUID    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
| Syntax            | [**Objeto (DS-DN)**](s-object-ds-dn.md)                            |



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
| É de valor único       | Verdadeiro                                                      |
| É indexado             | Falso                                                     |
| No catálogo global      | Falso                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes usadas em        | [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| ID do link                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| É de valor único       | Verdadeiro                                                      |
| É indexado             | Falso                                                     |
| No catálogo global      | Falso                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes usadas em        | [**NTFRS-conjunto de réplicas**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| ID do link                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| É de valor único       | Verdadeiro                                                      |
| É indexado             | Falso                                                     |
| No catálogo global      | Falso                                                     |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                              |
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
| Tem valor único       | Verdadeiro                                                      |
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
| Tem valor único       | Verdadeiro                                                      |
| É indexado             | Falso                                                     |
| No Catálogo Global      | Falso                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes usadas em        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a>Comentários

Esse é o nome diferenciado totalmente qualificado de um [**objeto NTFRS-Member.**](c-ntfrsmember.md) O nome diferenciado está no formato "CN= *<computerGuid>* , CN= *<Dfs Link Name>* , CN= , *<Dfs Root name>* CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."

 

 





