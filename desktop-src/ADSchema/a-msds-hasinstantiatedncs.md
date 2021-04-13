---
title: ms-DS-tem-atributo-NCs-instanciado
description: Informações de estado de replicação DS, análogas a (e um superconjunto de) os atributos existentes hasMasterNCs e hasPartialReplicaNCs. A ser usado pelo KCC ao configurar parceiros de replicação.
ms.assetid: 00dda441-e382-4fb2-b735-ae547901c11f
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-tem-instancie-NCs
- atributo msDS-HasInstantiatedNCs do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Has-Instantiated-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2900d68f82e859bac7ce1dabbfea2d28fd8998b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456217"
---
# <a name="ms-ds-has-instantiated-ncs-attribute"></a>ms-DS-tem-atributo-NCs-instanciado

Informações de estado de replicação DS, análogas a (e um superconjunto de) os atributos existentes hasMasterNCs e hasPartialReplicaNCs. A ser usado pelo KCC ao configurar parceiros de replicação.



| Entrada | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-tem-NCs-instanciáveis                                                                                                                                                                                  |
| LDAP-Display-Name | msDS-HasInstantiatedNCs                                                                                                                                                                                     |
| Tamanho              | 4 bytes                                                                                                                                                                                                     |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                                                                                                                                                                            |
| Frequência de atualização  | Aproximadamente duas vezes com a frequência de hasMasterNCs/hasPartialReplicaNCs. Esses atributos existentes são atualizados somente quando o DC adiciona ou remove uma partição (por exemplo, ao mudar de DC para GC ou vice-versa). |
| Attribute-Id      | 1.2.840.113556.1.4.1709                                                                                                                                                                                     |
| System-ID-GUID    | 11e9a5bc-4517-4049-af9c-51554fb0fc09                                                                                                                                                                        |
| Syntax            | [**Objeto (DN-binário)**](s-object-dn-binary.md)                                                                                                                                                             |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| É de valor único       | Falso                                    |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| É de valor único       | Falso                                    |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| É de valor único       | Falso                                    |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| É de valor único       | Falso                                    |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| É de valor único       | Falso                                    |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------|
| ID do link                | 2002                                     |
| MAPI-Id                | \-                                       |
| System-Only            | True                                     |
| É de valor único       | Falso                                    |
| É indexado             | Falso                                    |
| No catálogo global      | Falso                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                             |
| Range-Lower            | 4                                        |
| Range-Upper            | 4                                        |
| Search-Flags           | 0x00000000                               |
| System-Flags           | 0x00000010                               |
| Classes usadas em        | [**NTDS-DSA**](c-ntdsdsa.md)<br/> |



 

 





