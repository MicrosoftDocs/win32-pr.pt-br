---
title: Atributo NT-Security-Descriptor
description: O Windows NT descritor de segurança para o objeto de esquema. Um descritor de segurança é uma estrutura de dados que contém informações de segurança sobre um objeto, como a propriedade e as permissões do objeto.
ms.assetid: 3a17b584-97ea-441c-846e-3031aea171b2
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo NT-Security-Descriptor
- Esquema do AD do atributo nTSecurityDescriptor
topic_type:
- apiref
api_name:
- NT-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d33b5753429b63638f1f1c9a3103aa8d78bd8590b77ceebec4fff05b82e10dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703006"
---
# <a name="nt-security-descriptor-attribute"></a>Atributo NT-Security-Descriptor

O Windows NT descritor de segurança para o objeto de esquema. Um descritor de segurança é uma estrutura de dados que contém informações de segurança sobre um objeto, como a propriedade e as permissões do objeto.

Para obter informações sobre o formato desse valor, consulte Formato de cadeia de caracteres do descritor [de segurança (Windows)](https://msdn.microsoft.com/library(d=robot)/aa379570(d=robot,l=en-us,v=vs.85).aspx).



| Entrada | Valor |
|-------------------|-----------------------------------------------------|
| CN                | Descritor de segurança NT                              |
| Ldap-Display-Name | Ntsecuritydescriptor                                |
| Tamanho              | \-                                                  |
| Privilégio de atualização  | \-                                                  |
| Frequência de atualização  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.2.281                              |
| System-Id-Guid    | bf9679e3-0de6-11d0-a285-00aa003049e2                |
| Syntax            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Tem valor único       | Verdadeiro                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No Catálogo Global      | Verdadeiro                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x00000012                                                                                                                                         |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidade de segurança**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Tem valor único       | Verdadeiro                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No Catálogo Global      | Verdadeiro                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidade de segurança**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                           |
| MAPI-Id                | 0x8013                                                                                       |
| System-Only            | Falso                                                                                        |
| Tem valor único       | Verdadeiro                                                                                         |
| É indexado             | Falso                                                                                        |
| No catálogo global      | Verdadeiro                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                 |
| Range-Lower            | 0                                                                                            |
| Range-Upper            | 132096                                                                                       |
| Search-Flags           | 0x00000008                                                                                   |
| System-Flags           | 0x0000001A                                                                                   |
| Classes usadas em        | [**Segurança-principal**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| É de valor único       | Verdadeiro                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No catálogo global      | Verdadeiro                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| É de valor único       | Verdadeiro                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No catálogo global      | Verdadeiro                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| É de valor único       | Verdadeiro                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No catálogo global      | Verdadeiro                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Tem valor único       | Verdadeiro                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No Catálogo Global      | Verdadeiro                                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidade de segurança**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |



 

 





