---
title: Método IsStopAvailable IMediaRendererActionInformation
description: Recupera um valor que indica se a DMR está aceitando o método StopAsync no momento.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- API de Streaming de Mídia do método IsStopAvailable
- API de Streaming de Mídia do método IsStopAvailable, interface IMediaRendererActionInformation
- API de Streaming de Mídia da interface IMediaRendererActionInformation , método IsStopAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c177c46c62309525d9362f985075cec293105a80678b3b857eafa0524179d17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712886"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a>Método IMediaRendererActionInformation::IsStopAvailable

Recupera um valor que indica se a DMR está aceitando o [**método StopAsync**](imediarenderer-stopasync.md) no momento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Um valor boolário que será **True** se a DMR estiver aceitando o método [**StopAsync**](imediarenderer-stopasync.md) no momento e **False** se não estiver.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

