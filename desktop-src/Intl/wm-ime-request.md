---
description: Enviado a um aplicativo para fornecer comandos e informações de solicitação. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: Mensagem de WM_IME_REQUEST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0cea120d088fe1423b1d7dcb822307886675b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751461"
---
# <a name="wm_ime_request-message"></a><span data-ttu-id="581dd-104">WM_IME_REQUEST mensagem</span><span class="sxs-lookup"><span data-stu-id="581dd-104">WM_IME_REQUEST message</span></span>

<span data-ttu-id="581dd-105">Enviado a um aplicativo para fornecer comandos e informações de solicitação.</span><span class="sxs-lookup"><span data-stu-id="581dd-105">Sent to an application to provide commands and request information.</span></span> <span data-ttu-id="581dd-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="581dd-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="581dd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="581dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="581dd-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="581dd-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="581dd-109">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="581dd-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="581dd-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="581dd-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="581dd-111">Comando.</span><span class="sxs-lookup"><span data-stu-id="581dd-111">Command.</span></span> <span data-ttu-id="581dd-112">Esse parâmetro pode ter um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="581dd-112">This parameter can have one of the following values:</span></span>

<dl> 
<dd><span data-ttu-id="581dd-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="581dd-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="581dd-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="581dd-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="581dd-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="581dd-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="581dd-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="581dd-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span></span></dd> 
<dd><span data-ttu-id="581dd-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span><span class="sxs-lookup"><span data-stu-id="581dd-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span></span></dd> 
<dd><span data-ttu-id="581dd-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span><span class="sxs-lookup"><span data-stu-id="581dd-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span></span></dd> 
<dd><span data-ttu-id="581dd-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="581dd-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="581dd-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="581dd-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="581dd-121">Dados específicos do comando.</span><span class="sxs-lookup"><span data-stu-id="581dd-121">Command-specific data.</span></span> <span data-ttu-id="581dd-122">Para obter mais informações, consulte a descrição de cada comando.</span><span class="sxs-lookup"><span data-stu-id="581dd-122">For more information, see the description for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="581dd-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="581dd-123">Return value</span></span>

<span data-ttu-id="581dd-124">Retorna um valor específico de comando.</span><span class="sxs-lookup"><span data-stu-id="581dd-124">Returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="581dd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="581dd-125">Requirements</span></span>



| <span data-ttu-id="581dd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="581dd-126">Requirement</span></span> | <span data-ttu-id="581dd-127">Valor</span><span class="sxs-lookup"><span data-stu-id="581dd-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="581dd-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="581dd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="581dd-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="581dd-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="581dd-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="581dd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="581dd-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="581dd-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="581dd-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="581dd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="581dd-133"><dt>WinUser. h (incluir Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="581dd-133"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="581dd-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="581dd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="581dd-135">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="581dd-135">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="581dd-136">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="581dd-136">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="581dd-137">IMR_CANDIDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="581dd-137">IMR_CANDIDATEWINDOW</span></span>](imr-candidatewindow.md)
</dt> <dt>

[<span data-ttu-id="581dd-138">IMR_COMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="581dd-138">IMR_COMPOSITIONFONT</span></span>](imr-compositionfont.md)
</dt> <dt>

[<span data-ttu-id="581dd-139">IMR_COMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="581dd-139">IMR_COMPOSITIONWINDOW</span></span>](imr-compositionwindow.md)
</dt> <dt>

[<span data-ttu-id="581dd-140">IMR_CONFIRMRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="581dd-140">IMR_CONFIRMRECONVERTSTRING</span></span>](imr-confirmreconvertstring.md)
</dt> <dt>

[<span data-ttu-id="581dd-141">IMR_DOCUMENTFEED</span><span class="sxs-lookup"><span data-stu-id="581dd-141">IMR_DOCUMENTFEED</span></span>](imr-documentfeed.md)
</dt> <dt>

[<span data-ttu-id="581dd-142">IMR_QUERYCHARPOSITION</span><span class="sxs-lookup"><span data-stu-id="581dd-142">IMR_QUERYCHARPOSITION</span></span>](imr-querycharposition.md)
</dt> <dt>

[<span data-ttu-id="581dd-143">IMR_RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="581dd-143">IMR_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> </dl>

 

 
