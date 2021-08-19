---
title: Método IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync
description: Cria de forma assíncrona uma nova instância de um objeto que implementa a interface IMediaRenderer usando a interface IBasicDevice especificada.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- Api de Streaming de Mídia do método CreateMediaRendererFromBasicDeviceAsync
- CreateMediaRendererFromBasicDeviceAsync method Media Streaming API , interface IMediaRendererFactory
- API de Streaming de Mídia da interface IMediaRendererFactory , método CreateMediaRendererFromBasicDeviceAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b9ee80a4f681bb57d62f84d35cf3a254e38982a10f642a35e35187f6af9e48e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092282"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a>Método IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync

Cria de forma assíncrona uma nova instância de um objeto que implementa a interface [**IMediaRenderer**](imediarenderer.md) usando a interface [**IBasicDevice**](ibasicdevice.md) especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*basicDevice* \[ Em\]
</dt> <dd>

Um ponteiro para uma interface [**IBasicDevice**](ibasicdevice.md) que representa o dispositivo para o qual uma instância [**de IMediaRenderer**](imediarenderer.md) será criada.

</dd> <dt>

*value* \[ out, retval\]
</dt> <dd>

Recebe uma referência a [**um objeto CreateMediaRendererOperation**](createmediarendereroperation.md) usado para obter resultados da operação assíncrona.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

