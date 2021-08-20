---
title: Interface INapEnforcementClientBinding (NapEnforcementClient.h)
description: Os clientes de imposição usam para se comunicar com o NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- INapEnforcementClientBinding interface NAP
- NAP da interface INapEnforcementClientBinding, descrita
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad90e7f96a981a28e4c44351d5a2a4f55c75184826154e0e2effba54157049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134062"
---
# <a name="inapenforcementclientbinding-interface"></a>Interface INapEnforcementClientBinding

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **INapEnforcementClientBinding** fornece métodos que os clientes de imposição usam para se comunicar com o NapAgent.

## <a name="members"></a>Membros

A interface **INapEnforcementClientBinding** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapEnforcementClientBinding** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapEnforcementClientBinding** tem esses métodos.



| Método                                                                                                                           | Descrição                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientBinding::CreateConnection**](inapenforcementclientbinding-createconnection-method.md)                   | Usado por executores para criar objetos de conexão.<br/>                                                                                                                                                            |
| [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)                         | Usado pelo cliente de imposição quando ele precisa de uma solicitação SoH para uma conexão específica.<br/>                                                                                                                   |
| [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md)                               | Inicia o serviço NapAgent. O cliente de imposição deve chamar esse método antes de chamar qualquer outro método dessa interface.<br/>                                                                            |
| [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | Usado para informar o NapAgent de que uma conexão com um cliente de imposição foi inometada.<br/>                                                                                                                      |
| [**INapEnforcementClientBinding::NotifySoHChangeFailure**](inapenforcementclientbinding-notifysohchangefailure-method.md)       | Usado pelo cliente de imposição para informar ao NapAgent que ele não pôde processar um [**INapEnforcementClientCallback::NotifySoHChange anterior.**](inapenforcementclientcallback-notifysohchange-method.md)<br/> |
| [**INapEnforcementClientBinding::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md)               | Usado pelos clientes de imposição sempre que eles SoH-Response um blob de dados do servidor de imposição.<br/>                                                                                                       |
| [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)                           | Conclui o serviço NapAgent para esta conexão de cliente.<br/>                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

Todas as APIs nesta interface retornarão RPC \_ E \_ DISCONNECTED se o NapAgent for interrompido. Esse objeto será recuperado automaticamente e reabinado ao NapAgent, depois que ele for reiniciado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[NAP Interfaces](nap-interfaces.md)
</dt> <dt>

[Referência nap](nap-reference.md)
</dt> </dl>

 

