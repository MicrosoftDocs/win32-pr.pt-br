---
title: Propriedade GetVolumeOperation. Completed
description: Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo GetVolumeAsync é concluída.
ms.assetid: 34100EE7-C4CB-4AE0-BD3E-9E23A643F87E
keywords:
- API de streaming de mídia de propriedade concluída
- API de streaming de mídia de propriedade concluída, interface GetVolumeOperation
- API de streaming de mídia da interface GetVolumeOperation, Propriedade Completed
topic_type:
- apiref
api_name:
- GetVolumeOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21577d57e1e29aff1d2b12b92bcbef58a529eba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084479"
---
# <a name="getvolumeoperationcompleted-property"></a><span data-ttu-id="cadc3-106">Propriedade GetVolumeOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="cadc3-106">GetVolumeOperation.Completed property</span></span>

<span data-ttu-id="cadc3-107">Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) é concluída.</span><span class="sxs-lookup"><span data-stu-id="cadc3-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) is completed.</span></span>

<span data-ttu-id="cadc3-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cadc3-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cadc3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cadc3-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="cadc3-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cadc3-110">Property value</span></span>

<span data-ttu-id="cadc3-111">O manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="cadc3-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="cadc3-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="cadc3-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cadc3-113">**GetVolumeOperation**</span><span class="sxs-lookup"><span data-stu-id="cadc3-113">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

 