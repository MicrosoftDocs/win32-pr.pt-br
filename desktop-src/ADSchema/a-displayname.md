---
title: Display-Name atributo
description: O nome de exibição de um objeto .
ms.assetid: 0ecf5ede-0351-4d59-bdbf-44baf729f2e2
ms.tgt_platform: multiple
keywords:
- Display-Name atributo AD Schema
- Esquema do AD do atributo displayName
topic_type:
- apiref
api_name:
- Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d4be2c6823fa068f07a14ab478a797c0db92e4f91b25656439319da5a25db1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049586"
---
# <a name="display-name-attribute"></a>Display-Name atributo

O nome de exibição de um objeto . Geralmente, essa é a combinação do nome dos usuários, inicial do meio e sobrenome.



| Entrada | Valor |
|-------------------|------------------------------------------------------------------------------|
| CN                | Display-Name                                                                 |
| Ldap-Display-Name | displayName                                                                  |
| Tamanho              | \-                                                                           |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.                                       |
| Frequência de atualização  | Quando o registro do usuário é criado e quando o nome de exibição precisa ser alterado. |
| Attribute-Id      | 1.2.840.113556.1.2.13                                                        |
| System-Id-Guid    | bf967953-0de6-11d0-a285-00aa003049e2                                         |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                  |



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
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                            |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                             |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                             |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                             |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                       |
| Classes usadas em        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Modelo de endereço**](c-addresstemplate.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Modelo de endereço**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Verdadeiro                            |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
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
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Modelo de endereço**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Modelo de endereço**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Tem valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| No Catálogo Global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
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
| É de valor único       | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| É indexado             | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| No catálogo global      | Verdadeiro                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classes usadas em        | [**Catálogo de endereços-contêiner**](c-addressbookcontainer.md)<br/> [**Endereço-modelo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificado-modelo**](c-pkicertificatetemplate.md)<br/> [**Classe de serviço**](c-serviceclass.md)<br/> [**Instância de serviço**](c-serviceinstance.md)<br/> [**Início**](c-top.md)<br/> |



 

 





