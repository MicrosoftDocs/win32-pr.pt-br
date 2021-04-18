---
title: Interface INapEnforcementClientCallback (NapEnforcementClient. h)
description: Os clientes de imposição devem implementar o para permitir que o NapAgent se comunique com eles.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- INapEnforcementClientCallback da interface NAP
- INapEnforcementClientCallback interface NAP, descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780618"
---
# <a name="inapenforcementclientcallback-interface"></a>Interface INapEnforcementClientCallback

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapEnforcementClientCallback** fornece métodos de retorno de chamada que os clientes de imposição devem implementar para permitir que o NapAgent se comunique com eles.

## <a name="members"></a>Membros

A interface **INapEnforcementClientCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapEnforcementClientCallback** tem esses métodos.



| Método                                                                                                         | Descrição                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientCallback:: GetConnections**](inapenforcementclientcallback-getconnections-method.md)   | Usado pelo NapAgent para recuperar conexões.<br/>                         |
| [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) | Usado pelo NapAgent para informar o cliente de imposição de alterações SoH.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



 

