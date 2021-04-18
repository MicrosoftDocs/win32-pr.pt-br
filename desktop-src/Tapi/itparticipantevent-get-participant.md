---
description: O \_ método Get participante obtém um ponteiro para uma matriz de interfaces ITParticipant que representa os participantes envolvidos no evento.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'Método ITParticipantEvent:: get_Participant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756995"
---
# <a name="itparticipanteventget_participant-method"></a>Método ITParticipantEvent:: get \_ participante

\[**obter \_ O participante** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ participante** Obtém um ponteiro para uma matriz de interfaces [**ITParticipant**](itparticipant.md) que representa os participantes envolvidos no evento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppParticipant* \[ fora\]
</dt> <dd>

Ponteiro para matriz de interfaces [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                           | Significado                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Há memória insuficiente para executar a operação.<br/>  |
| <dl> <dt>**TAPI \_ E \_ noitems**</dt> </dl> | Não há participantes associados ao evento.<br/>  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>       | O parâmetro *ppParticipant* não é um ponteiro válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




