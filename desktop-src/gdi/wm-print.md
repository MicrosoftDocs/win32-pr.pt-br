---
description: A mensagem de impressão do WM \_ é enviada a uma janela para solicitar que ela se desenhe no contexto do dispositivo especificado, mais comumente em um contexto de dispositivo de impressora.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: Mensagem de WM_PRINT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010877"
---
# <a name="wm_print-message"></a><span data-ttu-id="9b015-103">Mensagem de impressão do WM \_</span><span class="sxs-lookup"><span data-stu-id="9b015-103">WM\_PRINT message</span></span>

<span data-ttu-id="9b015-104">A mensagem de **\_ impressão do WM** é enviada a uma janela para solicitar que ela se desenhe no contexto do dispositivo especificado, mais comumente em um contexto de dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="9b015-104">The **WM\_PRINT** message is sent to a window to request that it draw itself in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="9b015-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9b015-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="9b015-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b015-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b015-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b015-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b015-108">Um identificador para o contexto do dispositivo para desenhar.</span><span class="sxs-lookup"><span data-stu-id="9b015-108">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="9b015-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b015-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b015-110">As opções de desenho.</span><span class="sxs-lookup"><span data-stu-id="9b015-110">The drawing options.</span></span> <span data-ttu-id="9b015-111">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9b015-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="9b015-112">Valor</span><span class="sxs-lookup"><span data-stu-id="9b015-112">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="9b015-113">Significado</span><span class="sxs-lookup"><span data-stu-id="9b015-113">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="9b015-114"><dt>**\_CHECKVISIBLE PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="9b015-114"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="9b015-115">Desenha a janela somente se ela estiver visível.</span><span class="sxs-lookup"><span data-stu-id="9b015-115">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="9b015-116"><dt>**filhos de PRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b015-116"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="9b015-117">Desenha todas as janelas filhas visíveis.</span><span class="sxs-lookup"><span data-stu-id="9b015-117">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="9b015-118"><dt>**\_cliente PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="9b015-118"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="9b015-119">Desenha a área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="9b015-119">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="9b015-120"><dt>**\_ERASEBKGND PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="9b015-120"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="9b015-121">Apaga o plano de fundo antes de desenhar a janela.</span><span class="sxs-lookup"><span data-stu-id="9b015-121">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="9b015-122"><dt>**Não \_ cliente PRF**</dt></span><span class="sxs-lookup"><span data-stu-id="9b015-122"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="9b015-123">Desenha a área não cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="9b015-123">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="9b015-124"><dt>**Propriedade do PRF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9b015-124"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="9b015-125">Desenha todas as janelas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="9b015-125">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b015-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b015-126">Remarks</span></span>

<span data-ttu-id="9b015-127">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processa essa mensagem com base na opção de desenho especificada: se Prf \_ CHECKVISIBLE for especificado e a janela não estiver visível, não faça nada, se PRF não \_ cliente for especificado, desenhe a área não-cliente no contexto do dispositivo especificado, se Prf \_ ERASEBKGND for especificado, envie a janela a uma mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) , se o \_ cliente PRF for especificado, envie a janela uma mensagem do [**WM \_ myclient**](wm-printclient.md) , se os filhos do Prf \_ estiverem definidos, envie cada janela filho visível a uma **\_** \_ **\_** mensagem de impressão do WM.</span><span class="sxs-lookup"><span data-stu-id="9b015-127">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes this message based on which drawing option is specified: if PRF\_CHECKVISIBLE is specified and the window is not visible, do nothing, if PRF\_NONCLIENT is specified, draw the nonclient area in the specified device context, if PRF\_ERASEBKGND is specified, send the window a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message, if PRF\_CLIENT is specified, send the window a [**WM\_PRINTCLIENT**](wm-printclient.md) message, if PRF\_CHILDREN is set, send each visible child window a **WM\_PRINT** message, if PRF\_OWNED is set, send each visible owned window a **WM\_PRINT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b015-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b015-128">Requirements</span></span>



| <span data-ttu-id="9b015-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b015-129">Requirement</span></span> | <span data-ttu-id="9b015-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9b015-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b015-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b015-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9b015-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9b015-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9b015-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b015-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9b015-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9b015-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9b015-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9b015-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b015-136"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b015-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b015-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b015-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b015-138">Visão geral de pintura e desenho</span><span class="sxs-lookup"><span data-stu-id="9b015-138">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="9b015-139">Pintura e desenho de mensagens</span><span class="sxs-lookup"><span data-stu-id="9b015-139">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="9b015-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9b015-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9b015-141">**ERASEBKGND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="9b015-141">**WM\_ERASEBKGND**</span></span>](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[<span data-ttu-id="9b015-142">**WM \_ FILEclient**</span><span class="sxs-lookup"><span data-stu-id="9b015-142">**WM\_PRINTCLIENT**</span></span>](wm-printclient.md)
</dt> </dl>

 

 
