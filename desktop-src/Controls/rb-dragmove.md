---
title: Mensagem de RB_DRAGMOVE (commctrl. h)
description: Atualiza a posição de arrastar no controle rebar após uma mensagem BEGINDRAG de RB anterior \_ .
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- Controles de RB_DRAGMOVE de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918784"
---
# <a name="rb_dragmove-message"></a><span data-ttu-id="9b31d-104">\_Mensagem DRAGMOVE RB</span><span class="sxs-lookup"><span data-stu-id="9b31d-104">RB\_DRAGMOVE message</span></span>

<span data-ttu-id="9b31d-105">Atualiza a posição de arrastar no controle rebar após uma mensagem [**\_ BEGINDRAG de RB**](rb-begindrag.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="9b31d-105">Updates the drag position in the rebar control after a previous [**RB\_BEGINDRAG**](rb-begindrag.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b31d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b31d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b31d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b31d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b31d-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9b31d-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9b31d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b31d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b31d-110">Valor **DWORD** que contém as novas coordenadas do mouse.</span><span class="sxs-lookup"><span data-stu-id="9b31d-110">**DWORD** value that contains the new mouse coordinates.</span></span> <span data-ttu-id="9b31d-111">A coordenada horizontal está contida no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e a coordenada vertical está contida no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9b31d-111">The horizontal coordinate is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical coordinate is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="9b31d-112">Se você passar (DWORD)-1, o controle Rebar usará a posição do mouse na última vez em que o thread do controle chamou [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).</span><span class="sxs-lookup"><span data-stu-id="9b31d-112">If you pass (DWORD)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b31d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b31d-113">Return value</span></span>

<span data-ttu-id="9b31d-114">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="9b31d-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b31d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b31d-115">Requirements</span></span>



| <span data-ttu-id="9b31d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b31d-116">Requirement</span></span> | <span data-ttu-id="9b31d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9b31d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b31d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b31d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9b31d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b31d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b31d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b31d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9b31d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9b31d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b31d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b31d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b31d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b31d-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b31d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b31d-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="9b31d-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9b31d-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9b31d-126">**ARRASTAR para a RB \_**</span><span class="sxs-lookup"><span data-stu-id="9b31d-126">**RB\_ENDDRAG**</span></span>](rb-enddrag.md)
</dt> </dl>

 

