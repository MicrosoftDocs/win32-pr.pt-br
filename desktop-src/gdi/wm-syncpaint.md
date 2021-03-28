---
description: A mensagem do WM \_ SYNCPAINT é usada para sincronizar a pintura enquanto evita a vinculação de threads de GUI independentes.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: Mensagem de WM_SYNCPAINT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988950"
---
# <a name="wm_syncpaint-message"></a><span data-ttu-id="6e5aa-103">Mensagem do WM \_ SYNCPAINT</span><span class="sxs-lookup"><span data-stu-id="6e5aa-103">WM\_SYNCPAINT message</span></span>

<span data-ttu-id="6e5aa-104">A mensagem do **WM \_ SYNCPAINT** é usada para sincronizar a pintura enquanto evita a vinculação de threads de GUI independentes.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-104">The **WM\_SYNCPAINT** message is used to synchronize painting while avoiding linking independent GUI threads.</span></span>

<span data-ttu-id="6e5aa-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6e5aa-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="6e5aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e5aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e5aa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e5aa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e5aa-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e5aa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e5aa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e5aa-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e5aa-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e5aa-111">Return value</span></span>

<span data-ttu-id="6e5aa-112">Um aplicativo retornará zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-112">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e5aa-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e5aa-113">Remarks</span></span>

<span data-ttu-id="6e5aa-114">Quando uma janela é oculta, mostrada, movida ou dimensionada, o sistema pode determinar que é necessário enviar uma mensagem do **WM \_ SYNCPAINT** para as janelas de nível superior de outros threads.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-114">When a window has been hidden, shown, moved, or sized, the system may determine that it is necessary to send a **WM\_SYNCPAINT** message to the top-level windows of other threads.</span></span> <span data-ttu-id="6e5aa-115">Os aplicativos devem passar o **WM \_ SYNCPAINT** para o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para processamento.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-115">Applications must pass **WM\_SYNCPAINT** to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  for processing.</span></span> <span data-ttu-id="6e5aa-116">A função **DefWindowProc** enviará uma mensagem do [**WM \_ NCPAINT**](wm-ncpaint.md) para o procedimento de janela se o quadro da janela precisar ser pintado e enviar uma mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) se o plano de fundo da janela precisar ser apagado.</span><span class="sxs-lookup"><span data-stu-id="6e5aa-116">The **DefWindowProc** function will send a [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e5aa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e5aa-117">Requirements</span></span>



| <span data-ttu-id="6e5aa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e5aa-118">Requirement</span></span> | <span data-ttu-id="6e5aa-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6e5aa-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5aa-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e5aa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6e5aa-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e5aa-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6e5aa-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e5aa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6e5aa-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e5aa-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e5aa-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6e5aa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e5aa-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e5aa-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e5aa-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e5aa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e5aa-127">Visão geral de pintura e desenho</span><span class="sxs-lookup"><span data-stu-id="6e5aa-127">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="6e5aa-128">Pintura e desenho de mensagens</span><span class="sxs-lookup"><span data-stu-id="6e5aa-128">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="6e5aa-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="6e5aa-130">**GetDCEx**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-130">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[<span data-ttu-id="6e5aa-131">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-131">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="6e5aa-132">**pintura do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6e5aa-132">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
