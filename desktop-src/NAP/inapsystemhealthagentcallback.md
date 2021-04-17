---
title: Interface INapSystemHealthAgentCallback (NapSystemHealthAgent. h)
description: São declaradas pelo sistema e implementadas pelo gravador de SHA para que o NapAgent possa se comunicar com o SHA.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- INapSystemHealthAgentCallback da interface NAP
- INapSystemHealthAgentCallback interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754748"
---
# <a name="inapsystemhealthagentcallback-interface"></a>Interface INapSystemHealthAgentCallback

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A interface **INapSystemHealthAgentCallback** fornece métodos de retorno de chamada que são declarados pelo sistema e implementados pelo gravador de SHA para que o NapAgent possa se comunicar com o Sha.

## <a name="members"></a>Membros

A interface **INapSystemHealthAgentCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSystemHealthAgentCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapSystemHealthAgentCallback** tem esses métodos.



| Método                                                                                                                                           | Descrição                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentCallback::CompareSoHRequests**](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | Usado pelo SHA para comparar o SoHs.<br/>                                                                      |
| [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | Chamado pelo NapAgent para determinar o estado do SHA.<br/>                                                 |
| [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | Chamado pelo NapAgent para consultar a solicitação SoH do SHA.<br/>                                                    |
| [**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | Chamado se uma solicitação SoH foi consultada a partir do SHA, mas a resposta nunca voltou.<br/>                      |
| [**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | Chamado pelo NapAgent para indicar que o estado de isolamento do sistema ou o tempo de término da experiência foi alterado.<br/> |
| [**INapSystemHealthAgentCallback::P rocessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md)                             | Chamado quando o NapAgent recebe uma resposta SoH destinada a este agente de integridade.<br/>                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

