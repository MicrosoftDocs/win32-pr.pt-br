---
title: Orientações de impressão – atributo com suporte
description: A rotação da página para impressão em paisagem.
ms.assetid: a3e910f1-452e-4b85-8ede-50b7274475a0
ms.tgt_platform: multiple
keywords:
- Orientações de impressão – esquema de anúncio de atributo com suporte
- Esquema de AD do atributo printOrientationsSupported
topic_type:
- apiref
api_name:
- Print-Orientations-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffe346318b043f988f04d3f5f99cfd6c138ffdaa984eec2b0cf06f5cfa1c92ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022364"
---
# <a name="print-orientations-supported-attribute"></a>Orientações de impressão – atributo com suporte

A rotação da página para impressão em paisagem.



| Entrada | Valor |
|-------------------|-------------------------------------------------------------|
| CN                | Orientações de impressão-com suporte                                |
| LDAP-Display-Name | printOrientationsSupported                                  |
| Tamanho              | 4 bytes. Valores possíveis: 0, 90, 270 e 0 = sem paisagem. |
| Privilégio de atualização  | \-                                                          |
| Frequência de atualização  | \-                                                          |
| Attribute-Id      | 1.2.840.113556.1.4.240                                      |
| System-ID-GUID    | 281416d0-1968-11d0-a28f-00aa003049e2                        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md)                 |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------|
| ID do link                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Falso                                          |
| É de valor único       | Falso                                          |
| É indexado             | Falso                                          |
| No catálogo global      | Falso                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                   |
| Range-Lower            | 1                                              |
| Range-Upper            | 256                                            |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Classes usadas em        | [**Fila de impressão**](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------|
| ID do link                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Falso                                          |
| É de valor único       | Falso                                          |
| É indexado             | Falso                                          |
| No catálogo global      | Falso                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                   |
| Range-Lower            | 1                                              |
| Range-Upper            | 256                                            |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Classes usadas em        | [**Fila de impressão**](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------|
| ID do link                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Falso                                          |
| É de valor único       | Falso                                          |
| É indexado             | Falso                                          |
| No catálogo global      | Falso                                          |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                   |
| Range-Lower            | 1                                              |
| Range-Upper            | 256                                            |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Classes usadas em        | [**Fila de Impressão**](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------|
| ID do link                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Falso                                          |
| Tem valor único       | Falso                                          |
| É indexado             | Falso                                          |
| No Catálogo Global      | Falso                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                   |
| Range-Lower            | 1                                              |
| Range-Upper            | 256                                            |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Classes usadas em        | [**Fila de Impressão**](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------|
| ID do link                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Falso                                          |
| Tem valor único       | Falso                                          |
| É indexado             | Falso                                          |
| No Catálogo Global      | Falso                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                   |
| Range-Lower            | 1                                              |
| Range-Upper            | 256                                            |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Classes usadas em        | [**Fila de Impressão**](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------|
| ID do link                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | Falso                                          |
| Tem valor único       | Falso                                          |
| É indexado             | Falso                                          |
| No Catálogo Global      | Falso                                          |
| Descritor de segurança NT | O:BAG:BAD:S:                                   |
| Range-Lower            | 1                                              |
| Range-Upper            | 256                                            |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Classes usadas em        | [**Fila de Impressão**](c-printqueue.md)<br/> |



 

 





