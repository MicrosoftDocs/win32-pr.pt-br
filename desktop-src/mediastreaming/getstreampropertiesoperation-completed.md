---
title: Propriedade GetStreamPropertiesOperation. Completed
description: Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo GetStreamPropertiesAsync é concluída.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- API de streaming de mídia de propriedade concluída
- API de streaming de mídia de propriedade concluída, interface GetStreamPropertiesOperation
- API de streaming de mídia da interface GetStreamPropertiesOperation, Propriedade Completed
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb60ad137c8dafa42a58394d58a105267dabda3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365913"
---
# <a name="getstreampropertiesoperationcompleted-property"></a><span data-ttu-id="ee3c6-106">Propriedade GetStreamPropertiesOperation. Completed</span><span class="sxs-lookup"><span data-stu-id="ee3c6-106">GetStreamPropertiesOperation.Completed property</span></span>

<span data-ttu-id="ee3c6-107">Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) é concluída.</span><span class="sxs-lookup"><span data-stu-id="ee3c6-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) is completed.</span></span>

<span data-ttu-id="ee3c6-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ee3c6-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee3c6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee3c6-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="ee3c6-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ee3c6-110">Property value</span></span>

<span data-ttu-id="ee3c6-111">O manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="ee3c6-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee3c6-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee3c6-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3c6-113">**GetStreamPropertiesOperation**</span><span class="sxs-lookup"><span data-stu-id="ee3c6-113">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

 