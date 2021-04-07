---
title: Mensagem de HDM_SETBITMAPMARGIN (commctrl. h)
description: Define a largura da margem, especificada em pixels, de um bitmap em um controle de cabeçalho existente. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetBitmapMargin do cabeçalho.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- Controles de HDM_SETBITMAPMARGIN de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824642"
---
# <a name="hdm_setbitmapmargin-message"></a><span data-ttu-id="bcbc8-105">\_Mensagem HDM SETBITMAPMARGIN</span><span class="sxs-lookup"><span data-stu-id="bcbc8-105">HDM\_SETBITMAPMARGIN message</span></span>

<span data-ttu-id="bcbc8-106">Define a largura da margem, especificada em pixels, de um bitmap em um controle de cabeçalho existente.</span><span class="sxs-lookup"><span data-stu-id="bcbc8-106">Sets the width of the margin, specified in pixels, of a bitmap in an existing header control.</span></span> <span data-ttu-id="bcbc8-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetBitmapMargin do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) .</span><span class="sxs-lookup"><span data-stu-id="bcbc8-107">You can send this message explicitly or use the [**Header\_SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcbc8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcbc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcbc8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcbc8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bcbc8-110">A largura, especificada em pixels, da margem que circunda um bitmap dentro de um controle de cabeçalho existente.</span><span class="sxs-lookup"><span data-stu-id="bcbc8-110">The width, specified in pixels, of the margin that surrounds a bitmap within an existing header control.</span></span>

</dd> <dt>

<span data-ttu-id="bcbc8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcbc8-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bcbc8-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bcbc8-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcbc8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bcbc8-113">Return value</span></span>

<span data-ttu-id="bcbc8-114">Retorna a largura da margem do bitmap, em pixels.</span><span class="sxs-lookup"><span data-stu-id="bcbc8-114">Returns the width of the bitmap margin, in pixels.</span></span> <span data-ttu-id="bcbc8-115">Se a margem do bitmap não tiver sido especificada anteriormente, o valor padrão de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*) será retornado.</span><span class="sxs-lookup"><span data-stu-id="bcbc8-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM\_CXEDGE*) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcbc8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcbc8-116">Requirements</span></span>



| <span data-ttu-id="bcbc8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcbc8-117">Requirement</span></span> | <span data-ttu-id="bcbc8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bcbc8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbc8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcbc8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbc8-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bcbc8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bcbc8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcbc8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbc8-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bcbc8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcbc8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bcbc8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcbc8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcbc8-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcbc8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcbc8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbc8-126">**HDM \_ GETBITMAPMARGIN**</span><span class="sxs-lookup"><span data-stu-id="bcbc8-126">**HDM\_GETBITMAPMARGIN**</span></span>](hdm-getbitmapmargin.md)
</dt> </dl>

 

