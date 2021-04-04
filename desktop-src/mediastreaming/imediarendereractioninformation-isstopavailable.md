---
title: Método IMediaRendererActionInformation IsStopAvailable
description: Recupera um valor que indica se o DMR está atualmente aceitando o método StopAsync.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- API de streaming de mídia do método IsStopAvailable
- API de streaming de mídia do método IsStopAvailable, interface IMediaRendererActionInformation
- API de streaming de mídia da interface IMediaRendererActionInformation, método IsStopAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0a031bafc9a755dfec2498f4e2a52cdd9ef5b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084514"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a>Método IMediaRendererActionInformation:: IsStopAvailable

Recupera um valor que indica se o DMR está atualmente aceitando o método [**StopAsync**](imediarenderer-stopasync.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do fora\]
</dt> <dd>

Um valor booliano que é **true** se o DMR estiver atualmente aceitando o método [**StopAsync**](imediarenderer-stopasync.md) e **false** se não for.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

