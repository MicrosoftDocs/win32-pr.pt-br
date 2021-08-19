---
title: Atributo ACS-DSBM-Priority
description: Esses atributos contêm a prioridade para esse SBM (Gerenciador de Largura de Banda de Sub-rede).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo ACS-DSBM-Priority
- Esquema do AD do atributo aCSDSBMPriority
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7a80c9c866b5c91f83f884ecaafe60e4596af4ca8d625791ed9264679c356
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637486"
---
# <a name="acs-dsbm-priority-attribute"></a>Atributo ACS-DSBM-Priority

Esses atributos contêm a prioridade para esse SBM (Gerenciador de Largura de Banda de Sub-rede). Quando um novo DSBM (Gerenciador de Largura de Banda de Sub-rede Designada) precisa ser selecionado, esse valor é enviado para outros SBMs no domínio como parte de uma mensagem de disposição do DSBM. \_ O SBM com a prioridade mais alta é selecionado como o novo DSBM.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ACS-DSBM-Priority                    |
| Ldap-Display-Name | aCSDSBMPriority                      |
| Tamanho              | 4 bytes                              |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.776               |
| System-Id-Guid    | 1cb3559e-56d0-11d1-a9c6-0000f80367c1 |
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
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sub-rede do ACS**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sub-rede do ACS**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sub-rede do ACS**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sub-rede do ACS**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sub-rede do ACS**](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------|
| ID do link                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Tem valor único       | Verdadeiro                                         |
| É indexado             | Falso                                        |
| No Catálogo Global      | Falso                                        |
| Descritor de segurança NT | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classes usadas em        | [**Sub-rede do ACS**](c-acssubnet.md)<br/> |



 

 





