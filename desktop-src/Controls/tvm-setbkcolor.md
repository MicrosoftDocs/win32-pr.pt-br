---
title: Mensagem de TVM_SETBKCOLOR (commctrl. h)
description: Define a cor do plano de fundo do controle. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetBkColor.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- Controles de TVM_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824513"
---
# <a name="tvm_setbkcolor-message"></a><span data-ttu-id="dedd2-105">\_Mensagem TVM SETBKCOLOR</span><span class="sxs-lookup"><span data-stu-id="dedd2-105">TVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="dedd2-106">Define a cor do plano de fundo do controle.</span><span class="sxs-lookup"><span data-stu-id="dedd2-106">Sets the background color of the control.</span></span> <span data-ttu-id="dedd2-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="dedd2-107">You can send this message explicitly or by using the [**TreeView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dedd2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dedd2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dedd2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dedd2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dedd2-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dedd2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dedd2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dedd2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dedd2-112">Valor [**COLORREF**](/windows/desktop/gdi/colorref) que contém a nova cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="dedd2-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new background color.</span></span> <span data-ttu-id="dedd2-113">Se esse valor for-1, o controle será revertido para usar a cor do sistema para a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="dedd2-113">If this value is -1, the control will revert to using the system color for the background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dedd2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dedd2-114">Return value</span></span>

<span data-ttu-id="dedd2-115">Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor do plano de fundo anterior.</span><span class="sxs-lookup"><span data-stu-id="dedd2-115">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous background color.</span></span> <span data-ttu-id="dedd2-116">Se esse valor for-1, o controle estava usando a cor do sistema para a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="dedd2-116">If this value is -1, the control was using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="dedd2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dedd2-117">Requirements</span></span>



| <span data-ttu-id="dedd2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dedd2-118">Requirement</span></span> | <span data-ttu-id="dedd2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="dedd2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dedd2-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dedd2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dedd2-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dedd2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dedd2-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dedd2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dedd2-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dedd2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dedd2-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dedd2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dedd2-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dedd2-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dedd2-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dedd2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dedd2-127">**TVM \_ GETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="dedd2-127">**TVM\_GETBKCOLOR**</span></span>](tvm-getbkcolor.md)
</dt> </dl>

 

