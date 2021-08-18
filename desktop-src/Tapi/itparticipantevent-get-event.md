---
description: O \_ método Get Event obtém um \_ descritor de evento participante do tipo de evento que ocorreu.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'Método ITParticipantEvent:: get_Event (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d45e8f6aab556eb1b6f5c6dc1b4b0cbadf9653e06fd77f4fb806b7ef89d7813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864697"
---
# <a name="itparticipanteventget_event-method"></a>Método de evento ITParticipantEvent:: get \_

\[**obter \_ o evento** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ Event** Obtém um descritor de [**\_ evento participante**](participant-event.md) do tipo de evento que ocorreu.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pParticipantEvent* \[ fora\]
</dt> <dd>

Ponteiro para um descritor de [**\_ evento de participante**](participant-event.md) do evento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>      |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pParticipantEvent* não é um ponteiro válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**evento de participante \_**](participant-event.md)
</dt> </dl>

 

 




