---
description: O método EnumerateStreams enumera fluxos atualmente com os participantes. Esse método é fornecido para aplicativos C e C++. Aplicativos cliente de automação, como aqueles escritos em Visual Basic, devem usar o método \_ get Fluxos.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: Método ITParticipant::EnumerateStreams (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ec901c81bb0df666877ee06462b88da965b41bedd961e71cebbf25cd78ee30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140299"
---
# <a name="itparticipantenumeratestreams-method"></a>Método ITParticipant::EnumerateStreams

\[**EnumerateStreams** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método EnumerateStreams** enumera fluxos atualmente com os participantes. Esse método é fornecido para aplicativos C e C++. Aplicativos cliente de automação, como aqueles escritos em Visual Basic, devem usar o [**método \_ get Fluxos.**](itparticipant-get-streams.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnumStream* \[ out\]
</dt> <dd>

Ponteiro para o ponteiro da interface [**IEnumStream.**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                     | Significado                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl> | O *parâmetro ppEnumStream* não é um ponteiro válido.<br/> |



 

## <a name="remarks"></a>Comentários

TAPI chama o **método AddRef** na interface [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) retornada por **ITParticipant::EnumerateStreams**. O aplicativo deve chamar **Release** na interface **IEnumStream** para liberar recursos associados a ele.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**obter \_ Fluxos**](itparticipant-get-streams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




