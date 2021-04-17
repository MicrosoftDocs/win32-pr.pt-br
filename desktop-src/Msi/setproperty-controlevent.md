---
description: 'A sintaxe para o evento SetProperty é diferente de para outros ControlEvents no lugar do nome do evento que coloca a propriedade entre colchetes: \[ nome da propriedade \_ \] .'
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: ControlEvent, SetProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758616"
---
# <a name="setproperty-controlevent"></a><span data-ttu-id="6b8ad-103">ControlEvent, SetProperty</span><span class="sxs-lookup"><span data-stu-id="6b8ad-103">SetProperty ControlEvent</span></span>

<span data-ttu-id="6b8ad-104">A sintaxe para o evento SetProperty é diferente de para outros ControlEvents no lugar do nome do evento que coloca a propriedade entre colchetes: \[ nome da propriedade \_ \] .</span><span class="sxs-lookup"><span data-stu-id="6b8ad-104">The syntax for the SetProperty event is different than for other ControlEvents In place of the name of the event one puts the property in square brackets: \[property\_name\].</span></span> <span data-ttu-id="6b8ad-105">O argumento é o novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6b8ad-105">The argument is the new value of the property.</span></span> <span data-ttu-id="6b8ad-106">Para remover a propriedade, o argumento deve ser {} .</span><span class="sxs-lookup"><span data-stu-id="6b8ad-106">To unset the property, the argument must be {}.</span></span> <span data-ttu-id="6b8ad-107">Isso é necessário, porque o argumento é uma chave primária na tabela e, portanto, não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="6b8ad-107">This is necessary, because the argument is a primary key in the table and so cannot be null.</span></span> <span data-ttu-id="6b8ad-108">O argumento será formatado usando o método FormatText, portanto, o argumento pode conter qualquer expressão que o método FormatText possa manipular.</span><span class="sxs-lookup"><span data-stu-id="6b8ad-108">The argument will be formatted using the FormatText method, therefore the argument can contain any expression that the FormatText method can handle.</span></span> <span data-ttu-id="6b8ad-109">Os valores de propriedade são avaliados no momento do ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="6b8ad-109">The property values are evaluated at the moment of the ControlEvent.</span></span>

<span data-ttu-id="6b8ad-110">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md), [controle de caixa de seleção](checkbox-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="6b8ad-110">This event can be published by a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="6b8ad-111">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="6b8ad-111">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="6b8ad-112">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="6b8ad-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="6b8ad-113">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6b8ad-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="6b8ad-114">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="6b8ad-114">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="6b8ad-115">Publicada por</span><span class="sxs-lookup"><span data-stu-id="6b8ad-115">Published By</span></span>

<span data-ttu-id="6b8ad-116">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="6b8ad-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="6b8ad-117">Argumento</span><span class="sxs-lookup"><span data-stu-id="6b8ad-117">Argument</span></span>

<span data-ttu-id="6b8ad-118">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="6b8ad-118">The new value of the property.</span></span> <span data-ttu-id="6b8ad-119">{} para NULL.</span><span class="sxs-lookup"><span data-stu-id="6b8ad-119">{} for null.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="6b8ad-120">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="6b8ad-120">Action on Subscribers</span></span>

<span data-ttu-id="6b8ad-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6b8ad-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="6b8ad-122">Usos comum</span><span class="sxs-lookup"><span data-stu-id="6b8ad-122">Typical Use</span></span>

<span data-ttu-id="6b8ad-123">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo vinculada a esse evento para que ele altere uma propriedade quando o botão é enviado por push.</span><span class="sxs-lookup"><span data-stu-id="6b8ad-123">A [PushButton](pushbutton-control.md) control on a dialog box linked to this event so it changes a property when the button is pushed.</span></span>

 

 



