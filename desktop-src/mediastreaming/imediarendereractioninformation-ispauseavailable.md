---
title: Método IMediaRendererActionInformation IsPauseAvailable
description: Recupera um valor que indica se o DMR está atualmente aceitando o método PauseAsync.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- API de streaming de mídia do método IsPauseAvailable
- API de streaming de mídia do método IsPauseAvailable, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método IsPauseAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fad69863306a8a937771f16c2ab9a83a2622c571d2cd5ee5658a279bf7564132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870843"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a>Método IMediaRendererActionInformation:: IsPauseAvailable

Recupera um valor que indica se o DMR está atualmente aceitando o método [**PauseAsync**](imediarenderer-pauseasync.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Um valor booliano que é **true** se o DMR estiver atualmente aceitando o método [**PauseAsync**](imediarenderer-pauseasync.md) e **false** se não for.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

