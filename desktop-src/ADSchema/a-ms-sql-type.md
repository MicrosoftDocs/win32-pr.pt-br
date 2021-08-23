---
title: Atributo MS-SQL-Type
description: O tipo de replicação usado por este SQL servidor.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo MS-SQL-Type
- Esquema do AD do atributo mS-SQL-Type
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15850884b8071fc103abf2c8d3f12ad68d4f5ed946ef2b491b4907b87b1cb524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583286"
---
# <a name="ms-sql-type-attribute"></a>Atributo MS-SQL-Type

O tipo de replicação usado por este SQL servidor. Os valores a seguir são os valores possíveis para esse atributo.



| Valor        | Descrição                           |
|--------------|---------------------------------------|
| 0<br/> | Replicação transacional.<br/> |
| 1<br/> | Replicação de instantâneo<br/>      |
| 2<br/> | Replicação de mesclagem.<br/>         |



 



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Tipo de SQL MS                                 |
| Ldap-Display-Name | mS-SQL-Type                                 |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio                        |
| Frequência de atualização  | Quando a replicação é configurada.                 |
| Attribute-Id      | 1.2.840.113556.1.4.1391                     |
| System-Id-Guid    | ca48eba8-ccee-11d2-9993-0000f87a57d4        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| Tem valor único       | Verdadeiro                                                                                                                                |
| É indexado             | Falso                                                                                                                               |
| No Catálogo Global      | Falso                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes usadas em        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| Tem valor único       | Verdadeiro                                                                                                                                |
| É indexado             | Falso                                                                                                                               |
| No Catálogo Global      | Falso                                                                                                                               |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes usadas em        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| Tem valor único       | Verdadeiro                                                                                                                                |
| É indexado             | Falso                                                                                                                               |
| No Catálogo Global      | Falso                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes usadas em        | [**MS-SQL-sqlpúblico**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| É de valor único       | Verdadeiro                                                                                                                                |
| É indexado             | Falso                                                                                                                               |
| No catálogo global      | Falso                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes usadas em        | [**MS-SQL-sqlpúblico**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| É de valor único       | Verdadeiro                                                                                                                                |
| É indexado             | Falso                                                                                                                               |
| No catálogo global      | Falso                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes usadas em        | [**MS-SQL-sqlpúblico**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| É de valor único       | Verdadeiro                                                                                                                                |
| É indexado             | Falso                                                                                                                               |
| No catálogo global      | Falso                                                                                                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classes usadas em        | [**MS-SQL-sqlpúblico**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



 

 





