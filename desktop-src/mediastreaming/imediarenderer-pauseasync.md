---
title: Método PauseAsync do IMediaRenderer
description: Instrui a DMR de forma assíncrona a pausar a reprodução do conteúdo atual. | Método PauseAsync do IMediaRenderer
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- API de Streaming de Mídia do método PauseAsync
- API de Streaming de Mídia do método PauseAsync, interface IMediaRenderer
- API de Streaming de Mídia da interface IMediaRenderer, método PauseAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a953d024ee0f90f7cb466574b29d7e3cfe150072bf1a3787734f8365916cb2a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972265"
---
# <a name="imediarendererpauseasync-method"></a>Método IMediaRenderer::P auseAsync

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

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





