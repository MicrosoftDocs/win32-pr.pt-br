---
description: ControlEvents são análogos a mensagens do Microsoft Windows em aplicativos baseados no Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Visão geral do ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837112"
---
# <a name="controlevent-overview"></a><span data-ttu-id="d2174-103">Visão geral do ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-103">ControlEvent Overview</span></span>

<span data-ttu-id="d2174-104">ControlEvents são análogos a mensagens do Microsoft Windows em aplicativos baseados no Win32.</span><span class="sxs-lookup"><span data-stu-id="d2174-104">ControlEvents are analogous to Microsoft Windows messages in Win32-based applications.</span></span> <span data-ttu-id="d2174-105">No entanto, em vez de criar uma função de retorno de chamada para receber mensagens do Windows e enviar mensagens do Windows com a função [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) , o instalador da interface do usuário (IU) e os controles publicam [ControlEvents](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="d2174-105">However, rather than creating a callback function to receive Windows messages and sending Windows messages with the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function, the user interface (UI) installer and controls publish [ControlEvents](control-events.md).</span></span> <span data-ttu-id="d2174-106">Outros controles e o instalador podem ser especificados para assinar ControlEvents específicos que, em seguida, alterarão os atributos do controle de assinatura.</span><span class="sxs-lookup"><span data-stu-id="d2174-106">Other controls and the installer can be specified to subscribe to particular ControlEvents that will then change attributes of the subscribing control.</span></span> <span data-ttu-id="d2174-107">Para adicionar controles de trabalho a caixas de diálogo, o autor da interface do usuário especifica a publicação de ControlEvents na [tabela ControlEvent,](controlevent-table.md) e assina os controles em ControlEvents na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="d2174-107">To add working controls to dialog boxes, the author of the UI specifies the publication of ControlEvents in the [ControlEvent table](controlevent-table.md) and subscribes controls to ControlEvents in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="d2174-108">O instalador publicará os seguintes eventos nos controles de assinatura listados na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="d2174-108">The installer will publish the following events to subscribing controls listed in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="d2174-109">Um controle [ProgressBar](progressbar-control.md) ou [controle de mensagem](billboard-control.md) normalmente se inscreve em setProgress, o restante é assinado por [controles de texto](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="d2174-109">A [ProgressBar control](progressbar-control.md) or [Billboard control](billboard-control.md) typically subscribes to SetProgress, the rest are subscribed to by [Text controls](text-control.md).</span></span>

[<span data-ttu-id="d2174-110">ActionData ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-110">ActionData ControlEvent</span></span>](actiondata-controlevent.md)

[<span data-ttu-id="d2174-111">ActionText ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-111">ActionText ControlEvent</span></span>](actiontext-controlevent.md)

[<span data-ttu-id="d2174-112">ControlEvent, de reprogress</span><span class="sxs-lookup"><span data-stu-id="d2174-112">SetProgress ControlEvent</span></span>](setprogress-controlevent.md)

[<span data-ttu-id="d2174-113">ControlEvent, do timecontinueing</span><span class="sxs-lookup"><span data-stu-id="d2174-113">TimeRemaining ControlEvent</span></span>](timeremaining-controlevent.md)

[<span data-ttu-id="d2174-114">ScriptInProgress ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-114">ScriptInProgress ControlEvent</span></span>](scriptinprogress-controlevent.md)

<span data-ttu-id="d2174-115">Os eventos a seguir são publicados pelo controle quando a seleção de item é movida em um controle [SelectionTree](selectiontree-control.md) ou [directorylist](directorylist-control.md).</span><span class="sxs-lookup"><span data-stu-id="d2174-115">The following events are published by the control when the item selection is moved in a [SelectionTree control](selectiontree-control.md) or [DirectoryList Control](directorylist-control.md).</span></span> <span data-ttu-id="d2174-116">Os controles de assinatura devem estar localizados na mesma caixa de diálogo e listados na tabela EventMappings.</span><span class="sxs-lookup"><span data-stu-id="d2174-116">Subscribing controls must be located on the same dialog box and listed in the EventMapping table.</span></span>

[<span data-ttu-id="d2174-117">IgnoreChange ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-117">IgnoreChange ControlEvent</span></span>](ignorechange-controlevent.md)

[<span data-ttu-id="d2174-118">SelectionDescription ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-118">SelectionDescription ControlEvent</span></span>](selectiondescription-controlevent.md)

[<span data-ttu-id="d2174-119">SelectionSize ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-119">SelectionSize ControlEvent</span></span>](selectionsize-controlevent.md)

[<span data-ttu-id="d2174-120">SelectionPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-120">SelectionPath ControlEvent</span></span>](selectionpath-controlevent.md)

[<span data-ttu-id="d2174-121">ControlEvent, selectionaction</span><span class="sxs-lookup"><span data-stu-id="d2174-121">SelectionAction ControlEvent</span></span>](selectionaction-controlevent.md)

[<span data-ttu-id="d2174-122">SelectionNoItems ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-122">SelectionNoItems ControlEvent</span></span>](selectionnoitems-controlevent.md)

<span data-ttu-id="d2174-123">Os ControlEvents a seguir podem ser publicados a critério de um usuário interagindo com um controle de [pressão](pushbutton-control.md) ou [controle de caixa de seleção](checkbox-control.md) em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d2174-123">The following ControlEvents can be published at the discretion of a user by interacting with a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) on a dialog box.</span></span> <span data-ttu-id="d2174-124">O controle CheckBox só pode publicar os eventos ADDLOCAL, addsource, remove, DoAction e SetProperty.</span><span class="sxs-lookup"><span data-stu-id="d2174-124">The Checkbox control can only publish the AddLocal, AddSource, Remove, DoAction, and SetProperty events.</span></span> <span data-ttu-id="d2174-125">Com as versões Windows Installer fornecidas com o Windows Server 2003 e posterior, o [controle SelectionTree](selectiontree-control.md) pode publicar o ControlEvents DoAction, ControlEvent, e SetProperty.</span><span class="sxs-lookup"><span data-stu-id="d2174-125">With Windows Installer versions that shipped with Windows Server 2003 and later, the [SelectionTree control](selectiontree-control.md) can publish the DoAction, ControlEvent and SetProperty ControlEvents.</span></span> <span data-ttu-id="d2174-126">O autor da interface do usuário deve listar o ControlEvent, na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="d2174-126">The author of the UI should list the ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="d2174-127">O manipulador de interface do usuário do instalador é o assinante desses eventos.</span><span class="sxs-lookup"><span data-stu-id="d2174-127">The UI handler of the installer is the subscriber to these events.</span></span>

[<span data-ttu-id="d2174-128">ControlEvent, ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="d2174-128">AddLocal ControlEvent</span></span>](addlocal-controlevent.md)

[<span data-ttu-id="d2174-129">ControlEvent, addsource</span><span class="sxs-lookup"><span data-stu-id="d2174-129">AddSource ControlEvent</span></span>](addsource-controlevent.md)

[<span data-ttu-id="d2174-130">CheckExistingTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-130">CheckExistingTargetPath ControlEvent</span></span>](checkexistingtargetpath-controlevent.md)

[<span data-ttu-id="d2174-131">CheckTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-131">CheckTargetPath ControlEvent</span></span>](checktargetpath-controlevent.md)

[<span data-ttu-id="d2174-132">ControlEvent, de doação</span><span class="sxs-lookup"><span data-stu-id="d2174-132">DoAction ControlEvent</span></span>](doaction-controlevent.md)

[<span data-ttu-id="d2174-133">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-133">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

[<span data-ttu-id="d2174-134">EndDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-134">EndDialog ControlEvent</span></span>](enddialog-controlevent.md)

[<span data-ttu-id="d2174-135">NewDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-135">NewDialog ControlEvent</span></span>](newdialog-controlevent.md)

[<span data-ttu-id="d2174-136">Reinstalar o ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-136">Reinstall ControlEvent</span></span>](reinstall-controlevent.md)

[<span data-ttu-id="d2174-137">Reinstalar o ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-137">ReinstallMode ControlEvent</span></span>](reinstallmode-controlevent.md)

[<span data-ttu-id="d2174-138">Remover ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-138">Remove ControlEvent</span></span>](remove-controlevent.md)

[<span data-ttu-id="d2174-139">Redefinir ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-139">Reset ControlEvent</span></span>](reset-controlevent.md)

[<span data-ttu-id="d2174-140">SetInstallLevel ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-140">SetInstallLevel ControlEvent</span></span>](setinstalllevel-controlevent.md)

[<span data-ttu-id="d2174-141">ControlEvent, SetProperty</span><span class="sxs-lookup"><span data-stu-id="d2174-141">SetProperty ControlEvent</span></span>](setproperty-controlevent.md)

[<span data-ttu-id="d2174-142">SetTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-142">SetTargetPath ControlEvent</span></span>](settargetpath-controlevent.md)

[<span data-ttu-id="d2174-143">SpawnDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-143">SpawnDialog ControlEvent</span></span>](spawndialog-controlevent.md)

[<span data-ttu-id="d2174-144">SpawnWaitDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-144">SpawnWaitDialog ControlEvent</span></span>](spawnwaitdialog-controlevent.md)

[<span data-ttu-id="d2174-145">ValidateProductID ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-145">ValidateProductID ControlEvent</span></span>](validateproductid-controlevent.md)

<span data-ttu-id="d2174-146">Um [controle de pressão](pushbutton-control.md) pode publicar os eventos a seguir em um controle [SelectionTree](selectiontree-control.md) ou um controle [directorylist](directorylist-control.md) da assinatura localizado na mesma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d2174-146">A [PushButton control](pushbutton-control.md) can publish the following events to a subscribing [SelectionTree control](selectiontree-control.md) or [DirectoryList control](directorylist-control.md) located in the same dialog box.</span></span> <span data-ttu-id="d2174-147">O controle de pressão deve ser listado na tabela ControlEvent, e os controles de assinatura devem ser listados na tabela EventMappings.</span><span class="sxs-lookup"><span data-stu-id="d2174-147">The PushButton Control should be listed in the ControlEvent table and the subscribing controls should be listed in the EventMapping table.</span></span>

[<span data-ttu-id="d2174-148">SelectionBrowse ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-148">SelectionBrowse ControlEvent</span></span>](selectionbrowse-controlevent.md)

[<span data-ttu-id="d2174-149">DirectoryListUp ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-149">DirectoryListUp ControlEvent</span></span>](directorylistup-controlevent.md)

[<span data-ttu-id="d2174-150">DirectoryListNew ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-150">DirectoryListNew ControlEvent</span></span>](directorylistnew-controlevent.md)

[<span data-ttu-id="d2174-151">DirectoryListOpen ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2174-151">DirectoryListOpen ControlEvent</span></span>](directorylistopen-controlevent.md)

<span data-ttu-id="d2174-152">Eventos de controle geralmente exigem que a interface do usuário seja executada no nível [*completo da interface do usuário*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d2174-152">Control events generally require that the UI be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="d2174-153">A maioria dos ControlEvents não funcionará com uma [*interface do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md) , pois esses níveis só exibem caixas de diálogo sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="d2174-153">Most ControlEvents will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md) because these levels only display modeless dialog boxes.</span></span> <span data-ttu-id="d2174-154">Os eventos ActionText, addsource, setProgress, timepersisting e ScriptInProgress são exceções e funcionarão na interface do usuário reduzida ou básica.</span><span class="sxs-lookup"><span data-stu-id="d2174-154">The ActionText, AddSource, SetProgress, TimeRemaining, and ScriptInProgress events are exceptions and will work in reduced or basic UI.</span></span> <span data-ttu-id="d2174-155">Para obter mais informações sobre níveis de IU, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d2174-155">For more information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="d2174-156">Você pode executar [ações personalizadas](custom-actions.md) publicando um ControlEvent, de um controle de [pressão](pushbutton-control.md) ou [controle de caixa de seleção](checkbox-control.md).</span><span class="sxs-lookup"><span data-stu-id="d2174-156">You can run [custom actions](custom-actions.md) by publishing a ControlEvent from a [PushButton control](pushbutton-control.md) or [Checkbox control](checkbox-control.md).</span></span> <span data-ttu-id="d2174-157">Adicione um registro à [tabela ControlEvent,](controlevent-table.md) com os nomes da caixa de diálogo e o controle que está publicando o ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="d2174-157">Add a record to the [ControlEvent table](controlevent-table.md) with the names of the dialog and the control publishing the ControlEvent.</span></span> <span data-ttu-id="d2174-158">Esse controle deve publicar uma [doação ControlEvent,](doaction-controlevent.md) notificando o instalador para executar a ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="d2174-158">This control should publish a [DoAction ControlEvent](doaction-controlevent.md) notifying the installer to run the custom action.</span></span> <span data-ttu-id="d2174-159">No Windows XP ou em sistemas anteriores, você não pode executar uma ação personalizada publicando um ControlEvent, de um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="d2174-159">On Windows XP or earlier systems, you cannot run a custom action by publishing a ControlEvent from a [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="d2174-160">Para obter mais informações sobre ControlEvents específicos, consulte a lista de [ControlEvents](control-events.md) padrão na [referência da interface do usuário](user-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d2174-160">For a more information about particular ControlEvents, see the list of standard [ControlEvents](control-events.md) in [User Interface Reference](user-interface-reference.md).</span></span>

 

 
