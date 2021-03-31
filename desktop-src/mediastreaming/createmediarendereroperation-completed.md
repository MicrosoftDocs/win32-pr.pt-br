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
# <a name="createmediarendereroperationcompleted-property"></a><span data-ttu-id="47160-106">Propriedade CreateMediaRendererOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="47160-106">CreateMediaRendererOperation.Completed property</span></span>

<span data-ttu-id="47160-107">Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada por [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) ou [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) é concluída.</span><span class="sxs-lookup"><span data-stu-id="47160-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) or [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) is completed.</span></span>

<span data-ttu-id="47160-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="47160-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47160-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="47160-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a><span data-ttu-id="47160-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="47160-110">Property value</span></span>

<span data-ttu-id="47160-111">O manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="47160-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="47160-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="47160-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47160-113">**CreateMediaRendererOperation**</span><span class="sxs-lookup"><span data-stu-id="47160-113">**CreateMediaRendererOperation**</span></span>](createmediarendereroperation.md)
</dt> </dl>

 

 




