---
description: A mensagem do WM \_ DISPLAYCHANGE é enviada para todas as janelas quando a resolução de vídeo é alterada.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Mensagem de WM_DISPLAYCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169130"
---
# <a name="wm_displaychange-message"></a><span data-ttu-id="08d70-103">Mensagem do WM \_ DISPLAYCHANGE</span><span class="sxs-lookup"><span data-stu-id="08d70-103">WM\_DISPLAYCHANGE message</span></span>

<span data-ttu-id="08d70-104">A mensagem do **WM \_ DISPLAYCHANGE** é enviada para todas as janelas quando a resolução de vídeo é alterada.</span><span class="sxs-lookup"><span data-stu-id="08d70-104">The **WM\_DISPLAYCHANGE** message is sent to all windows when the display resolution has changed.</span></span>

<span data-ttu-id="08d70-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="08d70-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="08d70-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08d70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d70-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08d70-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08d70-108">A nova profundidade da imagem da exibição, em bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="08d70-108">The new image depth of the display, in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="08d70-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08d70-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08d70-110">A palavra de ordem inferior Especifica a resolução horizontal da tela.</span><span class="sxs-lookup"><span data-stu-id="08d70-110">The low-order word specifies the horizontal resolution of the screen.</span></span>

<span data-ttu-id="08d70-111">A palavra de ordem superior especifica a resolução vertical da tela.</span><span class="sxs-lookup"><span data-stu-id="08d70-111">The high-order word specifies the vertical resolution of the screen.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08d70-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="08d70-112">Remarks</span></span>

<span data-ttu-id="08d70-113">Essa mensagem é enviada somente para janelas de nível superior.</span><span class="sxs-lookup"><span data-stu-id="08d70-113">This message is only sent to top-level windows.</span></span> <span data-ttu-id="08d70-114">Para todas as outras janelas, ele é Postado.</span><span class="sxs-lookup"><span data-stu-id="08d70-114">For all other windows it is posted.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d70-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08d70-115">Requirements</span></span>



| <span data-ttu-id="08d70-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="08d70-116">Requirement</span></span> | <span data-ttu-id="08d70-117">Valor</span><span class="sxs-lookup"><span data-stu-id="08d70-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d70-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08d70-118">Minimum supported client</span></span><br/> | <span data-ttu-id="08d70-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="08d70-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="08d70-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08d70-120">Minimum supported server</span></span><br/> | <span data-ttu-id="08d70-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="08d70-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08d70-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="08d70-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="08d70-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08d70-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08d70-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="08d70-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d70-125">Visão geral de pintura e desenho</span><span class="sxs-lookup"><span data-stu-id="08d70-125">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="08d70-126">Pintura e desenho de mensagens</span><span class="sxs-lookup"><span data-stu-id="08d70-126">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

<span data-ttu-id="08d70-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08d70-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="08d70-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08d70-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

 
