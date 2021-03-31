---
title: Mensagem de TVM_SETTEXTCOLOR (commctrl. h)
description: Define a cor do texto do controle. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetTextColor.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- Controles de TVM_SETTEXTCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644774"
---
# <a name="tvm_settextcolor-message"></a><span data-ttu-id="12dd7-105">\_Mensagem TVM SETTEXTCOLOR</span><span class="sxs-lookup"><span data-stu-id="12dd7-105">TVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="12dd7-106">Define a cor do texto do controle.</span><span class="sxs-lookup"><span data-stu-id="12dd7-106">Sets the text color of the control.</span></span> <span data-ttu-id="12dd7-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) .</span><span class="sxs-lookup"><span data-stu-id="12dd7-107">You can send this message explicitly or by using the [**TreeView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="12dd7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12dd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12dd7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12dd7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="12dd7-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="12dd7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="12dd7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12dd7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12dd7-112">Valor [**COLORREF**](/windows/desktop/gdi/colorref) que contém a nova cor do texto.</span><span class="sxs-lookup"><span data-stu-id="12dd7-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new text color.</span></span> <span data-ttu-id="12dd7-113">Se esse argumento for-1, o controle será revertido para usar a cor do sistema para a cor do texto.</span><span class="sxs-lookup"><span data-stu-id="12dd7-113">If this argument is -1, the control will revert to using the system color for the text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12dd7-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12dd7-114">Return value</span></span>

<span data-ttu-id="12dd7-115">Retorna um valor **COLORREF** que representa a cor do texto anterior.</span><span class="sxs-lookup"><span data-stu-id="12dd7-115">Returns a **COLORREF** value that represents the previous text color.</span></span> <span data-ttu-id="12dd7-116">Se esse valor for-1, o controle estava usando a cor do sistema para a cor do texto.</span><span class="sxs-lookup"><span data-stu-id="12dd7-116">If this value is -1, the control was using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="12dd7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12dd7-117">Requirements</span></span>



| <span data-ttu-id="12dd7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="12dd7-118">Requirement</span></span> | <span data-ttu-id="12dd7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="12dd7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12dd7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12dd7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="12dd7-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12dd7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12dd7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12dd7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="12dd7-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12dd7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12dd7-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12dd7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="12dd7-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12dd7-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12dd7-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="12dd7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12dd7-127">**TVM \_ GETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="12dd7-127">**TVM\_GETTEXTCOLOR**</span></span>](tvm-gettextcolor.md)
</dt> </dl>

 

