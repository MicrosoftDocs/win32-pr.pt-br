---
title: Mensagem de LVM_REDRAWITEMS (commctrl. h)
description: Força um controle de exibição de lista a redesenhar um intervalo de itens. Você pode enviar essa mensagem explicitamente ou usando a \_ macro RedrawItems do ListView.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- Controles de LVM_REDRAWITEMS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009349"
---
# <a name="lvm_redrawitems-message"></a><span data-ttu-id="43597-105">\_Mensagem REDRAWITEMS LVM</span><span class="sxs-lookup"><span data-stu-id="43597-105">LVM\_REDRAWITEMS message</span></span>

<span data-ttu-id="43597-106">Força um controle de exibição de lista a redesenhar um intervalo de itens.</span><span class="sxs-lookup"><span data-stu-id="43597-106">Forces a list-view control to redraw a range of items.</span></span> <span data-ttu-id="43597-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ RedrawItems do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .</span><span class="sxs-lookup"><span data-stu-id="43597-107">You can send this message explicitly or by using the [**ListView\_RedrawItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="43597-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43597-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43597-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43597-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43597-110">Índice do primeiro item a ser redesenhado.</span><span class="sxs-lookup"><span data-stu-id="43597-110">Index of the first item to redraw.</span></span>

</dd> <dt>

<span data-ttu-id="43597-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43597-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43597-112">Índice do último item a ser redesenhado.</span><span class="sxs-lookup"><span data-stu-id="43597-112">Index of the last item to redraw.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43597-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43597-113">Return value</span></span>

<span data-ttu-id="43597-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="43597-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="43597-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="43597-115">Remarks</span></span>

<span data-ttu-id="43597-116">Os itens especificados não são, na verdade, redesenhados até que a janela de exibição de lista receba uma mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) para redesenhar.</span><span class="sxs-lookup"><span data-stu-id="43597-116">The specified items are not actually redrawn until the list-view window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message to repaint.</span></span> <span data-ttu-id="43597-117">Para redesenhar imediatamente, chame a função [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) depois de usar essa macro.</span><span class="sxs-lookup"><span data-stu-id="43597-117">To repaint immediately, call the [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) function after using this macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="43597-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43597-118">Requirements</span></span>



| <span data-ttu-id="43597-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="43597-119">Requirement</span></span> | <span data-ttu-id="43597-120">Valor</span><span class="sxs-lookup"><span data-stu-id="43597-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43597-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43597-121">Minimum supported client</span></span><br/> | <span data-ttu-id="43597-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43597-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43597-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43597-123">Minimum supported server</span></span><br/> | <span data-ttu-id="43597-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="43597-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43597-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43597-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="43597-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43597-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

