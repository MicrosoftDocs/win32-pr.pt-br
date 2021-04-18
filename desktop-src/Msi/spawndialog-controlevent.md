---
description: O SpawnDialog ControlEvent, notifica o instalador para criar um filho de uma caixa de diálogo modal enquanto mantém a caixa de diálogo presente em execução.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: SpawnDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758761"
---
# <a name="spawndialog-controlevent"></a><span data-ttu-id="103b5-103">SpawnDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="103b5-103">SpawnDialog ControlEvent</span></span>

<span data-ttu-id="103b5-104">O SpawnDialog ControlEvent, notifica o instalador para criar um filho de uma caixa de diálogo modal enquanto mantém a caixa de diálogo presente em execução.</span><span class="sxs-lookup"><span data-stu-id="103b5-104">The SpawnDialog ControlEvent notifies the installer to create a child of a modal dialog box while keeping the present dialog box running.</span></span>

<span data-ttu-id="103b5-105">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="103b5-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="103b5-106">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="103b5-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="103b5-107">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="103b5-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="103b5-108">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="103b5-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="103b5-109">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="103b5-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="103b5-110">Publicada por</span><span class="sxs-lookup"><span data-stu-id="103b5-110">Published By</span></span>

<span data-ttu-id="103b5-111">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="103b5-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="103b5-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="103b5-112">Argument</span></span>

<span data-ttu-id="103b5-113">Uma cadeia de caracteres que é o nome da nova caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="103b5-113">A string that is the name of the new dialog box.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="103b5-114">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="103b5-114">Action on Subscribers</span></span>

<span data-ttu-id="103b5-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="103b5-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="103b5-116">Usos comum</span><span class="sxs-lookup"><span data-stu-id="103b5-116">Typical Use</span></span>

<span data-ttu-id="103b5-117">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para criar uma caixa de diálogo filho, como "tem certeza de que deseja cancelar?"</span><span class="sxs-lookup"><span data-stu-id="103b5-117">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to create a child dialog, such as an "Are you sure you want to cancel?"</span></span> <span data-ttu-id="103b5-118">.</span><span class="sxs-lookup"><span data-stu-id="103b5-118">dialog box.</span></span>

 

 



