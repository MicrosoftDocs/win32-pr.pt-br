---
description: Windows Installer implementa vários controles padrão que os autores de pacotes podem fazer nas caixas de diálogo. No entanto, nem todos os controles padrão do Microsoft Windows estão disponíveis, e os controles personalizados não podem ser criados para uso com a interface do usuário do instalador.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Visão geral dos controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fbd8477416eb5a126eca56cb1050112309b0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755088"
---
# <a name="controls-overview"></a><span data-ttu-id="47f28-104">Visão geral dos controles</span><span class="sxs-lookup"><span data-stu-id="47f28-104">Controls Overview</span></span>

<span data-ttu-id="47f28-105">Windows Installer implementa vários controles padrão que os autores de pacotes podem fazer nas caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="47f28-105">Windows Installer implements a number of standard controls that package authors can place onto dialog boxes.</span></span> <span data-ttu-id="47f28-106">No entanto, nem todos os controles padrão do Microsoft Windows estão disponíveis, e os controles personalizados não podem ser criados para uso com a interface do usuário do instalador.</span><span class="sxs-lookup"><span data-stu-id="47f28-106">However, not all standard Microsoft Windows controls are available, and custom controls cannot be created for use with the installer UI.</span></span>

<span data-ttu-id="47f28-107">Os controles são criados em caixas de diálogo no instalador de maneira semelhante a como as caixas de diálogo são criadas programaticamente usando a API da interface do usuário do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="47f28-107">Controls are created on dialog boxes in the installer in a manner similar to how dialog boxes are created programmatically using the Microsoft Windows user interface API.</span></span> <span data-ttu-id="47f28-108">Um controle é criado a partir de um modelo registrado na tabela de controle.</span><span class="sxs-lookup"><span data-stu-id="47f28-108">A control is created from a template recorded in the Control table.</span></span> <span data-ttu-id="47f28-109">Esse modelo é ligeiramente diferente, pois contém o nome exclusivo da caixa de diálogo na qual o controle é exibido.</span><span class="sxs-lookup"><span data-stu-id="47f28-109">This template is slightly different in that it contains the unique name of the dialog box on which the control appears.</span></span>

<span data-ttu-id="47f28-110">Na API da interface do usuário do Microsoft Windows, a interação do usuário é realizada criando uma função de retorno de chamada para tratar as mensagens postadas pelo controle.</span><span class="sxs-lookup"><span data-stu-id="47f28-110">In the Microsoft Windows user interface API, user interaction is accomplished by creating a callback function to handle messages posted by the control.</span></span> <span data-ttu-id="47f28-111">Além disso, a maioria dos controles do Microsoft Windows recebe mensagens, como as enviadas pela função [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="47f28-111">Also, most Microsoft Windows controls receive messages, such as those sent by the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="47f28-112">A comunicação entre o usuário e os controles é realizada no instalador por meio do uso de [ControlEvents](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="47f28-112">Communication between the user and controls is accomplished in the installer through the use of [ControlEvents](controlevent-overview.md).</span></span> <span data-ttu-id="47f28-113">No entanto, há um conjunto limitado de ControlEvents que são específicos de cada controle no conjunto limitado de controles no Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="47f28-113">However, there is a limited set of ControlEvents that are specific to each control in the limited set of controls in Windows Installer.</span></span> <span data-ttu-id="47f28-114">Os controles podem postar mais de um ControlEvent, e podem receber mais de um ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="47f28-114">Controls may post more than one ControlEvent and may receive more than one ControlEvent.</span></span>

<span data-ttu-id="47f28-115">Os controles podem publicar ControlEvents específicos por meio do uso da tabela ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="47f28-115">Controls can publish specific ControlEvents through the use of the ControlEvent table.</span></span> <span data-ttu-id="47f28-116">Os controles podem receber ControlEvents por meio do uso da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="47f28-116">Controls can receive ControlEvents through the use of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="47f28-117">Windows Installer publica ControlEvents durante a execução de algumas ações também, e os controles assinados para essas ControlEvents na tabela EventMappings as recebem.</span><span class="sxs-lookup"><span data-stu-id="47f28-117">Windows Installer publishes ControlEvents during the execution of some actions as well, and controls subscribed to these ControlEvents in the EventMapping table receive them.</span></span>

 

 
