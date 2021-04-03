---
title: Método IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync
description: Cria de forma assíncrona uma nova instância de um objeto que implementa a interface IMediaRenderer usando a interface IBasicDevice especificada.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- API de streaming de mídia do método CreateMediaRendererFromBasicDeviceAsync
- API de streaming de mídia do método CreateMediaRendererFromBasicDeviceAsync, interface IMediaRendererFactory
- API de streaming de mídia da interface IMediaRendererFactory, método CreateMediaRendererFromBasicDeviceAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007449"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a>Método IMediaRendererFactory:: CreateMediaRendererFromBasicDeviceAsync

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

*basicDevice* \[ no\]
</dt> <dd>

Um ponteiro para uma interface [**IBasicDevice**](ibasicdevice.md) que representa o dispositivo para o qual uma instância de [**IMediaRenderer**](imediarenderer.md) será criada.

</dd> <dt>

*valor* \[ do out, retval\]
</dt> <dd>

Recebe uma referência a um objeto [**CreateMediaRendererOperation**](createmediarendereroperation.md) que é usado para obter resultados da operação assíncrona.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

