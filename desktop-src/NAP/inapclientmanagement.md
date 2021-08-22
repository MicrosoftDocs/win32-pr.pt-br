---
title: Interface INapClientManagement (NapManagement. h)
description: Fornece métodos para o gerenciamento de cliente NAP. | Interface INapClientManagement (NapManagement. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- INapClientManagement da interface NAP
- INapClientManagement interface NAP, descrita
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a9d338cdaad8ed46fd3c3c730ca3ae4c2065cda9803c283ae262addd939713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622112"
---
# <a name="inapclientmanagement-interface"></a>Interface INapClientManagement

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapClientManagement** fornece métodos para o gerenciamento de cliente NAP.

> [!Note]  
> [**INapClientManagement2**](inapclientmanagement2.md) herda todos os métodos dessa interface e deve ser usado em seu lugar.

 

## <a name="members"></a>Membros

A interface **INapClientManagement** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapClientManagement** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapClientManagement** tem esses métodos.



| Método                                                                                                                | Descrição                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**INapClientManagement::GetNapClientInfo**](inapclientmanagement-getnapclientinfo.md)                               | Recupera informações sobre um cliente NAP.<br/>                          |
| [**INapClientManagement::GetRegisteredEnforcementClients**](inapclientmanagement-getregisteredenforcementclients.md) | Recupera informações sobre os clientes de imposição registrados.<br/>    |
| [**INapClientManagement::GetRegisteredSystemHealthAgents**](inapclientmanagement-getregisteredsystemhealthagents.md) | Recuperar informações sobre um SHA registrado.<br/>                       |
| [**INapClientManagement::GetSystemIsolationInfo**](inapclientmanagement-getsystemisolationinfo.md)                   | Recupera informações sobre o estado de isolamento do cliente NAP.<br/> |
| [**INapClientManagement::RegisterEnforcementClient**](inapclientmanagement-registerenforcementclient.md)             | Registra um cliente de imposição com o sistema NAP.<br/>               |
| [**INapClientManagement::RegisterSystemHealthAgent**](inapclientmanagement-registersystemhealthagent.md)             | Registra um SHA com o sistema NAP.<br/>                              |
| [**INapClientManagement::UnregisterEnforcementClient**](inapclientmanagement-unregisterenforcementclient.md)         | Cancela o registro de um cliente de imposição com o sistema NAP.<br/>             |
| [**INapClientManagement::UnregisterSystemHealthAgent**](inapclientmanagement-unregistersystemhealthagent.md)         | Cancela o registro de um SHA com o sistema NAP.<br/>                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

