---
title: Método IsPlayAvailable de IMediaRendererActionInformation
description: Recupera um valor que indica se a DMR está aceitando os métodos PlayAsync e PlayAtSpeedAsync no momento.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- API de Streaming de Mídia do método IsPlayAvailable
- API de Streaming de Mídia do método IsPlayAvailable, interface IMediaRendererActionInformation
- API de Streaming de Mídia da interface IMediaRendererActionInformation , método IsPlayAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 912e5478ef1d9bd7114d198a9671d38ba7b721c9dbd82d2a8080b5a7876e76cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235841"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a>Método IMediaRendererActionInformation::IsPlayAvailable

Recupera um valor que indica se a DMR está aceitando os métodos [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) e [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) no momento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Um valor boolário que será **True** se a DMR estiver aceitando atualmente os métodos [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) e [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) e **False** se não estiver.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Veja também

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

