---
title: Mensagem de TB_SETPADDING (commctrl. h)
description: Define o preenchimento de um controle ToolBar.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- Controles de TB_SETPADDING de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086246"
---
# <a name="tb_setpadding-message"></a><span data-ttu-id="e2a37-104">\_Mensagem SETpadding de TB</span><span class="sxs-lookup"><span data-stu-id="e2a37-104">TB\_SETPADDING message</span></span>

<span data-ttu-id="e2a37-105">Define o preenchimento de um controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="e2a37-105">Sets the padding for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2a37-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2a37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2a37-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2a37-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2a37-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e2a37-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e2a37-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2a37-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2a37-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o preenchimento horizontal, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e2a37-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the horizontal padding, in pixels.</span></span> <span data-ttu-id="e2a37-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o preenchimento vertical, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e2a37-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2a37-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2a37-112">Return value</span></span>

<span data-ttu-id="e2a37-113">Retorna um valor **DWORD** que contém o preenchimento horizontal anterior no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e o preenchimento vertical anterior no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), em pixels.</span><span class="sxs-lookup"><span data-stu-id="e2a37-113">Returns a **DWORD** value that contains the previous horizontal padding in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous vertical padding in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2a37-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2a37-114">Remarks</span></span>

<span data-ttu-id="e2a37-115">Os valores de preenchimento são usados para criar uma área em branco entre a borda do botão e a imagem e/ou o texto do botão.</span><span class="sxs-lookup"><span data-stu-id="e2a37-115">The padding values are used to create a blank area between the edge of the button and the button's image and/or text.</span></span> <span data-ttu-id="e2a37-116">Onde e quanto preenchimento é realmente aplicado depende do tipo do botão e se ele tem uma imagem.</span><span class="sxs-lookup"><span data-stu-id="e2a37-116">Where and how much padding is actually applied depends on the type of the button and whether it has an image.</span></span> <span data-ttu-id="e2a37-117">O preenchimento horizontal é aplicado à direita e à esquerda do botão e o preenchimento vertical é aplicado tanto na parte superior e inferior do botão.</span><span class="sxs-lookup"><span data-stu-id="e2a37-117">The horizontal padding is applied to both the right and left of the button, and the vertical padding is applied to both the top and bottom of the button.</span></span> <span data-ttu-id="e2a37-118">O preenchimento só é aplicado a botões que têm o estilo [**\_ AUTOSIZE de TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="e2a37-118">Padding is only applied to buttons that have the [**TBSTYLE\_AUTOSIZE**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2a37-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2a37-119">Requirements</span></span>



| <span data-ttu-id="e2a37-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2a37-120">Requirement</span></span> | <span data-ttu-id="e2a37-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e2a37-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a37-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2a37-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e2a37-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2a37-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2a37-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2a37-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e2a37-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2a37-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2a37-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2a37-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2a37-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2a37-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a37-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2a37-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a37-129">**autopadding TB \_**</span><span class="sxs-lookup"><span data-stu-id="e2a37-129">**TB\_GETPADDING**</span></span>](tb-getpadding.md)
</dt> </dl>

 

