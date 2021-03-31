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
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640745"
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

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

