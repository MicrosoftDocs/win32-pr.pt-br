---
title: Mensagem de EM_GETSTORYTYPE (RichEdit. h)
description: Obtém o tipo de história.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- Controles de EM_GETSTORYTYPE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824364"
---
# <a name="em_getstorytype-message"></a><span data-ttu-id="ba994-104">\_Mensagem em GEThistóriatype</span><span class="sxs-lookup"><span data-stu-id="ba994-104">EM\_GETSTORYTYPE message</span></span>

<span data-ttu-id="ba994-105">Obtém o tipo de história.</span><span class="sxs-lookup"><span data-stu-id="ba994-105">Gets the story type.</span></span>


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a><span data-ttu-id="ba994-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba994-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba994-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba994-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba994-108">O índice da história.</span><span class="sxs-lookup"><span data-stu-id="ba994-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="ba994-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ba994-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba994-110">Reservado deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="ba994-110">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba994-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba994-111">Return value</span></span>

<span data-ttu-id="ba994-112">Retorna o tipo de história, que pode ser um valor personalizado definido pelo cliente ou um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ba994-112">Returns the story type, which can be a client-defined custom value, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ba994-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="ba994-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="ba994-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ba994-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba994-128">Requirements</span></span>



| <span data-ttu-id="ba994-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba994-129">Requirement</span></span> | <span data-ttu-id="ba994-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ba994-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba994-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba994-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ba994-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ba994-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ba994-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba994-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ba994-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ba994-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba994-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba994-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba994-136"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba994-136"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba994-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba994-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba994-138">**em \_ SEThistóriatype**</span><span class="sxs-lookup"><span data-stu-id="ba994-138">**EM\_SETSTORYTYPE**</span></span>](em-setstorytype.md)
</dt> <dt>

[<span data-ttu-id="ba994-139">**ITextStoryRanges:: item**</span><span class="sxs-lookup"><span data-stu-id="ba994-139">**ITextStoryRanges::Item**</span></span>](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





