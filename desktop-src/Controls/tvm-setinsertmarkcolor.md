---
title: Mensagem de TVM_SETINSERTMARKCOLOR (commctrl. h)
description: Define a cor usada para desenhar a marca de inserção para o modo de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetInsertMarkColor.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- Controles de TVM_SETINSERTMARKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085721"
---
# <a name="tvm_setinsertmarkcolor-message"></a><span data-ttu-id="00703-105">\_Mensagem TVM SETINSERTMARKCOLOR</span><span class="sxs-lookup"><span data-stu-id="00703-105">TVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="00703-106">Define a cor usada para desenhar a marca de inserção para o modo de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="00703-106">Sets the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="00703-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) .</span><span class="sxs-lookup"><span data-stu-id="00703-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="00703-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00703-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00703-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00703-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="00703-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="00703-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="00703-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00703-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00703-112">Valor [**COLORREF**](/windows/desktop/gdi/colorref) que contém a nova cor de marca de inserção.</span><span class="sxs-lookup"><span data-stu-id="00703-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00703-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00703-113">Return value</span></span>

<span data-ttu-id="00703-114">Retorna um valor **COLORREF** que contém a cor de marca de inserção anterior.</span><span class="sxs-lookup"><span data-stu-id="00703-114">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="00703-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00703-115">Requirements</span></span>



| <span data-ttu-id="00703-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="00703-116">Requirement</span></span> | <span data-ttu-id="00703-117">Valor</span><span class="sxs-lookup"><span data-stu-id="00703-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00703-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00703-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00703-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00703-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00703-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00703-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00703-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="00703-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00703-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00703-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="00703-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="00703-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00703-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="00703-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00703-125">**TVM \_ GETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="00703-125">**TVM\_GETINSERTMARKCOLOR**</span></span>](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

