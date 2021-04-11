---
description: Esse evento seleciona e realça um diretório no controle Directorylist que o usuário optou por abrir. Para obter informações relacionadas, consulte caixa de diálogo procurar.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172338"
---
# <a name="directorylistopen-controlevent"></a><span data-ttu-id="3127d-104">DirectoryListOpen ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="3127d-104">DirectoryListOpen ControlEvent</span></span>

<span data-ttu-id="3127d-105">Esse evento seleciona e realça um diretório no [controle directorylist](directorylist-control.md) que o usuário optou por abrir.</span><span class="sxs-lookup"><span data-stu-id="3127d-105">This event selects and highlights a directory in the [DirectoryList control](directorylist-control.md) that the user has chosen to open.</span></span> <span data-ttu-id="3127d-106">Para obter informações relacionadas, consulte [caixa de diálogo Procurar](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="3127d-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="3127d-107">Esse evento deve ser publicado por um [controle de pressão](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle assinando esse evento.</span><span class="sxs-lookup"><span data-stu-id="3127d-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="3127d-108">O evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="3127d-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="3127d-109">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="3127d-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="3127d-110">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3127d-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="3127d-111">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="3127d-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="3127d-112">Se nenhum diretório tiver sido selecionado no [controle directorylist](directorylist-control.md), um evento DirectoryListOpen desabilitará quaisquer outros controles que publiquem um evento DirectoryListOpen.</span><span class="sxs-lookup"><span data-stu-id="3127d-112">If no directory has been selected in the [DirectoryList control](directorylist-control.md), a DirectoryListOpen event disables any other controls that publish a DirectoryListOpen event.</span></span>

## <a name="published-by"></a><span data-ttu-id="3127d-113">Publicada por</span><span class="sxs-lookup"><span data-stu-id="3127d-113">Published By</span></span>

[<span data-ttu-id="3127d-114">Directorylist</span><span class="sxs-lookup"><span data-stu-id="3127d-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="3127d-115">Argumento</span><span class="sxs-lookup"><span data-stu-id="3127d-115">Argument</span></span>

<span data-ttu-id="3127d-116">Este ControlEvent, não usa um argumento.</span><span class="sxs-lookup"><span data-stu-id="3127d-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="3127d-117">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="3127d-117">Action on Subscribers</span></span>

<span data-ttu-id="3127d-118">Este ControlEvent, não executa nenhuma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="3127d-118">This ControlEvent performs no action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="3127d-119">Usos comum</span><span class="sxs-lookup"><span data-stu-id="3127d-119">Typical Use</span></span>

<span data-ttu-id="3127d-120">Um controle de [pressão](pushbutton-control.md) na mesma caixa de diálogo modal que a directorylist é usado para disparar a depuração no caminho.</span><span class="sxs-lookup"><span data-stu-id="3127d-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping down in the path.</span></span>

 

 



