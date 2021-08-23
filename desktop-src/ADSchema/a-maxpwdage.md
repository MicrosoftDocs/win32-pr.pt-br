---
title: Atributo Max-Pwd-Age
description: A quantidade máxima de tempo, em intervalos de 100 nanossegundos, uma senha é válida.
ms.assetid: b4b48207-6481-42a1-b848-6baf37a367ce
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Max-Pwd-Age
- Esquema do AD do atributo maxPwdAge
topic_type:
- apiref
api_name:
- Max-Pwd-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93c647d05d0ddca2947878b908d3a7f7f5b293e308c6e799fb6e1d85db7e97ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301036"
---
# <a name="max-pwd-age-attribute"></a>Atributo Max-Pwd-Age

A quantidade máxima de tempo, em intervalos de 100 nanossegundos, uma senha é válida. Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 nanossegundos a partir do momento em que a senha foi definida antes que a senha expire.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Max-Pwd-Age                          |
| Ldap-Display-Name | maxPwdAge                            |
| Tamanho              | \-                                   |
| Privilégio de atualização  | Administrador de domínio                 |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.74                |
| System-Id-Guid    | bf9679bb-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervalo**](s-interval.md)       |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Tem valor único       | Verdadeiro                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Tem valor único       | Verdadeiro                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Tem valor único       | Verdadeiro                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Tem valor único       | Verdadeiro                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Tem valor único       | Verdadeiro                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Tem valor único       | Verdadeiro                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No Catálogo Global      | Falso                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Domínio Sam**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





