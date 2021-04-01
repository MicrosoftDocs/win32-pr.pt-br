---
description: O instalador usa esse evento para publicar o nome da ação atual. O nome pode ser exibido em uma caixa de diálogo por um controle de texto que assina esse ControlEvent,. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921532"
---
# <a name="actiontext-controlevent"></a><span data-ttu-id="47dcc-105">ActionText ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="47dcc-105">ActionText ControlEvent</span></span>

<span data-ttu-id="47dcc-106">O instalador usa esse evento para publicar o nome da ação atual.</span><span class="sxs-lookup"><span data-stu-id="47dcc-106">The installer uses this event to publish the name of the present action.</span></span> <span data-ttu-id="47dcc-107">O nome pode ser exibido em uma caixa de diálogo por um [controle de texto](text-control.md) que assina esse ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="47dcc-107">The name can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="47dcc-108">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="47dcc-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="47dcc-109">Esse ControlEvent, pode ser manipulado por uma interface do usuário executada na [*interface da usuário básica*](b-gly.md), na [*IU reduzida*](r-gly.md)ou em níveis [*completos da interface*](f-gly.md) de usuários.</span><span class="sxs-lookup"><span data-stu-id="47dcc-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="47dcc-110">Para obter informações sobre níveis de interface do usuário, consulte [níveis de interface de usuários](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="47dcc-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="47dcc-111">Publicada por</span><span class="sxs-lookup"><span data-stu-id="47dcc-111">Published By</span></span>

<span data-ttu-id="47dcc-112">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="47dcc-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="47dcc-113">Argumento</span><span class="sxs-lookup"><span data-stu-id="47dcc-113">Argument</span></span>

<span data-ttu-id="47dcc-114">Este ControlEvent, não usa um argumento.</span><span class="sxs-lookup"><span data-stu-id="47dcc-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="47dcc-115">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="47dcc-115">Action on Subscribers</span></span>

<span data-ttu-id="47dcc-116">Os assinantes são mostrados quando novos dados de progresso chegam do instalador.</span><span class="sxs-lookup"><span data-stu-id="47dcc-116">The subscribers are shown when a new progress data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="47dcc-117">Usos comum</span><span class="sxs-lookup"><span data-stu-id="47dcc-117">Typical Use</span></span>

<span data-ttu-id="47dcc-118">Um [controle de texto](text-control.md) em uma caixa de diálogo sem janela restrita assina esse evento por meio da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="47dcc-118">A [Text Control](text-control.md) on a modeless dialog subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="47dcc-119">O [atributo de controle de texto](text-control-attribute.md) deve estar listado no campo atributos desta tabela para receber o nome da ação atual.</span><span class="sxs-lookup"><span data-stu-id="47dcc-119">The [Text Control Attribute](text-control-attribute.md) should be listed in the Attributes field of this table to receive the name of the current action.</span></span>

 

 



