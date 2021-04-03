---
description: Esse evento notifica o controle Directorylist que o usuário deseja selecionar o pai do diretório atual. Para obter informações relacionadas, consulte caixa de diálogo procurar.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: DirectoryListUp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922986"
---
# <a name="directorylistup-controlevent"></a><span data-ttu-id="1b179-104">DirectoryListUp ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="1b179-104">DirectoryListUp ControlEvent</span></span>

<span data-ttu-id="1b179-105">Esse evento notifica o [controle directorylist](directorylist-control.md) que o usuário deseja selecionar o pai do diretório atual.</span><span class="sxs-lookup"><span data-stu-id="1b179-105">This event notifies the [DirectoryList control](directorylist-control.md) that the user wants to select the parent of the present directory.</span></span> <span data-ttu-id="1b179-106">Para obter informações relacionadas, consulte [caixa de diálogo Procurar](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="1b179-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="1b179-107">Esse evento deve ser publicado por um [controle de pressão](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle assinando esse evento.</span><span class="sxs-lookup"><span data-stu-id="1b179-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="1b179-108">O evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="1b179-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="1b179-109">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="1b179-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="1b179-110">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1b179-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="1b179-111">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="1b179-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="1b179-112">Se o diretório atual for o diretório raiz da unidade, um evento DirectoryListUp desabilitará quaisquer outros controles que publiquem um evento DirectoryListUp.</span><span class="sxs-lookup"><span data-stu-id="1b179-112">If the current directory is the root directory of the drive, a DirectoryListUp event disables any other controls that publish a DirectoryListUp event.</span></span>

## <a name="published-by"></a><span data-ttu-id="1b179-113">Publicada por</span><span class="sxs-lookup"><span data-stu-id="1b179-113">Published By</span></span>

[<span data-ttu-id="1b179-114">Directorylist</span><span class="sxs-lookup"><span data-stu-id="1b179-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="1b179-115">Argumento</span><span class="sxs-lookup"><span data-stu-id="1b179-115">Argument</span></span>

<span data-ttu-id="1b179-116">Este ControlEvent, não usa um argumento.</span><span class="sxs-lookup"><span data-stu-id="1b179-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="1b179-117">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="1b179-117">Action on Subscribers</span></span>

<span data-ttu-id="1b179-118">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="1b179-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="1b179-119">Usos comum</span><span class="sxs-lookup"><span data-stu-id="1b179-119">Typical Use</span></span>

<span data-ttu-id="1b179-120">Um controle de [supressão](pushbutton-control.md) na mesma caixa de diálogo modal que a directorylist é usado para disparar a reversão no caminho.</span><span class="sxs-lookup"><span data-stu-id="1b179-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping up in the path.</span></span>

 

 



