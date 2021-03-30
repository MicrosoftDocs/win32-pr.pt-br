---
title: Propriedade GetMuteOperation. Completed
description: Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo GetMuteAsync é concluída.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- API de streaming de mídia de propriedade concluída
- API de streaming de mídia de propriedade concluída, interface GetMuteOperation
- API de streaming de mídia da interface GetMuteOperation, Propriedade Completed
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40c360dc3597d8cf04d1a8c505e479a38136f592
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640919"
---
# <a name="getmuteoperationcompleted-property"></a><span data-ttu-id="158cb-106">Propriedade GetMuteOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="158cb-106">GetMuteOperation.Completed property</span></span>

<span data-ttu-id="158cb-107">Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) é concluída.</span><span class="sxs-lookup"><span data-stu-id="158cb-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) is completed.</span></span>

<span data-ttu-id="158cb-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="158cb-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="158cb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="158cb-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="158cb-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="158cb-110">Property value</span></span>

<span data-ttu-id="158cb-111">O manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="158cb-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="158cb-112">Consulte também</span><span class="sxs-lookup"><span data-stu-id="158cb-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="158cb-113">**GetMuteOperation**</span><span class="sxs-lookup"><span data-stu-id="158cb-113">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

 