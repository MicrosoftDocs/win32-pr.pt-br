---
title: Conjunto de propriedades de restrições de conta do usuário
description: Conjunto de propriedades que contém os atributos de usuário que descrevem as restrições de conta.
ms.assetid: 5616fede-12b1-41bd-b445-11c0e1ff66db
ms.tgt_platform: multiple
keywords:
- Propriedade de restrições de conta do usuário definir esquema do AD
topic_type:
- apiref
api_name:
- User-Account-Restrictions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3c39c80c83f321c654e675ccd87950cfd4bcf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919290"
---
# <a name="user-account-restrictions-property-set"></a>Conjunto de propriedades de restrições de conta do usuário

Conjunto de propriedades que contém os atributos de usuário que descrevem as restrições de conta.



| Entrada | Valor |
|--------------|--------------------------------------|
| CN           | Restrições de conta de usuário            |
| Display-Name | Restrições de conta                 |
| GUID de direitos  | 4c164200-20c0-11d0-a768-00aa006e0529 |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Usuário**](c-user.md)<br/> [**Computador**](c-computer.md)<br/>                                                                                                                                                   |
| Localização-exibição-ID | 9                                                                                                                                                                                                                             |
| Membros do conjunto de propriedades    | [**Conta-expira**](a-accountexpires.md)<br/> [**Pwd-último-conjunto**](a-pwdlastset.md)<br/> [**Controle de conta de usuário**](a-useraccountcontrol.md)<br/> [**Parâmetros do usuário**](a-userparameters.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Usuário**](c-user.md)<br/> [**Computador**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Localização-exibição-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Membros do conjunto de propriedades    | [**Conta-expira**](a-accountexpires.md)<br/> [**ms-DS-usuário-conta-controle-calculado**](a-msds-user-account-control-computed.md)<br/> [**Pwd-último-conjunto**](a-pwdlastset.md)<br/> [**Controle de conta de usuário**](a-useraccountcontrol.md)<br/> [**Parâmetros do usuário**](a-userparameters.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | \-                                                                                                                                                                                                    |
| Localização-exibição-ID | 9                                                                                                                                                                                                     |
| Membros do conjunto de propriedades    | [**Conta-expira**](a-accountexpires.md)<br/> [**ms-DS-usuário-conta-controle-calculado**](a-msds-user-account-control-computed.md)<br/> [**Pwd-último-conjunto**](a-pwdlastset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Usuário**](c-user.md)<br/> [**Computador**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Localização-exibição-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Membros do conjunto de propriedades    | [**Conta-expira**](a-accountexpires.md)<br/> [**ms-DS-usuário-conta-controle-calculado**](a-msds-user-account-control-computed.md)<br/> [**Pwd-último-conjunto**](a-pwdlastset.md)<br/> [**Controle de conta de usuário**](a-useraccountcontrol.md)<br/> [**Parâmetros do usuário**](a-userparameters.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Usuário**](c-user.md)<br/> [**Computador**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                   |
| Localização-exibição-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membros do conjunto de propriedades    | [**Conta-expira**](a-accountexpires.md)<br/> [**ms-DS-usuário-conta-controle-calculado**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expires-time-computado**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-último-conjunto**](a-pwdlastset.md)<br/> [**Controle de conta de usuário**](a-useraccountcontrol.md)<br/> [**Parâmetros do usuário**](a-userparameters.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Usuário**](c-user.md)<br/> [**Computador**](c-computer.md)<br/> [**Conta de serviço do MS-DS-Managed-Service**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Localização-exibição-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membros do conjunto de propriedades    | [**Conta-expira**](a-accountexpires.md)<br/> [**ms-DS-usuário-conta-controle-calculado**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expires-time-computado**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-último-conjunto**](a-pwdlastset.md)<br/> [**Controle de conta de usuário**](a-useraccountcontrol.md)<br/> [**Parâmetros do usuário**](a-userparameters.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Usuário**](c-user.md)<br/> [**Computador**](c-computer.md)<br/> [**Conta de serviço do MS-DS-Managed-Service**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Localização-exibição-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Membros do conjunto de propriedades    | [**Conta-expira**](a-accountexpires.md)<br/> [**ms-DS-usuário-conta-controle-calculado**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expires-time-computado**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-último-conjunto**](a-pwdlastset.md)<br/> [**Controle de conta de usuário**](a-useraccountcontrol.md)<br/> [**Parâmetros do usuário**](a-userparameters.md)<br/> |



 

 





