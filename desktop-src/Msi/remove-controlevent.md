---
description: O instalador é notificado por esse evento quando um recurso ou todos os recursos são selecionados para remoção enquanto mantém a caixa de diálogo presente em execução.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: Remover ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780945"
---
# <a name="remove-controlevent"></a><span data-ttu-id="803f6-103">Remover ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="803f6-103">Remove ControlEvent</span></span>

<span data-ttu-id="803f6-104">O instalador é notificado por esse evento quando um recurso ou todos os recursos são selecionados para remoção enquanto mantém a caixa de diálogo presente em execução.</span><span class="sxs-lookup"><span data-stu-id="803f6-104">The installer is notified through this event when a feature or all features are selected for removal while keeping the present dialog box running.</span></span>

<span data-ttu-id="803f6-105">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md), [controle de caixa de seleção](checkbox-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="803f6-105">This event can be published by a [PushButton control](pushbutton-control.md), [CheckBox control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="803f6-106">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="803f6-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="803f6-107">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="803f6-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="803f6-108">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="803f6-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="803f6-109">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="803f6-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="803f6-110">Publicada por</span><span class="sxs-lookup"><span data-stu-id="803f6-110">Published By</span></span>

<span data-ttu-id="803f6-111">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="803f6-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="803f6-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="803f6-112">Argument</span></span>

<span data-ttu-id="803f6-113">Uma cadeia de caracteres que é o nome do recurso ou "todos".</span><span class="sxs-lookup"><span data-stu-id="803f6-113">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="803f6-114">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="803f6-114">Action on Subscribers</span></span>

<span data-ttu-id="803f6-115">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="803f6-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="action-by-publisher-when-subscriber-activated"></a><span data-ttu-id="803f6-116">Ação pelo Publicador quando o assinante foi ativado</span><span class="sxs-lookup"><span data-stu-id="803f6-116">Action by Publisher When Subscriber Activated</span></span>

<span data-ttu-id="803f6-117">O instalador mantém a caixa de diálogo presente em execução e notifica o instalador.</span><span class="sxs-lookup"><span data-stu-id="803f6-117">The installer keeps the present dialog box running and notifies the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="803f6-118">Usos comum</span><span class="sxs-lookup"><span data-stu-id="803f6-118">Typical Use</span></span>

<span data-ttu-id="803f6-119">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal vinculada a este evento.</span><span class="sxs-lookup"><span data-stu-id="803f6-119">A [PushButton](pushbutton-control.md) control on a modal dialog box tied to this event.</span></span>

 

 



