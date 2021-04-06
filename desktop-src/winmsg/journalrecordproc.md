---
UID: ''
title: Função de retorno de chamada JournalRecordProc
description: A função registra as mensagens que o sistema remove da fila de mensagens do sistema.
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
ms.openlocfilehash: bc255441ca82c86542dd8dd4729564122df6c719
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "103917093"
---
# <a name="journalrecordproc-function"></a><span data-ttu-id="c3a1c-103">Função JournalRecordProc</span><span class="sxs-lookup"><span data-stu-id="c3a1c-103">JournalRecordProc function</span></span>

## <a name="description"></a><span data-ttu-id="c3a1c-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3a1c-104">Description</span></span>

<span data-ttu-id="c3a1c-105">Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="c3a1c-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="c3a1c-106">A função registra as mensagens que o sistema remove da fila de mensagens do sistema.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-106">The function records messages the system removes from the system message queue.</span></span>
<span data-ttu-id="c3a1c-107">Posteriormente, um aplicativo pode usar um procedimento de gancho [JournalPlaybackProc](journalplaybackproc.md) para reproduzir as mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-107">Later, an application can use a [JournalPlaybackProc](journalplaybackproc.md) hook procedure to play back the messages.</span></span>

<span data-ttu-id="c3a1c-108">O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="c3a1c-109">**JournalRecordProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-109">**JournalRecordProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="c3a1c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3a1c-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="c3a1c-111">código [in]</span><span class="sxs-lookup"><span data-stu-id="c3a1c-111">code [in]</span></span>

<span data-ttu-id="c3a1c-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="c3a1c-112">Type: **int**</span></span>

<span data-ttu-id="c3a1c-113">Especifica como processar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-113">Specifies how to process the message.</span></span>
<span data-ttu-id="c3a1c-114">Se o *código* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="c3a1c-115">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="c3a1c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c3a1c-116">Value</span></span> | <span data-ttu-id="c3a1c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="c3a1c-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="c3a1c-118">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="c3a1c-118">**HC_ACTION** 0</span></span> | <span data-ttu-id="c3a1c-119">O parâmetro *lParam* é um ponteiro para uma estrutura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) que contém informações sobre uma mensagem removida da fila do sistema.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-119">The *lParam* parameter is a pointer to an [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure containing information about a message removed from the system queue.</span></span> <span data-ttu-id="c3a1c-120">O procedimento de gancho deve registrar o conteúdo da estrutura copiando-os para um buffer ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-120">The hook procedure must record the contents of the structure by copying them to a buffer or file.</span></span> |
| <span data-ttu-id="c3a1c-121">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="c3a1c-121">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="c3a1c-122">Uma caixa de diálogo modal do sistema foi destruída.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-122">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="c3a1c-123">O procedimento de gancho deve retomar a gravação.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-123">The hook procedure must resume recording.</span></span> |
| <span data-ttu-id="c3a1c-124">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="c3a1c-124">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="c3a1c-125">Uma caixa de diálogo modal do sistema está sendo exibida.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-125">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="c3a1c-126">Até que a caixa de diálogo seja destruída, o procedimento de gancho deve parar de gravar.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-126">Until the dialog box is destroyed, the hook procedure must stop recording.</span></span> |

### <a name="wparam"></a><span data-ttu-id="c3a1c-127">wParam</span><span class="sxs-lookup"><span data-stu-id="c3a1c-127">wParam</span></span>

<span data-ttu-id="c3a1c-128">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="c3a1c-128">Type: **WPARAM**</span></span>

<span data-ttu-id="c3a1c-129">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-129">This parameter is not used.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="c3a1c-130">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="c3a1c-130">lParam [in]</span></span>

<span data-ttu-id="c3a1c-131">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="c3a1c-131">Type: **LPARAM**</span></span>

<span data-ttu-id="c3a1c-132">Um ponteiro para uma estrutura **EVENTMSG** que contém a mensagem a ser registrada.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-132">A pointer to an **EVENTMSG** structure that contains the message to be recorded.</span></span>

## <a name="returns"></a><span data-ttu-id="c3a1c-133">Retornos</span><span class="sxs-lookup"><span data-stu-id="c3a1c-133">Returns</span></span>

<span data-ttu-id="c3a1c-134">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c3a1c-134">Type: **LRESULT**</span></span>

<span data-ttu-id="c3a1c-135">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-135">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a1c-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3a1c-136">Remarks</span></span>

<span data-ttu-id="c3a1c-137">Um procedimento de gancho **JournalRecordProc** deve copiar, mas não modificar as mensagens.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-137">A **JournalRecordProc** hook procedure must copy but not modify the messages.</span></span>
<span data-ttu-id="c3a1c-138">Depois que o procedimento de gancho retorna o controle para o sistema, a mensagem continua a ser processada.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-138">After the hook procedure returns control to the system, the message continues to be processed.</span></span>

<span data-ttu-id="c3a1c-139">Instale o procedimento de gancho **JournalRecordProc** especificando o tipo de [WH_JOURNALRECORD](about-hooks.md) e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="c3a1c-139">Install the **JournalRecordProc** hook procedure by specifying the [WH_JOURNALRECORD](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="c3a1c-140">Um procedimento de gancho **JournalRecordProc** não precisa residir em uma biblioteca de vínculo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-140">A **JournalRecordProc** hook procedure does not need to live in a dynamic-link library.</span></span>
<span data-ttu-id="c3a1c-141">Um procedimento de gancho **JournalRecordProc** pode residir no próprio aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-141">A **JournalRecordProc** hook procedure can live in the application itself.</span></span>

<span data-ttu-id="c3a1c-142">Ao contrário da maioria dos outros procedimentos de gancho global, os procedimentos de gancho **JournalRecordProc** e [JournalPlaybackProc](journalplaybackproc.md) são sempre chamados no contexto do thread que define o gancho.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-142">Unlike most other global hook procedures, the **JournalRecordProc** and [JournalPlaybackProc](journalplaybackproc.md) hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="c3a1c-143">Um aplicativo que instalou um procedimento de gancho **JournalRecordProc** deve observar o código de chave virtual [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) (que é implementado como a combinação de teclas Ctrl + Break na maioria dos teclados).</span><span class="sxs-lookup"><span data-stu-id="c3a1c-143">An application that has installed a **JournalRecordProc** hook procedure should watch for the [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) virtual key code (which is implemented as the CTRL+BREAK key combination on most keyboards).</span></span>
<span data-ttu-id="c3a1c-144">Esse código de chave virtual deve ser interpretado pelo aplicativo como um sinal que o usuário deseja parar a gravação do diário.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-144">This virtual key code should be interpreted by the application as a signal that the user wishes to stop journal recording.</span></span>
<span data-ttu-id="c3a1c-145">O aplicativo deve responder encerrando a sequência de gravação e removendo o procedimento de gancho **JournalRecordProc** .</span><span class="sxs-lookup"><span data-stu-id="c3a1c-145">The application should respond by ending the recording sequence and removing the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="c3a1c-146">A remoção é importante.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-146">Removal is important.</span></span>
<span data-ttu-id="c3a1c-147">Ele impede que um aplicativo de registro em log bloqueie o sistema ao travar dentro de um procedimento de gancho.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-147">It prevents a journaling application from locking up the system by hanging inside a hook procedure.</span></span>

<span data-ttu-id="c3a1c-148">Essa função como um sinal para parar a gravação de journl significa que uma combinação de teclas CTRL + BREAK não pode ser gravada.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-148">This role as a signal to stop journl recording means that a CTRL+BREAK key combination cannot itself be recorded.</span></span>
<span data-ttu-id="c3a1c-149">Como a combinação de teclas CTRL + C não tem nenhuma função como um sinal de diário, ela pode ser registrada.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-149">Since the CTRL+C key combination has no such role as a journaling signal, it can be recorded.</span></span>
<span data-ttu-id="c3a1c-150">Há duas outras combinações de teclas que não podem ser gravadas: CTRL + ESC e CTRL + ALT + DEL.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-150">There are two other key combinations that cannot be recorded: CTRL+ESC and CTRL+ALT+DEL.</span></span>
<span data-ttu-id="c3a1c-151">Essas duas combinações de teclas fazem com que o sistema pare todas as atividades do diário (registro ou reprodução), remova todos os ganchos do diário e poste uma mensagem de [WM_CANCELJOURNAL](wm-canceljournal.md) no aplicativo de registro em log.</span><span class="sxs-lookup"><span data-stu-id="c3a1c-151">Those two key combinations cause the system to stop all journaling activities (record or playback), remove all journaling hooks, and post a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3a1c-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3a1c-152">See also</span></span>

[<span data-ttu-id="c3a1c-153">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="c3a1c-153">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="c3a1c-154">EVENTMSG</span><span class="sxs-lookup"><span data-stu-id="c3a1c-154">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="c3a1c-155">JournalPlaybackProc</span><span class="sxs-lookup"><span data-stu-id="c3a1c-155">JournalPlaybackProc</span></span>](journalplaybackproc.md)

[<span data-ttu-id="c3a1c-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="c3a1c-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="c3a1c-157">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="c3a1c-157">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="c3a1c-158">Ganchos</span><span class="sxs-lookup"><span data-stu-id="c3a1c-158">Hooks</span></span>](hooks.md)
