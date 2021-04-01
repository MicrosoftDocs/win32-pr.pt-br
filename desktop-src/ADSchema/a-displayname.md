---
title: Display-Name atributo
description: O nome de exibição de um objeto.
ms.assetid: 0ecf5ede-0351-4d59-bdbf-44baf729f2e2
ms.tgt_platform: multiple
keywords:
- Esquema de Display-Name do atributo AD
- atributo displayName esquema do AD
topic_type:
- apiref
api_name:
- Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4fe662ccbdf2157c7ed51a311739cf7d16273b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645339"
---
# <a name="display-name-attribute"></a>Display-Name atributo

O nome de exibição de um objeto. Normalmente, essa é a combinação dos usuários nome, início médio e sobrenome.



| Entrada | Valor |
|-------------------|------------------------------------------------------------------------------|
| CN                | Display-Name                                                                 |
| LDAP-Display-Name | displayName                                                                  |
| Tamanho              | \-                                                                           |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                       |
| Frequência de atualização  | Quando o registro do usuário é criado e quando o nome de exibição precisa ser alterado. |
| Attribute-Id      | 1.2.840.113556.1.2.13                                                        |
| System-ID-GUID    | bf967953-0de6-11d0-a285-00aa003049e2                                         |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                                  |



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
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                            |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                             |
| É indexado             | True                                                                                                                                                                                                                                                                                                                                             |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**Catálogo de endereços-contêiner**](c-addressbookcontainer.md)<br/> [**Endereço-modelo**](c-addresstemplate.md)<br/> [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| É indexado             | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**Catálogo de endereços-contêiner**](c-addressbookcontainer.md)<br/> [**Endereço-modelo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| É de valor único       | True                            |
| É indexado             | True                            |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 256                             |
| Search-Flags           | 0x00000005                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| É indexado             | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**Catálogo de endereços-contêiner**](c-addressbookcontainer.md)<br/> [**Endereço-modelo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| É indexado             | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**Catálogo de endereços-contêiner**](c-addressbookcontainer.md)<br/> [**Endereço-modelo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| É indexado             | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**Catálogo de endereços-contêiner**](c-addressbookcontainer.md)<br/> [**Endereço-modelo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| É de valor único       | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| É indexado             | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**Catálogo de endereços-contêiner**](c-addressbookcontainer.md)<br/> [**Endereço-modelo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



 

 





