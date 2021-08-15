---
title: Propriedade GetTransportInformationOperation concluída
description: Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo GetTransportInformationAsync é concluída.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- API de streaming de mídia de propriedade concluída
- API de streaming de mídia de propriedade concluída, interface GetTransportInformationOperation
- API de streaming de mídia da interface GetTransportInformationOperation, Propriedade Completed
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 389d7b281c10458e854407f9ce02bd2656fe6d4b16574408d75ae06ccc06d7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735779"
---
# <a name="gettransportinformationoperationcompleted-property"></a>Propriedade GetTransportInformationOperation:: Completed

Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) é concluída.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Valor da propriedade

O manipulador de eventos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

 