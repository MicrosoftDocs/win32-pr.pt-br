---
description: O instalador usa esse evento para publicar dados na ação mais recente. Os dados podem ser exibidos em uma caixa de diálogo por um controle de texto que assina esse ControlEvent,. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780966"
---
# <a name="actiondata-controlevent"></a><span data-ttu-id="e6d74-105">ActionData ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="e6d74-105">ActionData ControlEvent</span></span>

<span data-ttu-id="e6d74-106">O instalador usa esse evento para publicar dados na ação mais recente.</span><span class="sxs-lookup"><span data-stu-id="e6d74-106">The installer uses this event to publish data on the latest action.</span></span> <span data-ttu-id="e6d74-107">Os dados podem ser exibidos em uma caixa de diálogo por um [controle de texto](text-control.md) que assina esse ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="e6d74-107">The data can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="e6d74-108">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="e6d74-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="e6d74-109">Esse ControlEvent, pode ser manipulado por uma interface do usuário executada na [*interface da usuário básica*](b-gly.md), na [*IU reduzida*](r-gly.md)ou em níveis [*completos da interface*](f-gly.md) de usuários.</span><span class="sxs-lookup"><span data-stu-id="e6d74-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="e6d74-110">Para obter informações sobre níveis de interface do usuário, consulte [níveis de interface de usuários](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e6d74-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="e6d74-111">Publicada por</span><span class="sxs-lookup"><span data-stu-id="e6d74-111">Published By</span></span>

<span data-ttu-id="e6d74-112">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="e6d74-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="e6d74-113">Argumento</span><span class="sxs-lookup"><span data-stu-id="e6d74-113">Argument</span></span>

<span data-ttu-id="e6d74-114">Este ControlEvent, não usa um argumento.</span><span class="sxs-lookup"><span data-stu-id="e6d74-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e6d74-115">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="e6d74-115">Action on Subscribers</span></span>

<span data-ttu-id="e6d74-116">Os assinantes ficam ocultos quando uma nova ação é iniciada e mostrada quando novos dados de ação chegam do instalador.</span><span class="sxs-lookup"><span data-stu-id="e6d74-116">The subscribers are hidden when a new action starts and shown when new action data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="e6d74-117">Usos comum</span><span class="sxs-lookup"><span data-stu-id="e6d74-117">Typical Use</span></span>

<span data-ttu-id="e6d74-118">Um [controle de texto](text-control.md) em uma caixa de diálogo sem janela restrita assina esse evento por meio da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="e6d74-118">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="e6d74-119">O [atributo controle de texto](text-control-attribute.md) é listado no campo atributos desta tabela para receber os dados de ação atuais.</span><span class="sxs-lookup"><span data-stu-id="e6d74-119">The [Text Control Attribute](text-control-attribute.md) is listed in the Attributes field of this table to receive the current action data.</span></span> <span data-ttu-id="e6d74-120">Normalmente usado para exibir os nomes dos arquivos copiados durante a cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e6d74-120">Typically used to display the names of the files copied during file copy.</span></span>

 

 



