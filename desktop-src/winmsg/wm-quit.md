---
description: Indica uma solicitação para encerrar um aplicativo e é gerado quando o aplicativo chama a função PostQuitMessage. Essa mensagem faz com que a função GetMessage retorne zero.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: Mensagem de WM_QUIT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011049"
---
# <a name="wm_quit-message"></a><span data-ttu-id="5d0a8-104">Mensagem de encerramento do WM \_</span><span class="sxs-lookup"><span data-stu-id="5d0a8-104">WM\_QUIT message</span></span>

<span data-ttu-id="5d0a8-105">Indica uma solicitação para encerrar um aplicativo e é gerado quando o aplicativo chama a função [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="5d0a8-105">Indicates a request to terminate an application, and is generated when the application calls the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span> <span data-ttu-id="5d0a8-106">Essa mensagem faz com que a função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) retorne zero.</span><span class="sxs-lookup"><span data-stu-id="5d0a8-106">This message causes the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) function to return zero.</span></span>


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a><span data-ttu-id="5d0a8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d0a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d0a8-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d0a8-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d0a8-109">O código de saída fornecido na função [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .</span><span class="sxs-lookup"><span data-stu-id="5d0a8-109">The exit code given in the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="5d0a8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d0a8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d0a8-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="5d0a8-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d0a8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d0a8-112">Return value</span></span>

<span data-ttu-id="5d0a8-113">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5d0a8-113">Type: **LRESULT**</span></span>

<span data-ttu-id="5d0a8-114">Essa mensagem não tem um valor de retorno porque faz com que o loop de mensagem seja encerrado antes que a mensagem seja enviada ao procedimento de janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5d0a8-114">This message does not have a return value because it causes the message loop to terminate before the message is sent to the application's window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d0a8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d0a8-115">Remarks</span></span>

<span data-ttu-id="5d0a8-116">A mensagem do **WM \_ Quit** não está associada a uma janela e, portanto, nunca será recebida por meio de um procedimento de janela da janela.</span><span class="sxs-lookup"><span data-stu-id="5d0a8-116">The **WM\_QUIT** message is not associated with a window and therefore will never be received through a window's window procedure.</span></span> <span data-ttu-id="5d0a8-117">Ele é recuperado somente pelas funções [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="5d0a8-117">It is retrieved only by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions.</span></span>

<span data-ttu-id="5d0a8-118">Não poste a mensagem do **WM \_ Quit** usando a função [**CreateMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) ; use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="5d0a8-118">Do not post the **WM\_QUIT** message using the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function; use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d0a8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d0a8-119">Requirements</span></span>



| <span data-ttu-id="5d0a8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d0a8-120">Requirement</span></span> | <span data-ttu-id="5d0a8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5d0a8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d0a8-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d0a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5d0a8-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d0a8-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5d0a8-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d0a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5d0a8-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5d0a8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5d0a8-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5d0a8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d0a8-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d0a8-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d0a8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d0a8-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d0a8-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5d0a8-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5d0a8-130">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="5d0a8-130">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="5d0a8-131">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="5d0a8-131">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="5d0a8-132">**PostQuitMessage**</span><span class="sxs-lookup"><span data-stu-id="5d0a8-132">**PostQuitMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

<span data-ttu-id="5d0a8-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5d0a8-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5d0a8-134">Windows</span><span class="sxs-lookup"><span data-stu-id="5d0a8-134">Windows</span></span>](windows.md)
</dt> </dl>

 

 
