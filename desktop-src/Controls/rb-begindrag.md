---
title: Mensagem de RB_BEGINDRAG (commctrl. h)
description: Coloca o controle rebar no modo arrastar e soltar. Essa mensagem não faz com que uma \_ notificação RBN BEGINDRAG seja enviada.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- Controles de RB_BEGINDRAG de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455537"
---
# <a name="rb_begindrag-message"></a><span data-ttu-id="4b27d-105">\_Mensagem BEGINDRAG RB</span><span class="sxs-lookup"><span data-stu-id="4b27d-105">RB\_BEGINDRAG message</span></span>

<span data-ttu-id="4b27d-106">Coloca o controle rebar no modo arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="4b27d-106">Puts the rebar control in drag-and-drop mode.</span></span> <span data-ttu-id="4b27d-107">Essa mensagem não faz com que uma notificação [RBN \_ BEGINDRAG](rbn-begindrag.md) seja enviada.</span><span class="sxs-lookup"><span data-stu-id="4b27d-107">This message does not cause a [RBN\_BEGINDRAG](rbn-begindrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b27d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b27d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b27d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b27d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b27d-110">Índice de base zero da banda que a operação de arrastar e soltar afetará.</span><span class="sxs-lookup"><span data-stu-id="4b27d-110">Zero-based index of the band that the drag-and-drop operation will affect.</span></span>

</dd> <dt>

<span data-ttu-id="4b27d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b27d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4b27d-112">Valor **DWORD** que contém as coordenadas de início do mouse.</span><span class="sxs-lookup"><span data-stu-id="4b27d-112">**DWORD** value that contains the starting mouse coordinates.</span></span> <span data-ttu-id="4b27d-113">A coordenada horizontal está contida no LOWORD e a coordenada vertical está contida no HIWORD.</span><span class="sxs-lookup"><span data-stu-id="4b27d-113">The horizontal coordinate is contained in the LOWORD and the vertical coordinate is contained in the HIWORD.</span></span> <span data-ttu-id="4b27d-114">Se você passar (**DWORD**)-1, o controle Rebar usará a posição do mouse na última vez em que o thread do controle chamou [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span><span class="sxs-lookup"><span data-stu-id="4b27d-114">If you pass (**DWORD**)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b27d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b27d-115">Return value</span></span>

<span data-ttu-id="4b27d-116">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="4b27d-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b27d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b27d-117">Remarks</span></span>

<span data-ttu-id="4b27d-118">As **mensagens \_ RB BEGINDRAG**, [**RB \_ DRAGMOVE**](rb-dragmove.md)e [**RB \_ EndDrag**](rb-enddrag.md) permitem que você implemente uma interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="4b27d-118">The **RB\_BEGINDRAG**, [**RB\_DRAGMOVE**](rb-dragmove.md), and [**RB\_ENDDRAG**](rb-enddrag.md) messages allow you to implement an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface for a rebar control.</span></span> <span data-ttu-id="4b27d-119">Você envia a mensagem **RB \_ BEGINDRAG** em resposta a [**IDropTarget::D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), envia a mensagem de **\_ DRAGMOVE RB** em resposta [**a IDROPTARGET::D ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)e a mensagem **RB \_ endarraste** em resposta a [**IDropTarget::D ROP**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) e [**IDropTarget::D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span><span class="sxs-lookup"><span data-stu-id="4b27d-119">You send the **RB\_BEGINDRAG** message in response to [**IDropTarget::DragEnter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), send the **RB\_DRAGMOVE** message in response to [**IDropTarget::DragOver**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover), and the **RB\_ENDDRAG** message in response to [**IDropTarget::Drop**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) and [**IDropTarget::DragLeave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b27d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b27d-120">Requirements</span></span>



| <span data-ttu-id="4b27d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b27d-121">Requirement</span></span> | <span data-ttu-id="4b27d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4b27d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b27d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b27d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4b27d-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b27d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b27d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b27d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4b27d-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b27d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b27d-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b27d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b27d-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b27d-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

