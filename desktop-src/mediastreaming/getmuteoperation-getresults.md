---
title: Método GetMuteOperation.GetResults
description: Retorna os resultados da operação assíncrona iniciada por GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- API de Streaming de Mídia do método GetResults
- API de Streaming de Mídia do método GetResults, interface GetMuteOperation
- API de Streaming de Mídia da interface GetMuteOperation, método GetResults
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37b8356a677f5e752fdf4e4ec658cc4077a17fa76b6181097d5753d898eef89e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972405"
---
# <a name="getmuteoperationgetresults-method"></a>Método GetMuteOperation.GetResults

Retorna os resultados da operação assíncrona iniciada por [**GetMuteAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

O valor de mute. Um valor true indica que o áudio está mudo no momento. Um valor false indica que o áudio não está mudo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

O **método GetResults** normalmente é chamado do manipulador de eventos que foi registrado definindo a [**propriedade**](getmuteoperation-completed.md) Completed.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

