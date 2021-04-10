---
description: O evento SetInstallLevel altera o nível de instalação para o valor especificado pelo argumento.
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: SetInstallLevel ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347f54cee1494b2ff91f7dc1701f0b7749d47e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164736"
---
# <a name="setinstalllevel-controlevent"></a><span data-ttu-id="3bd5a-103">SetInstallLevel ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="3bd5a-103">SetInstallLevel ControlEvent</span></span>

<span data-ttu-id="3bd5a-104">O evento SetInstallLevel altera o nível de instalação para o valor especificado pelo argumento.</span><span class="sxs-lookup"><span data-stu-id="3bd5a-104">The SetInstallLevel event changes the installation level to the value specified by the argument.</span></span>

<span data-ttu-id="3bd5a-105">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="3bd5a-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="3bd5a-106">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="3bd5a-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="3bd5a-107">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="3bd5a-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="3bd5a-108">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3bd5a-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="3bd5a-109">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="3bd5a-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="3bd5a-110">Publicada por</span><span class="sxs-lookup"><span data-stu-id="3bd5a-110">Published By</span></span>

<span data-ttu-id="3bd5a-111">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="3bd5a-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="3bd5a-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="3bd5a-112">Argument</span></span>

<span data-ttu-id="3bd5a-113">Um inteiro que é o novo valor do nível de instalação.</span><span class="sxs-lookup"><span data-stu-id="3bd5a-113">An integer that is the new value of the installation level.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="3bd5a-114">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="3bd5a-114">Action on Subscribers</span></span>

<span data-ttu-id="3bd5a-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="3bd5a-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="3bd5a-116">Usos comum</span><span class="sxs-lookup"><span data-stu-id="3bd5a-116">Typical Use</span></span>

<span data-ttu-id="3bd5a-117">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para alterar o nível de instalação.</span><span class="sxs-lookup"><span data-stu-id="3bd5a-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to change the installation level.</span></span>

 

 



