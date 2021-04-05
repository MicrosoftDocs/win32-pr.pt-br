---
title: Atributo de descrição (esquema do AD)
description: Contém a descrição a ser exibida para um objeto. Esse valor é restrito como de valor único para compatibilidade com versões anteriores em alguns casos, mas pode ter vários valores em outros. Consulte Observações.
ms.assetid: 97dad871-5db0-4d1e-b931-1b053559f9c2
ms.tgt_platform: multiple
keywords:
- Atributo de descrição esquema do AD
- atributo de descrição esquema do AD
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ccb155c9c65a42c29a022a6912b7aea7087477
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645343"
---
# <a name="description-attribute-ad-schema"></a>Atributo de descrição (esquema do AD)

Contém a descrição a ser exibida para um objeto. Esse valor é restrito como de valor único para compatibilidade com versões anteriores em alguns casos, mas pode ter vários valores em outros. Consulte Observações.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Descrição                                 |
| LDAP-Display-Name | descrição                                 |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio ou proprietário da conta.      |
| Frequência de atualização  | Sempre que a descrição precisar ser alterada.   |
| Attribute-Id      | 2.5.4.13                                    |
| System-ID-GUID    | bf967950-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



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
|------------------------|------------------------------------------------------------------------------|
| ID do link                | \-                                                                           |
| MAPI-Id                | 0x806F                                                                       |
| System-Only            | Falso                                                                        |
| É de valor único       | Falso                                                                        |
| É indexado             | Falso                                                                        |
| No catálogo global      | True                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                 |
| Range-Lower            | 0                                                                            |
| Range-Upper            | 1024                                                                         |
| Search-Flags           | 0x00000000                                                                   |
| System-Flags           | 0x00000010                                                                   |
| Classes usadas em        | [**Sam-domínio**](c-samdomain.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                         |
| MAPI-Id                | 0x806F                                                                                                                                     |
| System-Only            | Falso                                                                                                                                      |
| É de valor único       | Falso                                                                                                                                      |
| É indexado             | Falso                                                                                                                                      |
| No catálogo global      | True                                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                               |
| Range-Lower            | 0                                                                                                                                          |
| Range-Upper            | 1024                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Classes usadas em        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x806F                          |
| System-Only            | Falso                           |
| É de valor único       | Falso                           |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 1024                            |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classes usadas em        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Início**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classes usadas em        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Início**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classes usadas em        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Início**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| É de valor único       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| É indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| No catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Classes usadas em        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Início**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**o POSIX**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="remarks"></a>Comentários

O atributo de descrição é implementado como um atributo de valores múltiplos no esquema para os casos em que isso é permitido. Para um objeto que não é uma classe gerenciada por SAM, a descrição tem valores múltiplos. Para um atributo que é uma classe gerenciada SAM, o atributo de descrição é de valor único. As classes gerenciadas SAM são para coisas como entidades de segurança, portanto, se você tiver, por exemplo, um contêiner ou uma classe própria, o esquema permitirá que você use vários valores. Esse comportamento do atributo Description é para compatibilidade com versões anteriores com sistemas operacionais mais antigos, pois o atributo existia nas APIs SAM antes que o AD existisse.

 

 





