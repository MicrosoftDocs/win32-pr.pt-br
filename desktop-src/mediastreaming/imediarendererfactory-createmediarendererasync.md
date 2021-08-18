---
title: Método IMediaRendererFactory CreateMediaRendererAsync
description: Cria de forma assíncrona uma nova instância de um objeto que implementa a interface IMediaRenderer usando o nome de dispositivo exclusivo especificado (UDN).
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- API de streaming de mídia do método CreateMediaRendererAsync
- API de streaming de mídia do método CreateMediaRendererAsync, interface IMediaRendererFactory
- API de streaming de mídia da interface IMediaRendererFactory, método CreateMediaRendererAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e459324d96f031ab3433f0d8bfe8ba5de562d76c95f51affd7b72d130655fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735482"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a>Método IMediaRendererFactory:: CreateMediaRendererAsync

Cria de forma assíncrona uma nova instância de um objeto que implementa a interface [**IMediaRenderer**](imediarenderer.md) usando o nome de dispositivo exclusivo especificado (UDN).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*deviceIdentifier* \[ no\]
</dt> <dd>

Um HSTRING que contém um UDN que identifica o dispositivo DMR DLNA para o qual uma instância de [**IMediaRenderer**](imediarenderer.md) será criada.

</dd> <dt>

*valor* \[ do out, retval\]
</dt> <dd>

Recebe uma referência a um objeto [**CreateMediaRendererOperation**](createmediarendereroperation.md) que é usado para obter resultados da operação assíncrona.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

