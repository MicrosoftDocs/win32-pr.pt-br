---
description: Enviado por um aplicativo para direcionar a janela do IME para executar o comando solicitado.
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: Mensagem de WM_IME_CONTROL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0adc534883bc0b31984c8d3e9b57a04b555987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827155"
---
# <a name="wm_ime_control-message"></a><span data-ttu-id="edc3d-103">WM_IME_CONTROL mensagem</span><span class="sxs-lookup"><span data-stu-id="edc3d-103">WM_IME_CONTROL message</span></span>

<span data-ttu-id="edc3d-104">Enviado por um aplicativo para direcionar a janela do IME para executar o comando solicitado.</span><span class="sxs-lookup"><span data-stu-id="edc3d-104">Sent by an application to direct the IME window to carry out the requested command.</span></span> <span data-ttu-id="edc3d-105">O aplicativo usa essa mensagem para controlar a janela do IME que ela criou.</span><span class="sxs-lookup"><span data-stu-id="edc3d-105">The application uses this message to control the IME window that it has created.</span></span> <span data-ttu-id="edc3d-106">Para enviar essa mensagem, o aplicativo chama a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) com os parâmetros a seguir.</span><span class="sxs-lookup"><span data-stu-id="edc3d-106">To send this message, the application calls the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage(
  HWND   hwnd,
  WM_IME_CONTROL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="edc3d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edc3d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc3d-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="edc3d-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="edc3d-109">Identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="edc3d-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="edc3d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="edc3d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edc3d-111">O comando.</span><span class="sxs-lookup"><span data-stu-id="edc3d-111">The command.</span></span> <span data-ttu-id="edc3d-112">Esse parâmetro pode ter um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="edc3d-112">This parameter can have one of the following values:</span></span>

<dl>
<dd><span data-ttu-id="edc3d-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="edc3d-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="edc3d-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="edc3d-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="edc3d-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="edc3d-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="edc3d-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="edc3d-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="edc3d-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="edc3d-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span></span></dd> 
<dd><span data-ttu-id="edc3d-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="edc3d-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="edc3d-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="edc3d-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="edc3d-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span><span class="sxs-lookup"><span data-stu-id="edc3d-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span></span></dd> 
<dd><span data-ttu-id="edc3d-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="edc3d-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="edc3d-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="edc3d-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl>
</dd>

<dt>

<span data-ttu-id="edc3d-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="edc3d-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="edc3d-124">Dados específicos do comando, com formato dependente do valor do parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="edc3d-124">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="edc3d-125">Para obter mais informações, consulte a documentação de cada comando.</span><span class="sxs-lookup"><span data-stu-id="edc3d-125">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc3d-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="edc3d-126">Return value</span></span>

<span data-ttu-id="edc3d-127">A mensagem retorna um valor específico de comando.</span><span class="sxs-lookup"><span data-stu-id="edc3d-127">The message returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="edc3d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edc3d-128">Requirements</span></span>



| <span data-ttu-id="edc3d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="edc3d-129">Requirement</span></span> | <span data-ttu-id="edc3d-130">Valor</span><span class="sxs-lookup"><span data-stu-id="edc3d-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edc3d-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edc3d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="edc3d-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="edc3d-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="edc3d-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edc3d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="edc3d-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="edc3d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="edc3d-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="edc3d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="edc3d-136"><dt>WinUser. h (incluir Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edc3d-136"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edc3d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="edc3d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc3d-138">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="edc3d-138">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="edc3d-139">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="edc3d-139">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="edc3d-140">IMC_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="edc3d-140">IMC_CLOSESTATUSWINDOW</span></span>](imc-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="edc3d-141">IMC_GETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="edc3d-141">IMC_GETCANDIDATEPOS</span></span>](imc-getcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="edc3d-142">IMC_GETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="edc3d-142">IMC_GETCOMPOSITIONFONT</span></span>](imc-getcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="edc3d-143">IMC_GETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="edc3d-143">IMC_GETCOMPOSITIONWINDOW</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="edc3d-144">IMC_GETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="edc3d-144">IMC_GETSTATUSWINDOWPOS</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="edc3d-145">IMC_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="edc3d-145">IMC_OPENSTATUSWINDOW</span></span>](imc-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="edc3d-146">IMC_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="edc3d-146">IMC_SETCANDIDATEPOS</span></span>](imc-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="edc3d-147">IMC_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="edc3d-147">IMC_SETCOMPOSITIONFONT</span></span>](imc-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="edc3d-148">IMC_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="edc3d-148">IMC_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="edc3d-149">IMC_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="edc3d-149">IMC_SETSTATUSWINDOWPOS</span></span>](imc-setstatuswindowpos.md)
</dt> </dl>

 

 
