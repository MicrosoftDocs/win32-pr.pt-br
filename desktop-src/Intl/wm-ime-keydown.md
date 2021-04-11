---
description: Enviado a um aplicativo pelo IME para notificar o aplicativo de um pressionamento de tecla e para manter a ordem das mensagens. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: Mensagem de WM_IME_KEYDOWN (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3089af3c839f70e7f55895ae13158e7b2240605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164514"
---
# <a name="wm_ime_keydown-message"></a><span data-ttu-id="a1cea-104">\_Mensagem de KEYDOWN IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="a1cea-104">WM\_IME\_KEYDOWN message</span></span>

<span data-ttu-id="a1cea-105">Enviado a um aplicativo pelo IME para notificar o aplicativo de um pressionamento de tecla e para manter a ordem das mensagens.</span><span class="sxs-lookup"><span data-stu-id="a1cea-105">Sent to an application by the IME to notify the application of a key press and to keep message order.</span></span> <span data-ttu-id="a1cea-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a1cea-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
  WPARAM wParam, 
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="a1cea-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1cea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1cea-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a1cea-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a1cea-109">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="a1cea-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="a1cea-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1cea-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1cea-111">Código de chave virtual da chave.</span><span class="sxs-lookup"><span data-stu-id="a1cea-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="a1cea-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1cea-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1cea-113">Contagem de repetição, código de verificação, sinalizador de chave estendida, código de contexto, sinalizador de estado de chave anterior e sinalizador de estado de transição, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1cea-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown in the following table.</span></span>



| <span data-ttu-id="a1cea-114">bit</span><span class="sxs-lookup"><span data-stu-id="a1cea-114">Bit</span></span>   | <span data-ttu-id="a1cea-115">Significado</span><span class="sxs-lookup"><span data-stu-id="a1cea-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="a1cea-116">0-15</span><span class="sxs-lookup"><span data-stu-id="a1cea-116">0-15</span></span>  | <span data-ttu-id="a1cea-117">Contagem de repetições.</span><span class="sxs-lookup"><span data-stu-id="a1cea-117">Repeat count.</span></span>                                                               |
| <span data-ttu-id="a1cea-118">16-23</span><span class="sxs-lookup"><span data-stu-id="a1cea-118">16-23</span></span> | <span data-ttu-id="a1cea-119">Código de verificação.</span><span class="sxs-lookup"><span data-stu-id="a1cea-119">Scan code.</span></span>                                                                  |
| <span data-ttu-id="a1cea-120">24</span><span class="sxs-lookup"><span data-stu-id="a1cea-120">24</span></span>    | <span data-ttu-id="a1cea-121">Chave estendida.</span><span class="sxs-lookup"><span data-stu-id="a1cea-121">Extended key.</span></span> <span data-ttu-id="a1cea-122">Esse valor será 1 se for uma chave estendida.</span><span class="sxs-lookup"><span data-stu-id="a1cea-122">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="a1cea-123">Caso contrário, é 0.</span><span class="sxs-lookup"><span data-stu-id="a1cea-123">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="a1cea-124">25-28</span><span class="sxs-lookup"><span data-stu-id="a1cea-124">25-28</span></span> | <span data-ttu-id="a1cea-125">Não usado.</span><span class="sxs-lookup"><span data-stu-id="a1cea-125">Not used.</span></span>                                                                   |
| <span data-ttu-id="a1cea-126">29</span><span class="sxs-lookup"><span data-stu-id="a1cea-126">29</span></span>    | <span data-ttu-id="a1cea-127">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="a1cea-127">Context code.</span></span> <span data-ttu-id="a1cea-128">Esse valor é sempre 0.</span><span class="sxs-lookup"><span data-stu-id="a1cea-128">This value is always 0.</span></span>                                       |
| <span data-ttu-id="a1cea-129">30</span><span class="sxs-lookup"><span data-stu-id="a1cea-129">30</span></span>    | <span data-ttu-id="a1cea-130">Estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="a1cea-130">Previous key state.</span></span> <span data-ttu-id="a1cea-131">Esse valor será 1 se a chave estiver inoperante ou 0 se estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="a1cea-131">This value is 1 if the key is down or 0 if it is up.</span></span>    |
| <span data-ttu-id="a1cea-132">31</span><span class="sxs-lookup"><span data-stu-id="a1cea-132">31</span></span>    | <span data-ttu-id="a1cea-133">Estado de transição.</span><span class="sxs-lookup"><span data-stu-id="a1cea-133">Transition state.</span></span> <span data-ttu-id="a1cea-134">Esse valor é sempre 0.</span><span class="sxs-lookup"><span data-stu-id="a1cea-134">This value is always 0.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1cea-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1cea-135">Return value</span></span>

<span data-ttu-id="a1cea-136">Um aplicativo deve retornar 0 se processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="a1cea-136">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1cea-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1cea-137">Remarks</span></span>

<span data-ttu-id="a1cea-138">Um aplicativo pode processar essa mensagem ou passá-la para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para gerar uma mensagem do [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="a1cea-138">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1cea-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1cea-139">Requirements</span></span>



| <span data-ttu-id="a1cea-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1cea-140">Requirement</span></span> | <span data-ttu-id="a1cea-141">Valor</span><span class="sxs-lookup"><span data-stu-id="a1cea-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1cea-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1cea-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a1cea-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a1cea-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a1cea-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1cea-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a1cea-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a1cea-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a1cea-146">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a1cea-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1cea-147"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1cea-147"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1cea-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1cea-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1cea-149">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cea-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="a1cea-150">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="a1cea-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
