---
description: A área de notificação é uma parte da barra de tarefas que fornece uma fonte temporária para notificações e status.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Notificações e a área de notificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296477"
---
# <a name="notifications-and-the-notification-area"></a><span data-ttu-id="6a204-103">Notificações e a área de notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-103">Notifications and the Notification Area</span></span>

<span data-ttu-id="6a204-104">A área de notificação é uma parte da barra de tarefas que fornece uma fonte temporária para notificações e status.</span><span class="sxs-lookup"><span data-stu-id="6a204-104">The notification area is a portion of the taskbar that provides a temporary source for notifications and status.</span></span> <span data-ttu-id="6a204-105">Ele também pode ser usado para exibir ícones de recursos do sistema e do programa que não têm nenhuma presença na área de trabalho, como nível da bateria, controle de volume e status da rede.</span><span class="sxs-lookup"><span data-stu-id="6a204-105">It can also be used to display icons for system and program features that have no presence on the desktop, such as battery level, volume control, and network status.</span></span> <span data-ttu-id="6a204-106">A área de notificação é conhecida historicamente como a área de status ou a bandeja do sistema.</span><span class="sxs-lookup"><span data-stu-id="6a204-106">The notification area has been known historically as the system tray or status area.</span></span>

<span data-ttu-id="6a204-107">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="6a204-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="6a204-108">Diretrizes de notificação e área de notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-108">Notification and Notification Area Guidelines</span></span>](#notification-and-notification-area-guidelines)
-   [<span data-ttu-id="6a204-109">Criando e exibindo uma notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-109">Creating and Displaying a Notification</span></span>](#notifications-and-the-notification-area)
    -   [<span data-ttu-id="6a204-110">Adicionar um ícone de notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-110">Add a Notification Icon</span></span>](#add-a-notification-icon)
    -   [<span data-ttu-id="6a204-111">Definir a versão do NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="6a204-111">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
    -   [<span data-ttu-id="6a204-112">Definir a aparência e o conteúdo da notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-112">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
    -   [<span data-ttu-id="6a204-113">Verificar o status do usuário</span><span class="sxs-lookup"><span data-stu-id="6a204-113">Check the User Status</span></span>](#check-the-user-status)
    -   [<span data-ttu-id="6a204-114">Exibir a notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-114">Display the Notification</span></span>](#display-the-notification)
    -   [<span data-ttu-id="6a204-115">Removendo um ícone</span><span class="sxs-lookup"><span data-stu-id="6a204-115">Removing an Icon</span></span>](#removing-an-icon)
-   [<span data-ttu-id="6a204-116">Exemplo de SDK</span><span class="sxs-lookup"><span data-stu-id="6a204-116">SDK Sample</span></span>](#sdk-sample)
-   [<span data-ttu-id="6a204-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a204-117">Related topics</span></span>](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a><span data-ttu-id="6a204-118">Diretrizes de notificação e área de notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-118">Notification and Notification Area Guidelines</span></span>

<span data-ttu-id="6a204-119">Consulte as seções da [área](../uxguide/winenv-notification.md) [notificações](../uxguide/mess-notif.md) e notificação das diretrizes de interação da experiência do usuário do Windows para obter as práticas recomendadas no uso de notificações e da área de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-119">See the [Notifications](../uxguide/mess-notif.md) and [Notification Area](../uxguide/winenv-notification.md) sections of the Windows User Experience Interaction Guidelines for best practices in the use of notifications and the notification area.</span></span> <span data-ttu-id="6a204-120">O objetivo é fornecer um benefício ao usuário por meio do uso apropriado de notificações, sem ser irritante ou distração.</span><span class="sxs-lookup"><span data-stu-id="6a204-120">The goal is to provide user benefit through appropriate use of notifications, without being annoying or distracting.</span></span>

<span data-ttu-id="6a204-121">A área de notificação não é para informações críticas que devem ser acionadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6a204-121">The notification area is not for critical information that must be acted on immediately.</span></span> <span data-ttu-id="6a204-122">Ele também não se destina a acesso rápido de programa ou comando.</span><span class="sxs-lookup"><span data-stu-id="6a204-122">It is also not intended for quick program or command access.</span></span> <span data-ttu-id="6a204-123">A partir do Windows 7, grande parte dessa funcionalidade é melhor realizada por meio do botão da barra de tarefas de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a204-123">As of Windows 7, much of that functionality is best accomplished through an application's taskbar button.</span></span>

<span data-ttu-id="6a204-124">O Windows 7 permite que um usuário omita todas as notificações de um aplicativo se elas escolherem, portanto, o design e o uso de notificações elaborados causará a inclinação do usuário para permitir que seu aplicativo continue a exibi-los.</span><span class="sxs-lookup"><span data-stu-id="6a204-124">Windows 7 allows a user to suppress all notifications from an application if they choose, so thoughtful notification design and use will incline the user to allow your application to continue to display them.</span></span> <span data-ttu-id="6a204-125">As notificações são uma interrupção; Certifique-se de que valem a pena.</span><span class="sxs-lookup"><span data-stu-id="6a204-125">Notifications are an interruption; ensure that they are worth it.</span></span>

<span data-ttu-id="6a204-126">O Windows 7 apresenta o conceito de "tempo de silêncio".</span><span class="sxs-lookup"><span data-stu-id="6a204-126">Windows 7 introduces the concept of "quiet time".</span></span> <span data-ttu-id="6a204-127">O tempo de silêncio é definido como a primeira hora depois que um novo usuário faz logon em sua conta pela primeira vez ou pela primeira vez após uma atualização do sistema operacional ou uma instalação limpa.</span><span class="sxs-lookup"><span data-stu-id="6a204-127">Quiet time is defined as the first hour after a new user logs into his or her account either for the first time or for the first time after an operating system upgrade or clean installation.</span></span> <span data-ttu-id="6a204-128">Esse tempo é reservado para permitir que o usuário Explore e se familiarize com o novo ambiente sem a distração de notificações.</span><span class="sxs-lookup"><span data-stu-id="6a204-128">This time is set aside to allow the user to explore and familiarize themselves with the new environment without the distraction of notifications.</span></span> <span data-ttu-id="6a204-129">Durante esse tempo, a maioria das notificações não deve ser enviada ou exibida.</span><span class="sxs-lookup"><span data-stu-id="6a204-129">During this time, most notifications should not be sent or shown.</span></span> <span data-ttu-id="6a204-130">As exceções incluem comentários que o usuário esperaria ver em resposta a uma ação do usuário, como quando ele se conecta a um dispositivo USB ou imprime um documento.</span><span class="sxs-lookup"><span data-stu-id="6a204-130">Exceptions include feedback that the user would expect to see in response to a user action, such as when he or she plugs in a USB device or prints a document.</span></span> <span data-ttu-id="6a204-131">As especificidades de API de em relação ao tempo de silêncio são discutidas posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="6a204-131">API specifics of regarding quiet time are discussed later in this topic.</span></span>

## <a name="creating-and-displaying-a-notification"></a><span data-ttu-id="6a204-132">Criando e exibindo uma notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-132">Creating and Displaying a Notification</span></span>

<span data-ttu-id="6a204-133">As seções restantes neste tópico descrevem o procedimento básico a ser seguido para exibir uma notificação do seu aplicativo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="6a204-133">The remaining sections in this topic outline the basic procedure to follow to display a notification from your application to the user.</span></span>

1.  [<span data-ttu-id="6a204-134">Adicionar um ícone de notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-134">Add a Notification Icon</span></span>](#add-a-notification-icon)
2.  [<span data-ttu-id="6a204-135">Definir a versão do NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="6a204-135">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
3.  [<span data-ttu-id="6a204-136">Definir a aparência e o conteúdo da notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-136">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
4.  [<span data-ttu-id="6a204-137">Verificar o status do usuário</span><span class="sxs-lookup"><span data-stu-id="6a204-137">Check the User Status</span></span>](#check-the-user-status)
5.  [<span data-ttu-id="6a204-138">Exibir a notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-138">Display the Notification</span></span>](#display-the-notification)
6.  [<span data-ttu-id="6a204-139">Removendo um ícone</span><span class="sxs-lookup"><span data-stu-id="6a204-139">Removing an Icon</span></span>](#removing-an-icon)

### <a name="add-a-notification-icon"></a><span data-ttu-id="6a204-140">Adicionar um ícone de notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-140">Add a Notification Icon</span></span>

<span data-ttu-id="6a204-141">Para exibir uma notificação, você deve ter um ícone na área de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-141">To display a notification, you must have an icon in the notification area.</span></span> <span data-ttu-id="6a204-142">Em determinados casos, como o Microsoft Communicator ou o nível da bateria, esse ícone já estará presente.</span><span class="sxs-lookup"><span data-stu-id="6a204-142">In certain cases, such as Microsoft Communicator or battery level, that icon will already be present.</span></span> <span data-ttu-id="6a204-143">Em muitos outros casos, no entanto, você adicionará um ícone à área de notificação somente contanto que seja necessário para mostrar a notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-143">In many other cases, however, you will add an icon to the notification area only as long as is needed to show the notification.</span></span> <span data-ttu-id="6a204-144">Em ambos os casos, isso é feito usando a função [**\_ NotifyIcon do Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .</span><span class="sxs-lookup"><span data-stu-id="6a204-144">In either case, this is accomplished using the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) function.</span></span> <span data-ttu-id="6a204-145">**Shell \_ do NotifyIcon** permite adicionar, modificar ou excluir um ícone na área de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-145">**Shell\_NotifyIcon** allows you to add, modify, or delete an icon in the notification area.</span></span>

![área de notificação contendo três ícones](images/taskbar/notificationareaicons.png)

<span data-ttu-id="6a204-147">Quando um ícone é adicionado à área de notificação no Windows 7, ele é adicionado à seção de estouro da área de notificação por padrão.</span><span class="sxs-lookup"><span data-stu-id="6a204-147">When an icon is added to the notification area on Windows 7, it is added to the overflow section of the notification area by default.</span></span> <span data-ttu-id="6a204-148">Essa área contém ícones de área de notificação que estão ativos, mas que não estão visíveis na área de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-148">This area contains notification area icons that are active, but not visible in the notification area.</span></span> <span data-ttu-id="6a204-149">Somente o usuário pode promover um ícone do estouro para a área de notificação, embora em determinadas circunstâncias o sistema possa promover temporariamente um ícone para a área de notificação como uma breve visualização (em um minuto).</span><span class="sxs-lookup"><span data-stu-id="6a204-149">Only the user can promote an icon from the overflow to the notification area, although in certain circumstances the system can temporarily promote an icon into the notification area as a short preview (under one minute).</span></span>

> [!Note]  
> <span data-ttu-id="6a204-150">O usuário deve ter a dizer final sobre quais ícones eles desejam ver na área de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-150">The user should have the final say on which icons they want to see in their notification area.</span></span> <span data-ttu-id="6a204-151">Antes de instalar um ícone não transitório na área de notificação, o usuário deve receber uma solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="6a204-151">Before installing a non-transient icon in the notification area, the user should be asked for permission.</span></span> <span data-ttu-id="6a204-152">Eles também devem receber a opção (normalmente, embora seu menu de atalho) Remova o ícone da área de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-152">They should also be given the option (normally though its shortcut menu) to remove the icon from the notification area.</span></span>

 

<span data-ttu-id="6a204-153">A estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) enviada na chamada para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contém informações que especificam o ícone da área de notificação e a própria notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-153">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification itself.</span></span> <span data-ttu-id="6a204-154">Estes são os itens específicos para o ícone da área de notificação em si, que podem ser definidos por meio de **NOTIFYICONDATA**.</span><span class="sxs-lookup"><span data-stu-id="6a204-154">The following are those items specific to the notification area icon itself that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="6a204-155">O recurso do qual o ícone é tirado.</span><span class="sxs-lookup"><span data-stu-id="6a204-155">The resource from which the icon is taken.</span></span>
-   <span data-ttu-id="6a204-156">Um identificador exclusivo para o ícone.</span><span class="sxs-lookup"><span data-stu-id="6a204-156">A unique identifier for the icon.</span></span>
-   <span data-ttu-id="6a204-157">O estilo da dica de ferramenta do ícone.</span><span class="sxs-lookup"><span data-stu-id="6a204-157">The style of the icon's tooltip.</span></span>
-   <span data-ttu-id="6a204-158">O estado do ícone (oculto, compartilhado ou ambos) na área de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-158">The icon's state (hidden, shared, or both) in the notification area.</span></span>
-   <span data-ttu-id="6a204-159">O identificador de uma janela de aplicativo associada ao ícone.</span><span class="sxs-lookup"><span data-stu-id="6a204-159">The handle of an application window associated with the icon.</span></span>
-   <span data-ttu-id="6a204-160">Um identificador de mensagem de retorno de chamada que permite que o ícone comunique eventos que ocorrem dentro do retângulo delimitador do ícone e a notificação de balão com a janela do aplicativo associada.</span><span class="sxs-lookup"><span data-stu-id="6a204-160">A callback message identifier that allows the icon to communicate events that occur within the icon's bounding rectangle and balloon notification with the associated application window.</span></span> <span data-ttu-id="6a204-161">O retângulo delimitador do ícone pode ser recuperado por meio do [**shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span><span class="sxs-lookup"><span data-stu-id="6a204-161">The icon's bounding rectangle can be retrieved through [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span></span>

<span data-ttu-id="6a204-162">Cada ícone na área de notificação pode ser identificado de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="6a204-162">Each icon in the notification area can be identified in two ways:</span></span>

-   <span data-ttu-id="6a204-163">O GUID com o qual o ícone é declarado no registro.</span><span class="sxs-lookup"><span data-stu-id="6a204-163">The GUID with which the icon is declared in the registry.</span></span> <span data-ttu-id="6a204-164">Esse é o método preferencial no Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="6a204-164">This is the preferred method on Windows 7 and later.</span></span>
-   <span data-ttu-id="6a204-165">O identificador de uma janela associada ao ícone da área de notificação, além de um identificador de ícone definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a204-165">The handle of a window associated with the notification area icon, plus an application-defined icon identifier.</span></span> <span data-ttu-id="6a204-166">Esse método é usado no Windows Vista e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="6a204-166">This method is used on Windows Vista and earlier.</span></span>

<span data-ttu-id="6a204-167">Os ícones na área de notificação podem ter uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="6a204-167">Icons in the notification area can have a tooltip.</span></span> <span data-ttu-id="6a204-168">A dica de ferramenta pode ser uma dica de ferramenta padrão (preferencial) ou uma interface do usuário de pop-up, desenhada por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a204-168">The tooltip can be either a standard tooltip (preferred) or an application-drawn, pop-up UI.</span></span> <span data-ttu-id="6a204-169">Embora uma dica de ferramenta não seja necessária, é recomendável.</span><span class="sxs-lookup"><span data-stu-id="6a204-169">While a tooltip is not required, it is recommended.</span></span>

<span data-ttu-id="6a204-170">Os ícones da área de notificação devem ter reconhecimento de DPI alta.</span><span class="sxs-lookup"><span data-stu-id="6a204-170">Notification area icons should be high-DPI aware.</span></span> <span data-ttu-id="6a204-171">Um aplicativo deve fornecer um ícone de 16x16 pixels e um ícone de 32x32 em seu arquivo de recurso e, em seguida, usar [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) para garantir que o ícone correto seja carregado e dimensionado adequadamente.</span><span class="sxs-lookup"><span data-stu-id="6a204-171">An application should provide both a 16x16 pixel icon and a 32x32 icon in its resource file, and then use [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) to ensure that the correct icon is loaded and scaled appropriately.</span></span>

<span data-ttu-id="6a204-172">O aplicativo responsável pelo ícone da área de notificação deve lidar com um clique do mouse para esse ícone.</span><span class="sxs-lookup"><span data-stu-id="6a204-172">The application responsible for the notification area icon should handle a mouse click for that icon.</span></span> <span data-ttu-id="6a204-173">Quando um usuário clica com o botão direito do mouse no ícone, ele deve abrir um menu de atalho normal.</span><span class="sxs-lookup"><span data-stu-id="6a204-173">When a user right-clicks the icon, it should bring up a normal shortcut menu.</span></span> <span data-ttu-id="6a204-174">No entanto, o resultado de um único clique com o botão esquerdo do mouse irá variar com a função do ícone.</span><span class="sxs-lookup"><span data-stu-id="6a204-174">However, the result of a single click with the left mouse button will vary with the function of the icon.</span></span> <span data-ttu-id="6a204-175">Ele deve exibir o que o usuário esperaria ver no formulário mais adequado para esse conteúdo — uma janela pop-up, uma caixa de diálogo ou a própria janela do programa.</span><span class="sxs-lookup"><span data-stu-id="6a204-175">It should display what the user would expect to see in the form best suited to that content—a popup window, a dialog box or the program window itself.</span></span> <span data-ttu-id="6a204-176">Por exemplo, ele pode mostrar o texto de status de um ícone de status ou um controle deslizante para o controle de volume.</span><span class="sxs-lookup"><span data-stu-id="6a204-176">For instance, it could show status text for a status icon, or a slider for the volume control.</span></span>

<span data-ttu-id="6a204-177">O posicionamento de uma janela pop-up ou caixa de diálogo que resulta do clique deve ser colocado próximo à coordenada do clique na área de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-177">The placement of a popup window or dialog box that results from the click should be placed near the coordinate of the click in the notification area.</span></span> <span data-ttu-id="6a204-178">Use o [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) para determinar sua localização.</span><span class="sxs-lookup"><span data-stu-id="6a204-178">Use the [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) to determine its location.</span></span>

<span data-ttu-id="6a204-179">O ícone pode ser adicionado à área de notificação sem exibir uma notificação definindo somente os membros específicos do ícone de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (discutidos acima) e chamando o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="6a204-179">The icon can be added to the notification area without displaying a notification by defining only the icon-specific members of [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (discussed above) and calling [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) as shown here:</span></span>


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



<span data-ttu-id="6a204-180">Você também pode adicionar o ícone à área de notificação e exibir uma notificação em uma chamada para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="6a204-180">You can also add the icon to the notification area and display a notification all in one call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="6a204-181">Para fazer isso, continue com as instruções neste tópico.</span><span class="sxs-lookup"><span data-stu-id="6a204-181">To do so, continue with the instructions in this topic.</span></span>

### <a name="define-the-notifyicondata-version"></a><span data-ttu-id="6a204-182">Definir a versão do NOTIFYICONDATA</span><span class="sxs-lookup"><span data-stu-id="6a204-182">Define the NOTIFYICONDATA Version</span></span>

<span data-ttu-id="6a204-183">À medida que o Windows progrediu, a estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) expandiu-se para incluir mais membros para definir mais funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="6a204-183">As Windows has progressed, the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure has expanded to include more members to define more functionality.</span></span> <span data-ttu-id="6a204-184">As constantes são usadas para declarar qual versão do **NOTIFYICONDATA** usar com o ícone da área de notificação para permitir a compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="6a204-184">Constants are used to declare which version of **NOTIFYICONDATA** to use with your notification area icon, to allow for backward compatibility.</span></span> <span data-ttu-id="6a204-185">A menos que haja um motivo convincente para fazer o contrário, é altamente recomendável que você use a \_ versão do NOTIFYICON versão \_ 4, introduzida no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a204-185">Unless there is a compelling reason to do otherwise, it is strongly recommended that you use the NOTIFYICON\_VERSION\_4 version, introduced in Windows Vista.</span></span> <span data-ttu-id="6a204-186">Essa versão fornece a funcionalidade completa disponível, incluindo a capacidade preferida de identificar o ícone da área de notificação, embora um GUID registrado, um mecanismo de retorno de chamada superior e melhor acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="6a204-186">This version provides the full available functionality, including the preferred ability to identify the notification area icon though a registered GUID, a superior callback mechanism, and better accessibility.</span></span>

<span data-ttu-id="6a204-187">Defina a versão por meio das seguintes chamadas:</span><span class="sxs-lookup"><span data-stu-id="6a204-187">Set the version through the following calls:</span></span>


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



<span data-ttu-id="6a204-188">Observe que essa chamada para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) não exibe uma notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-188">Note that this call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) does not display a notification.</span></span>

### <a name="define-the-notification-look-and-contents"></a><span data-ttu-id="6a204-189">Definir a aparência e o conteúdo da notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-189">Define the Notification Look and Contents</span></span>

<span data-ttu-id="6a204-190">Uma notificação é um tipo especial de controle de dica de ferramenta de balão.</span><span class="sxs-lookup"><span data-stu-id="6a204-190">A notification is a special type of balloon tooltip control.</span></span> <span data-ttu-id="6a204-191">Ele contém um título, corpo de texto e um ícone.</span><span class="sxs-lookup"><span data-stu-id="6a204-191">It contains a title, body text, and an icon.</span></span> <span data-ttu-id="6a204-192">Como uma janela, ele tem um botão **fechar** no canto superior direito.</span><span class="sxs-lookup"><span data-stu-id="6a204-192">Like a window, it has a **Close** button in its upper right corner.</span></span> <span data-ttu-id="6a204-193">Ele também contém um botão **Opções** que abre o item ícones da área de notificação no painel de controle, que permite ao usuário mostrar ou ocultar o ícone ou mostrar apenas as notificações sem um ícone.</span><span class="sxs-lookup"><span data-stu-id="6a204-193">It also contains a **Options** button that opens the Notification Area Icons item in the Control Panel, which allows the user to show or hide the icon or show only notifications without an icon.</span></span>

![captura de tela do balão de notificação indicando que a energia da bateria está baixa](images/taskbar/notificationballoon.png)

<span data-ttu-id="6a204-195">A estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) enviada na chamada para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contém informações que especificam o ícone da área de notificação e o próprio balão de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-195">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification balloon itself.</span></span> <span data-ttu-id="6a204-196">Estes são os itens específicos para a notificação que podem ser definidos por meio de **NOTIFYICONDATA**.</span><span class="sxs-lookup"><span data-stu-id="6a204-196">The following are those items specific to the notification that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="6a204-197">Um ícone a ser exibido no balão de notificação, que é especificado pelo tipo de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-197">An icon to display in the notification balloon, which is specified by the notification type.</span></span> <span data-ttu-id="6a204-198">O tamanho do ícone pode ser especificado, bem como ícones personalizados.</span><span class="sxs-lookup"><span data-stu-id="6a204-198">The size of the icon can be specified, as well as custom icons.</span></span>
-   <span data-ttu-id="6a204-199">Um título de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-199">A notification title.</span></span> <span data-ttu-id="6a204-200">Este título deve ter no máximo 48 caracteres de comprimento em inglês (para acomodar a localização).</span><span class="sxs-lookup"><span data-stu-id="6a204-200">This title should be a maximum of 48 characters long in English (to accommodate localization).</span></span> <span data-ttu-id="6a204-201">O título é a primeira linha da notificação e é definido de acordo com o uso do tamanho da fonte, da cor e do peso.</span><span class="sxs-lookup"><span data-stu-id="6a204-201">The title is the first line of the notification, and set apart through the use of font size, color, and weight.</span></span>
-   <span data-ttu-id="6a204-202">Texto a ser usado no corpo da notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-202">Text for use in the body of the notification.</span></span> <span data-ttu-id="6a204-203">Esse texto deve ter no máximo 200 caracteres em inglês (para acomodar a localização).</span><span class="sxs-lookup"><span data-stu-id="6a204-203">This text should be a maximum of 200 characters in English (to accommodate localization).</span></span>
-   <span data-ttu-id="6a204-204">Se a notificação deve ser descartada se não puder ser exibida imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6a204-204">Whether the notification should be discarded if it cannot be displayed immediately.</span></span>
-   <span data-ttu-id="6a204-205">Um tempo limite para a notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-205">A timeout for the notification.</span></span> <span data-ttu-id="6a204-206">Essa configuração é ignorada no Windows Vista e em sistemas posteriores em favor de uma configuração de tempo limite de acessibilidade em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="6a204-206">This setting is ignored in Windows Vista and later systems in favor of a system-wide accessibility timeout setting.</span></span>
-   <span data-ttu-id="6a204-207">Se a notificação deve respeitar o tempo de silêncio, defina por meio do sinalizador [**NIIF \_ respeitar o \_ \_ tempo de silêncio**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) .</span><span class="sxs-lookup"><span data-stu-id="6a204-207">Whether the notification should respect quiet time, set through the [**NIIF\_RESPECT\_QUIET\_TIME**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) flag.</span></span>

> [!Note]  
> <span data-ttu-id="6a204-208">As interfaces [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) e [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) são wrappers Component Object Model (com) para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="6a204-208">The [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) and [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) interfaces are Component Object Model (COM) wrappers for [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="6a204-209">No entanto, neste momento, eles não fornecem a funcionalidade totalmente NOTIFYICON da \_ versão \_ 4 disponível por meio do **shell \_ NotifyIcon** diretamente, incluindo o uso de um GUID para identificar o ícone da área de notificação.</span><span class="sxs-lookup"><span data-stu-id="6a204-209">However, at this time, they do not provide the full NOTIFYICON\_VERSION\_4 functionality available through **Shell\_NotifyIcon** directly, including the use of a GUID to identify the notification area icon.</span></span>

 

### <a name="check-the-user-status"></a><span data-ttu-id="6a204-210">Verificar o status do usuário</span><span class="sxs-lookup"><span data-stu-id="6a204-210">Check the User Status</span></span>

<span data-ttu-id="6a204-211">O sistema usa a função [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) é usada para verificar se o usuário está em tempo de silêncio, fora do computador ou em um estado ininterrupto, como o modo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="6a204-211">The system uses the [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) function is used to check whether the user is in quiet time, away from the computer, or in an uninterruptable state such as Presentation mode.</span></span> <span data-ttu-id="6a204-212">Se o sistema exibe sua notificação depende desse Estado.</span><span class="sxs-lookup"><span data-stu-id="6a204-212">Whether the system displays your notification depends on this state.</span></span>

> [!Note]  
> <span data-ttu-id="6a204-213">Se seu aplicativo estiver usando um método de notificação personalizado que não usa [**o \_ shell NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)ou [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), ele deverá sempre chamar explicitamente [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) para determinar se ele deve exibir a interface do usuário de notificação nesse momento.</span><span class="sxs-lookup"><span data-stu-id="6a204-213">If your application is using a custom notification method that does not use [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification), or [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), it should always explicitly call [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) to determine whether it should display notification UI at that time.</span></span>

 

<span data-ttu-id="6a204-214">As notificações enviadas quando o usuário está ausente são enfileiradas para exibição, mas como não é possível saber quando o usuário retornará ou se a notificação ainda será válida nesse momento, você poderá considerar reenviar a notificação mais tarde.</span><span class="sxs-lookup"><span data-stu-id="6a204-214">Notifications sent when the user is away are queued for display, but because you cannot know when the user will return or whether the notification will still be valid at that time, you might consider resending the notification later.</span></span>

<span data-ttu-id="6a204-215">As notificações enviadas durante o tempo de silêncio são descartadas não mostradas.</span><span class="sxs-lookup"><span data-stu-id="6a204-215">Notifications sent during quiet time are discarded unshown.</span></span> <span data-ttu-id="6a204-216">As diretrizes de design solicitam que todas as notificações sejam ignoradas.</span><span class="sxs-lookup"><span data-stu-id="6a204-216">Design guidelines ask that all notifications be ignorable.</span></span> <span data-ttu-id="6a204-217">Eles não devem exigir ação imediata do usuário.</span><span class="sxs-lookup"><span data-stu-id="6a204-217">They should not require immediate user action.</span></span> <span data-ttu-id="6a204-218">Portanto, nenhuma notificação é tão importante que ela deve substituir o tempo de silêncio.</span><span class="sxs-lookup"><span data-stu-id="6a204-218">Therefore, no notification is so important that it should override quiet time.</span></span>

### <a name="display-the-notification"></a><span data-ttu-id="6a204-219">Exibir a notificação</span><span class="sxs-lookup"><span data-stu-id="6a204-219">Display the Notification</span></span>

<span data-ttu-id="6a204-220">Depois de ter definido a versão [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e definido a notificação em uma estrutura **NOTIFYICONDATA** , chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para exibir o ícone.</span><span class="sxs-lookup"><span data-stu-id="6a204-220">Once you have set the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) version and defined the notification in a **NOTIFYICONDATA** structure, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to display the icon.</span></span>

-   <span data-ttu-id="6a204-221">Se o ícone da área de notificação não estiver presente, chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para adicionar o ícone.</span><span class="sxs-lookup"><span data-stu-id="6a204-221">If the notification area icon is not present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to add the icon.</span></span> <span data-ttu-id="6a204-222">Faça isso para ícones transitórios e não transitórios.</span><span class="sxs-lookup"><span data-stu-id="6a204-222">Do this for both transient and non-transient icons.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   <span data-ttu-id="6a204-223">Se o ícone da área de notificação já estiver presente, chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para modificar o ícone.</span><span class="sxs-lookup"><span data-stu-id="6a204-223">If the notification area icon is already present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to modify the icon.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

<span data-ttu-id="6a204-224">O código a seguir mostra um exemplo de como definir dados de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e enviá-los por meio do [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="6a204-224">The following code shows an example of setting [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) data and sending it through [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="6a204-225">Observe que este exemplo identifica o ícone de notificação por meio de um GUID (preferencial no Windows 7).</span><span class="sxs-lookup"><span data-stu-id="6a204-225">Note that this example identifies the notification icon through a GUID (preferred in Windows 7).</span></span>


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a><span data-ttu-id="6a204-226">Removendo um ícone</span><span class="sxs-lookup"><span data-stu-id="6a204-226">Removing an Icon</span></span>

<span data-ttu-id="6a204-227">Para remover um ícone — por exemplo, quando você adicionou apenas o ícone temporariamente para transmitir uma notificação — chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="6a204-227">To remove an icon—for instance, when you have only added the icon temporarily to broadcast a notification—call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)as shown here.</span></span> <span data-ttu-id="6a204-228">Somente uma estrutura de [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) mínima que identifica o ícone é necessária nesta chamada.</span><span class="sxs-lookup"><span data-stu-id="6a204-228">Only a minimal [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure that identifies the icon is needed in this call.</span></span>


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> <span data-ttu-id="6a204-229">Quando um aplicativo é desinstalado, seu ícone da área de notificação ainda pode aparecer para o usuário como uma opção na página ícones da área de notificação no painel de controle por até sete dias.</span><span class="sxs-lookup"><span data-stu-id="6a204-229">When an application is uninstalled, its notification area icon can still appear to the user as an option in the Notification Area Icons page in the Control Panel for up to seven days.</span></span> <span data-ttu-id="6a204-230">No entanto, qualquer alteração feita ali não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="6a204-230">However, any changes made there will have no effect.</span></span>

 

## <a name="sdk-sample"></a><span data-ttu-id="6a204-231">Exemplo de SDK</span><span class="sxs-lookup"><span data-stu-id="6a204-231">SDK Sample</span></span>

<span data-ttu-id="6a204-232">Consulte o exemplo de exemplo [NotificationIcon](samples-notificationicon.md) no SDK (Software Development Kit) do Windows para obter um exemplo completo do uso [**de \_ NotifyIcon do Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="6a204-232">See the [NotificationIcon Sample](samples-notificationicon.md) sample in the Windows Software Development Kit (SDK) for a full example of the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a204-233">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a204-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a204-234">**NotifyIcon do Shell \_**</span><span class="sxs-lookup"><span data-stu-id="6a204-234">**Shell\_NotifyIcon**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[<span data-ttu-id="6a204-235">**NotifyIconGetRect do Shell \_**</span><span class="sxs-lookup"><span data-stu-id="6a204-235">**Shell\_NotifyIconGetRect**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[<span data-ttu-id="6a204-236">**NOTIFYICONDATA**</span><span class="sxs-lookup"><span data-stu-id="6a204-236">**NOTIFYICONDATA**</span></span>](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[<span data-ttu-id="6a204-237">**SHQueryUserNotificationState**</span><span class="sxs-lookup"><span data-stu-id="6a204-237">**SHQueryUserNotificationState**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[<span data-ttu-id="6a204-238">**IUserNotification**</span><span class="sxs-lookup"><span data-stu-id="6a204-238">**IUserNotification**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[<span data-ttu-id="6a204-239">**IUserNotification2**</span><span class="sxs-lookup"><span data-stu-id="6a204-239">**IUserNotification2**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[<span data-ttu-id="6a204-240">A barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="6a204-240">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="6a204-241">Extensões da barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="6a204-241">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
