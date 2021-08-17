---
title: Propriedade GetStreamPropertiesOperation.Completed
description: Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada por GetStreamPropertiesAsync é concluída.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- Api de Streaming de Mídia concluída
- Api de Streaming de Mídia concluída, interface GetStreamPropertiesOperation
- GetStreamPropertiesOperation interface API de Streaming de Mídia , propriedade Completed
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6fc6982866ed97f70467d13cb5e899d94a1459266ca0149d12400d154aad784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100660"
---
# <a name="getstreampropertiesoperationcompleted-property"></a>Propriedade GetStreamPropertiesOperation.Completed

Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada por [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) é concluída.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a>Valor da propriedade

O manipulador de eventos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)
</dt> </dl>

 

 