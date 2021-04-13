---
title: Atributo NT-Security-Descriptor
description: O descritor de segurança do Windows NT para o objeto de esquema. Um descritor de segurança é uma estrutura de dados que contém informações de segurança sobre um objeto, como a propriedade e as permissões do objeto.
ms.assetid: 3a17b584-97ea-441c-846e-3031aea171b2
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo NT-Security-Descriptor
- Esquema de AD do atributo nTSecurityDescriptor
topic_type:
- apiref
api_name:
- NT-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e951e28ce97b04380609774baf57e4c6bf8c545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499964"
---
# <a name="nt-security-descriptor-attribute"></a>Atributo NT-Security-Descriptor

O descritor de segurança do Windows NT para o objeto de esquema. Um descritor de segurança é uma estrutura de dados que contém informações de segurança sobre um objeto, como a propriedade e as permissões do objeto.

Para obter informações sobre o formato desse valor, consulte [Security Descriptor String Format (Windows)](https://msdn.microsoft.com/library(d=robot)/aa379570(d=robot,l=en-us,v=vs.85).aspx).



| Entrada | Valor |
|-------------------|-----------------------------------------------------|
| CN                | NT-Security-Descriptor                              |
| LDAP-Display-Name | nTSecurityDescriptor                                |
| Tamanho              | \-                                                  |
| Privilégio de atualização  | \-                                                  |
| Frequência de atualização  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.2.281                              |
| System-ID-GUID    | bf9679e3-0de6-11d0-a285-00aa003049e2                |
| Syntax            | [**Cadeia de caracteres (NT-SEC-DESC)**](s-string-nt-sec-desc.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| É de valor único       | True                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No catálogo global      | True                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x00000012                                                                                                                                         |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| É de valor único       | True                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No catálogo global      | True                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                           |
| MAPI-Id                | 0x8013                                                                                       |
| System-Only            | Falso                                                                                        |
| É de valor único       | True                                                                                         |
| É indexado             | Falso                                                                                        |
| No catálogo global      | True                                                                                         |
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
| É de valor único       | True                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No catálogo global      | True                                                                                                                                               |
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
| É de valor único       | True                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No catálogo global      | True                                                                                                                                               |
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
| É de valor único       | True                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No catálogo global      | True                                                                                                                                               |
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
| É de valor único       | True                                                                                                                                               |
| É indexado             | Falso                                                                                                                                              |
| No catálogo global      | True                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> [**Segurança-principal**](c-securityprincipal.md)<br/> [**Início**](c-top.md)<br/> |



 

 





