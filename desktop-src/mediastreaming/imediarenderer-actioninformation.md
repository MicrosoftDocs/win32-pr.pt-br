---
title: Método IMediaRenderer ActionInformation
description: Recupera informações sobre quais métodos podem ser invocados atualmente no DMR.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- API de streaming de mídia do método ActionInformation
- API de streaming de mídia do método ActionInformation, interface IMediaRenderer
- API de streaming de mídia da interface IMediaRenderer, método ActionInformation
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3caf251c080f218b99861d4a81920cd5c95c1f0e53bc6b006c84536f33f7f29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735519"
---
# <a name="imediarendereractioninformation-method"></a>Método IMediaRenderer:: ActionInformation

Recupera informações sobre quais métodos podem ser invocados atualmente no DMR.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Recebe uma referência a uma interface [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

