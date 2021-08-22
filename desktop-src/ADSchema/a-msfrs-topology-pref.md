---
title: atributo ms-FRS-Topology-pref
description: O atributo ms-FRS-Topology-pref é usado para registrar as configurações de topologia de NTFRS preferenciais.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-FRS-Topology-pref
- Esquema de AD de atributos msFRS-Topology-pref
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8467a038db4f5c263253d31c33cb7dc01bb548712918d654b27b7778079d5c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960525"
---
# <a name="ms-frs-topology-pref-attribute"></a>atributo ms-FRS-Topology-pref

O atributo **MS-FRS-Topology-pref** é usado para registrar as configurações de topologia de NTFRS preferenciais. Quando um membro do FRS é adicionado ou excluído ao conjunto de réplicas, esses atributos são referenciados e os ajustes feitos nas conexões entre o restante dos membros do FRS no conjunto de réplicas.

Os valores válidos para esse atributo são os seguintes.

| Valor | Descrição                              |
|-------|------------------------------------------|
| 1     | \_anel RSTOPOLOGYPREF do FRS \_<br/>     |
| 2     | \_HUBSPOKE RSTOPOLOGYPREF do FRS \_<br/> |
| 3     | \_FULLMESH RSTOPOLOGYPREF do FRS \_<br/> |
| 4     | RSTOPOLOGYPREF de FRS \_ \_ personalizado<br/>   |



 



| Entrada | Valor |
|-------------------|--------------------------------------------------------------------|
| CN                | MS-FRS-Topology-pref                                               |
| LDAP-Display-Name | msFRS-Topology-pref                                                |
| Tamanho              | \-                                                                 |
| Privilégio de atualização  | Administrador de domínio                                               |
| Frequência de atualização  | Quando o conjunto de réplicas é criado ou a topologia preferida é alterada. |
| Attribute-Id      | 1.2.840.113556.1.4.1692                                            |
| System-ID-GUID    | 92aa27e0-5c50-402d-9ec1-ee847def9788                               |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                        |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| ID do link                | \-                                                        |
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
| ID do link                | \-                                                        |
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
| ID do link                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| É de valor único       | Verdadeiro                                                      |
| É indexado             | Falso                                                     |
| No catálogo global      | Falso                                                     |
| Descritor de segurança NT | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classes usadas em        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------|
| ID do link                | \-                                                        |
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
| ID do link                | \-                                                        |
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



 

 





