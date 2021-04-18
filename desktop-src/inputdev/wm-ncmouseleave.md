---
title: Mensagem de WM_NCMOUSELEAVE (WinUser. h)
description: Postado em uma janela quando o cursor sai da área não cliente da janela especificada em uma chamada anterior para TrackMouseEvent.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- Entrada de mouse e teclado de mensagem WM_NCMOUSELEAVE
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf7f9d0931c2623d2e92010abfca96f391107b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788970"
---
# <a name="wm_ncmouseleave-message"></a><span data-ttu-id="5912a-104">Mensagem do WM \_ NCMOUSELEAVE</span><span class="sxs-lookup"><span data-stu-id="5912a-104">WM\_NCMOUSELEAVE message</span></span>

<span data-ttu-id="5912a-105">Postado em uma janela quando o cursor sai da área não cliente da janela especificada em uma chamada anterior para [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="5912a-105">Posted to a window when the cursor leaves the nonclient area of the window specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="5912a-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5912a-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSELEAVE                 0x02A2
```



## <a name="parameters"></a><span data-ttu-id="5912a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5912a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5912a-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5912a-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5912a-109">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5912a-109">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5912a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5912a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5912a-111">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5912a-111">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5912a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5912a-112">Return value</span></span>

<span data-ttu-id="5912a-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="5912a-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5912a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5912a-114">Remarks</span></span>

<span data-ttu-id="5912a-115">Todo o controle solicitado por [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) é cancelado quando esta mensagem é gerada.</span><span class="sxs-lookup"><span data-stu-id="5912a-115">All tracking requested by [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) is canceled when this message is generated.</span></span> <span data-ttu-id="5912a-116">O aplicativo deve chamar **TrackMouseEvent** quando o mouse reinserir sua janela se precisar de mais controle sobre o comportamento de focalização do mouse.</span><span class="sxs-lookup"><span data-stu-id="5912a-116">The application must call **TrackMouseEvent** when the mouse reenters its window if it requires further tracking of mouse hover behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="5912a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5912a-117">Requirements</span></span>



| <span data-ttu-id="5912a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5912a-118">Requirement</span></span> | <span data-ttu-id="5912a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5912a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5912a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5912a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5912a-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5912a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5912a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5912a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5912a-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5912a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5912a-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5912a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5912a-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5912a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5912a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5912a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="5912a-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5912a-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5912a-128">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="5912a-128">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="5912a-129">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="5912a-129">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="5912a-130">**SYSCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="5912a-130">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="5912a-131">**MOUSELEAVE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="5912a-131">**WM\_MOUSELEAVE**</span></span>](wm-mouseleave.md)
</dt> <dt>

<span data-ttu-id="5912a-132">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5912a-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5912a-133">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="5912a-133">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

