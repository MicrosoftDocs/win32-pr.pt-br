---
title: Método MediaRenderer. PauseAsync
description: Instrui o DMR de forma assíncrona a pausar a reprodução do conteúdo atual. | Método MediaRenderer. PauseAsync
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- API de streaming de mídia do método PauseAsync
- API de streaming de mídia do método PauseAsync, interface MediaRenderer
- API de streaming de mídia da interface MediaRenderer, método PauseAsync
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105788648"
---
# <a name="mediarendererpauseasync-method"></a>Método MediaRenderer. PauseAsync

Instrui o DMR de forma assíncrona a pausar a reprodução do conteúdo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe uma referência a um objeto [**PlaybackOperation**](playbackoperation.md) que é usado para obter resultados da operação assíncrona.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





