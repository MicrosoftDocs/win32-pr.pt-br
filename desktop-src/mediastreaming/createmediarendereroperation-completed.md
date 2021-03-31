---
title: Propriedade CreateMediaRendererOperation. Completed
description: Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada por CreateMediaRendererAsync ou CreateMediaRendererFromBasicDeviceAsync é concluída.
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- API de streaming de mídia de propriedade concluída
- API de streaming de mídia de propriedade concluída, interface CreateMediaRendererOperation
- API de streaming de mídia da interface CreateMediaRendererOperation, Propriedade Completed
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3b4ebafc1441741a352f4573709495228bf13e4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638541"
---
# <a name="createmediarendereroperationcompleted-property"></a>Propriedade CreateMediaRendererOperation. Completed

Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada por [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) ou [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) é concluída.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a>Valor da propriedade

O manipulador de eventos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CreateMediaRendererOperation**](createmediarendereroperation.md)
</dt> </dl>

 

 




