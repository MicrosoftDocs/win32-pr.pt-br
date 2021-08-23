---
title: USN-Created atributo
description: O número de sequência de atualização (USN) atribuído na criação do objeto. Consulte também, USN-alterado.
ms.assetid: c38456b8-fc8f-4ea0-8f3d-e2bb3b44ff50
ms.tgt_platform: multiple
keywords:
- Esquema de USN-Created do atributo AD
- Esquema de AD do atributo uSNCreated
topic_type:
- apiref
api_name:
- USN-Created
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6cd8e2483e7a5e73fbc68dd123a358f098a729a2f2a0159ccd4e8b3e03d894
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702856"
---
# <a name="usn-created-attribute"></a>USN-Created atributo

O número de sequência de atualização (USN) atribuído na criação do objeto. Consulte também, [**USN-alterado**](a-usnchanged.md).



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | USN-Created                          |
| LDAP-Display-Name | uSNCreated                           |
| Tamanho              | 8 bytes                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.     |
| Frequência de atualização  | Quando o objeto é criado.          |
| Attribute-Id      | 1.2.840.113556.1.2.19                |
| System-ID-GUID    | bf967a70-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervalo**](s-interval.md)       |



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
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x8154                          |
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Verdadeiro                            |
| No catálogo global      | Verdadeiro                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000009                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x8154                          |
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Verdadeiro                            |
| No catálogo global      | Verdadeiro                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000009                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x8154                          |
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Verdadeiro                            |
| No catálogo global      | Verdadeiro                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000009                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x8154                          |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Verdadeiro                            |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000009                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x8154                          |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Verdadeiro                            |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000009                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x8154                          |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Verdadeiro                            |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000009                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x8154                          |
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Verdadeiro                            |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000009                      |
| System-Flags           | 0x00000013                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



 

 





