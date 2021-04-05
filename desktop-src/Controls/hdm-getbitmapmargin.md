---
title: Mensagem de HDM_GETBITMAPMARGIN (commctrl. h)
description: Obtém a largura da margem de bitmap para um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetBitmapMargin do cabeçalho.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- Controles de HDM_GETBITMAPMARGIN de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918489"
---
# <a name="hdm_getbitmapmargin-message"></a><span data-ttu-id="ad5ba-105">\_Mensagem HDM GETBITMAPMARGIN</span><span class="sxs-lookup"><span data-stu-id="ad5ba-105">HDM\_GETBITMAPMARGIN message</span></span>

<span data-ttu-id="ad5ba-106">Obtém a largura da margem de bitmap para um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ad5ba-106">Gets the width of the bitmap margin for a header control.</span></span> <span data-ttu-id="ad5ba-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetBitmapMargin do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) .</span><span class="sxs-lookup"><span data-stu-id="ad5ba-107">You can send this message explicitly or use the [**Header\_GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ad5ba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad5ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad5ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad5ba-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ad5ba-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ad5ba-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ad5ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad5ba-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ad5ba-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ad5ba-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad5ba-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad5ba-113">Return value</span></span>

<span data-ttu-id="ad5ba-114">Retorna a largura da margem do bitmap em pixels.</span><span class="sxs-lookup"><span data-stu-id="ad5ba-114">Returns the width of the bitmap margin in pixels.</span></span> <span data-ttu-id="ad5ba-115">Se a margem do bitmap não tiver sido especificada anteriormente, o valor padrão de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ CXEDGE) será retornado.</span><span class="sxs-lookup"><span data-stu-id="ad5ba-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM\_CXEDGE) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad5ba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad5ba-116">Requirements</span></span>



| <span data-ttu-id="ad5ba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad5ba-117">Requirement</span></span> | <span data-ttu-id="ad5ba-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ad5ba-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad5ba-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad5ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ad5ba-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ad5ba-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ad5ba-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad5ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ad5ba-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad5ba-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad5ba-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad5ba-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad5ba-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad5ba-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad5ba-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad5ba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad5ba-126">**HDM \_ SETBITMAPMARGIN**</span><span class="sxs-lookup"><span data-stu-id="ad5ba-126">**HDM\_SETBITMAPMARGIN**</span></span>](hdm-setbitmapmargin.md)
</dt> </dl>

 

