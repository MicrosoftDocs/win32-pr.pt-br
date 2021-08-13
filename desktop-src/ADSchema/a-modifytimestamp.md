---
title: Atributo Modify-Time-Stamp
description: Um atributo computado que representa a data em que esse objeto foi alterado pela última vez. Esse valor não é replicado.
ms.assetid: ad8fea90-9a78-484d-9549-26d78e87ec44
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo Modify-Time-Stamp
- Esquema do AD do atributo modifyTimeStamp
topic_type:
- apiref
api_name:
- Modify-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc32a0142d47f842429c3bf67d766ec708b7fc42b9f3285ee360ce3789c1a84f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119300366"
---
# <a name="modify-time-stamp-attribute"></a>Atributo Modify-Time-Stamp

Um atributo computado que representa a data em que esse objeto foi alterado pela última vez. Esse valor não é replicado.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------|
| CN                | Modificar carimbo de data/hora                                             |
| Ldap-Display-Name | modifyTimeStamp                                               |
| Tamanho              | 8 bytes                                                       |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                              |
| Frequência de atualização  | \-                                                            |
| Attribute-Id      | 2.5.18.2                                                      |
| System-Id-Guid    | 9a7ad94a-ca53-11d1-bbd0-0080c76670c0                          |
| Syntax            | [**String(Generalized-Time)**](s-string-generalized-time.md) |



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
|------------------------|-----------------------------------------------------------------------------|
| ID do link                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Verdadeiro                                                                        |
| Tem valor único       | Verdadeiro                                                                        |
| É indexado             | Falso                                                                       |
| No Catálogo Global      | Falso                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| Classes usadas em        | [**SubSchema**](c-subschema.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------|
| ID do link                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Verdadeiro                                                                        |
| Tem valor único       | Verdadeiro                                                                        |
| É indexado             | Falso                                                                       |
| No Catálogo Global      | Falso                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| Classes usadas em        | [**SubSchema**](c-subschema.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------|
| ID do link                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Verdadeiro                                                                        |
| Tem valor único       | Verdadeiro                                                                        |
| É indexado             | Falso                                                                       |
| No Catálogo Global      | Falso                                                                       |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| Classes usadas em        | [**Subesquema**](c-subschema.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------|
| ID do link                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Verdadeiro                                                                        |
| É de valor único       | Verdadeiro                                                                        |
| É indexado             | Falso                                                                       |
| No catálogo global      | Falso                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| Classes usadas em        | [**Subesquema**](c-subschema.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------|
| ID do link                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Verdadeiro                                                                        |
| É de valor único       | Verdadeiro                                                                        |
| É indexado             | Falso                                                                       |
| No catálogo global      | Falso                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| Classes usadas em        | [**Subesquema**](c-subschema.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------|
| ID do link                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Verdadeiro                                                                        |
| É de valor único       | Verdadeiro                                                                        |
| É indexado             | Falso                                                                       |
| No catálogo global      | Falso                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| Classes usadas em        | [**Subesquema**](c-subschema.md)<br/> [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------|
| ID do link                | \-                                                                          |
| MAPI-Id                | \-                                                                          |
| System-Only            | Verdadeiro                                                                        |
| É de valor único       | Verdadeiro                                                                        |
| É indexado             | Falso                                                                       |
| No catálogo global      | Falso                                                                       |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                |
| Range-Lower            | \-                                                                          |
| Range-Upper            | \-                                                                          |
| Search-Flags           | 0x00000000                                                                  |
| System-Flags           | 0x08000014                                                                  |
| Classes usadas em        | [**Subesquema**](c-subschema.md)<br/> [**Início**](c-top.md)<br/> |



 

 





