---
title: Instalar-atributo de nível de interface do usuário
description: Esse atributo contém informações para o tipo (nível) de instalação que é usado para a interface do usuário.
ms.assetid: 718e04c7-ea96-4519-b312-12534ffd66df
ms.tgt_platform: multiple
keywords:
- Install-esquema de atributos de atributo de nível de interface do usuário
- Esquema de AD do atributo installUiLevel
topic_type:
- apiref
api_name:
- Install-Ui-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b93900bb401d1bdcd72f8881fb78026745c4e8f6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919319"
---
# <a name="install-ui-level-attribute"></a>Instalar-atributo de nível de interface do usuário

Esse atributo contém informações para o tipo (nível) de instalação que é usado para a interface do usuário. Os níveis de instalação possíveis são os seguintes: 2 INSTALLUILEVEL \_ None (instalação silenciosa) 3 INSTALLUILEVEL \_ Basic (instalação simples com tratamento de erros) 4 INSTALLUILEVEL \_ reduzido (interface do usuário criada, caixas de diálogo de assistente suprimidas) 5 INSTALLUILEVEL \_ completo (IU criada com assistentes, progresso, erros)



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Instalar-nível da interface do usuário                     |
| LDAP-Display-Name | installUiLevel                       |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.847               |
| System-ID-GUID    | 96a7dd64-9118-11d1-aebc-0000f80367c1 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| ID do link                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| É de valor único       | True                                                             |
| É indexado             | Falso                                                            |
| No catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes usadas em        | [**Registro de pacote**](c-packageregistration.md)<br/> |



 

 





