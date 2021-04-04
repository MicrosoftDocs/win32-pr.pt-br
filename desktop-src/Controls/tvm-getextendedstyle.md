---
title: Mensagem de TVM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera o estilo estendido para um controle de exibição de árvore. Envie essa mensagem explicitamente ou usando a macro TreeView \_ Extended.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- Controles de TVM_GETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824748"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a><span data-ttu-id="2f7e1-105">Mensagem de TVM_GETEXTENDEDSTYLE (commctrl. h)</span><span class="sxs-lookup"><span data-stu-id="2f7e1-105">TVM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="2f7e1-106">Recupera o estilo estendido para um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="2f7e1-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="2f7e1-107">Envie essa mensagem explicitamente ou usando a macro [**TreeView \_ Extended**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="2f7e1-107">Send this message explicitly or by using the [**TreeView\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f7e1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f7e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f7e1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f7e1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f7e1-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2f7e1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f7e1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f7e1-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f7e1-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2f7e1-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f7e1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f7e1-113">Return value</span></span>

<span data-ttu-id="2f7e1-114">Retorna o valor do estilo estendido. Para obter mais informações sobre estilos, consulte [controle de exibição de árvore estilos estendidos](tree-view-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="2f7e1-114">Returns the value of extended style.For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2f7e1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f7e1-115">Remarks</span></span>

<span data-ttu-id="2f7e1-116">Os estilos estendidos para um controle de exibição em árvore não têm nada a ver com os estilos estendidos usados com a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="2f7e1-116">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7e1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f7e1-117">Requirements</span></span>



| <span data-ttu-id="2f7e1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7e1-118">Requirement</span></span> | <span data-ttu-id="2f7e1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2f7e1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7e1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f7e1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f7e1-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f7e1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f7e1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f7e1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f7e1-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f7e1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f7e1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f7e1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f7e1-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f7e1-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

