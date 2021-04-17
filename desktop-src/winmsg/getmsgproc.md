---
UID: ''
title: Função de retorno de chamada GetMsgProc
description: O sistema chama essa função quando uma função de mensagem recebe uma mensagem de uma fila de mensagens do aplicativo.
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
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "105760961"
---
# <a name="getmsgproc-function"></a><span data-ttu-id="3eac5-103">Função GetMsgProc</span><span class="sxs-lookup"><span data-stu-id="3eac5-103">GetMsgProc function</span></span>

## <a name="-description"></a><span data-ttu-id="3eac5-104">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3eac5-104">-description</span></span>

<span data-ttu-id="3eac5-105">Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="3eac5-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span> <span data-ttu-id="3eac5-106">O sistema chama essa função sempre que a função [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) recuperou uma mensagem de uma fila de mensagens do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3eac5-106">The system calls this function whenever the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function has retrieved a message from an application message queue.</span></span>
<span data-ttu-id="3eac5-107">Antes de retornar a mensagem recuperada para o chamador, o sistema passa a mensagem para o procedimento de gancho.</span><span class="sxs-lookup"><span data-stu-id="3eac5-107">Before returning the retrieved message to the caller, the system passes the message to the hook procedure.</span></span>

<span data-ttu-id="3eac5-108">O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="3eac5-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="3eac5-109">**GetMsgProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3eac5-109">**GetMsgProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a><span data-ttu-id="3eac5-110">-parâmetros</span><span class="sxs-lookup"><span data-stu-id="3eac5-110">-parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="3eac5-111">código [in]</span><span class="sxs-lookup"><span data-stu-id="3eac5-111">code [in]</span></span>

<span data-ttu-id="3eac5-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3eac5-112">Type: **int**</span></span>

<span data-ttu-id="3eac5-113">Especifica se o procedimento de gancho deve processar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3eac5-113">Specifies whether the hook procedure must process the message.</span></span>
<span data-ttu-id="3eac5-114">Se o *código* for **HC_ACTION**, o procedimento de gancho deverá processar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3eac5-114">If *code* is **HC_ACTION**, the hook procedure must process the message.</span></span>
<span data-ttu-id="3eac5-115">Se o *código* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="3eac5-115">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>

### <a name="wparam-in"></a><span data-ttu-id="3eac5-116">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="3eac5-116">wParam [in]</span></span>

<span data-ttu-id="3eac5-117">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="3eac5-117">Type: **WPARAM**</span></span>

<span data-ttu-id="3eac5-118">Especifica se a mensagem foi removida da fila.</span><span class="sxs-lookup"><span data-stu-id="3eac5-118">Specifies whether the message has been removed from the queue.</span></span>
<span data-ttu-id="3eac5-119">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3eac5-119">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="3eac5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3eac5-120">Value</span></span> | <span data-ttu-id="3eac5-121">Significado</span><span class="sxs-lookup"><span data-stu-id="3eac5-121">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="3eac5-122">**PM_NOREMOVE** 0x0000</span><span class="sxs-lookup"><span data-stu-id="3eac5-122">**PM_NOREMOVE** 0x0000</span></span> | <span data-ttu-id="3eac5-123">A mensagem não foi removida da fila.</span><span class="sxs-lookup"><span data-stu-id="3eac5-123">The message has not been removed from the queue.</span></span> <span data-ttu-id="3eac5-124">(Um aplicativo chamado a função **PeekMessage** , especificando o sinalizador **PM_NOREMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="3eac5-124">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |
| <span data-ttu-id="3eac5-125">**PM_REMOVE** 0x0001</span><span class="sxs-lookup"><span data-stu-id="3eac5-125">**PM_REMOVE** 0x0001</span></span> | <span data-ttu-id="3eac5-126">A mensagem foi removida da fila.</span><span class="sxs-lookup"><span data-stu-id="3eac5-126">The message has been removed from the queue.</span></span> <span data-ttu-id="3eac5-127">(Um aplicativo chamado **GetMessage** ou ele chamou a função  **PeekMessage** , especificando o sinalizador **PM_REMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="3eac5-127">(An application called **GetMessage**, or it called the  **PeekMessage** function, specifying the **PM_REMOVE** flag.)</span></span>|

### <a name="lparam-in"></a><span data-ttu-id="3eac5-128">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="3eac5-128">lParam [in]</span></span>

<span data-ttu-id="3eac5-129">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="3eac5-129">Type: **LPARAM**</span></span>

<span data-ttu-id="3eac5-130">Um ponteiro para uma estrutura de [msg](/windows/desktop/api/winuser/ns-winuser-msg) que contém detalhes sobre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3eac5-130">A pointer to an [MSG](/windows/desktop/api/winuser/ns-winuser-msg) structure that contains details about the message.</span></span>

## <a name="-returns"></a><span data-ttu-id="3eac5-131">-Retorna</span><span class="sxs-lookup"><span data-stu-id="3eac5-131">-returns</span></span>

<span data-ttu-id="3eac5-132">Se o *código* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span><span class="sxs-lookup"><span data-stu-id="3eac5-132">If *code* is less than zero, the hook procedure must return the value returned by [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span></span>

<span data-ttu-id="3eac5-133">Se o *código* for maior ou igual a zero, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_GETMESSAGE](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.</span><span class="sxs-lookup"><span data-stu-id="3eac5-133">If *code* is greater than or equal to zero, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_GETMESSAGE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="3eac5-134">Se o procedimento de gancho não chamar **CallNextHookEx**, o valor de retorno deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="3eac5-134">If the hook procedure does not call **CallNextHookEx**, the return value should be zero.</span></span>

## <a name="-remarks"></a><span data-ttu-id="3eac5-135">-Comentários</span><span class="sxs-lookup"><span data-stu-id="3eac5-135">-remarks</span></span>

<span data-ttu-id="3eac5-136">O procedimento de gancho **GetMsgProc** pode examinar ou modificar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="3eac5-136">The **GetMsgProc** hook procedure can examine or modify the message.</span></span>
<span data-ttu-id="3eac5-137">Depois que o procedimento de gancho retorna o controle para o sistema, a função **GetMessage** ou **PeekMessage** retorna a mensagem, juntamente com quaisquer modificações, para o aplicativo que o chamou originalmente.</span><span class="sxs-lookup"><span data-stu-id="3eac5-137">After the hook procedure returns control to the system, the **GetMessage** or **PeekMessage** function returns the message, along with any modifications, to the application that originally called it.</span></span>

<span data-ttu-id="3eac5-138">Um aplicativo instala esse procedimento de gancho especificando o tipo de gancho **WH_GETMESSAGE** e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="3eac5-138">An application installs this hook procedure by specifying the **WH_GETMESSAGE** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="3eac5-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="3eac5-139">See also</span></span>

[<span data-ttu-id="3eac5-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="3eac5-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="3eac5-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="3eac5-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="3eac5-142">MSG</span><span class="sxs-lookup"><span data-stu-id="3eac5-142">MSG</span></span>](/windows/desktop/api/winuser/ns-winuser-msg)

[<span data-ttu-id="3eac5-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="3eac5-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="3eac5-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="3eac5-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="3eac5-145">Ganchos</span><span class="sxs-lookup"><span data-stu-id="3eac5-145">Hooks</span></span>](hooks.md)
