---
title: Mensagem de WM_MOUSELEAVE (WinUser. h)
description: Postado em uma janela quando o cursor sai da área do cliente da janela especificada em uma chamada anterior para TrackMouseEvent.
ms.assetid: b23d24ff-531a-4b6d-8848-f82ac5568995
keywords:
- Entrada de mouse e teclado de mensagem WM_MOUSELEAVE
topic_type:
- apiref
api_name:
- WM_MOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc96022e94df7f518b21b1c9a46895fc9204b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454955"
---
# <a name="wm_mouseleave-message"></a><span data-ttu-id="3849e-104">Mensagem de MOUSELEAVE do WM \_</span><span class="sxs-lookup"><span data-stu-id="3849e-104">WM\_MOUSELEAVE message</span></span>

<span data-ttu-id="3849e-105">Postado em uma janela quando o cursor sai da área do cliente da janela especificada em uma chamada anterior para [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="3849e-105">Posted to a window when the cursor leaves the client area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="3849e-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3849e-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSELEAVE                   0x02A3
```



## <a name="parameters"></a><span data-ttu-id="3849e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3849e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3849e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3849e-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3849e-109">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3849e-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3849e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3849e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3849e-111">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3849e-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3849e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3849e-112">Return value</span></span>

<span data-ttu-id="3849e-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="3849e-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3849e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3849e-114">Remarks</span></span>

<span data-ttu-id="3849e-115">Todo o controle solicitado por [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) é cancelado quando esta mensagem é gerada.</span><span class="sxs-lookup"><span data-stu-id="3849e-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="3849e-116">O aplicativo deve chamar **TrackMouseEvent** quando o mouse reinserir sua janela se precisar de mais controle sobre o comportamento de focalização do mouse.</span><span class="sxs-lookup"><span data-stu-id="3849e-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="3849e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3849e-117">Requirements</span></span>



| <span data-ttu-id="3849e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3849e-118">Requirement</span></span> | <span data-ttu-id="3849e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3849e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3849e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3849e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3849e-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3849e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3849e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3849e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3849e-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3849e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3849e-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3849e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3849e-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3849e-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3849e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3849e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="3849e-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="3849e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3849e-128">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="3849e-128">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="3849e-129">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="3849e-129">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="3849e-130">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="3849e-130">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="3849e-131">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="3849e-131">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="3849e-132">**NCMOUSELEAVE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3849e-132">**WM\_NCMOUSELEAVE**</span></span>](wm-ncmouseleave.md)
</dt> <dt>

<span data-ttu-id="3849e-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="3849e-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3849e-134">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="3849e-134">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

