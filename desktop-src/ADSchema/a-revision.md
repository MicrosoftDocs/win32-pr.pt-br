---
title: Atributo de revisão
description: O nível de revisão para um descritor de segurança ou outra alteração. Usado somente nos objetos Sam-Server e DS-UI-Settings.
ms.assetid: 480de80f-3e76-4a62-a4a7-29a67f910a62
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo de revisão
- Esquema de AD do atributo de revisão
topic_type:
- apiref
api_name:
- Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8948bd865db776c52ac021d296792a6f7d0720dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499954"
---
# <a name="revision-attribute"></a>Atributo de revisão

O nível de revisão para um descritor de segurança ou outra alteração. Usado somente nos objetos Sam-Server e DS-UI-Settings.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Revisão                             |
| LDAP-Display-Name | revisão                             |
| Tamanho              | 4 bytes                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.     |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.145               |
| System-ID-GUID    | bf967a21-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



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
|------------------------|---------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falso                                                                                 |
| É de valor único       | True                                                                                  |
| É indexado             | Falso                                                                                 |
| No catálogo global      | Falso                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falso                                                                                 |
| É de valor único       | True                                                                                  |
| É indexado             | Falso                                                                                 |
| No catálogo global      | Falso                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| É de valor único       | True                            |
| É indexado             | Falso                           |
| No catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falso                                                                                 |
| É de valor único       | True                                                                                  |
| É indexado             | Falso                                                                                 |
| No catálogo global      | Falso                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falso                                                                                 |
| É de valor único       | True                                                                                  |
| É indexado             | Falso                                                                                 |
| No catálogo global      | Falso                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falso                                                                                 |
| É de valor único       | True                                                                                  |
| É indexado             | Falso                                                                                 |
| No catálogo global      | Falso                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falso                                                                                 |
| É de valor único       | True                                                                                  |
| É indexado             | Falso                                                                                 |
| No catálogo global      | Falso                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Início**](c-top.md)<br/> |



 

 





