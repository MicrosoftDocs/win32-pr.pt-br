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
ms.openlocfilehash: 2948af2ed84a70c9f37efbc4aae985e9b1ab5804
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105763017"
---
# <a name="gettransportinformationoperationcompleted-property"></a><span data-ttu-id="e2607-106">Propriedade GetTransportInformationOperation:: Completed</span><span class="sxs-lookup"><span data-stu-id="e2607-106">GetTransportInformationOperation::Completed property</span></span>

<span data-ttu-id="e2607-107">Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) é concluída.</span><span class="sxs-lookup"><span data-stu-id="e2607-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) is completed.</span></span>

<span data-ttu-id="e2607-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e2607-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2607-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2607-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="e2607-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e2607-110">Property value</span></span>

<span data-ttu-id="e2607-111">O manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="e2607-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2607-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2607-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2607-113">**GetTransportInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="e2607-113">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

 