---
UID: ''
title: Função de retorno de chamada MouseProc
description: O sistema chama essa função quando um aplicativo chama uma função de mensagem e há uma mensagem do mouse a ser processada.
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "105764487"
---
# <a name="mouseproc-function"></a><span data-ttu-id="b63e9-103">Função MouseProc</span><span class="sxs-lookup"><span data-stu-id="b63e9-103">MouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="b63e9-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="b63e9-104">Description</span></span>

<span data-ttu-id="b63e9-105">Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="b63e9-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="b63e9-106">O sistema chama essa função sempre que um aplicativo chama a função [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) e há uma mensagem do mouse a ser processada.</span><span class="sxs-lookup"><span data-stu-id="b63e9-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a mouse message to be processed.</span></span>

<span data-ttu-id="b63e9-107">O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b63e9-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="b63e9-108">**MouseProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b63e9-108">**MouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="b63e9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b63e9-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="b63e9-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="b63e9-110">nCode [in]</span></span>

<span data-ttu-id="b63e9-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="b63e9-111">Type: **int**</span></span>

<span data-ttu-id="b63e9-112">Um código que o procedimento de gancho usa para determinar como processar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="b63e9-112">A code that the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="b63e9-113">Se *nCode* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="b63e9-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="b63e9-114">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b63e9-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="b63e9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b63e9-115">Value</span></span> | <span data-ttu-id="b63e9-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b63e9-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="b63e9-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="b63e9-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="b63e9-118">Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem do mouse.</span><span class="sxs-lookup"><span data-stu-id="b63e9-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |
| <span data-ttu-id="b63e9-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="b63e9-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="b63e9-120">Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem do mouse e a mensagem do mouse não foi removida da fila de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b63e9-120">The *wParam* and *lParam* parameters contain information about a mouse message, and the mouse message has not been removed from the message queue.</span></span> <span data-ttu-id="b63e9-121">(Um aplicativo chamado a função **PeekMessage** , especificando o sinalizador **PM_NOREMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="b63e9-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="b63e9-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="b63e9-122">wParam [in]</span></span>

<span data-ttu-id="b63e9-123">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="b63e9-123">Type: **WPARAM**</span></span>

<span data-ttu-id="b63e9-124">O identificador da mensagem do mouse.</span><span class="sxs-lookup"><span data-stu-id="b63e9-124">The identifier of the mouse message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="b63e9-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="b63e9-125">lParam [in]</span></span>

<span data-ttu-id="b63e9-126">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="b63e9-126">Type: **LPARAM**</span></span>

<span data-ttu-id="b63e9-127">Um ponteiro para uma estrutura [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) .</span><span class="sxs-lookup"><span data-stu-id="b63e9-127">A pointer to a [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="b63e9-128">Retornos</span><span class="sxs-lookup"><span data-stu-id="b63e9-128">Returns</span></span>

<span data-ttu-id="b63e9-129">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b63e9-129">Type: **LRESULT**</span></span>

<span data-ttu-id="b63e9-130">Se *nCode* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="b63e9-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="b63e9-131">Se *nCode* for maior ou igual a zero, e o procedimento de gancho não processar a mensagem, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_MOUSE](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.</span><span class="sxs-lookup"><span data-stu-id="b63e9-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="b63e9-132">Se o procedimento de gancho tiver processado a mensagem, ele poderá retornar um valor diferente de zero para impedir que o sistema passe a mensagem para o procedimento de janela de destino.</span><span class="sxs-lookup"><span data-stu-id="b63e9-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b63e9-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="b63e9-133">Remarks</span></span>

<span data-ttu-id="b63e9-134">Um aplicativo instala o procedimento de gancho especificando o tipo de gancho WH_MOUSE e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="b63e9-134">An application installs the hook procedure by specifying the WH_MOUSE hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="b63e9-135">O procedimento de gancho não deve instalar uma função de retorno de chamada [WH_JOURNALPLAYBACK](about-hooks.md) .</span><span class="sxs-lookup"><span data-stu-id="b63e9-135">The hook procedure must not install a [WH_JOURNALPLAYBACK](about-hooks.md) callback function.</span></span>

<span data-ttu-id="b63e9-136">Esse gancho pode ser chamado no contexto do thread que o instalou.</span><span class="sxs-lookup"><span data-stu-id="b63e9-136">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="b63e9-137">A chamada é feita enviando uma mensagem para o thread que instalou o gancho.</span><span class="sxs-lookup"><span data-stu-id="b63e9-137">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="b63e9-138">Portanto, o thread que instalou o gancho deve ter um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b63e9-138">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="b63e9-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b63e9-139">See also</span></span>

[<span data-ttu-id="b63e9-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="b63e9-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="b63e9-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="b63e9-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="b63e9-142">MOUSEHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="b63e9-142">MOUSEHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[<span data-ttu-id="b63e9-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="b63e9-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="b63e9-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="b63e9-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="b63e9-145">Ganchos</span><span class="sxs-lookup"><span data-stu-id="b63e9-145">Hooks</span></span>](hooks.md)

[<span data-ttu-id="b63e9-146">Sobre ganchos</span><span class="sxs-lookup"><span data-stu-id="b63e9-146">About Hooks</span></span>](about-hooks.md)
