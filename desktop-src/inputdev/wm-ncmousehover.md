---
title: Mensagem de WM_NCMOUSEHOVER (WinUser. h)
description: Postado em uma janela quando o cursor passa sobre a área não cliente da janela pelo período de tempo especificado em uma chamada anterior para TrackMouseEvent.
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- Entrada de mouse e teclado de mensagem WM_NCMOUSEHOVER
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde2e70b04602de5936e945789007a6c5fea8542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009682"
---
# <a name="wm_ncmousehover-message"></a><span data-ttu-id="b2b18-104">Mensagem do WM \_ NCMOUSEHOVER</span><span class="sxs-lookup"><span data-stu-id="b2b18-104">WM\_NCMOUSEHOVER message</span></span>

<span data-ttu-id="b2b18-105">Postado em uma janela quando o cursor passa sobre a área não cliente da janela pelo período de tempo especificado em uma chamada anterior para [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="b2b18-105">Posted to a window when the cursor hovers over the nonclient area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="b2b18-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b2b18-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSEHOVER                 0x02A0
```



## <a name="parameters"></a><span data-ttu-id="b2b18-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2b18-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b18-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2b18-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2b18-109">O valor de teste de clique retornado pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado do processamento da mensagem [**\_ NCHITTEST do WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="b2b18-109">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="b2b18-110">Para obter uma lista de valores de teste de clique, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="b2b18-110">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="b2b18-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2b18-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b2b18-112">Uma estrutura de [**pontos**](/previous-versions//dd162808(v=vs.85)) que contém as coordenadas x e y do cursor.</span><span class="sxs-lookup"><span data-stu-id="b2b18-112">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="b2b18-113">As coordenadas são relativas ao canto superior esquerdo da tela.</span><span class="sxs-lookup"><span data-stu-id="b2b18-113">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2b18-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2b18-114">Return value</span></span>

<span data-ttu-id="b2b18-115">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="b2b18-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2b18-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2b18-116">Remarks</span></span>

<span data-ttu-id="b2b18-117">O controle de foco para quando essa mensagem é gerada.</span><span class="sxs-lookup"><span data-stu-id="b2b18-117">Hover tracking stops when this message is generated.</span></span> <span data-ttu-id="b2b18-118">O aplicativo deve chamar [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) novamente se precisar de mais controle sobre o comportamento de focalização do mouse.</span><span class="sxs-lookup"><span data-stu-id="b2b18-118">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="b2b18-119">Você também pode usar as macros [**Get \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) e [**Get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extrair os valores das coordenadas X e y do *lParam*.</span><span class="sxs-lookup"><span data-stu-id="b2b18-119">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="b2b18-120">Não use as macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ou [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extrair as coordenadas x e y da posição do cursor, pois essas macros retornam resultados incorretos em sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="b2b18-120">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="b2b18-121">Sistemas com vários monitores podem ter coordenadas x e y negativas e **LOWORD** e **HIWORD** tratam as coordenadas como quantidades não assinadas.</span><span class="sxs-lookup"><span data-stu-id="b2b18-121">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2b18-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2b18-122">Requirements</span></span>



| <span data-ttu-id="b2b18-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b18-123">Requirement</span></span> | <span data-ttu-id="b2b18-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b2b18-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b18-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2b18-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b18-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b2b18-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b2b18-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2b18-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b18-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b2b18-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b2b18-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b2b18-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2b18-130"><dt>WinUser. h (incluir Windowsx. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2b18-130"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b18-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2b18-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2b18-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b2b18-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2b18-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="b2b18-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b2b18-134">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="b2b18-134">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="b2b18-135">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="b2b18-135">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="b2b18-136">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="b2b18-136">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="b2b18-137">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="b2b18-137">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="b2b18-138">**NCHITTEST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b2b18-138">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="b2b18-139">**MOUSEHOVER do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b2b18-139">**WM\_MOUSEHOVER**</span></span>](wm-mousehover.md)
</dt> <dt>

<span data-ttu-id="b2b18-140">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b2b18-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b2b18-141">Entrada do mouse</span><span class="sxs-lookup"><span data-stu-id="b2b18-141">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="b2b18-142">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="b2b18-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b2b18-143">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="b2b18-143">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="b2b18-144">[**FAIXAS**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2b18-144">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

