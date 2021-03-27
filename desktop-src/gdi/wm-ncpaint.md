---
description: A mensagem do WM \_ NCPAINT é enviada para uma janela quando seu quadro deve ser pintado.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: Mensagem de WM_NCPAINT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6c2e211f3dc1602821b0197d295f940606c262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827988"
---
# <a name="wm_ncpaint-message"></a><span data-ttu-id="8d62f-103">Mensagem do WM \_ NCPAINT</span><span class="sxs-lookup"><span data-stu-id="8d62f-103">WM\_NCPAINT message</span></span>

<span data-ttu-id="8d62f-104">A mensagem do **WM \_ NCPAINT** é enviada para uma janela quando seu quadro deve ser pintado.</span><span class="sxs-lookup"><span data-stu-id="8d62f-104">The **WM\_NCPAINT** message is sent to a window when its frame must be painted.</span></span>

<span data-ttu-id="8d62f-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8d62f-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="8d62f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d62f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d62f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d62f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d62f-108">Um identificador para a região de atualização da janela.</span><span class="sxs-lookup"><span data-stu-id="8d62f-108">A handle to the update region of the window.</span></span> <span data-ttu-id="8d62f-109">A região de atualização é recortada no quadro da janela.</span><span class="sxs-lookup"><span data-stu-id="8d62f-109">The update region is clipped to the window frame.</span></span>

</dd> <dt>

<span data-ttu-id="8d62f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d62f-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d62f-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="8d62f-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d62f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d62f-112">Return value</span></span>

<span data-ttu-id="8d62f-113">Um aplicativo retornará zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="8d62f-113">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d62f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d62f-114">Remarks</span></span>

<span data-ttu-id="8d62f-115">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pinta o quadro da janela.</span><span class="sxs-lookup"><span data-stu-id="8d62f-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function paints the window frame.</span></span>

<span data-ttu-id="8d62f-116">Um aplicativo pode interceptar a mensagem **\_ NCPAINT do WM** e pintar seu próprio quadro de janela personalizado.</span><span class="sxs-lookup"><span data-stu-id="8d62f-116">An application can intercept the **WM\_NCPAINT** message and paint its own custom window frame.</span></span> <span data-ttu-id="8d62f-117">A região de recorte para uma janela é sempre retangular, mesmo que a forma do quadro seja alterada.</span><span class="sxs-lookup"><span data-stu-id="8d62f-117">The clipping region for a window is always rectangular, even if the shape of the frame is altered.</span></span>

<span data-ttu-id="8d62f-118">O valor *wParam* pode ser passado para [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="8d62f-118">The *wParam* value can be passed to [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) as in the following example.</span></span>


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a><span data-ttu-id="8d62f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d62f-119">Requirements</span></span>



| <span data-ttu-id="8d62f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d62f-120">Requirement</span></span> | <span data-ttu-id="8d62f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8d62f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d62f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d62f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8d62f-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d62f-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8d62f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d62f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8d62f-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d62f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8d62f-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8d62f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d62f-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d62f-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d62f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d62f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d62f-129">Visão geral de pintura e desenho</span><span class="sxs-lookup"><span data-stu-id="8d62f-129">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="8d62f-130">Pintura e desenho de mensagens</span><span class="sxs-lookup"><span data-stu-id="8d62f-130">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="8d62f-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="8d62f-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="8d62f-132">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="8d62f-132">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="8d62f-133">**pintura do WM \_**</span><span class="sxs-lookup"><span data-stu-id="8d62f-133">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> <dt>

[<span data-ttu-id="8d62f-134">**GetDCEx**</span><span class="sxs-lookup"><span data-stu-id="8d62f-134">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
