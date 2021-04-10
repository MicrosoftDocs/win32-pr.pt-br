---
description: O ControlEvent, DoAction notifica o instalador para executar uma ação personalizada. Esse evento pode ser publicado por um controle de pressão, controle de caixa de seleção ou um controle SelectionTree. Esse evento deve ser criado na tabela ControlEvent,.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: ControlEvent, de doação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089990"
---
# <a name="doaction-controlevent"></a><span data-ttu-id="f0ef6-105">ControlEvent, de doação</span><span class="sxs-lookup"><span data-stu-id="f0ef6-105">DoAction ControlEvent</span></span>

<span data-ttu-id="f0ef6-106">O ControlEvent, DoAction notifica o instalador para executar uma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-106">The DoAction ControlEvent notifies the installer to execute a custom action.</span></span> <span data-ttu-id="f0ef6-107">Esse evento pode ser publicado por um controle de [pressão](pushbutton-control.md) , controle de [caixa de seleção](checkbox-control.md) ou um controle [SelectionTree](selectiontree-control.md) .</span><span class="sxs-lookup"><span data-stu-id="f0ef6-107">This event can be published by a [PushButton](pushbutton-control.md) control, [CheckBox](checkbox-control.md) control, or a [SelectionTree](selectiontree-control.md) control.</span></span> <span data-ttu-id="f0ef6-108">Esse evento deve ser criado na tabela [ControlEvent,](controlevent-table.md) .</span><span class="sxs-lookup"><span data-stu-id="f0ef6-108">This event should be authored into the [ControlEvent](controlevent-table.md) table.</span></span>

<span data-ttu-id="f0ef6-109">Observe que as ações personalizadas iniciadas por uma ControlEvent, de doação podem enviar uma mensagem com o [**método Message**](session-message.md), mas não podem enviar uma mensagem com [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span><span class="sxs-lookup"><span data-stu-id="f0ef6-109">Note that custom actions launched by a DoAction ControlEvent can send a message with the [**Message Method**](session-message.md), but cannot send a message with [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="f0ef6-110">Em sistemas anteriores ao Windows Server 2003, as ações personalizadas iniciadas por uma ação ControlEvent, não podem enviar mensagens com o método **MsiProcessMessage** ou **Message**.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-110">On systems prior to Windows Server 2003, custom actions launched by a DoAction ControlEvent cannot send messages with **MsiProcessMessage** or **Message Method**.</span></span> <span data-ttu-id="f0ef6-111">Para obter mais informações, consulte [enviando mensagens para Windows Installer usando MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="f0ef6-111">For more information, see [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="f0ef6-112">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f0ef6-113">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f0ef6-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f0ef6-114">Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f0ef6-114">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="f0ef6-115">Publicada por</span><span class="sxs-lookup"><span data-stu-id="f0ef6-115">Published By</span></span>

<span data-ttu-id="f0ef6-116">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="f0ef6-117">Argumento</span><span class="sxs-lookup"><span data-stu-id="f0ef6-117">Argument</span></span>

<span data-ttu-id="f0ef6-118">Uma cadeia de caracteres, o nome da ação personalizada a ser executada.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-118">A string, the name of the custom action to be executed.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f0ef6-119">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="f0ef6-119">Action on Subscribers</span></span>

<span data-ttu-id="f0ef6-120">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-120">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f0ef6-121">Usos comum</span><span class="sxs-lookup"><span data-stu-id="f0ef6-121">Typical Use</span></span>

<span data-ttu-id="f0ef6-122">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo é vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para invocar uma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="f0ef6-122">A [PushButton](pushbutton-control.md) control on a dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to invoke a custom action.</span></span>

 

 



