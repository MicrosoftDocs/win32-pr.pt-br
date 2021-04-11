---
title: Propriedade GetPositionInformationOperation. Completed
description: Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo GetPositionInformationAsync é concluída.
ms.assetid: 144065AE-6C23-4E9D-B9D0-6849E7FB74C4
keywords:
- API de streaming de mídia de propriedade concluída
- API de streaming de mídia de propriedade concluída, interface GetPositionInformationOperation
- API de streaming de mídia da interface GetPositionInformationOperation, Propriedade Completed
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90b4ed4a6402b8c7bfc1ee559bd0b43765a64cec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365981"
---
# <a name="getpositioninformationoperationcompleted-property"></a><span data-ttu-id="0e15f-106">Propriedade GetPositionInformationOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="0e15f-106">GetPositionInformationOperation.Completed property</span></span>

<span data-ttu-id="0e15f-107">Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) é concluída.</span><span class="sxs-lookup"><span data-stu-id="0e15f-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) is completed.</span></span>

<span data-ttu-id="0e15f-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0e15f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e15f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e15f-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetPositionInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetPositionInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="0e15f-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0e15f-110">Property value</span></span>

<span data-ttu-id="0e15f-111">O manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="0e15f-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e15f-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e15f-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e15f-113">**GetPositionInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="0e15f-113">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

 