---
description: O \_ subStream get obtém um ponteiro para uma matriz de interfaces ITSubStream que representam os substreams envolvidos no evento.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: Método ITParticipantEvent::get_SubStream (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258f68815a5bc7cd201d94ab55199d59ebe6759eb2e279a1c80add91ea6c3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774656"
---
# <a name="itparticipanteventget_substream-method"></a>Método ITParticipantEvent::get \_ SubStream

\[**get \_ O SubStream** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **\_ subStream get** obtém um ponteiro para uma matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representam os substreams envolvidos no evento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSubStream* \[ out\]
</dt> <dd>

Ponteiro para a matriz de [**ponteiros ITSubStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor                                                                                           | Significado                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | Não há substreams associados ao evento.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>       | O *parâmetro ppSubStream* não é um ponteiro válido.<br/>  |



 

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

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

