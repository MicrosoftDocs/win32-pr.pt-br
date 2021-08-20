---
title: Método GetConnections INapEnforcementClientCallback (NapEnforcementClient. h)
description: É chamado pelo NapAgent e implementado pelo cliente de imposição para retornar um conjunto de conexões.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Método GetConnections NAP
- Método GetConnections NAP, interface INapEnforcementClientCallback
- Interface INapEnforcementClientCallback NAP, método GetConnections
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f6c6fdb4adc416cb25fa0e402c8fee2d8baf3270400f15a8de67966eff7a9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134025"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a>Método INapEnforcementClientCallback:: GetConnections

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método de retorno de chamada **INapEnforcementClientCallback:: GetConnections** é chamado pelo NapAgent e implementado pelo cliente de imposição para retornar um conjunto de conexões.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*conexões* \[ do fora\]
</dt> <dd>

Um ponteiro para o conjunto atual de [**conexões**](connections-struct.md)mantidas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método de retorno de chamada deve retornar um dos seguintes códigos de erro.



| Código de retorno                                                                                                | Descrição                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Retorne esse valor se a operação tiver êxito.<br/>                                                                                                                                                              |
| <dl> <dt>**\_servidor RPC \_ S \_ não disponível**</dt> </dl> | Retornar esse valor faz com que o imforcer seja removido da lista Bound-SHA e a entrada de cache NapAgent correspondente seja liberada. O SHA com falha pode inicializar novamente com o NapAgent.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





