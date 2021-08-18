---
title: Método NotifySoHChange INapEnforcementClientCallback (NapEnforcementClient.h)
description: É usado pelo NapAgent para informar o cliente de imposição de alterações de SoH.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- NAP do método NotifySoHChange
- Interface NAP do método NotifySoHChange, INapEnforcementClientCallback
- Interface NAP INapEnforcementClientCallback , método NotifySoHChange
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9011db09b698f886bd10ad19298a104668d038cc2bb11136b6e4ac58035e3425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940130"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a>Método INapEnforcementClientCallback::NotifySoHChange

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O método de retorno de chamada **INapEnforcementClientCallback::NotifySoHChange** é usado pelo NapAgent para informar o cliente de imposição de alterações de SoH.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método de retorno de chamada deve retornar um dos códigos de erro a seguir.



| Código de retorno                                                                                                | Descrição                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Retornará esse valor se a operação for bem-sucedida.<br/>                                                                                                                                                              |
| <dl> <dt>**SERVIDOR RPC \_ S \_ \_ INDISPONÍVEL**</dt> </dl> | Retornar esse valor faz com que o executor seja removido da lista bound-SHA e a entrada de cache NapAgent correspondente seja liberado. O SHA com falha pode então se inicializar com o NapAgent.<br/> |



 

## <a name="remarks"></a>Comentários

A conclusão da correção do sistema é um evento de alteração de saúde do sistema. Isso significa que você deve chamar **NotifySoHChange** quando uma notificação [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indicar que o cliente foi corrigido. Quando um cliente é  fixo, o membro de estado da estrutura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) retornada por **GetFixupInfo** tem um valor **de fixupStateSuccess**.

Depois de ser chamado pelo NapAgent por meio desse retorno de chamada, o agente de imposição deve chamar [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) para recuperar a nova solicitação. Essa chamada pode ser feita no mesmo thread que **INapEnforcementClientCallback::NotifySoHChange**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





