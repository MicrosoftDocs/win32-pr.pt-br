---
title: Método MediaRenderer. StopAsync
description: Instrui o DMR de forma assíncrona a interromper a reprodução do conteúdo atual. | Método MediaRenderer. StopAsync
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- API de streaming de mídia do método StopAsync
- API de streaming de mídia do método StopAsync, interface MediaRenderer
- API de streaming de mídia da interface MediaRenderer, método StopAsync
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 205c69a83572539974c1b8ad2cf45159c45335cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104091927"
---
# <a name="mediarendererstopasync-method"></a>Método MediaRenderer. StopAsync

Instrui o DMR de forma assíncrona a interromper a reprodução do conteúdo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StopAsync(
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



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**MediaRenderer**](mediarenderer.md)
</dt> </dl>

 

 





