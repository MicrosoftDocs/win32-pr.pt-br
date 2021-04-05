---
title: Mensagem de TVM_GETINSERTMARKCOLOR (commctrl. h)
description: Recupera a cor usada para desenhar a marca de inserção para o modo de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetInsertMarkColor.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- Controles de TVM_GETINSERTMARKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919076"
---
# <a name="tvm_getinsertmarkcolor-message"></a><span data-ttu-id="1b8c4-105">\_Mensagem TVM GETINSERTMARKCOLOR</span><span class="sxs-lookup"><span data-stu-id="1b8c4-105">TVM\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="1b8c4-106">Recupera a cor usada para desenhar a marca de inserção para o modo de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="1b8c4-106">Retrieves the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="1b8c4-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) .</span><span class="sxs-lookup"><span data-stu-id="1b8c4-107">You can send this message explicitly or by using the [**TreeView\_GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b8c4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b8c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b8c4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b8c4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1b8c4-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1b8c4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1b8c4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b8c4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1b8c4-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1b8c4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b8c4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b8c4-113">Return value</span></span>

<span data-ttu-id="1b8c4-114">Retorna um valor [**COLORREF**](/windows/desktop/gdi/colorref) que contém a cor da marca de inserção atual.</span><span class="sxs-lookup"><span data-stu-id="1b8c4-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b8c4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b8c4-115">Requirements</span></span>



| <span data-ttu-id="1b8c4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b8c4-116">Requirement</span></span> | <span data-ttu-id="1b8c4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1b8c4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b8c4-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b8c4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8c4-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b8c4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b8c4-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b8c4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8c4-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b8c4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b8c4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b8c4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b8c4-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b8c4-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b8c4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b8c4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b8c4-125">**TVM \_ SETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="1b8c4-125">**TVM\_SETINSERTMARKCOLOR**</span></span>](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

