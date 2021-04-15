---
title: MS-DS-Replicas-NC-atributo Reason
description: Atributo do objeto ntdsConnection que indica por que (ou se) o KCC mostra que a conexão é útil na topologia de replicação. Tem vários valores e tem uma sintaxe Distname + binária, em que a parte binária é um campo de bits de tamanho int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- MS-DS-Replicas-NC-atributo Reason esquema do AD
- Esquema de AD do atributo mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369956"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a>MS-DS-Replicas-NC-atributo Reason

Atributo do objeto ntdsConnection que indica por que (ou se) o KCC mostra que a conexão é útil na topologia de replicação. Tem vários valores e tem uma sintaxe Distname + binária, em que a parte binária é um campo de bits de tamanho int.



| Entrada | Valor |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-Replicas-NC-Reason                                                                                                                 |
| LDAP-Display-Name | mS-DS-ReplicatesNCReason                                                                                                                   |
| Tamanho              | Valor para a parte binária: 0 = não \_ motivo, 1 = \_ topologia de GC, 2 = \_ topologia de anel, 4 = minimizar a \_ \_ topologia de saltos, 8 = topologia de servidores obsoletos \_ \_ . |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                                                                                                           |
| Frequência de atualização  | Pode mudar em resposta a alterações na topologia de rede.                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1408                                                                                                                    |
| System-ID-GUID    | 0ea12b84-08b3-11d3-91bc-0000f87a57d4                                                                                                       |
| Syntax            | [**Objeto (DN-binário)**](s-object-dn-binary.md)                                                                                            |



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



## <a name="windows-server-2003"></a>Windows Server 2003



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



## <a name="adam"></a>ADAM



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



 

 





