---
title: Método IsVideoSupported de IMediaRenderer
description: Recupera um valor que indica se a DMR é capaz de tocar conteúdo de vídeo.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- API de Streaming de Mídia do método IsVideoSupported
- API de Streaming de Mídia do método IsVideoSupported, interface IMediaRenderer
- API de Streaming de Mídia da interface IMediaRenderer, método IsVideoSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c1f6fa149c6c5025d3fd2c785dc2f4a8451fabed3906b559674d8038662c21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972305"
---
# <a name="imediarendererisvideosupported-method"></a>Método IMediaRenderer::IsVideoSupported

Recupera um valor que indica se a DMR é capaz de tocar conteúdo de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Um valor booliana que será **True se** a DMR for capaz de tocar conteúdo de vídeo e **False** se não for.

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

 

 





