---
title: Método INapEnforcementClientCallback NotifySoHChange (NapEnforcementClient. h)
description: É usado pelo NapAgent para informar o cliente de imposição de alterações SoH.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Método NotifySoHChange NAP
- Método NotifySoHChange NAP, interface INapEnforcementClientCallback
- INapEnforcementClientCallback interface NAP, método NotifySoHChange
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
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086473"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a>Método INapEnforcementClientCallback:: NotifySoHChange

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método de retorno de chamada **INapEnforcementClientCallback:: NotifySoHChange** é usado pelo NapAgent para informar o cliente de imposição de alterações soh.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método de retorno de chamada deve retornar um dos seguintes códigos de erro.



| Código de retorno                                                                                                | Descrição                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Retorne esse valor se a operação tiver êxito.<br/>                                                                                                                                                              |
| <dl> <dt>**\_servidor RPC \_ S \_ não disponível**</dt> </dl> | Retornar esse valor faz com que o imforcer seja removido da lista Bound-SHA e a entrada de cache NapAgent correspondente seja liberada. O SHA com falha pode inicializar novamente com o NapAgent.<br/> |



 

## <a name="remarks"></a>Comentários

A conclusão da correção do sistema é um evento de alteração de integridade do sistema. Isso significa que você deve chamar **NotifySoHChange** quando uma notificação [**INapSystemHealthAgentCallback:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indicar que o cliente está corrigido. Quando um cliente é corrigido, o membro de **estado** da estrutura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) retornada por **GetFixupInfo** tem um valor de **fixupStateSuccess**.

Depois de ser chamado pelo NapAgent por meio desse retorno de chamada, o agente de imposição deve chamar [**INapEnforcementClientBinding:: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) para recuperar a nova solicitação. Essa chamada pode ser feita no mesmo thread que **INapEnforcementClientCallback:: NotifySoHChange**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





