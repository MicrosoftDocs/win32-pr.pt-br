---
title: Interface INapEnforcementClientBinding (NapEnforcementClient. h)
description: Os clientes de imposição usam o para se comunicar com o NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- INapEnforcementClientBinding da interface NAP
- INapEnforcementClientBinding interface NAP, descrita
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
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824800"
---
# <a name="inapenforcementclientbinding-interface"></a>Interface INapEnforcementClientBinding

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O **INapEnforcementClientBinding** fornece métodos que os clientes imposição usam para se comunicar com o NapAgent.

## <a name="members"></a>Membros

A interface **INapEnforcementClientBinding** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientBinding** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapEnforcementClientBinding** tem esses métodos.



| Método                                                                                                                           | Descrição                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientBinding:: CreateConnection**](inapenforcementclientbinding-createconnection-method.md)                   | Usado por imforcers para criar objetos de conexão.<br/>                                                                                                                                                            |
| [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)                         | Usado pelo cliente de imposição quando ele precisa de uma solicitação SoH para uma conexão específica.<br/>                                                                                                                   |
| [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md)                               | Inicia o serviço NapAgent. O cliente de imposição deve chamar esse método antes de chamar qualquer outro método dessa interface.<br/>                                                                            |
| [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | Usado para informar ao NapAgent que uma conexão com um cliente de imposição foi desativada.<br/>                                                                                                                      |
| [**INapEnforcementClientBinding::NotifySoHChangeFailure**](inapenforcementclientbinding-notifysohchangefailure-method.md)       | Usado pelo cliente de imposição para informar ao NapAgent que ele não pôde processar um [**INapEnforcementClientCallback:: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)anterior.<br/> |
| [**INapEnforcementClientBinding::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md)               | Usado por clientes de imposição sempre que eles recebem um blob de dados de SoH-Response do servidor de imposição.<br/>                                                                                                       |
| [**INapEnforcementClientBinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)                           | Conclui o serviço NapAgent para esta conexão de cliente.<br/>                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

Todas as APIs nesta interface retornarão RPC \_ E \_ desconectadas se o NapAgent for interrompido. Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

