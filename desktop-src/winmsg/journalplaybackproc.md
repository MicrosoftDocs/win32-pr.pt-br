---
UID: ''
title: Função de retorno de chamada JournalPlaybackProc
description: Reproduz uma série de mensagens do mouse e do teclado registradas anteriormente.
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
ms.openlocfilehash: 9bceede3cd6ab009aace4679dfb3d4d85bd37276
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "104365804"
---
# <a name="journalplaybackproc-function"></a><span data-ttu-id="e1065-103">Função JournalPlaybackProc</span><span class="sxs-lookup"><span data-stu-id="e1065-103">JournalPlaybackProc function</span></span>

## <a name="description"></a><span data-ttu-id="e1065-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1065-104">Description</span></span>

<span data-ttu-id="e1065-105">Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="e1065-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="e1065-106">Normalmente, um aplicativo usa essa função para reproduzir uma série de mensagens de mouse e teclado registradas anteriormente pelo procedimento de gancho **JournalRecordProc** .</span><span class="sxs-lookup"><span data-stu-id="e1065-106">Typically, an application uses this function to play back a series of mouse and keyboard messages recorded previously by the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="e1065-107">Desde que um procedimento de gancho **JournalPlaybackProc** esteja instalado, a entrada regular de mouse e teclado estará desabilitada.</span><span class="sxs-lookup"><span data-stu-id="e1065-107">As long as a **JournalPlaybackProc** hook procedure is installed, regular mouse and keyboard input is disabled.</span></span>

<span data-ttu-id="e1065-108">O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e1065-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="e1065-109">**JournalPlaybackProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e1065-109">**JournalPlaybackProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="e1065-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1065-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="e1065-111">código [in]</span><span class="sxs-lookup"><span data-stu-id="e1065-111">code [in]</span></span>

<span data-ttu-id="e1065-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="e1065-112">Type: **int**</span></span>

<span data-ttu-id="e1065-113">Um código que o procedimento de gancho usa para determinar como processar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e1065-113">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="e1065-114">Se o *código* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="e1065-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="e1065-115">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1065-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="e1065-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e1065-116">Value</span></span> | <span data-ttu-id="e1065-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e1065-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="e1065-118">**HC_GETNEXT** 1</span><span class="sxs-lookup"><span data-stu-id="e1065-118">**HC_GETNEXT** 1</span></span> | <span data-ttu-id="e1065-119">O procedimento de gancho deve copiar a mensagem atual do mouse ou do teclado para a estrutura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) apontada pelo parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="e1065-119">The hook procedure must copy the current mouse or keyboard message to the [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure pointed to by the *lParam* parameter.</span></span> |
| <span data-ttu-id="e1065-120">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="e1065-120">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="e1065-121">Um aplicativo chamou a função [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) com wRemoveMsg definido como **PM_NOREMOVE**, indicando que a mensagem não é removida da fila de mensagens após o processamento de **PeekMessage** .</span><span class="sxs-lookup"><span data-stu-id="e1065-121">An application has called the [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function with wRemoveMsg set to **PM_NOREMOVE**, indicating that the message is not removed from the message queue after **PeekMessage** processing.</span></span> |
| <span data-ttu-id="e1065-122">**HC_NOREMOVE** 2</span><span class="sxs-lookup"><span data-stu-id="e1065-122">**HC_NOREMOVE** 2</span></span> | <span data-ttu-id="e1065-123">O procedimento de gancho deve se preparar para copiar a próxima mensagem do mouse ou do teclado para a estrutura **EVENTMSG** apontada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="e1065-123">The hook procedure must prepare to copy the next mouse or keyboard message to the **EVENTMSG** structure pointed to by *lParam*.</span></span> <span data-ttu-id="e1065-124">Após receber o código de **HC_GETNEXT** , o procedimento de gancho deve copiar a mensagem para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="e1065-124">Upon receiving the **HC_GETNEXT** code, the hook procedure must copy the message to the structure.</span></span> |
| <span data-ttu-id="e1065-125">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="e1065-125">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="e1065-126">Uma caixa de diálogo modal do sistema foi destruída.</span><span class="sxs-lookup"><span data-stu-id="e1065-126">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="e1065-127">O procedimento de gancho deve retomar a reprodução das mensagens.</span><span class="sxs-lookup"><span data-stu-id="e1065-127">The hook procedure must resume playing back the messages.</span></span> |
| <span data-ttu-id="e1065-128">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="e1065-128">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="e1065-129">Uma caixa de diálogo modal do sistema está sendo exibida.</span><span class="sxs-lookup"><span data-stu-id="e1065-129">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="e1065-130">Até que a caixa de diálogo seja destruída, o procedimento de gancho deve parar de reproduzir mensagens.</span><span class="sxs-lookup"><span data-stu-id="e1065-130">Until the dialog box is destroyed, the hook procedure must stop playing back messages.</span></span> |

### <a name="wparam"></a><span data-ttu-id="e1065-131">wParam</span><span class="sxs-lookup"><span data-stu-id="e1065-131">wParam</span></span>

<span data-ttu-id="e1065-132">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="e1065-132">Type: **WPARAM**</span></span>

<span data-ttu-id="e1065-133">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="e1065-133">This parameter is not used.</span></span>

### <a name="lparam"></a><span data-ttu-id="e1065-134">lParam</span><span class="sxs-lookup"><span data-stu-id="e1065-134">lParam</span></span>

<span data-ttu-id="e1065-135">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="e1065-135">Type: **LPARAM**</span></span>

<span data-ttu-id="e1065-136">Um ponteiro para uma estrutura **EVENTMSG** que representa uma mensagem sendo processada pelo procedimento de gancho.</span><span class="sxs-lookup"><span data-stu-id="e1065-136">A pointer to an **EVENTMSG** structure that represents a message being processed by the hook procedure.</span></span>
<span data-ttu-id="e1065-137">Esse parâmetro é válido somente quando o parâmetro de *código* é **HC_GETNEXT**.</span><span class="sxs-lookup"><span data-stu-id="e1065-137">This parameter is valid only when the *code* parameter is **HC_GETNEXT**.</span></span>

## <a name="returns"></a><span data-ttu-id="e1065-138">Retornos</span><span class="sxs-lookup"><span data-stu-id="e1065-138">Returns</span></span>

<span data-ttu-id="e1065-139">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e1065-139">Type: **LRESULT**</span></span>

<span data-ttu-id="e1065-140">Para que o sistema aguarde antes de processar a mensagem, o valor de retorno deve ser a quantidade de tempo, em tiques de relógio, que o sistema deve aguardar.</span><span class="sxs-lookup"><span data-stu-id="e1065-140">To have the system wait before processing the message, the return value must be the amount of time, in clock ticks, that the system should wait.</span></span>

<span data-ttu-id="e1065-141">(Esse valor pode ser calculado calculando a diferença entre os membros de hora nas mensagens de entrada atuais e anteriores.)</span><span class="sxs-lookup"><span data-stu-id="e1065-141">(This value can be computed by calculating the difference between the time members in the current and previous input messages.)</span></span>

<span data-ttu-id="e1065-142">Para processar a mensagem imediatamente, o valor de retorno deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e1065-142">To process the message immediately, the return value should be zero.</span></span> <span data-ttu-id="e1065-143">O valor de retorno será usado somente se o código do gancho for **HC_GETNEXT**; caso contrário, será ignorado.</span><span class="sxs-lookup"><span data-stu-id="e1065-143">The return value is used only if the hook code is **HC_GETNEXT**; otherwise, it is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1065-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1065-144">Remarks</span></span>

<span data-ttu-id="e1065-145">Um procedimento de gancho **JournalPlaybackProc** deve copiar uma mensagem de entrada para o parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="e1065-145">A **JournalPlaybackProc** hook procedure should copy an input message to The *lParam* parameter.</span></span>
<span data-ttu-id="e1065-146">A mensagem deve ter sido registrada anteriormente usando um procedimento de gancho **JournalRecordProc** , que não deve modificar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e1065-146">The message must have been previously recorded by using a **JournalRecordProc** hook procedure, which should not modify the message.</span></span>

<span data-ttu-id="e1065-147">Para recuperar a mesma mensagem repetidamente, o procedimento de gancho pode ser chamado várias vezes com o parâmetro de *código* definido como **HC_GETNEXT** sem uma chamada intermediária com o *código* definido como **HC_SKIP**.</span><span class="sxs-lookup"><span data-stu-id="e1065-147">To retrieve the same message over and over, the hook procedure can be called several times with the *code* parameter set to **HC_GETNEXT** without an intervening call with *code* set to **HC_SKIP**.</span></span>

<span data-ttu-id="e1065-148">Se o *código* for **HC_GETNEXT** e o valor de retorno for maior que zero, o sistema será suspenso para o número de milissegundos especificado pelo valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e1065-148">If *code* is **HC_GETNEXT** and the return value is greater than zero, the system sleeps for the number of milliseconds specified by the return value.</span></span> <span data-ttu-id="e1065-149">Quando o sistema continuar, ele chamará o procedimento de gancho novamente com o conjunto de *códigos* para **HC_GETNEXT** para recuperar a mesma mensagem.</span><span class="sxs-lookup"><span data-stu-id="e1065-149">When the system continues, it calls the hook procedure again with *code* set to **HC_GETNEXT** to retrieve the same message.</span></span>
<span data-ttu-id="e1065-150">O valor de retorno desta nova chamada para **JournalPlaybackProc** deve ser zero; caso contrário, o sistema voltará ao estado de suspensão para o número de milissegundos especificado pelo valor de retorno, chamará **JournalPlaybackProc** novamente e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e1065-150">The return value from this new call to **JournalPlaybackProc** should be zero; otherwise, the system will go back to sleep for the number of milliseconds specified by the return value, call **JournalPlaybackProc** again, and so on.</span></span>
<span data-ttu-id="e1065-151">O sistema parece não estar respondendo.</span><span class="sxs-lookup"><span data-stu-id="e1065-151">The system will appear to be not responding.</span></span>

<span data-ttu-id="e1065-152">Ao contrário da maioria dos outros procedimentos de gancho global, os procedimentos de gancho **JournalRecordProc** e **JournalPlaybackProc** são sempre chamados no contexto do thread que define o gancho.</span><span class="sxs-lookup"><span data-stu-id="e1065-152">Unlike most other global hook procedures, the **JournalRecordProc** and **JournalPlaybackProc** hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="e1065-153">Depois que o procedimento de gancho retorna o controle para o sistema, a mensagem continua a ser processada.</span><span class="sxs-lookup"><span data-stu-id="e1065-153">After the hook procedure returns control to the system, the message continues to be processed.</span></span> <span data-ttu-id="e1065-154">Se o *código* for **HC_SKIP**, o procedimento de gancho deverá se preparar para retornar a próxima mensagem de evento gravada em sua próxima chamada.</span><span class="sxs-lookup"><span data-stu-id="e1065-154">If *code* is **HC_SKIP**, the hook procedure must prepare to return the next recorded event message on its next call.</span></span>

<span data-ttu-id="e1065-155">Instale o procedimento de gancho **JournalPlaybackProc** especificando o tipo de [WH_JOURNALPLAYBACK](about-hooks.md) e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="e1065-155">Install the **JournalPlaybackProc** hook procedure by specifying the [WH_JOURNALPLAYBACK](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="e1065-156">Se o usuário pressionar CTRL + ESC ou CTRL + ALT + DEL durante a reprodução do diário, o sistema interromperá a reprodução, desvinculará o procedimento de reprodução do diário e lançará uma mensagem de [WM_CANCELJOURNAL](wm-canceljournal.md) no aplicativo de registro no diário.</span><span class="sxs-lookup"><span data-stu-id="e1065-156">If the user presses CTRL+ESC OR CTRL+ALT+DEL during journal playback, the system stops the playback, unhooks the journal playback procedure, and posts a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

<span data-ttu-id="e1065-157">Se o procedimento de gancho retornar uma mensagem no intervalo **WM_KEYFIRST** para **WM_KEYLAST**, as seguintes condições se aplicarão:</span><span class="sxs-lookup"><span data-stu-id="e1065-157">If the hook procedure returns a message in the range **WM_KEYFIRST** to **WM_KEYLAST**, the following conditions apply:</span></span>

* <span data-ttu-id="e1065-158">O membro **paraml** da estrutura **EVENTMSG** especifica o código de chave virtual da chave que foi pressionada.</span><span class="sxs-lookup"><span data-stu-id="e1065-158">The **paramL** member of the **EVENTMSG** structure specifies the virtual key code of the key that was pressed.</span></span>
* <span data-ttu-id="e1065-159">O membro **paramH** da estrutura **EVENTMSG** especifica o código de verificação.</span><span class="sxs-lookup"><span data-stu-id="e1065-159">The **paramH** member of the **EVENTMSG** structure specifies the scan code.</span></span>
* <span data-ttu-id="e1065-160">Não há como especificar uma contagem de repetição.</span><span class="sxs-lookup"><span data-stu-id="e1065-160">There's no way to specify a repeat count.</span></span>
<span data-ttu-id="e1065-161">O evento sempre é usado para representar um evento de chave.</span><span class="sxs-lookup"><span data-stu-id="e1065-161">The event is always taken to represent one key event.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1065-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1065-162">See also</span></span>

[<span data-ttu-id="e1065-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="e1065-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="e1065-164">EVENTMSG</span><span class="sxs-lookup"><span data-stu-id="e1065-164">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="e1065-165">JournalRecordProc</span><span class="sxs-lookup"><span data-stu-id="e1065-165">JournalRecordProc</span></span>](journalrecordproc.md)

[<span data-ttu-id="e1065-166">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="e1065-166">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="e1065-167">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="e1065-167">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="e1065-168">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="e1065-168">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="e1065-169">Ganchos</span><span class="sxs-lookup"><span data-stu-id="e1065-169">Hooks</span></span>](hooks.md)
