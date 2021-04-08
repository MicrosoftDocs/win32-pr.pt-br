---
description: O instalador executará a sequência do assistente de instalação de exemplo somente se o nível completo da interface do usuário for usado para instalar o aplicativo.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Adicionar um evento de controle ao final da instalação para executar a inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921530"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a><span data-ttu-id="4b559-103">Adicionar um evento de controle ao final da instalação para executar a inicialização</span><span class="sxs-lookup"><span data-stu-id="4b559-103">Adding a Control Event at the End of the Installation to Run Launch</span></span>

<span data-ttu-id="4b559-104">O instalador executará a sequência do assistente de instalação de exemplo somente se o nível [*completo da interface do usuário*](f-gly.md) for usado para instalar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b559-104">The installer runs the sample's installation wizard sequence only if the [*full UI*](f-gly.md) level is used to install the application.</span></span> <span data-ttu-id="4b559-105">A última caixa de diálogo da sequência de diálogo de exemplo é uma caixa de [diálogo de saída](exit-dialog.md) chamada ExitDialog.</span><span class="sxs-lookup"><span data-stu-id="4b559-105">The last dialog box of the sample dialog sequence is an [Exit Dialog](exit-dialog.md) named ExitDialog.</span></span> <span data-ttu-id="4b559-106">Quando um usuário interage com o botão OK em ExitDialog, isso primeiro publica um [ControlEvent, EndDialog](enddialog-controlevent.md) que retorna o controle ao instalador.</span><span class="sxs-lookup"><span data-stu-id="4b559-106">When a user interacts with the OK button on ExitDialog, this first publishes an [EndDialog ControlEvent](enddialog-controlevent.md) that returns control to the installer.</span></span> <span data-ttu-id="4b559-107">Em seguida, o controle publica um [ControlEvent, DoAction](doaction-controlevent.md) que executa a ação personalizada de inicialização.</span><span class="sxs-lookup"><span data-stu-id="4b559-107">The control then publishes a [DoAction ControlEvent](doaction-controlevent.md) that runs the Launch custom action.</span></span> <span data-ttu-id="4b559-108">Cada evento de controle requer um registro na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="4b559-108">Each control event requires a record in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="4b559-109">Consulte [visão geral do ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4b559-109">See [ControlEvent Overview](controlevent-overview.md).</span></span>

[<span data-ttu-id="4b559-110">Tabela ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="4b559-110">ControlEvent Table</span></span>](controlevent-table.md)



| <span data-ttu-id="4b559-111">caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="4b559-111">Dialog</span></span>     | <span data-ttu-id="4b559-112">controle\_</span><span class="sxs-lookup"><span data-stu-id="4b559-112">Control\_</span></span> | <span data-ttu-id="4b559-113">Evento</span><span class="sxs-lookup"><span data-stu-id="4b559-113">Event</span></span>     | <span data-ttu-id="4b559-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="4b559-114">Argument</span></span> | <span data-ttu-id="4b559-115">Condição</span><span class="sxs-lookup"><span data-stu-id="4b559-115">Condition</span></span>                     | <span data-ttu-id="4b559-116">Ordenando</span><span class="sxs-lookup"><span data-stu-id="4b559-116">Ordering</span></span> |
|------------|-----------|-----------|----------|-------------------------------|----------|
| <span data-ttu-id="4b559-117">ExitDialog</span><span class="sxs-lookup"><span data-stu-id="4b559-117">ExitDialog</span></span> | <span data-ttu-id="4b559-118">OK</span><span class="sxs-lookup"><span data-stu-id="4b559-118">OK</span></span>        | <span data-ttu-id="4b559-119">EndDialog</span><span class="sxs-lookup"><span data-stu-id="4b559-119">EndDialog</span></span> | <span data-ttu-id="4b559-120">Retorno</span><span class="sxs-lookup"><span data-stu-id="4b559-120">Return</span></span>   | <span data-ttu-id="4b559-121">1</span><span class="sxs-lookup"><span data-stu-id="4b559-121">1</span></span>                             | <span data-ttu-id="4b559-122">1</span><span class="sxs-lookup"><span data-stu-id="4b559-122">1</span></span>        |
| <span data-ttu-id="4b559-123">ExitDialog</span><span class="sxs-lookup"><span data-stu-id="4b559-123">ExitDialog</span></span> | <span data-ttu-id="4b559-124">OK</span><span class="sxs-lookup"><span data-stu-id="4b559-124">OK</span></span>        | <span data-ttu-id="4b559-125">DoAction</span><span class="sxs-lookup"><span data-stu-id="4b559-125">DoAction</span></span>  | <span data-ttu-id="4b559-126">Inicializar</span><span class="sxs-lookup"><span data-stu-id="4b559-126">Launch</span></span>   | <span data-ttu-id="4b559-127">NÃO instalado e $Tutorial = 3</span><span class="sxs-lookup"><span data-stu-id="4b559-127">NOT Installed AND $Tutorial=3</span></span> | <span data-ttu-id="4b559-128">2</span><span class="sxs-lookup"><span data-stu-id="4b559-128">2</span></span>        |



 

<span data-ttu-id="4b559-129">A condição no controle DoAction garante que a ação personalizada só seja executada durante a primeira instalação do aplicativo e que esteja sendo instalada localmente.</span><span class="sxs-lookup"><span data-stu-id="4b559-129">The condition on the DoAction control ensures the custom action only runs during the first installation of the application and that it is being installed locally.</span></span> <span data-ttu-id="4b559-130">A frase $Tutorial = 3 significa que o estado de ação do componente tutorial está definido como local.</span><span class="sxs-lookup"><span data-stu-id="4b559-130">The phrase $Tutorial=3 means the action state of the Tutorial component is set to local.</span></span> <span data-ttu-id="4b559-131">Consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="4b559-131">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="4b559-132">Isso conclui o exemplo.</span><span class="sxs-lookup"><span data-stu-id="4b559-132">This completes the sample.</span></span>

 

 



