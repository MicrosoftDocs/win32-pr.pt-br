---
title: Método GetMuteOperation. GetResults
description: Retorna os resultados da operação assíncrona iniciada pelo GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface GetMuteOperation
- API de streaming de mídia da interface GetMuteOperation, método GetResults
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084480"
---
# <a name="getmuteoperationgetresults-method"></a>Método GetMuteOperation. GetResults

Retorna os resultados da operação assíncrona iniciada pelo [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do out, retval\]
</dt> <dd>

O valor de mudo. Um valor true indica que o áudio está mudo no momento. Um valor false indica que o áudio não está mudo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

O método **GetResults** é normalmente chamado a partir do manipulador de eventos que foi registrado pela configuração da propriedade [**Completed**](getmuteoperation-completed.md) .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

