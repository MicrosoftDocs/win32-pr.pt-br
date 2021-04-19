---
title: Método IMediaRenderer PauseAsync
description: Instrui o DMR de forma assíncrona a pausar a reprodução do conteúdo atual. | Método IMediaRenderer PauseAsync
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- API de streaming de mídia do método PauseAsync
- API de streaming de mídia do método PauseAsync, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método PauseAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8713fa4b2fe46a694024c2873cd50a0ec89ce898
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105812040"
---
# <a name="imediarendererpauseasync-method"></a>IMediaRenderer: método auseAsync de:P

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

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





