---
title: atributo ms-TAPI-Unique-Identifier
description: Fornece o nome de uma conferência multicast TAPI. É o atributo de nomenclatura da classe Rt-Conference.
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- MS-TAPI-atributo de identificador exclusivo do esquema do AD
- Esquema de AD do atributo msTAPI-UID
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e929ecb48cdc7d12b0b75eb275a338e0a6371f365d4591ed532b399aaff03a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508536"
---
# <a name="ms-tapi-unique-identifier-attribute"></a>atributo ms-TAPI-Unique-Identifier

Fornece o nome de uma conferência multicast TAPI. É o atributo de nomenclatura da classe Rt-Conference.



| Entrada | Valor |
|-------------------|-----------------------------------------------------------------------|
| CN                | MS-TAPI-identificador exclusivo                                             |
| LDAP-Display-Name | msTAPI-UID                                                            |
| Tamanho              | Pode ser uma cadeia de caracteres arbitrária, normalmente abaixo de 100 caracteres de comprimento. |
| Privilégio de atualização  | Nenhum privilégio especial é necessário.                                       |
| Frequência de atualização  | Defina uma vez no momento da criação do objeto de Rt-Conference.            |
| Attribute-Id      | 1.2.840.113556.1.4.1698                                               |
| System-ID-GUID    | 70a4e7ea-b3b9-4643-8918-e6dd2471bfd4                                  |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                           |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | Falso                                                                                                                       |
| É de valor único       | Verdadeiro                                                                                                                        |
| É indexado             | Falso                                                                                                                       |
| No catálogo global      | Falso                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Classes usadas em        | [**MS-TAPI-RT-Conference**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | Falso                                                                                                                       |
| É de valor único       | Verdadeiro                                                                                                                        |
| É indexado             | Falso                                                                                                                       |
| No catálogo global      | Falso                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Classes usadas em        | [**MS-TAPI-RT-Conference**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | Falso                                                                                                                       |
| É de valor único       | Verdadeiro                                                                                                                        |
| É indexado             | Falso                                                                                                                       |
| No catálogo global      | Falso                                                                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Classes usadas em        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> [**ms-TAPI-Rt-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | Falso                                                                                                                       |
| Tem valor único       | Verdadeiro                                                                                                                        |
| É indexado             | Falso                                                                                                                       |
| No Catálogo Global      | Falso                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Classes usadas em        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> [**ms-TAPI-Rt-Person**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | Falso                                                                                                                       |
| Tem valor único       | Verdadeiro                                                                                                                        |
| É indexado             | Falso                                                                                                                       |
| No Catálogo Global      | Falso                                                                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Classes usadas em        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> [**ms-TAPI-Rt-Person**](c-mstapi-rtperson.md)<br/> |



 

 





