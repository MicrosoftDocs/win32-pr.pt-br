---
title: Interface INapSystemHealthAgentBinding (NapSystemHealthAgent.h)
description: Os SHAs usam para se comunicar com o NapAgent. | Interface INapSystemHealthAgentBinding (NapSystemHealthAgent.h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- INapSystemHealthAgentBinding interface NAP
- NAP da interface INapSystemHealthAgentBinding, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38fe66a5cd6883114ff46da3e98174d299f1813e670ed5ce67ee3843dc210d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799181"
---
# <a name="inapsystemhealthagentbinding-interface"></a>Interface INapSystemHealthAgentBinding

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **INapSystemHealthAgentBinding** fornece métodos que os SHAs usam para se comunicar com o NapAgent.

> [!Note]  
> [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) herda todos os métodos dessa interface e deve ser usado em vez disso.

 

## <a name="members"></a>Membros

A interface **INapSystemHealthAgentBinding** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthAgentBinding** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapSystemHealthAgentBinding** tem esses métodos.



| Método                                                                                                                     | Descrição                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding::FlushCache**](inapsystemhealthagentbinding-flushcache-method.md)                         | Chamado por um SHA para liberar seu cache SoH.<br/>                                                |
| [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | Chamado por SHAs para determinar o estado de isolamento do sistema.<br/>                                 |
| [**INapSystemHealthAgentBinding::Initialize**](inapsystemhealthagentbinding-initialize-method.md)                         | Inicializa o SHA e vincula o SHA ao serviço NapAgent. <br/>                         |
| [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md)               | Chamado por SHAs quando seu SoH muda.<br/>                                                  |
| [**INapSystemHealthAgentBinding::Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md)                     | Chamado por SHAs para fazer com que o NapAgent libere todas as suas referências a ponteiros SHA COM.<br/> |



 

## <a name="remarks"></a>Comentários

Todas as APIs nesta interface retornarão **RPC \_ E \_ DISCONNECTED** se o NapAgent for interrompido. Esse objeto será recuperado automaticamente e reabinado ao NapAgent, depois que ele for reiniciado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referência nap](nap-reference.md)
</dt> </dl>

 

