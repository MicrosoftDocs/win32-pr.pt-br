---
title: Mensagem de TCM_SETITEMSIZE (commctrl. h)
description: Define a largura e a altura das guias em um controle de tabulação de largura fixa ou de desenho proprietário. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setitems TabCtrl.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- Controles de TCM_SETITEMSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824146"
---
# <a name="tcm_setitemsize-message"></a><span data-ttu-id="fdc10-105">\_Mensagem de SETitems TCM</span><span class="sxs-lookup"><span data-stu-id="fdc10-105">TCM\_SETITEMSIZE message</span></span>

<span data-ttu-id="fdc10-106">Define a largura e a altura das guias em um controle de tabulação de largura fixa ou de desenho proprietário.</span><span class="sxs-lookup"><span data-stu-id="fdc10-106">Sets the width and height of tabs in a fixed-width or owner-drawn tab control.</span></span> <span data-ttu-id="fdc10-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setitems TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) .</span><span class="sxs-lookup"><span data-stu-id="fdc10-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fdc10-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdc10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdc10-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fdc10-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fdc10-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fdc10-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fdc10-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fdc10-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fdc10-112">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um valor **int** que especifica a nova largura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="fdc10-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the new width, in pixels.</span></span> <span data-ttu-id="fdc10-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um valor **int** que especifica a nova altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="fdc10-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the new height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdc10-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fdc10-114">Return value</span></span>

<span data-ttu-id="fdc10-115">Retorna a largura e a altura antigas.</span><span class="sxs-lookup"><span data-stu-id="fdc10-115">Returns the old width and height.</span></span> <span data-ttu-id="fdc10-116">A largura está em [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) do valor de retorno e a altura está no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fdc10-116">The width is in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the height is in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="fdc10-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdc10-117">Remarks</span></span>

<span data-ttu-id="fdc10-118">Se a largura for definida como um valor menor que a largura da imagem definida por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), a largura da guia será definida com o menor valor que for maior que a largura da imagem.</span><span class="sxs-lookup"><span data-stu-id="fdc10-118">If the width is set to a value less than the image width set by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), the width of the tab is set to the lowest value that is greater than the image width.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdc10-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdc10-119">Requirements</span></span>



| <span data-ttu-id="fdc10-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdc10-120">Requirement</span></span> | <span data-ttu-id="fdc10-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fdc10-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc10-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdc10-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc10-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fdc10-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fdc10-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdc10-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc10-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fdc10-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdc10-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdc10-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdc10-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdc10-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

