---
title: Propriedade StreamSelectOperation. Completed
description: Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo SelectBestStreamAsync é concluída.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- API de streaming de mídia de propriedade concluída
- API de streaming de mídia de propriedade concluída, interface StreamSelectOperation
- API de streaming de mídia da interface StreamSelectOperation, Propriedade Completed
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74cfdf1a3db4f6843a5f12522b688e889e156f33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105812279"
---
# <a name="streamselectoperationcompleted-property"></a><span data-ttu-id="ce8b7-106">Propriedade StreamSelectOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="ce8b7-106">StreamSelectOperation.Completed property</span></span>

<span data-ttu-id="ce8b7-107">Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) é concluída.</span><span class="sxs-lookup"><span data-stu-id="ce8b7-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span>

<span data-ttu-id="ce8b7-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ce8b7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce8b7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce8b7-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="ce8b7-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ce8b7-110">Property value</span></span>

<span data-ttu-id="ce8b7-111">O manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="ce8b7-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce8b7-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce8b7-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce8b7-113">**StreamSelectOperation**</span><span class="sxs-lookup"><span data-stu-id="ce8b7-113">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

 