---
UID: ''
title: Função de retorno de chamada LowLevelMouseProc
description: O sistema chama essa função toda vez que um novo evento de entrada do mouse está prestes a ser Postado em uma fila de entrada de thread.
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
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/26/2020
ms.locfileid: "104008551"
---
# <a name="lowlevelmouseproc-function"></a><span data-ttu-id="65ffd-103">Função LowLevelMouseProc</span><span class="sxs-lookup"><span data-stu-id="65ffd-103">LowLevelMouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="65ffd-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="65ffd-104">Description</span></span>

<span data-ttu-id="65ffd-105">Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="65ffd-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="65ffd-106">O sistema chama essa função toda vez que um novo evento de entrada do mouse está prestes a ser Postado em uma fila de entrada de thread.</span><span class="sxs-lookup"><span data-stu-id="65ffd-106">The system calls this function every time a new mouse input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="65ffd-107">O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="65ffd-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="65ffd-108">**LowLevelMouseProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="65ffd-108">**LowLevelMouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="65ffd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65ffd-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="65ffd-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="65ffd-110">nCode [in]</span></span>

<span data-ttu-id="65ffd-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="65ffd-111">Type: **int**</span></span>

<span data-ttu-id="65ffd-112">Um código que o procedimento de gancho usa para determinar como processar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="65ffd-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="65ffd-113">Se *nCode* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="65ffd-114">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="65ffd-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="65ffd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="65ffd-115">Value</span></span> | <span data-ttu-id="65ffd-116">Significado</span><span class="sxs-lookup"><span data-stu-id="65ffd-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="65ffd-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="65ffd-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="65ffd-118">Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem do mouse.</span><span class="sxs-lookup"><span data-stu-id="65ffd-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="65ffd-119">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="65ffd-119">wParam [in]</span></span>

<span data-ttu-id="65ffd-120">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="65ffd-120">Type: **WPARAM**</span></span>

<span data-ttu-id="65ffd-121">O identificador da mensagem do mouse.</span><span class="sxs-lookup"><span data-stu-id="65ffd-121">The identifier of the mouse message.</span></span>
<span data-ttu-id="65ffd-122">Esse parâmetro pode ser uma das seguintes mensagens: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) ou [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span><span class="sxs-lookup"><span data-stu-id="65ffd-122">This parameter can be one of the following messages: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) or [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="65ffd-123">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="65ffd-123">lParam [in]</span></span>

<span data-ttu-id="65ffd-124">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="65ffd-124">Type: **LPARAM**</span></span>

<span data-ttu-id="65ffd-125">Um ponteiro para uma estrutura [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) .</span><span class="sxs-lookup"><span data-stu-id="65ffd-125">A pointer to an [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="65ffd-126">Retornos</span><span class="sxs-lookup"><span data-stu-id="65ffd-126">Returns</span></span>

<span data-ttu-id="65ffd-127">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="65ffd-127">Type: **LRESULT**</span></span>

<span data-ttu-id="65ffd-128">Se *nCode* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-128">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="65ffd-129">Se *nCode* for maior ou igual a zero, e o procedimento de gancho não processar a mensagem, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_MOUSE_LL](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.</span><span class="sxs-lookup"><span data-stu-id="65ffd-129">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="65ffd-130">Se o procedimento de gancho tiver processado a mensagem, ele poderá retornar um valor diferente de zero para impedir que o sistema passe a mensagem para o restante da cadeia de conexão ou o procedimento de janela de destino.</span><span class="sxs-lookup"><span data-stu-id="65ffd-130">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="65ffd-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="65ffd-131">Remarks</span></span>

<span data-ttu-id="65ffd-132">Um aplicativo instala o procedimento de gancho especificando o tipo de gancho **WH_MOUSE_LL** e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="65ffd-132">An application installs the hook procedure by specifying the **WH_MOUSE_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="65ffd-133">Esse gancho é chamado no contexto do thread que o instalou.</span><span class="sxs-lookup"><span data-stu-id="65ffd-133">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="65ffd-134">A chamada é feita enviando uma mensagem para o thread que instalou o gancho.</span><span class="sxs-lookup"><span data-stu-id="65ffd-134">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="65ffd-135">Portanto, o thread que instalou o gancho deve ter um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="65ffd-135">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="65ffd-136">A entrada do mouse pode vir do driver de mouse local ou de chamadas para a função [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) .</span><span class="sxs-lookup"><span data-stu-id="65ffd-136">The mouse input can come from the local mouse driver or from calls to the [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) function.</span></span>
<span data-ttu-id="65ffd-137">Se a entrada vier de uma chamada para **mouse_event**, a entrada era "injetada".</span><span class="sxs-lookup"><span data-stu-id="65ffd-137">If the input comes from a call to **mouse_event**, the input was "injected".</span></span>
<span data-ttu-id="65ffd-138">No entanto, o gancho de **WH_MOUSE_LL** não é injetado em outro processo.</span><span class="sxs-lookup"><span data-stu-id="65ffd-138">However, the **WH_MOUSE_LL** hook is not injected into another process.</span></span>
<span data-ttu-id="65ffd-139">Em vez disso, o contexto volta para o processo que instalou o gancho e ele é chamado em seu contexto original.</span><span class="sxs-lookup"><span data-stu-id="65ffd-139">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="65ffd-140">Em seguida, o contexto volta para o aplicativo que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="65ffd-140">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="65ffd-141">O procedimento de gancho deve processar uma mensagem em menos tempo que a entrada de dados especificada no valor **LowLevelHooksTimeout** na seguinte chave do registro: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-141">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="65ffd-142">O valor está em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="65ffd-142">The value is in milliseconds.</span></span>
<span data-ttu-id="65ffd-143">Se o procedimento de gancho atingir o tempo limite, o sistema passará a mensagem para o próximo gancho.</span><span class="sxs-lookup"><span data-stu-id="65ffd-143">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="65ffd-144">No entanto, no Windows 7 e posterior, o gancho é removido silenciosamente sem ser chamado.</span><span class="sxs-lookup"><span data-stu-id="65ffd-144">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="65ffd-145">Não há como o aplicativo saber se o gancho foi removido.</span><span class="sxs-lookup"><span data-stu-id="65ffd-145">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="65ffd-146">**Observação:**  Os ganchos de depuração não podem controlar esse tipo de gancho de baixo nível do mouse.</span><span class="sxs-lookup"><span data-stu-id="65ffd-146">**Note:**  Debug hooks cannot track this type of low level mouse hooks.</span></span>
<span data-ttu-id="65ffd-147">Se o aplicativo precisar usar ganchos de nível baixo, ele deverá executar os ganchos em um thread dedicado que passa o trabalho para um thread de trabalho e retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="65ffd-147">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="65ffd-148">Na maioria dos casos em que o aplicativo precisa usar ganchos de nível baixo, ele deve monitorar a entrada bruta em vez disso.</span><span class="sxs-lookup"><span data-stu-id="65ffd-148">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="65ffd-149">Isso ocorre porque a entrada bruta pode monitorar de forma assíncrona as mensagens de mouse e teclado que são destinadas a outros threads com mais eficiência do que os ganchos de nível baixo</span><span class="sxs-lookup"><span data-stu-id="65ffd-149">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="65ffd-150">Para obter mais informações sobre a entrada bruta, consulte [RAW Input](/windows/desktop/inputdev/raw-input).</span><span class="sxs-lookup"><span data-stu-id="65ffd-150">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="65ffd-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="65ffd-151">See also</span></span>

[<span data-ttu-id="65ffd-152">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="65ffd-152">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="65ffd-153">mouse_event</span><span class="sxs-lookup"><span data-stu-id="65ffd-153">mouse_event</span></span>](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[<span data-ttu-id="65ffd-154">KBDLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="65ffd-154">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="65ffd-155">MSLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="65ffd-155">MSLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[<span data-ttu-id="65ffd-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="65ffd-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="65ffd-157">WM_LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="65ffd-157">WM_LBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-lbuttondown)

[<span data-ttu-id="65ffd-158">WM_LBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="65ffd-158">WM_LBUTTONUP</span></span>](/windows/desktop/inputdev/wm-lbuttonup)

[<span data-ttu-id="65ffd-159">WM_MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="65ffd-159">WM_MOUSEMOVE</span></span>](/windows/desktop/inputdev/wm-mousemove)

[<span data-ttu-id="65ffd-160">WM_MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="65ffd-160">WM_MOUSEWHEEL</span></span>](/windows/desktop/inputdev/wm-mousewheel)

[<span data-ttu-id="65ffd-161">WM_RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="65ffd-161">WM_RBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-rbuttondown)

[<span data-ttu-id="65ffd-162">WM_RBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="65ffd-162">WM_RBUTTONUP</span></span>](/windows/desktop/inputdev/wm-rbuttonup)

[<span data-ttu-id="65ffd-163">Ganchos</span><span class="sxs-lookup"><span data-stu-id="65ffd-163">Hooks</span></span>](hooks.md)

[<span data-ttu-id="65ffd-164">Sobre ganchos</span><span class="sxs-lookup"><span data-stu-id="65ffd-164">About Hooks</span></span>](about-hooks.md)
