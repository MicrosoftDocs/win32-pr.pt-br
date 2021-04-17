---
UID: ''
title: Função de retorno de chamada KeyboardProc
description: O sistema chama essa função obtém uma função de mensagem e há uma mensagem de teclado a ser processada.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "105754695"
---
# <a name="keyboardproc-function"></a><span data-ttu-id="6d30b-103">Função KeyboardProc</span><span class="sxs-lookup"><span data-stu-id="6d30b-103">KeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="6d30b-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d30b-104">Description</span></span>

<span data-ttu-id="6d30b-105">Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="6d30b-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="6d30b-106">O sistema chama essa função sempre que um aplicativo chama a função [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) e há uma mensagem de teclado ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) ou [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) a ser processada.</span><span class="sxs-lookup"><span data-stu-id="6d30b-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a keyboard message ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) or [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) to be processed.</span></span>

<span data-ttu-id="6d30b-107">O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6d30b-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="6d30b-108">**KeyboardProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6d30b-108">**KeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="6d30b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d30b-109">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="6d30b-110">código [in]</span><span class="sxs-lookup"><span data-stu-id="6d30b-110">code [in]</span></span>

<span data-ttu-id="6d30b-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="6d30b-111">Type: **int**</span></span>

<span data-ttu-id="6d30b-112">Um código que o procedimento de gancho usa para determinar como processar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d30b-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="6d30b-113">Se o *código* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="6d30b-113">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="6d30b-114">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d30b-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="6d30b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6d30b-115">Value</span></span> | <span data-ttu-id="6d30b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="6d30b-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="6d30b-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="6d30b-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="6d30b-118">Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem de pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="6d30b-118">The *wParam* and *lParam* parameters contain information about a keystroke message.</span></span> |
| <span data-ttu-id="6d30b-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="6d30b-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="6d30b-120">Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem de pressionamento de tecla e a mensagem de pressionamento de tecla não foi removida da fila de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6d30b-120">The *wParam* and *lParam* parameters contain information about a keystroke message, and the keystroke message has not been removed from the message queue.</span></span> <span data-ttu-id="6d30b-121">(Um aplicativo chamado a função **PeekMessage** , especificando o sinalizador **PM_NOREMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="6d30b-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="6d30b-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="6d30b-122">wParam [in]</span></span>

<span data-ttu-id="6d30b-123">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="6d30b-123">Type: **WPARAM**</span></span>

<span data-ttu-id="6d30b-124">O [código de chave virtual](/windows/desktop/inputdev/virtual-key-codes) da chave que gerou a mensagem de pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="6d30b-124">The [virtual-key code](/windows/desktop/inputdev/virtual-key-codes) of the key that generated the keystroke message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="6d30b-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="6d30b-125">lParam [in]</span></span>

<span data-ttu-id="6d30b-126">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="6d30b-126">Type: **LPARAM**</span></span>

<span data-ttu-id="6d30b-127">A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição.</span><span class="sxs-lookup"><span data-stu-id="6d30b-127">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span>
<span data-ttu-id="6d30b-128">Para obter mais informações sobre o parâmetro *lParam* , consulte [sinalizadores de mensagem de pressionamento de tecla](/windows/desktop/inputdev/about-keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="6d30b-128">For more information about The *lParam* parameter, see [Keystroke Message Flags](/windows/desktop/inputdev/about-keyboard-input).</span></span>
<span data-ttu-id="6d30b-129">A tabela a seguir descreve os bits desse valor.</span><span class="sxs-lookup"><span data-stu-id="6d30b-129">The following table describes the bits of this value.</span></span>

| <span data-ttu-id="6d30b-130">Bits</span><span class="sxs-lookup"><span data-stu-id="6d30b-130">Bits</span></span> | <span data-ttu-id="6d30b-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d30b-131">Description</span></span> |
|-------|---------|
| <span data-ttu-id="6d30b-132">0-15</span><span class="sxs-lookup"><span data-stu-id="6d30b-132">0-15</span></span> | <span data-ttu-id="6d30b-133">A contagem de repetição.</span><span class="sxs-lookup"><span data-stu-id="6d30b-133">The repeat count.</span></span> <span data-ttu-id="6d30b-134">O valor é o número de vezes que o pressionamento de tecla é repetido como resultado do usuário que está mantendo a chave.</span><span class="sxs-lookup"><span data-stu-id="6d30b-134">The value is the number of times the keystroke is repeated as a result of the user's holding down the key.</span></span> |
| <span data-ttu-id="6d30b-135">16-23</span><span class="sxs-lookup"><span data-stu-id="6d30b-135">16-23</span></span> | <span data-ttu-id="6d30b-136">O código de verificação.</span><span class="sxs-lookup"><span data-stu-id="6d30b-136">The scan code.</span></span> <span data-ttu-id="6d30b-137">O valor depende do OEM.</span><span class="sxs-lookup"><span data-stu-id="6d30b-137">The value depends on the OEM.</span></span> |
| <span data-ttu-id="6d30b-138">24</span><span class="sxs-lookup"><span data-stu-id="6d30b-138">24</span></span> | <span data-ttu-id="6d30b-139">Indica se a chave é uma chave estendida, como uma tecla de função ou uma chave no teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="6d30b-139">Indicates whether the key is an extended key, such as a function key or a key on the numeric keypad.</span></span> <span data-ttu-id="6d30b-140">O valor será 1 se a chave for uma chave estendida; caso contrário, será 0.</span><span class="sxs-lookup"><span data-stu-id="6d30b-140">The value is 1 if the key is an extended key; otherwise, it is 0.</span></span> |
| <span data-ttu-id="6d30b-141">25-28</span><span class="sxs-lookup"><span data-stu-id="6d30b-141">25-28</span></span> | <span data-ttu-id="6d30b-142">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6d30b-142">Reserved.</span></span> |
| <span data-ttu-id="6d30b-143">29</span><span class="sxs-lookup"><span data-stu-id="6d30b-143">29</span></span> | <span data-ttu-id="6d30b-144">O código do contexto.</span><span class="sxs-lookup"><span data-stu-id="6d30b-144">The context code.</span></span> <span data-ttu-id="6d30b-145">O valor será 1 se a tecla ALT estiver inoperante; caso contrário, será 0.</span><span class="sxs-lookup"><span data-stu-id="6d30b-145">The value is 1 if the ALT key is down; otherwise, it is 0.</span></span> |
| <span data-ttu-id="6d30b-146">30</span><span class="sxs-lookup"><span data-stu-id="6d30b-146">30</span></span> | <span data-ttu-id="6d30b-147">O estado de chave anterior.</span><span class="sxs-lookup"><span data-stu-id="6d30b-147">The previous key state.</span></span> <span data-ttu-id="6d30b-148">O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada; será 0 se a chave estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="6d30b-148">The value is 1 if the key is down before the message is sent; it is 0 if the key is up.</span></span> |
| <span data-ttu-id="6d30b-149">31</span><span class="sxs-lookup"><span data-stu-id="6d30b-149">31</span></span> | <span data-ttu-id="6d30b-150">O estado de transição.</span><span class="sxs-lookup"><span data-stu-id="6d30b-150">The transition state.</span></span> <span data-ttu-id="6d30b-151">O valor será 0 se a chave estiver sendo pressionada e 1 se estiver sendo liberada.</span><span class="sxs-lookup"><span data-stu-id="6d30b-151">The value is 0 if the key is being pressed and 1 if it is being released.</span></span> |

## <a name="returns"></a><span data-ttu-id="6d30b-152">Retornos</span><span class="sxs-lookup"><span data-stu-id="6d30b-152">Returns</span></span>

<span data-ttu-id="6d30b-153">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6d30b-153">Type: **LRESULT**</span></span>

<span data-ttu-id="6d30b-154">Se o *código* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="6d30b-154">If *code* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="6d30b-155">Se o *código* for maior ou igual a zero e o procedimento de gancho não processar a mensagem, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_KEYBOARD](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.</span><span class="sxs-lookup"><span data-stu-id="6d30b-155">If *code* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="6d30b-156">Se o procedimento de gancho tiver processado a mensagem, ele poderá retornar um valor diferente de zero para impedir que o sistema passe a mensagem para o restante da cadeia de conexão ou o procedimento de janela de destino.</span><span class="sxs-lookup"><span data-stu-id="6d30b-156">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d30b-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d30b-157">Remarks</span></span>

<span data-ttu-id="6d30b-158">Um aplicativo instala o procedimento de gancho especificando o tipo de gancho **WH_KEYBOARD** e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="6d30b-158">An application installs the hook procedure by specifying the **WH_KEYBOARD** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="6d30b-159">Esse gancho pode ser chamado no contexto do thread que o instalou.</span><span class="sxs-lookup"><span data-stu-id="6d30b-159">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="6d30b-160">A chamada é feita enviando uma mensagem para o thread que instalou o gancho.</span><span class="sxs-lookup"><span data-stu-id="6d30b-160">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="6d30b-161">Portanto, o thread que instalou o gancho deve ter um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d30b-161">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d30b-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d30b-162">See also</span></span>

[<span data-ttu-id="6d30b-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="6d30b-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="6d30b-164">GetMessage</span><span class="sxs-lookup"><span data-stu-id="6d30b-164">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="6d30b-165">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="6d30b-165">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="6d30b-166">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="6d30b-166">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="6d30b-167">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="6d30b-167">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="6d30b-168">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="6d30b-168">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="6d30b-169">Ganchos</span><span class="sxs-lookup"><span data-stu-id="6d30b-169">Hooks</span></span>](hooks.md)
