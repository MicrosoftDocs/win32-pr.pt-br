---
description: Uma barra de ferramentas de área de trabalho do aplicativo (também chamada de AppBar) é uma janela semelhante à barra de tarefas do Windows.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Usando as barras de ferramentas da área de trabalho do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090031"
---
# <a name="using-application-desktop-toolbars"></a><span data-ttu-id="7a6bd-103">Usando as barras de ferramentas da área de trabalho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7a6bd-103">Using Application Desktop Toolbars</span></span>

<span data-ttu-id="7a6bd-104">Uma *barra de ferramentas de área de trabalho do aplicativo* (também chamada de AppBar) é uma janela semelhante à barra de tarefas do Windows.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-104">An *application desktop toolbar* (also called an appbar) is a window that is similar to the Windows taskbar.</span></span> <span data-ttu-id="7a6bd-105">Ele é ancorado em uma borda da tela e normalmente contém botões que dão ao usuário acesso rápido a outros aplicativos e janelas.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-105">It is anchored to an edge of the screen, and it typically contains buttons that give the user quick access to other applications and windows.</span></span> <span data-ttu-id="7a6bd-106">O sistema impede que outros aplicativos usem a área de trabalho usada por um AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-106">The system prevents other applications from using the desktop area used by an appbar.</span></span> <span data-ttu-id="7a6bd-107">Qualquer número de appbars pode existir na área de trabalho em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-107">Any number of appbars can exist on the desktop at any given time.</span></span>

<span data-ttu-id="7a6bd-108">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7a6bd-109">Sobre as barras de ferramentas da área de trabalho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7a6bd-109">About Application Desktop Toolbars</span></span>](#about-application-desktop-toolbars)
    -   [<span data-ttu-id="7a6bd-110">Enviando mensagens</span><span class="sxs-lookup"><span data-stu-id="7a6bd-110">Sending Messages</span></span>](#sending-messages)
    -   [<span data-ttu-id="7a6bd-111">Registro</span><span class="sxs-lookup"><span data-stu-id="7a6bd-111">Registration</span></span>](#registration)
    -   [<span data-ttu-id="7a6bd-112">Tamanho e posição do AppBar</span><span class="sxs-lookup"><span data-stu-id="7a6bd-112">Appbar Size and Position</span></span>](#appbar-size-and-position)
    -   [<span data-ttu-id="7a6bd-113">Ocultar automaticamente barras de ferramentas da área de trabalho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7a6bd-113">Autohide Application Desktop Toolbars</span></span>](#autohide-application-desktop-toolbars)
    -   [<span data-ttu-id="7a6bd-114">Mensagens de notificação do AppBar</span><span class="sxs-lookup"><span data-stu-id="7a6bd-114">Appbar Notification Messages</span></span>](#appbar-notification-messages)
-   [<span data-ttu-id="7a6bd-115">Registrando uma barra de ferramentas de área de trabalho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7a6bd-115">Registering an Application Desktop Toolbar</span></span>](#registering-an-application-desktop-toolbar)
-   [<span data-ttu-id="7a6bd-116">Definindo o tamanho e a posição de AppBar</span><span class="sxs-lookup"><span data-stu-id="7a6bd-116">Setting the Appbar Size and Position</span></span>](#setting-the-appbar-size-and-position)
-   [<span data-ttu-id="7a6bd-117">Processando mensagens de notificação AppBar</span><span class="sxs-lookup"><span data-stu-id="7a6bd-117">Processing Appbar Notification Messages</span></span>](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a><span data-ttu-id="7a6bd-118">Sobre as barras de ferramentas da área de trabalho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7a6bd-118">About Application Desktop Toolbars</span></span>

<span data-ttu-id="7a6bd-119">O Windows fornece uma API que permite que você aproveite os serviços AppBar fornecidos pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-119">Windows provides an API that lets you take advantage of appbar services provided by the system.</span></span> <span data-ttu-id="7a6bd-120">Os serviços ajudam a garantir que os appbars definidos pelo aplicativo operem suavemente entre si e com a barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-120">The services help ensure that application-defined appbars operate smoothly with one another and with the taskbar.</span></span> <span data-ttu-id="7a6bd-121">O sistema mantém informações sobre cada AppBar e envia as mensagens appbars para notificá-las sobre eventos que podem afetar seu tamanho, posição e aparência.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-121">The system maintains information about each appbar and sends the appbars messages to notify them about events that can affect their size, position, and appearance.</span></span>

### <a name="sending-messages"></a><span data-ttu-id="7a6bd-122">enviando mensagens</span><span class="sxs-lookup"><span data-stu-id="7a6bd-122">Sending Messages</span></span>

<span data-ttu-id="7a6bd-123">Um aplicativo usa um conjunto especial de mensagens, chamadas de mensagens AppBar, para adicionar ou remover um AppBar, definir o tamanho e a posição de um AppBar e recuperar informações sobre o tamanho, a posição e o estado da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-123">An application uses a special set of messages, called appbar messages, to add or remove an appbar, set an appbar's size and position, and retrieve information about the size, position, and state of the taskbar.</span></span> <span data-ttu-id="7a6bd-124">Para enviar uma mensagem AppBar, um aplicativo deve usar a função [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-124">To send an appbar message, an application must use the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function.</span></span> <span data-ttu-id="7a6bd-125">Os parâmetros da função incluem um identificador de mensagem, como [**ABM \_ New**](abm-new.md)e o endereço de uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-125">The function's parameters include a message identifier, such as [**ABM\_NEW**](abm-new.md), and the address of an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="7a6bd-126">Os membros da estrutura contêm informações que o sistema precisa para processar a mensagem determinada.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-126">The structure members contain information that the system needs to process the given message.</span></span>

<span data-ttu-id="7a6bd-127">Para qualquer mensagem AppBar determinada, o sistema usa alguns membros da estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) e ignora os outros.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-127">For any given appbar message, the system uses some members of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure and ignores the others.</span></span> <span data-ttu-id="7a6bd-128">No entanto, o sistema sempre usa os membros **cbSize** e **HWND** , portanto, um aplicativo deve preencher esses membros para cada mensagem AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-128">However, the system always uses the **cbSize** and **hWnd** members, so an application must fill these members for every appbar message.</span></span> <span data-ttu-id="7a6bd-129">O membro **cbSize** especifica o tamanho da estrutura e o membro **HWND** é o identificador para a janela do AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-129">The **cbSize** member specifies the size of the structure, and the **hWnd** member is the handle to the appbar's window.</span></span>

<span data-ttu-id="7a6bd-130">Algumas mensagens AppBar solicitam informações do sistema.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-130">Some appbar messages request information from the system.</span></span> <span data-ttu-id="7a6bd-131">Ao processar essas mensagens, o sistema copia as informações solicitadas na estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-131">When processing these messages, the system copies the requested information into the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

### <a name="registration"></a><span data-ttu-id="7a6bd-132">Registro</span><span class="sxs-lookup"><span data-stu-id="7a6bd-132">Registration</span></span>

<span data-ttu-id="7a6bd-133">O sistema mantém uma lista interna de appbars e mantém informações sobre cada barra na lista.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-133">The system keeps an internal list of appbars and maintains information about each bar in the list.</span></span> <span data-ttu-id="7a6bd-134">O sistema usa as informações para gerenciar o appbars, executar serviços para eles e enviar mensagens de notificação.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-134">The system uses the information to manage appbars, perform services for them, and send them notification messages.</span></span>

<span data-ttu-id="7a6bd-135">Um aplicativo deve registrar um AppBar (ou seja, adicioná-lo à lista interna) antes de poder receber serviços AppBar do sistema.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-135">An application must register an appbar (that is, add it to the internal list) before it can receive appbar services from the system.</span></span> <span data-ttu-id="7a6bd-136">Para registrar um AppBar, um aplicativo envia a [**\_ nova**](abm-new.md) mensagem do ABM.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-136">To register an appbar, an application sends the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="7a6bd-137">A estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) acompanhante inclui o identificador para a janela do AppBar e um identificador de mensagem definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-137">The accompanying [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure includes the handle to the appbar's window and an application-defined message identifier.</span></span> <span data-ttu-id="7a6bd-138">O sistema usa o identificador de mensagem para enviar mensagens de notificação para o procedimento de janela da janela AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-138">The system uses the message identifier to send notification messages to the window procedure of the appbar window.</span></span> <span data-ttu-id="7a6bd-139">Para obter mais informações, consulte mensagens de notificação do AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-139">For more information, see Appbar Notification Messages.</span></span>

<span data-ttu-id="7a6bd-140">Um aplicativo cancela o registro de um AppBar enviando a mensagem [**ABM \_ Remove**](abm-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-140">An application unregisters an appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="7a6bd-141">O cancelamento do registro de um AppBar o Remove da lista interna do appbars do sistema.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-141">Unregistering an appbar removes it from the system's internal list of appbars.</span></span> <span data-ttu-id="7a6bd-142">O sistema não envia mais mensagens de notificação para o AppBar ou impede que outros aplicativos usem a área de tela usada pelo AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-142">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span> <span data-ttu-id="7a6bd-143">Um aplicativo sempre deve enviar **ABM \_ remover** antes de destruir um AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-143">An application should always send **ABM\_REMOVE** before destroying an appbar.</span></span>

### <a name="appbar-size-and-position"></a><span data-ttu-id="7a6bd-144">Tamanho e posição do AppBar</span><span class="sxs-lookup"><span data-stu-id="7a6bd-144">Appbar Size and Position</span></span>

<span data-ttu-id="7a6bd-145">Um aplicativo deve definir o tamanho e a posição de um AppBar para que ele não interfira em nenhum outro appbars ou na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-145">An application should set an appbar's size and position so that it does not interfere with any other appbars or the taskbar.</span></span> <span data-ttu-id="7a6bd-146">Cada AppBar deve ser ancorado a uma borda específica da tela, e vários appbars podem ser ancorados a uma borda.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-146">Every appbar must be anchored to a particular edge of the screen, and multiple appbars can be anchored to an edge.</span></span> <span data-ttu-id="7a6bd-147">No entanto, se um AppBar for ancorado à mesma borda da barra de tarefas, o sistema garantirá que a barra de tarefas esteja sempre na borda mais externa.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-147">However, if an appbar is anchored to the same edge as the taskbar, the system ensures that the taskbar is always on the outermost edge.</span></span>

<span data-ttu-id="7a6bd-148">Para definir o tamanho e a posição de um AppBar, um aplicativo primeiro propõe uma borda de tela e um retângulo delimitador para o AppBar enviando a mensagem [**ABM \_ QUERYPOS**](abm-querypos.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-148">To set the size and position of an appbar, an application first proposes a screen edge and bounding rectangle for the appbar by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="7a6bd-149">O sistema determina se qualquer parte da área da tela dentro do retângulo proposto é usada pela barra de tarefas ou por outro AppBar, ajusta o retângulo (se necessário) e retorna o retângulo ajustado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-149">The system determines whether any part of the screen area within the proposed rectangle is used by the taskbar or another appbar, adjusts the rectangle (if necessary), and returns the adjusted rectangle to the application.</span></span>

<span data-ttu-id="7a6bd-150">Em seguida, o aplicativo envia a mensagem [**ABM \_ SETPOS**](abm-setpos.md) para definir o novo retângulo delimitador para o AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-150">Next, the application sends the [**ABM\_SETPOS**](abm-setpos.md) message to set the new bounding rectangle for the appbar.</span></span> <span data-ttu-id="7a6bd-151">Novamente, o sistema pode ajustar o retângulo antes de retorná-lo para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-151">Again, the system may adjust the rectangle before returning it to the application.</span></span> <span data-ttu-id="7a6bd-152">Por esse motivo, o aplicativo deve usar o retângulo ajustado retornado por **ABM \_ SETPOS** para definir o tamanho final e a posição.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-152">For this reason, the application should use the adjusted rectangle returned by **ABM\_SETPOS** to set the final size and position.</span></span> <span data-ttu-id="7a6bd-153">O aplicativo pode usar a função [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para mover o AppBar para a posição.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-153">The application can use the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="7a6bd-154">Usando um processo de duas etapas para definir o tamanho e a posição, o sistema permite que o aplicativo forneça comentários intermediários ao usuário durante a operação de movimentação.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-154">By using a two-step process to set the size and position, the system enables the application to provide intermediate feedback to the user during the move operation.</span></span> <span data-ttu-id="7a6bd-155">Por exemplo, se o usuário arrastar um AppBar, o aplicativo poderá exibir um retângulo sombreado indicando que a nova posição antes da AppBar realmente se moverá.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-155">For example, if the user drags an appbar, the application might display a shaded rectangle indicating the new position before the appbar actually moves.</span></span>

<span data-ttu-id="7a6bd-156">Um aplicativo deve definir o tamanho e a posição de seu AppBar depois de registrá-lo e sempre que o AppBar receber a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-156">An application should set the size and position of its appbar after registering it and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="7a6bd-157">Um AppBar recebe essa mensagem de notificação sempre que ocorre uma alteração no estado de tamanho, posição ou visibilidade da barra de tarefas e sempre que outro AppBar no mesmo lado da tela é redimensionado, adicionado ou removido.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-157">An appbar receives this notification message whenever a change occurs in the taskbar's size, position, or visibility state and whenever another appbar on the same side of the screen is resized, added, or removed.</span></span>

<span data-ttu-id="7a6bd-158">Sempre que um AppBar recebe a \_ mensagem de ativação do WM, ele deve enviar a mensagem de [**\_ ativação do ABM**](abm-activate.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-158">Whenever an appbar receives the WM\_ACTIVATE message, it should send the [**ABM\_ACTIVATE**](abm-activate.md) message.</span></span> <span data-ttu-id="7a6bd-159">Da mesma forma, quando um AppBar recebe uma mensagem do WM \_ WINDOWPOSCHANGED, ele deve chamar [**ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md).</span><span class="sxs-lookup"><span data-stu-id="7a6bd-159">Similarly, when an appbar receives a WM\_WINDOWPOSCHANGED message, it must call [**ABM\_WINDOWPOSCHANGED**](abm-windowposchanged.md).</span></span> <span data-ttu-id="7a6bd-160">O envio dessas mensagens garante que o sistema Defina corretamente a ordem z de qualquer AutoOcultar appbars na mesma borda.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-160">Sending these messages ensures that the system properly sets the z-order of any autohide appbars on the same edge.</span></span>

### <a name="autohide-application-desktop-toolbars"></a><span data-ttu-id="7a6bd-161">Ocultar automaticamente barras de ferramentas da área de trabalho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7a6bd-161">Autohide Application Desktop Toolbars</span></span>

<span data-ttu-id="7a6bd-162">Um AutoOcultar AppBar é aquele que normalmente é oculto, mas fica visível quando o usuário move o cursor do mouse para a borda da tela com a qual o AppBar está associado.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-162">An autohide appbar is one that is normally hidden but becomes visible when the user moves the mouse cursor to the screen edge with which the appbar is associated.</span></span> <span data-ttu-id="7a6bd-163">O AppBar se oculta novamente quando o usuário move o cursor do mouse para fora do retângulo delimitador da barra.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-163">The appbar hides itself again when the user moves the mouse cursor out of the bar's bounding rectangle.</span></span>

<span data-ttu-id="7a6bd-164">Embora o sistema permita uma série de appbars diferentes a qualquer momento, ele permite apenas um AutoOcultar AppBar de cada vez para cada borda de tela de acordo com uma base de chegada, servida primeiro.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-164">Although the system allows a number of different appbars at any given time, it allows only one autohide appbar at a time for each screen edge on a first-come, first-served basis.</span></span> <span data-ttu-id="7a6bd-165">O sistema mantém automaticamente a ordem z de um AutoOcultar AppBar (somente dentro de seu grupo de ordem z).</span><span class="sxs-lookup"><span data-stu-id="7a6bd-165">The system automatically maintains the z-order of an autohide appbar (within its z-order group only).</span></span>

<span data-ttu-id="7a6bd-166">Um aplicativo usa a mensagem [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) para registrar ou cancelar o registro de um AutoOcultar AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-166">An application uses the [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) message to register or unregister an autohide appbar.</span></span> <span data-ttu-id="7a6bd-167">A mensagem Especifica a borda para o AppBar e um sinalizador que especifica se o AppBar deve ser registrado ou cancelado.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-167">The message specifies the edge for the appbar and a flag that specifies whether the appbar is to be registered or unregistered.</span></span> <span data-ttu-id="7a6bd-168">A mensagem falhará se uma AutoOcultar AppBar estiver sendo registrada, mas já houver uma associada à borda especificada.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-168">The message fails if an autohide appbar is being registered but one is already associated with the specified edge.</span></span> <span data-ttu-id="7a6bd-169">Um aplicativo pode recuperar o identificador para o AppBar de AutoOcultar associado a uma borda enviando a mensagem [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-169">An application can retrieve the handle to the autohide appbar associated with an edge by sending the [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) message.</span></span>

<span data-ttu-id="7a6bd-170">Um AutoOcultar AppBar não precisa se registrar como um AppBar normal; ou seja, ele não precisa ser registrado enviando a [**\_ nova mensagem ABM**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-170">An autohide appbar does not need to register as a normal appbar; that is, it does not need to be registered by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="7a6bd-171">Um AppBar que não está registrado por **ABM \_** se sobrepõe a qualquer appbars ancorado na mesma borda da tela.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-171">An appbar that is not registered by **ABM\_NEW** overlaps any appbars anchored on the same edge of the screen.</span></span>

### <a name="appbar-notification-messages"></a><span data-ttu-id="7a6bd-172">Mensagens de notificação do AppBar</span><span class="sxs-lookup"><span data-stu-id="7a6bd-172">Appbar Notification Messages</span></span>

<span data-ttu-id="7a6bd-173">O sistema envia mensagens para notificar um AppBar sobre os eventos que podem afetar sua posição e aparência.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-173">The system sends messages to notify an appbar about events that can affect its position and appearance.</span></span> <span data-ttu-id="7a6bd-174">As mensagens são enviadas no contexto de uma mensagem definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-174">The messages are sent in the context of an application-defined message.</span></span> <span data-ttu-id="7a6bd-175">O aplicativo especifica o identificador da mensagem quando envia a nova mensagem [**ABM \_**](abm-new.md) para registrar o AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-175">The application specifies the identifier of the message when it sends the [**ABM\_NEW**](abm-new.md) message to register the appbar.</span></span> <span data-ttu-id="7a6bd-176">O código de notificação está no parâmetro *wParam* da mensagem definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-176">The notification code is in the *wParam* parameter of the application-defined message.</span></span>

<span data-ttu-id="7a6bd-177">Um AppBar recebe a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) quando o tamanho, a posição ou o estado de visibilidade da barra de tarefas é alterado, quando outro AppBar é adicionado à mesma borda da tela ou quando outro AppBar na mesma borda da tela é redimensionado ou removido.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-177">An appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message when the taskbar's size, position, or visibility state changes, when another appbar is added to the same edge of the screen, or when another appbar on the same edge of the screen is resized or removed.</span></span> <span data-ttu-id="7a6bd-178">Um AppBar deve responder a essa mensagem de notificação enviando mensagens [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-178">An appbar should respond to this notification message by sending [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="7a6bd-179">Se uma posição de AppBar for alterada, ela deverá chamar a função [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para se mover para a nova posição.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-179">If an appbar's position has changed, it should call the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

<span data-ttu-id="7a6bd-180">O sistema envia a mensagem de notificação do [**ABN \_ STATECHANGE**](abn-statechange.md) sempre que o estado de ocultar automaticamente ou sempre visível da barra de tarefas for alterado — ou seja, quando o usuário marcar ou desmarcar a caixa de seleção **sempre visível** ou **ocultar automaticamente** na folha de propriedades da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-180">The system sends the [**ABN\_STATECHANGE**](abn-statechange.md) notification message whenever the taskbar's autohide or always-on-top state has changed—that is, when the user selects or clears the **Always on top** or **Auto hide** check box on the taskbar's property sheet.</span></span> <span data-ttu-id="7a6bd-181">Um AppBar pode usar essa mensagem de notificação para definir seu estado de acordo com a barra de tarefas, se desejado.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-181">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

<span data-ttu-id="7a6bd-182">Quando um aplicativo de tela inteira é iniciado ou quando o último aplicativo de tela inteira é fechado, um AppBar recebe a mensagem de notificação do [**ABN \_ FULLSCREENAPP**](abn-fullscreenapp.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-182">When a full-screen application is started or when the last full-screen application is closed, an appbar receives the [**ABN\_FULLSCREENAPP**](abn-fullscreenapp.md) notification message.</span></span> <span data-ttu-id="7a6bd-183">O parâmetro *lParam* indica se o aplicativo de tela inteira está abrindo ou fechando.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-183">The *lParam* parameter indicates whether the full-screen application is opening or closing.</span></span> <span data-ttu-id="7a6bd-184">Se estiver abrindo, o AppBar deverá soltar para a parte inferior da ordem z.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-184">If it is opening, the appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="7a6bd-185">O AppBar deve restaurar sua posição de ordem z quando o último aplicativo de tela inteira tiver sido fechado.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-185">The appbar should restore its z-order position when the last full-screen application has closed.</span></span>

<span data-ttu-id="7a6bd-186">Um AppBar recebe a mensagem de notificação do [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) quando o usuário seleciona o comando Cascade, Tile horizontal ou Tile verticalmente do lado do menu de atalho da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-186">An appbar receives the [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) notification message when the user selects the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span> <span data-ttu-id="7a6bd-187">O sistema envia a mensagem duas vezes — antes de reorganizar as janelas (*lParam* é **verdadeiro**) e depois de organizar as janelas (*lParam* é **falso**).</span><span class="sxs-lookup"><span data-stu-id="7a6bd-187">The system sends the message two times—before rearranging the windows (*lParam* is **TRUE**) and after arranging the windows (*lParam* is **FALSE**).</span></span>

<span data-ttu-id="7a6bd-188">Um AppBar pode usar mensagens do [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) para excluir a si mesmo da operação em cascata ou em bloco.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-188">An appbar can use [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) messages to exclude itself from the cascade or tile operation.</span></span> <span data-ttu-id="7a6bd-189">Para excluir a si mesmo, o AppBar deve se ocultar quando *lParam* for **true** e se mostrar quando *lParam* for **falso**.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-189">To exclude itself, the appbar should hide itself when *lParam* is **TRUE** and show itself when *lParam* is **FALSE**.</span></span> <span data-ttu-id="7a6bd-190">Se um AppBar se esconder em resposta a essa mensagem, ele não precisará enviar as mensagens [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) em resposta à operação em cascata ou em bloco.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-190">If an appbar hides itself in response to this message, it does not need to send the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages in response to the cascade or tile operation.</span></span>

## <a name="registering-an-application-desktop-toolbar"></a><span data-ttu-id="7a6bd-191">Registrando uma barra de ferramentas de área de trabalho do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7a6bd-191">Registering an Application Desktop Toolbar</span></span>

<span data-ttu-id="7a6bd-192">Um aplicativo deve registrar um AppBar enviando a [**\_ nova**](abm-new.md) mensagem do ABM.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-192">An application must register an appbar by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="7a6bd-193">O registro de um AppBar o adiciona à lista interna do sistema e fornece ao sistema um identificador de mensagem a ser usado para enviar mensagens de notificação para o AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-193">Registering an appbar adds it to the system's internal list and provides the system with a message identifier to use to send notification messages to the appbar.</span></span> <span data-ttu-id="7a6bd-194">Antes de sair, um aplicativo deve cancelar o registro do AppBar enviando a mensagem [**ABM \_ Remove**](abm-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-194">Before exiting, an application must unregister the appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="7a6bd-195">O cancelamento do registro remove o AppBar da lista interna do sistema e impede que a barra receba mensagens de notificação AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-195">Unregistering removes the appbar from the system's internal list and prevents the bar from receiving appbar notification messages.</span></span>

<span data-ttu-id="7a6bd-196">A função no exemplo a seguir registra ou cancela o registro de um AppBar, dependendo do valor de um parâmetro de sinalizador booliano.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-196">The function in the following example either registers or unregisters an appbar, depending on the value of a Boolean flag parameter.</span></span>


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a><span data-ttu-id="7a6bd-197">Definindo o tamanho e a posição de AppBar</span><span class="sxs-lookup"><span data-stu-id="7a6bd-197">Setting the Appbar Size and Position</span></span>

<span data-ttu-id="7a6bd-198">Um aplicativo deve definir o tamanho e a posição de um AppBar depois de registrar o AppBar, depois que o usuário move ou dimensiona o AppBar e sempre que o AppBar recebe a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-198">An application should set an appbar's size and position after registering the appbar, after the user user moves or sizes the appbar, and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="7a6bd-199">Antes de definir o tamanho e a posição do AppBar, o aplicativo consulta o sistema em busca de um retângulo delimitador aprovado enviando a mensagem [**\_ QUERYPOS do ABM**](abm-querypos.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-199">Before setting the size and position of the appbar, the application queries the system for an approved bounding rectangle by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="7a6bd-200">O sistema retorna um retângulo delimitador que não interfira na barra de tarefas ou em qualquer outro AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-200">The system returns a bounding rectangle that does not interfere with the taskbar or any other appbar.</span></span> <span data-ttu-id="7a6bd-201">O sistema ajusta o retângulo puramente por subtração de retângulo; Não faz nenhum esforço para preservar o tamanho inicial do retângulo.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-201">The system adjusts the rectangle purely by rectangle subtraction; it makes no effort to preserve the rectangle's initial size.</span></span> <span data-ttu-id="7a6bd-202">Por esse motivo, o AppBar deve reajustar o retângulo, conforme necessário, depois de enviar **ABM \_ QUERYPOS**.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-202">For this reason, the appbar should readjust the rectangle, as necessary, after sending **ABM\_QUERYPOS**.</span></span>

<span data-ttu-id="7a6bd-203">Em seguida, o aplicativo passa o retângulo delimitador de volta para o sistema usando a mensagem [**ABM \_ SETPOS**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="7a6bd-203">Next, the application passes the bounding rectangle back to the system by using the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span> <span data-ttu-id="7a6bd-204">Em seguida, ele chama a função [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para mover a AppBar para a posição.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-204">Then it calls the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="7a6bd-205">O exemplo a seguir mostra como definir o tamanho e a posição de um AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-205">The following example shows how to set an appbar's size and position.</span></span>


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a><span data-ttu-id="7a6bd-206">Processando mensagens de notificação AppBar</span><span class="sxs-lookup"><span data-stu-id="7a6bd-206">Processing Appbar Notification Messages</span></span>

<span data-ttu-id="7a6bd-207">Um AppBar recebe uma mensagem de notificação quando o estado da barra de tarefas é alterado, quando um aplicativo de tela inteira é iniciado (ou o último é fechado) ou quando ocorre um evento que pode afetar o tamanho e a posição do AppBar.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-207">An appbar receives a notification message when the state of the taskbar changes, when a full-screen application starts (or the last one closes), or when an event occurs that can affect the appbar's size and position.</span></span> <span data-ttu-id="7a6bd-208">O exemplo a seguir mostra como processar as várias mensagens de notificação.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-208">The following example shows how to process the various notification messages.</span></span>


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



<span data-ttu-id="7a6bd-209">A função a seguir ajusta o retângulo delimitador de um AppBar e, em seguida, chama a função AppBarQuerySetPos definida pelo aplicativo (incluída na seção anterior) para definir o tamanho e a posição da barra de acordo.</span><span class="sxs-lookup"><span data-stu-id="7a6bd-209">The following function adjusts an appbar's bounding rectangle and then calls the application-defined AppBarQuerySetPos function (included in the previous section) to set the bar's size and position accordingly.</span></span>


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
