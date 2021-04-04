---
UID: ''
title: Função de retorno de chamada LowLevelKeyboardProc
description: O sistema chama essa função toda vez que um novo evento de entrada de teclado está prestes a ser Postado em uma fila de entrada de thread.
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
ms.openlocfilehash: f33acbb6888bad97a03b610c513cbaf9c3750684
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "104007270"
---
# <a name="lowlevelkeyboardproc-function"></a><span data-ttu-id="c92e3-103">Função LowLevelKeyboardProc</span><span class="sxs-lookup"><span data-stu-id="c92e3-103">LowLevelKeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="c92e3-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="c92e3-104">Description</span></span>

<span data-ttu-id="c92e3-105">Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="c92e3-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="c92e3-106">O sistema chama essa função toda vez que um novo evento de entrada de teclado está prestes a ser Postado em uma fila de entrada de thread.</span><span class="sxs-lookup"><span data-stu-id="c92e3-106">The system calls this function every time a new keyboard input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="c92e3-107">**Observação:**  Quando essa função de retorno de chamada é chamada em resposta a uma alteração no estado de uma chave, a função de retorno de chamada é chamada antes que o estado assíncrono da chave seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="c92e3-107">**Note:**  When this callback function is called in response to a change in the state of a key, the callback function is called before the asynchronous state of the key is updated.</span></span>
<span data-ttu-id="c92e3-108">Consequentemente, o estado assíncrono da chave não pode ser determinado chamando [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) de dentro da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c92e3-108">Consequently, the asynchronous state of the key cannot be determined by calling [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) from within the callback function.</span></span>

<span data-ttu-id="c92e3-109">O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c92e3-109">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="c92e3-110">**LowLevelKeyboardProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c92e3-110">**LowLevelKeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="c92e3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c92e3-111">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="c92e3-112">código [in]</span><span class="sxs-lookup"><span data-stu-id="c92e3-112">code [in]</span></span>

<span data-ttu-id="c92e3-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="c92e3-113">Type: **int**</span></span>

<span data-ttu-id="c92e3-114">Um código que o procedimento de gancho usa para determinar como processar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c92e3-114">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="c92e3-115">Se *nCode* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="c92e3-115">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="c92e3-116">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c92e3-116">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="c92e3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c92e3-117">Value</span></span> | <span data-ttu-id="c92e3-118">Significado</span><span class="sxs-lookup"><span data-stu-id="c92e3-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="c92e3-119">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="c92e3-119">**HC_ACTION** 0</span></span> | <span data-ttu-id="c92e3-120">Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem de teclado.</span><span class="sxs-lookup"><span data-stu-id="c92e3-120">The *wParam* and *lParam* parameters contain information about a keyboard message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="c92e3-121">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="c92e3-121">wParam [in]</span></span>

<span data-ttu-id="c92e3-122">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="c92e3-122">Type: **WPARAM**</span></span>

<span data-ttu-id="c92e3-123">O identificador da mensagem do teclado.</span><span class="sxs-lookup"><span data-stu-id="c92e3-123">The identifier of the keyboard message.</span></span>
<span data-ttu-id="c92e3-124">Esse parâmetro pode ser uma das seguintes mensagens: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)ou [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span><span class="sxs-lookup"><span data-stu-id="c92e3-124">This parameter can be one of the following messages: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown), or [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="c92e3-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="c92e3-125">lParam [in]</span></span>

<span data-ttu-id="c92e3-126">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="c92e3-126">Type: **LPARAM**</span></span>

<span data-ttu-id="c92e3-127">Um ponteiro para uma estrutura [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) .</span><span class="sxs-lookup"><span data-stu-id="c92e3-127">A pointer to a [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="c92e3-128">Retornos</span><span class="sxs-lookup"><span data-stu-id="c92e3-128">Returns</span></span>

<span data-ttu-id="c92e3-129">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c92e3-129">Type: **LRESULT**</span></span>

<span data-ttu-id="c92e3-130">Se *nCode* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="c92e3-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="c92e3-131">Se *nCode* for maior ou igual a zero, e o procedimento de gancho não processar a mensagem, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_KEYBOARD_LL](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.</span><span class="sxs-lookup"><span data-stu-id="c92e3-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="c92e3-132">Se o procedimento de gancho tiver processado a mensagem, ele poderá retornar um valor diferente de zero para impedir que o sistema passe a mensagem para o restante da cadeia de conexão ou o procedimento de janela de destino.</span><span class="sxs-lookup"><span data-stu-id="c92e3-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c92e3-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="c92e3-133">Remarks</span></span>

<span data-ttu-id="c92e3-134">Um aplicativo instala o procedimento de gancho especificando o tipo de gancho **WH_KEYBOARD_LL** e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="c92e3-134">An application installs the hook procedure by specifying the **WH_KEYBOARD_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="c92e3-135">Esse gancho é chamado no contexto do thread que o instalou.</span><span class="sxs-lookup"><span data-stu-id="c92e3-135">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="c92e3-136">A chamada é feita enviando uma mensagem para o thread que instalou o gancho.</span><span class="sxs-lookup"><span data-stu-id="c92e3-136">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="c92e3-137">Portanto, o thread que instalou o gancho deve ter um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c92e3-137">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="c92e3-138">A entrada do teclado pode vir do driver de teclado local ou de chamadas para a função [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) .</span><span class="sxs-lookup"><span data-stu-id="c92e3-138">The keyboard input can come from the local keyboard driver or from calls to the [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) function.</span></span>
<span data-ttu-id="c92e3-139">Se a entrada vier de uma chamada para **keybd_event**, a entrada era "injetada".</span><span class="sxs-lookup"><span data-stu-id="c92e3-139">If the input comes from a call to **keybd_event**, the input was "injected".</span></span>
<span data-ttu-id="c92e3-140">No entanto, o gancho de WH_KEYBOARD_LL não é injetado em outro processo.</span><span class="sxs-lookup"><span data-stu-id="c92e3-140">However, the WH_KEYBOARD_LL hook is not injected into another process.</span></span>
<span data-ttu-id="c92e3-141">Em vez disso, o contexto volta para o processo que instalou o gancho e ele é chamado em seu contexto original.</span><span class="sxs-lookup"><span data-stu-id="c92e3-141">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="c92e3-142">Em seguida, o contexto volta para o aplicativo que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="c92e3-142">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="c92e3-143">O procedimento de gancho deve processar uma mensagem em menos tempo que a entrada de dados especificada no valor **LowLevelHooksTimeout** na seguinte chave do registro: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="c92e3-143">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="c92e3-144">O valor está em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="c92e3-144">The value is in milliseconds.</span></span>
<span data-ttu-id="c92e3-145">Se o procedimento de gancho atingir o tempo limite, o sistema passará a mensagem para o próximo gancho.</span><span class="sxs-lookup"><span data-stu-id="c92e3-145">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="c92e3-146">No entanto, no Windows 7 e posterior, o gancho é removido silenciosamente sem ser chamado.</span><span class="sxs-lookup"><span data-stu-id="c92e3-146">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="c92e3-147">Não há como o aplicativo saber se o gancho foi removido.</span><span class="sxs-lookup"><span data-stu-id="c92e3-147">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="c92e3-148">Observação: os ganchos de depuração não podem controlar esse tipo de ganchos de teclado de nível baixo.</span><span class="sxs-lookup"><span data-stu-id="c92e3-148">Note:  Debug hooks cannot track this type of low level keyboard hooks.</span></span>
<span data-ttu-id="c92e3-149">Se o aplicativo precisar usar ganchos de nível baixo, ele deverá executar os ganchos em um thread dedicado que passa o trabalho para um thread de trabalho e retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c92e3-149">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="c92e3-150">Na maioria dos casos em que o aplicativo precisa usar ganchos de nível baixo, ele deve monitorar a entrada bruta em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c92e3-150">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="c92e3-151">Isso ocorre porque a entrada bruta pode monitorar de forma assíncrona as mensagens de mouse e teclado que são destinadas a outros threads com mais eficiência do que os ganchos de nível baixo</span><span class="sxs-lookup"><span data-stu-id="c92e3-151">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="c92e3-152">Para obter mais informações sobre a entrada bruta, consulte [RAW Input](/windows/desktop/inputdev/raw-input).</span><span class="sxs-lookup"><span data-stu-id="c92e3-152">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="c92e3-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="c92e3-153">See also</span></span>

[<span data-ttu-id="c92e3-154">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="c92e3-154">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="c92e3-155">KBDLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="c92e3-155">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="c92e3-156">keybd_event</span><span class="sxs-lookup"><span data-stu-id="c92e3-156">keybd_event</span></span>](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[<span data-ttu-id="c92e3-157">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="c92e3-157">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="c92e3-158">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="c92e3-158">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="c92e3-159">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="c92e3-159">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="c92e3-160">WM_SYSKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="c92e3-160">WM_SYSKEYDOWN</span></span>](/windows/desktop/inputdev/wm-syskeydown)

[<span data-ttu-id="c92e3-161">WM_SYSKEYUP</span><span class="sxs-lookup"><span data-stu-id="c92e3-161">WM_SYSKEYUP</span></span>](/windows/desktop/inputdev/wm-syskeyup)

[<span data-ttu-id="c92e3-162">Ganchos</span><span class="sxs-lookup"><span data-stu-id="c92e3-162">Hooks</span></span>](hooks.md)

[<span data-ttu-id="c92e3-163">Sobre ganchos</span><span class="sxs-lookup"><span data-stu-id="c92e3-163">About Hooks</span></span>](about-hooks.md)
