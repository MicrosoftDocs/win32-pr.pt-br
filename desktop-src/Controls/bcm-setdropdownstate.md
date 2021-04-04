---
title: Mensagem de BCM_SETDROPDOWNSTATE (commctrl. h)
description: Define o estado de menu suspenso para um botão com a lista suspensa estilo TBSTYLE \_ . Envie essa mensagem explicitamente ou usando a \_ macro Setdropstate do botão.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- Controles de BCM_SETDROPDOWNSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085540"
---
# <a name="bcm_setdropdownstate-message"></a><span data-ttu-id="fee86-105">\_Mensagem de lista suspensa do BCM</span><span class="sxs-lookup"><span data-stu-id="fee86-105">BCM\_SETDROPDOWNSTATE message</span></span>

<span data-ttu-id="fee86-106">Define o estado de menu suspenso para um botão com [**a \_ lista**](toolbar-control-and-button-styles.md)suspensa estilo TBSTYLE.</span><span class="sxs-lookup"><span data-stu-id="fee86-106">Sets the drop down state for a button with style [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span> <span data-ttu-id="fee86-107">Envie essa mensagem explicitamente ou usando a macro [**\_ setdropstate do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) .</span><span class="sxs-lookup"><span data-stu-id="fee86-107">Send this message explicitly or by using the [**Button\_SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fee86-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fee86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fee86-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fee86-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fee86-110">Um **bool** que é **verdadeiro** para o estado de BST \_ DROPDOWNPUSHED ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fee86-110">A **BOOL** that is **TRUE** for state of BST\_DROPDOWNPUSHED, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="fee86-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fee86-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fee86-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fee86-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fee86-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fee86-113">Return value</span></span>

<span data-ttu-id="fee86-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fee86-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee86-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fee86-115">Requirements</span></span>



| <span data-ttu-id="fee86-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fee86-116">Requirement</span></span> | <span data-ttu-id="fee86-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fee86-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fee86-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fee86-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fee86-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fee86-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fee86-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fee86-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fee86-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fee86-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fee86-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fee86-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fee86-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fee86-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fee86-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fee86-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="fee86-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="fee86-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fee86-126">Estilos de botão</span><span class="sxs-lookup"><span data-stu-id="fee86-126">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="fee86-127">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="fee86-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fee86-128">Tipos de botão</span><span class="sxs-lookup"><span data-stu-id="fee86-128">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





