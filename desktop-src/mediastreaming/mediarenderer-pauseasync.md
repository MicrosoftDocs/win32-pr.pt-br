---
title: Método MediaRenderer.PauseAsync
description: Instrui a DMR de forma assíncrona a pausar a reprodução do conteúdo atual. | Método MediaRenderer.PauseAsync
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- API de Streaming de Mídia do método PauseAsync
- API de Streaming de Mídia do método PauseAsync, interface MediaRenderer
- API de Streaming de Mídia da interface MediaRenderer, método PauseAsync
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5dcb4474f7a7843f2812cf64e0119912eca8ae320b29b9acb0131a65bbbffa19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060246"
---
# <a name="mediarendererpauseasync-method"></a>Método MediaRenderer.PauseAsync

Instrui a DMR de forma assíncrona a pausar a reprodução do conteúdo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Recebe uma referência a um [**objeto PlaybackOperation**](playbackoperation.md) que é usado para obter resultados da operação assíncrona.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mediarenderer**](mediarenderer.md)
</dt> </dl>

 

 





