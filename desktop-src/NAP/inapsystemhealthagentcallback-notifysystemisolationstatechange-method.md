---
title: Método INapSystemHealthAgentCallback NotifySystemIsolationStateChange (NapSystemHealthAgent. h)
description: É chamado pelo NapAgent para indicar que o estado de isolamento do sistema ou o tempo de término da experiência foi alterado.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- Método NotifySystemIsolationStateChange NAP
- Método NotifySystemIsolationStateChange NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método NotifySystemIsolationStateChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644763"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a>Método INapSystemHealthAgentCallback:: NotifySystemIsolationStateChange

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSystemHealthAgentCallback:: NotifySystemIsolationStateChange** é chamado pelo NapAgent para indicar que o estado de isolamento do sistema ou o tempo de término da experiência foi alterado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                          | Description                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Indica êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.

O agente de integridade pode consultar o estado NAP do sistema usando [**INapSystemHealthAgentBinding:: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





