---
title: atributo ms-WMI-Author
description: O autor de uma instância de uma classe.
ms.assetid: 30f3763b-dc7d-4e01-a3a9-9246dd06299b
ms.tgt_platform: multiple
keywords:
- MS-WMI-Author atributo AD Schema
- msWMI-criar atributo AD Schema
topic_type:
- apiref
api_name:
- ms-WMI-Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f13ffe007e537fe8d3f63d99aafd768cce4e914af2afb454d3bfed285a908d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117837792"
---
# <a name="ms-wmi-author-attribute"></a>atributo ms-WMI-Author

O autor de uma instância de uma classe.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | MS-WMI-Author                               |
| LDAP-Display-Name | msWMI-autor                                |
| Tamanho              | Menos que 25 caracteres.                    |
| Privilégio de atualização  | Administrador de Política de Grupo                  |
| Frequência de atualização  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.1623                     |
| System-ID-GUID    | 6366c0c1-6972-4e66-b3a5-1d52ad0c0547        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                      |
| No catálogo global      | Falso                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                               |
| Range-Lower            | \-                                                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                 |
| Classes usadas em        | [**MS-WMI-Policytemplate**](c-mswmi-policytemplate.md)<br/> [**MS-WMI-PolicyType**](c-mswmi-policytype.md)<br/> [**MS-WMI-som**](c-mswmi-som.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                      |
| No catálogo global      | Falso                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                               |
| Range-Lower            | \-                                                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                 |
| Classes usadas em        | [**MS-WMI-Policytemplate**](c-mswmi-policytemplate.md)<br/> [**MS-WMI-PolicyType**](c-mswmi-policytype.md)<br/> [**MS-WMI-som**](c-mswmi-som.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                      |
| No catálogo global      | Falso                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                               |
| Range-Lower            | \-                                                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                 |
| Classes usadas em        | [**ms-WMI-PolicyTemplate**](c-mswmi-policytemplate.md)<br/> [**ms-WMI-PolicyType**](c-mswmi-policytype.md)<br/> [**ms-WMI-Som**](c-mswmi-som.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                      |
| No Catálogo Global      | Falso                                                                                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                               |
| Range-Lower            | \-                                                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                 |
| Classes usadas em        | [**ms-WMI-PolicyTemplate**](c-mswmi-policytemplate.md)<br/> [**ms-WMI-PolicyType**](c-mswmi-policytype.md)<br/> [**ms-WMI-Som**](c-mswmi-som.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                                                                                       |
| É indexado             | Falso                                                                                                                                                                      |
| No Catálogo Global      | Falso                                                                                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                               |
| Range-Lower            | \-                                                                                                                                                                         |
| Range-Upper            | \-                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                 |
| Classes usadas em        | [**ms-WMI-PolicyTemplate**](c-mswmi-policytemplate.md)<br/> [**ms-WMI-PolicyType**](c-mswmi-policytype.md)<br/> [**ms-WMI-Som**](c-mswmi-som.md)<br/> |



 

 





