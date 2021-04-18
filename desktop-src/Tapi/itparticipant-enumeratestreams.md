---
description: O método EnumerateStreams enumera fluxos atualmente com os participantes. Esse método é fornecido para aplicativos C e C++. Aplicativos cliente de automação, como aqueles escritos em Visual Basic, devem usar o \_ método Get Streams.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'Método ITParticipant:: EnumerateStreams (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760340"
---
# <a name="itparticipantenumeratestreams-method"></a>Método ITParticipant:: EnumerateStreams

\[O **EnumerateStreams** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **EnumerateStreams** enumera fluxos atualmente com os participantes. Esse método é fornecido para aplicativos C e C++. Aplicativos cliente de automação, como aqueles escritos em Visual Basic, devem usar o método [**Get \_ streams**](itparticipant-get-streams.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnumStream* \[ fora\]
</dt> <dd>

Ponteiro para ponteiro de interface [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                     | Significado                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | O parâmetro *ppEnumStream* não é um ponteiro válido.<br/> |



 

## <a name="remarks"></a>Comentários

A TAPI chama o método **AddRef** na interface [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) retornada por **ITParticipant:: EnumerateStreams**. O aplicativo deve chamar **Release** na interface **IEnumStream** para liberar recursos associados a ela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**obter \_ fluxos**](itparticipant-get-streams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




