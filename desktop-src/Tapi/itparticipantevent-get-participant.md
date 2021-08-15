---
description: O método \_ get Participant obtém um ponteiro para uma matriz de interfaces ITParticipant que representam os participantes envolvidos no evento.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: Método ITParticipantEvent::get_Participant (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d53b5269b0940888ca5a849e4ecc8cc98d053bbe80340dcfa1a858eabd6ceed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864510"
---
# <a name="itparticipanteventget_participant-method"></a>Método ItParticipantEvent::get \_ Participant

\[**get \_ O** participante não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método \_ get Participant** obtém um ponteiro para uma matriz de interfaces [**ITParticipant**](itparticipant.md) que representam os participantes envolvidos no evento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppParticipant* \[ out\]
</dt> <dd>

Ponteiro para matriz de [**interfaces ITParticipant.**](itparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                           | Significado                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Há memória insuficiente para executar a operação.<br/>  |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | Não há participantes associados ao evento.<br/>  |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>       | O *parâmetro ppParticipant* não é um ponteiro válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




