---
description: Enviado a um aplicativo pelo IME para notificar o aplicativo de uma versão de chave e manter a ordem das mensagens. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: Mensagem de WM_IME_KEYUP (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813081"
---
# <a name="wm_ime_keyup-message"></a><span data-ttu-id="6e826-104">\_Mensagem KEYUP IME do WM \_</span><span class="sxs-lookup"><span data-stu-id="6e826-104">WM\_IME\_KEYUP message</span></span>

<span data-ttu-id="6e826-105">Enviado a um aplicativo pelo IME para notificar o aplicativo de uma versão de chave e manter a ordem das mensagens.</span><span class="sxs-lookup"><span data-stu-id="6e826-105">Sent to an application by the IME to notify the application of a key release and to keep message order.</span></span> <span data-ttu-id="6e826-106">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6e826-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="6e826-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e826-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e826-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6e826-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6e826-109">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="6e826-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="6e826-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e826-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e826-111">Código de chave virtual da chave.</span><span class="sxs-lookup"><span data-stu-id="6e826-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="6e826-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e826-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e826-113">Contagem de repetição, código de verificação, sinalizador de chave estendida, código de contexto, sinalizador de estado de chave anterior e sinalizador de estado de transição, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="6e826-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown below.</span></span>



| <span data-ttu-id="6e826-114">bit</span><span class="sxs-lookup"><span data-stu-id="6e826-114">Bit</span></span>   | <span data-ttu-id="6e826-115">Significado</span><span class="sxs-lookup"><span data-stu-id="6e826-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6e826-116">0-15</span><span class="sxs-lookup"><span data-stu-id="6e826-116">0-15</span></span>  | <span data-ttu-id="6e826-117">Contagem de repetições.</span><span class="sxs-lookup"><span data-stu-id="6e826-117">Repeat count.</span></span> <span data-ttu-id="6e826-118">Esse valor é sempre 1.</span><span class="sxs-lookup"><span data-stu-id="6e826-118">This value is always 1.</span></span>                                       |
| <span data-ttu-id="6e826-119">16-23</span><span class="sxs-lookup"><span data-stu-id="6e826-119">16-23</span></span> | <span data-ttu-id="6e826-120">Código de verificação.</span><span class="sxs-lookup"><span data-stu-id="6e826-120">Scan code.</span></span>                                                                  |
| <span data-ttu-id="6e826-121">24</span><span class="sxs-lookup"><span data-stu-id="6e826-121">24</span></span>    | <span data-ttu-id="6e826-122">Chave estendida.</span><span class="sxs-lookup"><span data-stu-id="6e826-122">Extended key.</span></span> <span data-ttu-id="6e826-123">Esse valor será 1 se for uma chave estendida.</span><span class="sxs-lookup"><span data-stu-id="6e826-123">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="6e826-124">Caso contrário, é 0.</span><span class="sxs-lookup"><span data-stu-id="6e826-124">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="6e826-125">25-28</span><span class="sxs-lookup"><span data-stu-id="6e826-125">25-28</span></span> | <span data-ttu-id="6e826-126">Não usado.</span><span class="sxs-lookup"><span data-stu-id="6e826-126">Not used.</span></span>                                                                   |
| <span data-ttu-id="6e826-127">29</span><span class="sxs-lookup"><span data-stu-id="6e826-127">29</span></span>    | <span data-ttu-id="6e826-128">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="6e826-128">Context code.</span></span> <span data-ttu-id="6e826-129">Esse valor é sempre 0.</span><span class="sxs-lookup"><span data-stu-id="6e826-129">This value is always 0.</span></span>                                       |
| <span data-ttu-id="6e826-130">30</span><span class="sxs-lookup"><span data-stu-id="6e826-130">30</span></span>    | <span data-ttu-id="6e826-131">Estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="6e826-131">Previous key state.</span></span> <span data-ttu-id="6e826-132">Esse valor é sempre 1.</span><span class="sxs-lookup"><span data-stu-id="6e826-132">This value is always 1.</span></span>                                 |
| <span data-ttu-id="6e826-133">31</span><span class="sxs-lookup"><span data-stu-id="6e826-133">31</span></span>    | <span data-ttu-id="6e826-134">Estado de transição.</span><span class="sxs-lookup"><span data-stu-id="6e826-134">Transition state.</span></span> <span data-ttu-id="6e826-135">Esse valor é sempre 1.</span><span class="sxs-lookup"><span data-stu-id="6e826-135">This value is always 1.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e826-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e826-136">Return value</span></span>

<span data-ttu-id="6e826-137">Um aplicativo deve retornar 0 se processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e826-137">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e826-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e826-138">Remarks</span></span>

<span data-ttu-id="6e826-139">Um aplicativo pode processar essa mensagem ou passá-la para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  para gerar uma mensagem do [**WM \_ KEYUP**](../inputdev/wm-keyup.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="6e826-139">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYUP**](../inputdev/wm-keyup.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e826-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e826-140">Requirements</span></span>



| <span data-ttu-id="6e826-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e826-141">Requirement</span></span> | <span data-ttu-id="6e826-142">Valor</span><span class="sxs-lookup"><span data-stu-id="6e826-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e826-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e826-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6e826-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e826-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6e826-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e826-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6e826-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e826-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e826-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6e826-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e826-148"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e826-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e826-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e826-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e826-150">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="6e826-150">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6e826-151">Mensagens do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="6e826-151">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
