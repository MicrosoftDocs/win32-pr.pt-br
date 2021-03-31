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
# <a name="em_getstorytype-message"></a><span data-ttu-id="c22fa-104">\_Mensagem em GEThistóriatype</span><span class="sxs-lookup"><span data-stu-id="c22fa-104">EM\_GETSTORYTYPE message</span></span>

<span data-ttu-id="c22fa-105">Obtém o tipo de história.</span><span class="sxs-lookup"><span data-stu-id="c22fa-105">Gets the story type.</span></span>


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a><span data-ttu-id="c22fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c22fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c22fa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c22fa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c22fa-108">O índice da história.</span><span class="sxs-lookup"><span data-stu-id="c22fa-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="c22fa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c22fa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c22fa-110">Reservado deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="c22fa-110">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c22fa-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c22fa-111">Return value</span></span>

<span data-ttu-id="c22fa-112">Retorna o tipo de história, que pode ser um valor personalizado definido pelo cliente ou um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c22fa-112">Returns the story type, which can be a client-defined custom value, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c22fa-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="c22fa-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="c22fa-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c22fa-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c22fa-128">Requirements</span></span>



| <span data-ttu-id="c22fa-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c22fa-129">Requirement</span></span> | <span data-ttu-id="c22fa-130">Valor</span><span class="sxs-lookup"><span data-stu-id="c22fa-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c22fa-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c22fa-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c22fa-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c22fa-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c22fa-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c22fa-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c22fa-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c22fa-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c22fa-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c22fa-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c22fa-136"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c22fa-136"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c22fa-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c22fa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c22fa-138">**em \_ SEThistóriatype**</span><span class="sxs-lookup"><span data-stu-id="c22fa-138">**EM\_SETSTORYTYPE**</span></span>](em-setstorytype.md)
</dt> <dt>

[<span data-ttu-id="c22fa-139">**ITextStoryRanges:: item**</span><span class="sxs-lookup"><span data-stu-id="c22fa-139">**ITextStoryRanges::Item**</span></span>](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





