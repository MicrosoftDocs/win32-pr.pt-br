---
title: Extra-Columns atributo
description: Este é um atributo com vários valores, cujo valor consiste em uma tupla de 5 (nome do atributo), (título da coluna), (visibilidade padrão (0, 1)), (largura da coluna (\ 8211; 1 para largura automática)), 0 (reservado para uso futuro deve ser zero).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Esquema de Extra-Columns do atributo AD
- Esquema de AD do atributo extraColumns
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645369"
---
# <a name="extra-columns-attribute"></a>Extra-Columns atributo

Este é um atributo com vários valores, cujo valor consiste em uma tupla de 5: (nome do atributo), (título da coluna), (visibilidade padrão (0, 1)), (largura da coluna (1 para largura automática)), 0 (reservado para uso futuro deve ser zero). Esse valor é usado pelo console usuários e computadores do AD.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Extra-Columns                                                                                                                                                        |
| LDAP-Display-Name | extraColumns                                                                                                                                                         |
| Tamanho              | Cada valor seria o tamanho da cadeia de caracteres da tupla de 5. Por padrão, haverá 22 valores no objeto de exibição padrão no contêiner DisplaySpecifier. |
| Privilégio de atualização  | Administrador de domínio                                                                                                                                                 |
| Frequência de atualização  | Isso só será atualizado se um serviço como o Exchange estiver instalado.                                                                                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1687                                                                                                                                              |
| System-ID-GUID    | d24e2846-1dd9-4bcf-99d7-a6227cc86da7                                                                                                                                 |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| ID do link                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| É de valor único       | Falso                                                      |
| É indexado             | Falso                                                      |
| No catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes usadas em        | [**Especificador de exibição**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| ID do link                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| É de valor único       | Falso                                                      |
| É indexado             | Falso                                                      |
| No catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes usadas em        | [**Especificador de exibição**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| ID do link                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| É de valor único       | Falso                                                      |
| É indexado             | Falso                                                      |
| No catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes usadas em        | [**Especificador de exibição**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| ID do link                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| É de valor único       | Falso                                                      |
| É indexado             | Falso                                                      |
| No catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes usadas em        | [**Especificador de exibição**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| ID do link                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| É de valor único       | Falso                                                      |
| É indexado             | Falso                                                      |
| No catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classes usadas em        | [**Especificador de exibição**](c-displayspecifier.md)<br/> |



 

 





