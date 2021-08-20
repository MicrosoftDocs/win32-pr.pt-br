---
title: UAS-Compat atributo
description: Indica se o Gerenciador de contas de segurança impedirá tamanhos de dados para tornar Active Directory compatíveis com o UAS (sistema de conta de usuário) do LanManager.
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- Esquema de UAS-Compat do atributo AD
- Esquema de AD do atributo uASCompat
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7a0cb7b8787a55c710f283dbcd37bbe0f6a296505c75a5335bf35ea69c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681535"
---
# <a name="uas-compat-attribute"></a>UAS-Compat atributo

Indica se o Gerenciador de contas de segurança impedirá tamanhos de dados para tornar Active Directory compatíveis com o UAS (sistema de conta de usuário) do LanManager. Se esse valor for 0, nenhum limite será imposto. Se esse valor for 1, os limites a seguir serão impostos.



| Valor                          | Comprimento                         |
|--------------------------------|--------------------------------|
| Senha<br/>            | 0 a 14 caracteres<br/>  |
| Nome da Conta<br/>        | de 0 a 20 caracteres<br/>  |
| Nome de domínio<br/>         | de 0 a 15 caracteres<br/>  |
| Nome do Computador<br/>       | de 0 a 15 caracteres<br/>  |
| Comentários<br/>            | de 0 a 48 caracteres<br/>  |
| Diretório Base<br/>      | de 0 a 256 caracteres<br/> |
| Caminho do script<br/>         | de 0 a 256 caracteres<br/> |
| Unidades de tempo por semana<br/> | 168 bits (21 bytes)<br/> |



 



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | UAS-Compat                           |
| LDAP-Display-Name | uASCompat                            |
| Tamanho              | \-                                   |
| Privilégio de atualização  | Executado por um administrador.       |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.155               |
| System-ID-GUID    | bf967a61-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| É de valor único       | Verdadeiro                                                  |
| É indexado             | Falso                                                 |
| No catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| É de valor único       | True                                                  |
| É indexado             | Falso                                                 |
| No catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes usadas em        | [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Tem valor único       | Verdadeiro                                                  |
| É indexado             | Falso                                                 |
| No Catálogo Global      | Falso                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Tem valor único       | Verdadeiro                                                  |
| É indexado             | Falso                                                 |
| No Catálogo Global      | Falso                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Tem valor único       | True                                                  |
| É indexado             | Falso                                                 |
| No Catálogo Global      | Falso                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------|
| ID do link                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Tem valor único       | True                                                  |
| É indexado             | Falso                                                 |
| No Catálogo Global      | Falso                                                 |
| Descritor de segurança NT | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classes usadas em        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





