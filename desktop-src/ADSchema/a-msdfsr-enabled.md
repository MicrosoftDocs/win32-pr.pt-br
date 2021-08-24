---
title: atributo habilitado para MS-DFSR
description: Especifica se o objeto está habilitado.
ms.assetid: 60496ed7-ea72-4a3b-8d89-65f970d92baa
ms.tgt_platform: multiple
keywords:
- Esquema do AD de atributos habilitados para DFSR da MS
- Esquema de AD de atributo habilitado para msDFSR
topic_type:
- apiref
api_name:
- ms-DFSR-Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87bae0703d7acf06f1590e52922c07efb6d9af9652e6a052ad80e098eb2d0cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119298786"
---
# <a name="ms-dfsr-enabled-attribute"></a>atributo habilitado para MS-DFSR

Especifica se o objeto está habilitado.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | MS-DFSR habilitado                      |
| LDAP-Display-Name | Habilitado para msDFSR                       |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.6.13.3.9            |
| System-ID-GUID    | 03726ae7-8e7d-4446-8aae-a91657c00993 |
| Syntax            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | Falso                                                                                                                         |
| É de valor único       | True                                                                                                                          |
| É indexado             | Falso                                                                                                                         |
| No catálogo global      | Falso                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000000                                                                                                                    |
| Classes usadas em        | [**MS-DFSR-Subscription**](c-msdfsr-subscription.md)<br/> [**MS-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | Falso                                                                                                                         |
| É de valor único       | True                                                                                                                          |
| É indexado             | Falso                                                                                                                         |
| No catálogo global      | Falso                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000000                                                                                                                    |
| Classes usadas em        | [**MS-DFSR-Subscription**](c-msdfsr-subscription.md)<br/> [**MS-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | Falso                                                                                                                         |
| É de valor único       | True                                                                                                                          |
| É indexado             | Falso                                                                                                                         |
| No catálogo global      | Falso                                                                                                                         |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000000                                                                                                                    |
| Classes usadas em        | [**MS-DFSR-Subscription**](c-msdfsr-subscription.md)<br/> [**MS-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | Falso                                                                                                                         |
| Tem valor único       | Verdadeiro                                                                                                                          |
| É indexado             | Falso                                                                                                                         |
| No Catálogo Global      | Falso                                                                                                                         |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000000                                                                                                                    |
| Classes usadas em        | [**ms-DFSR-Subscription**](c-msdfsr-subscription.md)<br/> [**ms-DFSR-Connection**](c-msdfsr-connection.md)<br/> |



## <a name="remarks"></a>Comentários

O **atributo ms-DFSR-Enabled** faz parte do suporte ao serviço de replicação Sistema de Arquivos Distribuído (DFS).

 

 





