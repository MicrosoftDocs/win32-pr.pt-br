---
description: O método EnumerateParticipants enumera os participantes associados à conferência atual.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'Método ITParticipantControl:: EnumerateParticipants (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758117"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a>Método ITParticipantControl:: EnumerateParticipants

\[O **EnumerateParticipants** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **EnumerateParticipants** enumera os participantes associados à conferência atual. Esse método é fornecido para aplicativos C e C++. Aplicativos cliente de automação, como aqueles escritos em Visual Basic, devem usar o método [**Get \_ participantes**](itparticipantcontrol-get-participants.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnumParticipants* \[ fora\]
</dt> <dd>

Ponteiro para a interface [**IEnumParticipant**](ienumparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                         | Significado                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                          |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppEnumParticipants* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>       |



 

## <a name="remarks"></a>Comentários

A TAPI chama o método **AddRef** na interface [**IEnumParticipant**](ienumparticipant.md) retornada por **ITParticipantControl:: EnumerateParticipants**. O aplicativo deve chamar **Release** na interface **IEnumParticipant** para liberar recursos associados a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipantControl**](itparticipantcontrol.md)
</dt> <dt>

[**obter \_ participantes**](itparticipantcontrol-get-participants.md)
</dt> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




