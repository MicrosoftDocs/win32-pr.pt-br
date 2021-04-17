---
title: Mensagem de TVM_GETBKCOLOR (commctrl. h)
description: Recupera a cor do plano de fundo atual do controle. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetBkColor.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- Controles de TVM_GETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748251"
---
# <a name="tvm_getbkcolor-message"></a><span data-ttu-id="1be4d-105">\_Mensagem TVM GETBKCOLOR</span><span class="sxs-lookup"><span data-stu-id="1be4d-105">TVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="1be4d-106">Recupera a cor do plano de fundo atual do controle.</span><span class="sxs-lookup"><span data-stu-id="1be4d-106">Retrieves the current background color of the control.</span></span> <span data-ttu-id="1be4d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="1be4d-107">You can send this message explicitly or by using the [**TreeView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1be4d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1be4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1be4d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1be4d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1be4d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1be4d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1be4d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1be4d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1be4d-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1be4d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1be4d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1be4d-113">Return value</span></span>

<span data-ttu-id="1be4d-114">Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que representa a cor de plano de fundo atual.</span><span class="sxs-lookup"><span data-stu-id="1be4d-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current background color.</span></span> <span data-ttu-id="1be4d-115">Se esse valor for-1, o controle estará usando a cor do sistema para a cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="1be4d-115">If this value is -1, the control is using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="1be4d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1be4d-116">Requirements</span></span>



| <span data-ttu-id="1be4d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1be4d-117">Requirement</span></span> | <span data-ttu-id="1be4d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1be4d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1be4d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1be4d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1be4d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1be4d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1be4d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1be4d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1be4d-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1be4d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1be4d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1be4d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1be4d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1be4d-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1be4d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1be4d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1be4d-126">**TVM \_ SETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="1be4d-126">**TVM\_SETBKCOLOR**</span></span>](tvm-setbkcolor.md)
</dt> </dl>

 

