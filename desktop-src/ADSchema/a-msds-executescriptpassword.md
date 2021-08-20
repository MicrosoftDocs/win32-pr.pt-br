---
title: atributo ms-DS-ExecuteScriptPassword
description: Usado durante a renomeação do domínio. Esse valor não pode ser gravado ou lido usando o LDAP.
ms.assetid: 381c3676-0a11-4e53-8093-f04dbf156250
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-ExecuteScriptPassword
- atributo msDS-ExecuteScriptPassword do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-ExecuteScriptPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd9381d58c533341539e0957f787e166572ec60d4009aa34f84a327ba3a34ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118426749"
---
# <a name="ms-ds-executescriptpassword-attribute"></a>atributo ms-DS-ExecuteScriptPassword

Usado durante a renomeação do domínio. Esse valor não pode ser gravado ou lido usando o LDAP.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | ms-DS-ExecuteScriptPassword                           |
| LDAP-Display-Name | msDS-ExecuteScriptPassword                            |
| Tamanho              | \-                                                    |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                      |
| Frequência de atualização  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1783                               |
| System-ID-GUID    | 9d054a5a-d187-46c1-9d85-42dfc44a56dd                  |
| Syntax            | [**Objeto (link de réplica)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------|
| ID do link                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Verdadeiro                                                          |
| É de valor único       | Verdadeiro                                                          |
| É indexado             | Falso                                                         |
| No catálogo global      | Falso                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 64                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000011                                                    |
| Classes usadas em        | [**Entre referências-contêiner**](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------------------------------------|
| ID do link                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Verdadeiro                                                          |
| É de valor único       | Verdadeiro                                                          |
| É indexado             | Falso                                                         |
| No catálogo global      | Falso                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 64                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000011                                                    |
| Classes usadas em        | [**Entre referências-contêiner**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------|
| ID do link                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Verdadeiro                                                          |
| É de valor único       | Verdadeiro                                                          |
| É indexado             | Falso                                                         |
| No catálogo global      | Falso                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 64                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000011                                                    |
| Classes usadas em        | [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                      |
| MAPI-Id                | \-                                                                                                      |
| System-Only            | Verdadeiro                                                                                                    |
| Tem valor único       | Verdadeiro                                                                                                    |
| É indexado             | Falso                                                                                                   |
| No Catálogo Global      | Falso                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                            |
| Range-Lower            | 0                                                                                                       |
| Range-Upper            | 64                                                                                                      |
| Search-Flags           | 0x00000000                                                                                              |
| System-Flags           | 0x00000011                                                                                              |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                      |
| MAPI-Id                | \-                                                                                                      |
| System-Only            | Verdadeiro                                                                                                    |
| Tem valor único       | Verdadeiro                                                                                                    |
| É indexado             | Falso                                                                                                   |
| No Catálogo Global      | Falso                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                            |
| Range-Lower            | 0                                                                                                       |
| Range-Upper            | 64                                                                                                      |
| Search-Flags           | 0x00000000                                                                                              |
| System-Flags           | 0x00000011                                                                                              |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                      |
| MAPI-Id                | \-                                                                                                      |
| System-Only            | Verdadeiro                                                                                                    |
| Tem valor único       | Verdadeiro                                                                                                    |
| É indexado             | Falso                                                                                                   |
| No Catálogo Global      | Falso                                                                                                   |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                            |
| Range-Lower            | 0                                                                                                       |
| Range-Upper            | 64                                                                                                      |
| Search-Flags           | 0x00000000                                                                                              |
| System-Flags           | 0x00000011                                                                                              |
| Classes usadas em        | [**Computador**](c-computer.md)<br/> [**Cross-Ref-Container**](c-crossrefcontainer.md)<br/> |



 

 





