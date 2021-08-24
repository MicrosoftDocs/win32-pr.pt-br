---
title: Last-Logon atributo
description: A última vez que o usuário se registrou.
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- Last-Logon atributo AD Schema
- Esquema do AD do atributo lastLogon
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe319611e9190d828e6ccb9abb4eea9e6b5675980dfb3ab7c143dcad8e7bc4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322206"
---
# <a name="last-logon-attribute"></a>Last-Logon atributo

A última vez que o usuário se registrou. Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 nanossegundos desde 1º de janeiro de 1601 (UTC). Um valor de zero significa que a hora do último logon é desconhecida.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Last-Logon                           |
| Ldap-Display-Name | lastLogon                            |
| Tamanho              | 8 bytes                              |
| Privilégio de atualização  | Esse valor é definido pelo sistema.     |
| Frequência de atualização  | Cada vez que o usuário faz o login.          |
| Attribute-Id      | 1.2.840.113556.1.4.52                |
| System-Id-Guid    | bf967997-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------|
| ID do link                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Tem valor único       | Verdadeiro                              |
| É indexado             | Falso                             |
| No Catálogo Global      | Falso                             |
| Descritor de segurança NT | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



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
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



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
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



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
| System-Flags           | 0x00000011                        |
| Classes usadas em        | [**Usuário**](c-user.md)<br/> |



## <a name="remarks"></a>Comentários

A parte superior desse inteiro grande corresponde ao membro **dwHighDateTime** da estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e a parte inferior corresponde ao membro **dwLowDateTime** da estrutura **FILETIME** .

Esse atributo não é replicado e é mantido separadamente em cada controlador de domínio no domínio. Para obter um valor preciso para o último logon do usuário no domínio, o atributo de **último logon** para o usuário deve ser recuperado de cada controlador de domínio no domínio. O maior valor recuperado é a hora do último logon real para esse usuário.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

