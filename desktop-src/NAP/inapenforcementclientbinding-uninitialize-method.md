---
title: Método INapEnforcementClientBinding Uninitialize (NapEnforcementClient.h)
description: Conclui o serviço NapAgent.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Nap do método de não reinicialização
- Uninitialize method NAP , INapEnforcementClientBinding interface
- INapEnforcementClientBinding interface NAP , método Uninitialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613646eb169ab12c788cc294ab012962606a77b5f9fe5dfc8c041e6a4ad6fa35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940140"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a>Método INapEnforcementClientBinding::Uninitialize

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método INapEnforcementClientBinding::Uninitialize** conclui o serviço NapAgent.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O NapAgent bloqueia o processamento posterior até que todas as chamadas existentes nas interfaces [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) e [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) são concluídas. No final dessa chamada, o NapAgent libera todas as suas referências em ponteiros COM do cliente de imposição.

Antes que essa função seja chamada, o executor deve chamar [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) em todas as suas conexões ativas, para que os SHAs possam ser notificados se qualquer um dos seus SoH-Requests ficou órfão.

O cliente de imposição deve chamar o método [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding.**](inapenforcementclientbinding.md)

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





