---
title: Mensagem de WM_TOUCH (WinUser. h)
description: Notifica a janela quando um ou mais pontos de toque, como um dedo ou uma caneta, toca uma superfície digitalizadora sensível ao toque.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH a mensagem Windows Touch
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b6242d43b661240d946d2883237640d1bc92b3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369755"
---
# <a name="wm_touch-message"></a><span data-ttu-id="5377c-104">Mensagem de toque do WM \_</span><span class="sxs-lookup"><span data-stu-id="5377c-104">WM\_TOUCH message</span></span>

<span data-ttu-id="5377c-105">Notifica a janela quando um ou mais pontos de toque, como um dedo ou uma caneta, toca uma superfície digitalizadora sensível ao toque.</span><span class="sxs-lookup"><span data-stu-id="5377c-105">Notifies the window when one or more touch points, such as a finger or pen, touches a touch-sensitive digitizer surface.</span></span>

## <a name="parameters"></a><span data-ttu-id="5377c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5377c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5377c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5377c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5377c-108">A palavra de ordem inferior contém o número de pontos de toque associados a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="5377c-108">The low-order word contains the number of touch points associated with this message.</span></span> <span data-ttu-id="5377c-109">A palavra de ordem superior é reservada para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5377c-109">The high-order word is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="5377c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5377c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5377c-111">Contém um identificador de entrada por toque que pode ser usado em uma chamada para [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) para recuperar informações detalhadas sobre os pontos de toque associados a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="5377c-111">Contains a touch input handle that can be used in a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) to retrieve detailed information about the touch points associated with this message.</span></span>

<span data-ttu-id="5377c-112">Esse identificador é válido somente dentro do processo atual e não deve passar por processo cruzado, exceto como **lParam** em uma chamada **SendMessage** ou de **mensagem** .</span><span class="sxs-lookup"><span data-stu-id="5377c-112">This handle is valid only within the current process and should not be passed cross-process except as the **LPARAM** in a **SendMessage** or **PostMessage** call.</span></span>

<span data-ttu-id="5377c-113">Quando o aplicativo não requer mais esse identificador, o aplicativo deve chamar **CloseTouchInputHandle** para liberar a memória de processo associada a esse identificador.</span><span class="sxs-lookup"><span data-stu-id="5377c-113">When the application no longer requires this handle, the application must call **CloseTouchInputHandle** to free the process memory associated with this handle.</span></span> <span data-ttu-id="5377c-114">A falha ao fazer isso pode resultar em um vazamento de memória do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5377c-114">Failing to do so can result in an application memory leak.</span></span>

<span data-ttu-id="5377c-115">Observe que o identificador de entrada por toque nesse parâmetro não é mais válido depois que a mensagem foi passada para [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="5377c-115">Note that the touch input handle in this parameter is no longer valid after the message has been passed to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="5377c-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) fechará e invalidará esse identificador.</span><span class="sxs-lookup"><span data-stu-id="5377c-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will close and invalidate this handle.</span></span>

<span data-ttu-id="5377c-117">Observe também que o identificador de entrada por toque nesse parâmetro não é mais válido depois que a mensagem foi encaminhada [**usando a mensagem,**](sendmessage--postmessage--and-related-functions.md) **SendMessage** ou uma de suas variantes.</span><span class="sxs-lookup"><span data-stu-id="5377c-117">Note also that the touch input handle in this parameter is no longer valid after the message has been forwarded using [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage**, or one of their variants.</span></span> <span data-ttu-id="5377c-118">Essas funções serão fechadas e invalidarão esse identificador.</span><span class="sxs-lookup"><span data-stu-id="5377c-118">These functions will close and invalidate this handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5377c-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5377c-119">Return value</span></span>

<span data-ttu-id="5377c-120">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="5377c-120">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="5377c-121">Se o aplicativo não processar a mensagem, ele deverá chamar [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="5377c-121">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="5377c-122">Não fazer isso faz com que o aplicativo vazasse memória porque o identificador de entrada por toque não está fechado e a memória de processo associada não é liberada.</span><span class="sxs-lookup"><span data-stu-id="5377c-122">Not doing so causes the application to leak memory because the touch input handle is not closed and associated process memory is not freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="5377c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5377c-123">Remarks</span></span>

<span data-ttu-id="5377c-124">**WM \_** As mensagens de toque não respeitam regiões **HTTRANSPARENTs** do Windows.</span><span class="sxs-lookup"><span data-stu-id="5377c-124">**WM\_TOUCH** messages do not respect **HTTRANSPARENT** regions of windows.</span></span> <span data-ttu-id="5377c-125">Se uma janela retornar **HTTRANSPARENT** em resposta a uma mensagem do **WM \_ NCHITTEST** , as mensagens do mouse vão para o pai e as mensagens do **WM \_ Touch** vão diretamente para a janela.</span><span class="sxs-lookup"><span data-stu-id="5377c-125">If a window returns **HTTRANSPARENT** in response to a **WM\_NCHITTEST** message, mouse messages go to the parent, and **WM\_TOUCH** messages go directly to the window.</span></span>

## <a name="examples"></a><span data-ttu-id="5377c-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5377c-126">Examples</span></span>

<span data-ttu-id="5377c-127">O código a seguir é um exemplo de como obter informações detalhadas de entrada de toque associadas a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="5377c-127">The following code is an example of how to obtain detailed touch input information associated with this message.</span></span>


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a><span data-ttu-id="5377c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5377c-128">Requirements</span></span>



| <span data-ttu-id="5377c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5377c-129">Requirement</span></span> | <span data-ttu-id="5377c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5377c-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5377c-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5377c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5377c-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5377c-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="5377c-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5377c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5377c-134">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="5377c-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="5377c-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5377c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5377c-136"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5377c-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5377c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5377c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5377c-138">Mensagens</span><span class="sxs-lookup"><span data-stu-id="5377c-138">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="5377c-139">Manipulações e guia de programação inércia</span><span class="sxs-lookup"><span data-stu-id="5377c-139">Manipulations and Inertia Programming Guide</span></span>](manipulation-and-inertia.md)
</dt> <dt>

[<span data-ttu-id="5377c-140">Guia de programação de entrada do Windows Touch</span><span class="sxs-lookup"><span data-stu-id="5377c-140">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

