---
title: Atributo MS-DS-Replicates-NC-Reason
description: Atributo do objeto ntdsConnection que indica por que (ou se) o KCC mostra que a conexão é útil na topologia de replicação. Tem vários valores e tem sintaxe DistName+Binary, em que a parte binária é um campo de bits de tamanho int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo MS-DS-Replicates-NC-Reason
- Esquema do AD do atributo mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681105fe24584afae275a8869ad04698ff7a70daa32832140a98865318672863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118686967"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a>Atributo MS-DS-Replicates-NC-Reason

Atributo do objeto ntdsConnection que indica por que (ou se) o KCC mostra que a conexão é útil na topologia de replicação. Tem vários valores e tem sintaxe DistName+Binary, em que a parte binária é um campo de bits de tamanho int.



| Entrada | Valor |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-Replicates-NC-Reason                                                                                                                 |
| Ldap-Display-Name | mS-DS-ReplicatesNCReason                                                                                                                   |
| Tamanho              | Valor da parte binária: 0 = NO \_ REASON,1 = GC \_ TOPOLOGY, 2 = RING \_ TOPOLOGY, 4 = MINIMIZE \_ HOPS \_ TOPOLOGY, 8 = STALE \_ SERVERS \_ TOPOLOGY. |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                                                                                                           |
| Frequência de atualização  | Pode alterar em resposta a alterações na topologia de rede.                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1408                                                                                                                    |
| System-Id-Guid    | 0ea12b84-08b3-11d3-91bc-0000f87a57d4                                                                                                       |
| Sintaxe            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                            |



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
|------------------------|--------------------------------------------------------|
| ID do link                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| Tem valor único       | Falso                                                  |
| É indexado             | Falso                                                  |
| No Catálogo Global      | Falso                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes usadas em        | [**Conexão NTDS**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------------|
| ID do link                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| Tem valor único       | Falso                                                  |
| É indexado             | Falso                                                  |
| No Catálogo Global      | Falso                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes usadas em        | [**Conexão NTDS**](c-ntdsconnection.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|--------------------------------------------------------|
| ID do link                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| Tem valor único       | Falso                                                  |
| É indexado             | Falso                                                  |
| No Catálogo Global      | Falso                                                  |
| Descritor de segurança NT | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------|
| ID do link                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| É de valor único       | Falso                                                  |
| É indexado             | Falso                                                  |
| No catálogo global      | Falso                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------------|
| ID do link                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| É de valor único       | Falso                                                  |
| É indexado             | Falso                                                  |
| No catálogo global      | Falso                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------------|
| ID do link                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| É de valor único       | Falso                                                  |
| É indexado             | Falso                                                  |
| No catálogo global      | Falso                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------------|
| ID do link                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | Falso                                                  |
| É de valor único       | Falso                                                  |
| É indexado             | Falso                                                  |
| No catálogo global      | Falso                                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Classes usadas em        | [**NTDS-conexão**](c-ntdsconnection.md)<br/> |



 

 





