---
title: Mensagem de TVM_GETTEXTCOLOR (commctrl. h)
description: Recupera a cor do texto atual do controle. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetTextColor.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- Controles de TVM_GETTEXTCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009111"
---
# <a name="tvm_gettextcolor-message"></a><span data-ttu-id="7d3fc-105">\_Mensagem TVM GETTEXTCOLOR</span><span class="sxs-lookup"><span data-stu-id="7d3fc-105">TVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="7d3fc-106">Recupera a cor do texto atual do controle.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-106">Retrieves the current text color of the control.</span></span> <span data-ttu-id="7d3fc-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) .</span><span class="sxs-lookup"><span data-stu-id="7d3fc-107">You can send this message explicitly or by using the [**TreeView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d3fc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d3fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d3fc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d3fc-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7d3fc-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7d3fc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d3fc-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7d3fc-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d3fc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d3fc-113">Return value</span></span>

<span data-ttu-id="7d3fc-114">Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor do texto atual.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current text color.</span></span> <span data-ttu-id="7d3fc-115">Se esse valor for-1, o controle estará usando a cor do sistema para a cor do texto.</span><span class="sxs-lookup"><span data-stu-id="7d3fc-115">If this value is -1, the control is using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d3fc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d3fc-116">Requirements</span></span>



| <span data-ttu-id="7d3fc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d3fc-117">Requirement</span></span> | <span data-ttu-id="7d3fc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7d3fc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3fc-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d3fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7d3fc-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d3fc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d3fc-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d3fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7d3fc-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d3fc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d3fc-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d3fc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d3fc-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d3fc-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d3fc-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d3fc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d3fc-126">**TVM \_ SETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="7d3fc-126">**TVM\_SETTEXTCOLOR**</span></span>](tvm-settextcolor.md)
</dt> </dl>

 

