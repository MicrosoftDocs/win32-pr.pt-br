---
title: Propriedade GetVolumeOperation.Completed
description: Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada por GetVolumeAsync é concluída.
ms.assetid: 34100EE7-C4CB-4AE0-BD3E-9E23A643F87E
keywords:
- Api de Streaming de Mídia concluída
- Api de Streaming de Mídia concluída, interface GetVolumeOperation
- Api de Streaming de Mídia da interface GetVolumeOperation, propriedade Completed
topic_type:
- apiref
api_name:
- GetVolumeOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 84668f41f12c4920ec45bf70a3a931e6fc9234e213fe0a359ab93f3e34aac724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735752"
---
# <a name="getvolumeoperationcompleted-property"></a>Propriedade GetVolumeOperation.Completed

Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada por [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) é concluída.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a>Valor da propriedade

O manipulador de eventos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetVolumeOperation**](getvolumeoperation.md)
</dt> </dl>

 

 