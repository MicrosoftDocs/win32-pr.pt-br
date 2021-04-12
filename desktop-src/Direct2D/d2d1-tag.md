---
title: D2D1_TAG (D2d1. h)
description: Um valor de 64 bits definido pelo aplicativo usado para \ 160; marque um conjunto de operações de renderização.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294799"
---
# <a name="d2d1_tag"></a><span data-ttu-id="e83e7-104">Marca de D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="e83e7-104">D2D1\_TAG</span></span>

<span data-ttu-id="e83e7-105">Um valor de 64 bits definido pelo aplicativo usado para marcar um conjunto de operações de renderização.</span><span class="sxs-lookup"><span data-stu-id="e83e7-105">An application-defined 64-bit value used to mark a set of rendering operations.</span></span>


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a><span data-ttu-id="e83e7-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="e83e7-106">Remarks</span></span>

<span data-ttu-id="e83e7-107">Para definir uma marca antes de uma série de operações de renderização, use o método [**ID2D1RenderTarget:: settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="e83e7-107">To set a tag before a series of rendering operations, use the [**ID2D1RenderTarget::SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) method.</span></span> <span data-ttu-id="e83e7-108">Para recuperar a marca atual, use o método [**ID2D1RenderTarget:: gettags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) .</span><span class="sxs-lookup"><span data-stu-id="e83e7-108">To retrieve the current tag, use the [**ID2D1RenderTarget::GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e83e7-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e83e7-109">Requirements</span></span>



| <span data-ttu-id="e83e7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e83e7-110">Requirement</span></span> | <span data-ttu-id="e83e7-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e83e7-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e83e7-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e83e7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e83e7-113">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="e83e7-113">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="e83e7-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e83e7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e83e7-115">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e83e7-115">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="e83e7-116">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="e83e7-116">Minimum supported phone</span></span><br/>  | <span data-ttu-id="e83e7-117">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="e83e7-117">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="e83e7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e83e7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e83e7-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="e83e7-119"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="e83e7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e83e7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e83e7-121">**GetTags**</span><span class="sxs-lookup"><span data-stu-id="e83e7-121">**GetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[<span data-ttu-id="e83e7-122">**Settags**</span><span class="sxs-lookup"><span data-stu-id="e83e7-122">**SetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

