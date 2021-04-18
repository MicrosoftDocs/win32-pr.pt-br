---
UID: ''
title: Função de retorno de chamada ShellProc
description: A função recebe notificações de eventos do shell do sistema.
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
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "105807845"
---
# <a name="shellproc-function"></a><span data-ttu-id="9d753-103">Função ShellProc</span><span class="sxs-lookup"><span data-stu-id="9d753-103">ShellProc function</span></span>

## <a name="description"></a><span data-ttu-id="9d753-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d753-104">Description</span></span>

<span data-ttu-id="9d753-105">Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="9d753-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="9d753-106">A função recebe notificações de eventos do shell do sistema.</span><span class="sxs-lookup"><span data-stu-id="9d753-106">The function receives notifications of Shell events from the system.</span></span>

<span data-ttu-id="9d753-107">O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="9d753-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="9d753-108">**ShellProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9d753-108">**ShellProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="9d753-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d753-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="9d753-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="9d753-110">nCode [in]</span></span>

<span data-ttu-id="9d753-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="9d753-111">Type: **int**</span></span>

<span data-ttu-id="9d753-112">O código do gancho.</span><span class="sxs-lookup"><span data-stu-id="9d753-112">The hook code.</span></span>
<span data-ttu-id="9d753-113">Se *nCode* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="9d753-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="9d753-114">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d753-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="9d753-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9d753-115">Value</span></span> | <span data-ttu-id="9d753-116">Significado</span><span class="sxs-lookup"><span data-stu-id="9d753-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="9d753-117">**HSHELL_ACCESSIBILITYSTATE** 11</span><span class="sxs-lookup"><span data-stu-id="9d753-117">**HSHELL_ACCESSIBILITYSTATE** 11</span></span> | <span data-ttu-id="9d753-118">O estado de acessibilidade foi alterado.</span><span class="sxs-lookup"><span data-stu-id="9d753-118">The accessibility state has changed.</span></span> |
| <span data-ttu-id="9d753-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span><span class="sxs-lookup"><span data-stu-id="9d753-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span></span> | <span data-ttu-id="9d753-120">O Shell deve ativar sua janela principal.</span><span class="sxs-lookup"><span data-stu-id="9d753-120">The shell should activate its main window.</span></span> |
| <span data-ttu-id="9d753-121">**HSHELL_APPCOMMAND** 12</span><span class="sxs-lookup"><span data-stu-id="9d753-121">**HSHELL_APPCOMMAND** 12</span></span> | <span data-ttu-id="9d753-122">O usuário concluiu um evento de entrada (por exemplo, pressionou um botão de comando do aplicativo no mouse ou uma tecla de comando do aplicativo no teclado) e o aplicativo não manipula a mensagem de [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) gerada por essa entrada.</span><span class="sxs-lookup"><span data-stu-id="9d753-122">The user completed an input event (for example, pressed an application command button on the mouse or an application command key on the keyboard), and the application did not handle the [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) message generated by that input.</span></span> <span data-ttu-id="9d753-123">Se o procedimento do Shell manipular a mensagem de [WM_COMMAND](/windows/desktop/menurc/wm-command) , ele não deve chamar **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="9d753-123">If the Shell procedure handles the [WM_COMMAND](/windows/desktop/menurc/wm-command) message, it should not call **CallNextHookEx**.</span></span> <span data-ttu-id="9d753-124">Consulte a seção valor de retorno para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="9d753-124">See the Return Value section for more information.</span></span> |
| <span data-ttu-id="9d753-125">**HSHELL_GETMINRECT** 5</span><span class="sxs-lookup"><span data-stu-id="9d753-125">**HSHELL_GETMINRECT** 5</span></span> | <span data-ttu-id="9d753-126">Uma janela está sendo minimizada ou maximizada.</span><span class="sxs-lookup"><span data-stu-id="9d753-126">A window is being minimized or maximized.</span></span> <span data-ttu-id="9d753-127">O sistema precisa das coordenadas do retângulo minimizado para a janela.</span><span class="sxs-lookup"><span data-stu-id="9d753-127">The system needs the coordinates of the minimized rectangle for the window.</span></span> |
| <span data-ttu-id="9d753-128">**HSHELL_LANGUAGE** 8</span><span class="sxs-lookup"><span data-stu-id="9d753-128">**HSHELL_LANGUAGE** 8</span></span> | <span data-ttu-id="9d753-129">O idioma do teclado foi alterado ou um novo layout de teclado foi carregado.</span><span class="sxs-lookup"><span data-stu-id="9d753-129">Keyboard language was changed or a new keyboard layout was loaded.</span></span> |
| <span data-ttu-id="9d753-130">**HSHELL_REDRAW** 6</span><span class="sxs-lookup"><span data-stu-id="9d753-130">**HSHELL_REDRAW** 6</span></span> | <span data-ttu-id="9d753-131">O título de uma janela na barra de tarefas foi redesenhado.</span><span class="sxs-lookup"><span data-stu-id="9d753-131">The title of a window in the task bar has been redrawn.</span></span> |
| <span data-ttu-id="9d753-132">**HSHELL_TASKMAN** 7</span><span class="sxs-lookup"><span data-stu-id="9d753-132">**HSHELL_TASKMAN** 7</span></span> | <span data-ttu-id="9d753-133">O usuário selecionou a lista de tarefas.</span><span class="sxs-lookup"><span data-stu-id="9d753-133">The user has selected the task list.</span></span> <span data-ttu-id="9d753-134">Um aplicativo de shell que fornece uma lista de tarefas deve retornar **true** para impedir que o Windows inicie sua lista de tarefas.</span><span class="sxs-lookup"><span data-stu-id="9d753-134">A shell application that provides a task list should return **TRUE** to prevent Windows from starting its task list.</span></span> |
| <span data-ttu-id="9d753-135">**HSHELL_WINDOWACTIVATED** 4</span><span class="sxs-lookup"><span data-stu-id="9d753-135">**HSHELL_WINDOWACTIVATED** 4</span></span> | <span data-ttu-id="9d753-136">A ativação foi alterada para uma janela diferente de nível superior e sem proprietário.</span><span class="sxs-lookup"><span data-stu-id="9d753-136">The activation has changed to a different top-level, unowned window.</span></span> |
| <span data-ttu-id="9d753-137">**HSHELL_WINDOWCREATED** 1</span><span class="sxs-lookup"><span data-stu-id="9d753-137">**HSHELL_WINDOWCREATED** 1</span></span> | <span data-ttu-id="9d753-138">Uma janela de nível superior e sem proprietário foi criada.</span><span class="sxs-lookup"><span data-stu-id="9d753-138">A top-level, unowned window has been created.</span></span> <span data-ttu-id="9d753-139">A janela existe quando o sistema chama esse gancho.</span><span class="sxs-lookup"><span data-stu-id="9d753-139">The window exists when the system calls this hook.</span></span> |
| <span data-ttu-id="9d753-140">**HSHELL_WINDOWDESTROYED** 2</span><span class="sxs-lookup"><span data-stu-id="9d753-140">**HSHELL_WINDOWDESTROYED** 2</span></span> | <span data-ttu-id="9d753-141">Uma janela sem proprietário de nível superior está prestes a ser destruída.</span><span class="sxs-lookup"><span data-stu-id="9d753-141">A top-level, unowned window is about to be destroyed.</span></span> <span data-ttu-id="9d753-142">A janela ainda existe quando o sistema chama esse gancho.</span><span class="sxs-lookup"><span data-stu-id="9d753-142">The window still exists when the system calls this hook.</span></span> |
| <span data-ttu-id="9d753-143">**HSHELL_WINDOWREPLACED** 13</span><span class="sxs-lookup"><span data-stu-id="9d753-143">**HSHELL_WINDOWREPLACED** 13</span></span> | <span data-ttu-id="9d753-144">Uma janela de nível superior está sendo substituída.</span><span class="sxs-lookup"><span data-stu-id="9d753-144">A top-level window is being replaced.</span></span> <span data-ttu-id="9d753-145">A janela existe quando o sistema chama esse gancho.</span><span class="sxs-lookup"><span data-stu-id="9d753-145">The window exists when the system calls this hook.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="9d753-146">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="9d753-146">wParam [in]</span></span>

<span data-ttu-id="9d753-147">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="9d753-147">Type: **WPARAM**</span></span>

<span data-ttu-id="9d753-148">Esse parâmetro depende do valor do parâmetro *nCode* , conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d753-148">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="9d753-149">nCode</span><span class="sxs-lookup"><span data-stu-id="9d753-149">nCode</span></span> | <span data-ttu-id="9d753-150">wParam</span><span class="sxs-lookup"><span data-stu-id="9d753-150">wParam</span></span> |
|-------|---------|
| <span data-ttu-id="9d753-151">**HSHELL_ACCESSIBILITYSTATE**</span><span class="sxs-lookup"><span data-stu-id="9d753-151">**HSHELL_ACCESSIBILITYSTATE**</span></span> | <span data-ttu-id="9d753-152">Indica qual recurso de acessibilidade alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="9d753-152">Indicates which accessibility feature has changed state.</span></span> <span data-ttu-id="9d753-153">Esse valor é um dos seguintes: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** ou **ACCESS_STICKYKEYS**.</span><span class="sxs-lookup"><span data-stu-id="9d753-153">This value is one of the following: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS**, or **ACCESS_STICKYKEYS**.</span></span> |
| <span data-ttu-id="9d753-154">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="9d753-154">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="9d753-155">Indica onde a mensagem de **WM_APPCOMMAND** foi enviada originalmente; por exemplo, o identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="9d753-155">Indicates where the **WM_APPCOMMAND** message was originally sent; for example, the handle to a window.</span></span> <span data-ttu-id="9d753-156">Para obter mais informações, consulte parâmetro cmd em **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="9d753-156">For more information, see cmd parameter in **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="9d753-157">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="9d753-157">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="9d753-158">Um identificador para a janela minimizada ou maximizada.</span><span class="sxs-lookup"><span data-stu-id="9d753-158">A handle to the minimized or maximized window.</span></span> |
| <span data-ttu-id="9d753-159">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="9d753-159">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="9d753-160">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="9d753-160">A handle to the window.</span></span> |
| <span data-ttu-id="9d753-161">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="9d753-161">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="9d753-162">Um identificador para a janela redesenhar.</span><span class="sxs-lookup"><span data-stu-id="9d753-162">A handle to the redrawn window.</span></span> |
| <span data-ttu-id="9d753-163">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="9d753-163">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="9d753-164">Um identificador para a janela ativada.</span><span class="sxs-lookup"><span data-stu-id="9d753-164">A handle to the activated window.</span></span> |
| <span data-ttu-id="9d753-165">**HSHELL_WINDOWCREATED**</span><span class="sxs-lookup"><span data-stu-id="9d753-165">**HSHELL_WINDOWCREATED**</span></span> | <span data-ttu-id="9d753-166">Um identificador para a janela criada.</span><span class="sxs-lookup"><span data-stu-id="9d753-166">A handle to the created window.</span></span> |
| <span data-ttu-id="9d753-167">**HSHELL_WINDOWDESTROYED**</span><span class="sxs-lookup"><span data-stu-id="9d753-167">**HSHELL_WINDOWDESTROYED**</span></span> | <span data-ttu-id="9d753-168">Um identificador para a janela destruída.</span><span class="sxs-lookup"><span data-stu-id="9d753-168">A handle to the destroyed window.</span></span> |
| <span data-ttu-id="9d753-169">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="9d753-169">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="9d753-170">Um identificador para a janela que está sendo substituída.</span><span class="sxs-lookup"><span data-stu-id="9d753-170">A handle to the window being replaced.</span></span> <span data-ttu-id="9d753-171">Windows 2000: sem suporte.</span><span class="sxs-lookup"><span data-stu-id="9d753-171">Windows 2000:  Not supported.</span></span> |

### <a name="lparam-in"></a><span data-ttu-id="9d753-172">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="9d753-172">lParam [in]</span></span>

<span data-ttu-id="9d753-173">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="9d753-173">Type: **LPARAM**</span></span>

<span data-ttu-id="9d753-174">Esse parâmetro depende do valor do parâmetro *nCode* , conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d753-174">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="9d753-175">nCode</span><span class="sxs-lookup"><span data-stu-id="9d753-175">nCode</span></span> | <span data-ttu-id="9d753-176">lParam</span><span class="sxs-lookup"><span data-stu-id="9d753-176">lParam</span></span> |
|-------|---------|
| <span data-ttu-id="9d753-177">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="9d753-177">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="9d753-178">`GET_APPCOMMAND_LPARAM(lParam)` é o comando de aplicativo correspondente ao evento de entrada.</span><span class="sxs-lookup"><span data-stu-id="9d753-178">`GET_APPCOMMAND_LPARAM(lParam)` is the application command corresponding to the input event.</span></span> <span data-ttu-id="9d753-179">`GET_DEVICE_LPARAM(lParam)` indica o que gerou o evento de entrada; por exemplo, o mouse ou o teclado.</span><span class="sxs-lookup"><span data-stu-id="9d753-179">`GET_DEVICE_LPARAM(lParam)` indicates what generated the input event; for example, the mouse or keyboard.</span></span> <span data-ttu-id="9d753-180">Para obter mais informações, consulte a descrição do parâmetro *udevice* em **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="9d753-180">For more information, see the *uDevice* parameter description under **WM_APPCOMMAND**.</span></span> <span data-ttu-id="9d753-181">`GET_FLAGS_LPARAM(lParam)` depende do valor do *cmd* no **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="9d753-181">`GET_FLAGS_LPARAM(lParam)` depends on the value of *cmd* in **WM_APPCOMMAND**.</span></span> <span data-ttu-id="9d753-182">Por exemplo, isso pode indicar quais chaves virtuais foram mantidas quando a **WM_APPCOMMAND** mensagem foi enviada originalmente.</span><span class="sxs-lookup"><span data-stu-id="9d753-182">For example, it might indicate which virtual keys were held down when the **WM_APPCOMMAND** message was originally sent.</span></span> <span data-ttu-id="9d753-183">Para obter mais informações, consulte o parâmetro de descrição *dwCmdFlags* em **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="9d753-183">For more information, see the *dwCmdFlags* description parameter under **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="9d753-184">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="9d753-184">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="9d753-185">Um ponteiro para uma estrutura [Rect](/previous-versions/dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9d753-185">A pointer to a [RECT](/previous-versions/dd162897(v=vs.85)) structure.</span></span> |
| <span data-ttu-id="9d753-186">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="9d753-186">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="9d753-187">Um identificador para um layout de teclado.</span><span class="sxs-lookup"><span data-stu-id="9d753-187">A handle to a keyboard layout.</span></span> |
| <span data-ttu-id="9d753-188">**HSHELL_MONITORCHANGED**</span><span class="sxs-lookup"><span data-stu-id="9d753-188">**HSHELL_MONITORCHANGED**</span></span> | <span data-ttu-id="9d753-189">Um identificador para a janela que foi movida para um monitor diferente.</span><span class="sxs-lookup"><span data-stu-id="9d753-189">A handle to the window that moved to a different monitor.</span></span> |
| <span data-ttu-id="9d753-190">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="9d753-190">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="9d753-191">O valor será **true** se a janela estiver piscando, caso contrário, retornará **false** .</span><span class="sxs-lookup"><span data-stu-id="9d753-191">The value is **TRUE** if the window is flashing, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="9d753-192">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="9d753-192">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="9d753-193">O valor será TRUE se a janela estiver no modo de tela inteira ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9d753-193">The value is TRUE if the window is in full-screen mode, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="9d753-194">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="9d753-194">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="9d753-195">Um identificador para a nova janela.</span><span class="sxs-lookup"><span data-stu-id="9d753-195">A handle to the new window.</span></span> <span data-ttu-id="9d753-196">Windows 2000: sem suporte.</span><span class="sxs-lookup"><span data-stu-id="9d753-196">Windows 2000:  Not supported.</span></span> |

## <a name="returns"></a><span data-ttu-id="9d753-197">Retornos</span><span class="sxs-lookup"><span data-stu-id="9d753-197">Returns</span></span>

<span data-ttu-id="9d753-198">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9d753-198">Type: **LRESULT**</span></span>

<span data-ttu-id="9d753-199">O valor de retorno deve ser zero, a menos que o valor de nCode seja **HSHELL_APPCOMMAND** e o procedimento de shell manipule a mensagem de **WM_COMMAND** .</span><span class="sxs-lookup"><span data-stu-id="9d753-199">The return value should be zero unless the value of nCode is **HSHELL_APPCOMMAND** and the shell procedure handles the **WM_COMMAND** message.</span></span>
<span data-ttu-id="9d753-200">Nesse caso, o retorno deve ser diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="9d753-200">In this case, the return should be nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d753-201">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d753-201">Remarks</span></span>

<span data-ttu-id="9d753-202">Instale esse procedimento de conexão especificando o tipo de gancho [WH_SHELL](about-hooks.md) e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="9d753-202">Install this hook procedure by specifying the [WH_SHELL](about-hooks.md) hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d753-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d753-203">See also</span></span>

[<span data-ttu-id="9d753-204">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="9d753-204">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="9d753-205">SendMessage</span><span class="sxs-lookup"><span data-stu-id="9d753-205">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[<span data-ttu-id="9d753-206">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="9d753-206">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="9d753-207">WM_APPCOMMAND</span><span class="sxs-lookup"><span data-stu-id="9d753-207">WM_APPCOMMAND</span></span>](/windows/desktop/inputdev/wm-appcommand)

[<span data-ttu-id="9d753-208">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="9d753-208">WM_COMMAND</span></span>](/windows/desktop/menurc/wm-command)

[<span data-ttu-id="9d753-209">Ganchos</span><span class="sxs-lookup"><span data-stu-id="9d753-209">Hooks</span></span>](hooks.md)
