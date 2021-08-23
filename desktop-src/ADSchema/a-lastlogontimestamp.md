---
title: Atributo Last-login-timestamp
description: Esta é a hora em que o usuário fez o último logon no domínio.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- Atributo do AD do último logon-carimbo de data/hora
- Esquema de AD do atributo lastLogonTimestamp
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaea56a7456a46b7583633992f77e6fd836276151e6c9f6b792ba1abdd36b4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322145"
---
# <a name="last-logon-timestamp-attribute"></a>Atributo Last-login-timestamp

Esta é a hora em que o usuário fez o último logon no domínio. Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC). Sempre que um usuário faz logon, o valor desse atributo é lido no controlador de domínio. Se o valor for mais antigo \[ `current_time - msDS-LogonTimeSyncInterval` \] , o valor será atualizado. A atualização inicial após o aumento do nível funcional do domínio é calculada como 14 dias menos o percentual aleatório de 5 dias.



| Entrada | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| CN                | Último logon-carimbo de data/hora                                                                                                   |
| LDAP-Display-Name | lastLogonTimestamp                                                                                                     |
| Tamanho              | \-                                                                                                                     |
| Privilégio de atualização  | Esse valor é definido pelo sistema.                                                                                       |
| Frequência de atualização  | Quando o usuário fizer logon, e se esse valor for mais antigo que a hora atual menos o valor de msDS-LogonTimeSyncInterval. |
| Attribute-Id      | 1.2.840.113556.1.4.1696                                                                                                |
| System-ID-GUID    | c0e20a04-0e5a-4ff3-9482-5efeaecd7060                                                                                   |
| Syntax            | [**Intervalo**](s-interval.md)                                                                                         |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------|
| ID do link                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Verdadeiro                                                              |
| É de valor único       | Verdadeiro                                                              |
| É indexado             | Falso                                                             |
| No catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classes usadas em        | [**ms-DS-Vinculed-Object**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Verdadeiro                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Verdadeiro                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| É de valor único       | Verdadeiro                              |
| É indexado             | Verdadeiro                              |
| No catálogo global      | Verdadeiro                              |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



 

 





