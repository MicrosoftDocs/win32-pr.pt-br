---
title: Atributo well-known-Objects
description: Esse atributo contém uma lista de contêineres de objeto conhecidos por GUID e nome diferenciado.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo well-known-Objects
- Esquema de AD do atributo wellKnownObjects
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456243"
---
# <a name="well-known-objects-attribute"></a>Atributo well-known-Objects

Esse atributo contém uma lista de contêineres de objeto conhecidos por GUID e nome diferenciado. Os objetos bem conhecidos são contêineres do sistema. Essas informações são usadas para recuperar um objeto depois que ele é movido usando apenas o GUID e o nome de domínio. Sempre que o objeto for movido, o sistema atualizará automaticamente a parte do nome distinto dos valores de objetos conhecidos que referenciaram o objeto. O arquivo NTDSAPI. h contém as seguintes definições, que podem ser usadas para recuperar um objeto (os GUIDs associados a esses objetos estão contidos em NTDSAPI. h):

-   \_contêiner de usuários GUID \_ \_ W
-   \_contêiner COMPUTRS \_ GUID \_ W
-   contêiner de sistemas de GUID \_ \_ \_ W
-   contêiner de controladores de domínio do GUID \_ \_ \_ \_ W
-   contêiner de infraestrutura de GUID \_ \_ \_ W
-   \_contêiner de objetos excluídos de GUID \_ \_ \_ W
-   contêiner de LOSTANDFOUND de GUID \_ \_ \_ W
-   \_contêiner FOREIGNSECURITYPRINCIPALS \_ GUID \_ W
-   \_contêiner de dados do programa GUID \_ \_ \_ W
-   GUID \_ do \_ \_ contêiner de dados do programa \_ Microsoft \_
-   \_contêiner de \_ cotas NTDS de GUID \_ \_ W



| Entrada | Valor |
|-------------------|-------------------------------------------------|
| CN                | Objetos bem conhecidos                              |
| LDAP-Display-Name | wellKnownObjects                                |
| Tamanho              | \-                                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                |
| Frequência de atualização  | Sempre que um dos contêineres do sistema for movido. |
| Attribute-Id      | 1.2.840.113556.1.4.618                          |
| System-ID-GUID    | 05308983-7688-11d1-aded-00c04fd8d5cd            |
| Syntax            | [**Objeto (DN-binário)**](s-object-dn-binary.md) |



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
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



 

 





