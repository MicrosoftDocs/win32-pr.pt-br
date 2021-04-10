---
description: O instalador usa o evento timecontinueing para publicar o tempo aproximado restante, em segundos, para a sequência de progresso atual.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: ControlEvent, do timecontinueing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011672"
---
# <a name="timeremaining-controlevent"></a><span data-ttu-id="09209-103">ControlEvent, do timecontinueing</span><span class="sxs-lookup"><span data-stu-id="09209-103">TimeRemaining ControlEvent</span></span>

<span data-ttu-id="09209-104">O instalador usa o evento timecontinueing para publicar o tempo aproximado restante, em segundos, para a sequência de progresso atual.</span><span class="sxs-lookup"><span data-stu-id="09209-104">The installer uses the TimeRemaining event to publish the approximate time remaining, in seconds, for the current progress sequence.</span></span> <span data-ttu-id="09209-105">O tempo restante pode ser exibido em uma caixa de diálogo por um [controle de texto](text-control.md) que assina esse ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="09209-105">The time remaining can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="09209-106">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="09209-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="09209-107">Esse ControlEvent, pode ser manipulado por uma interface do usuário executada na [*interface da usuário básica*](b-gly.md), na [*IU reduzida*](r-gly.md)ou em níveis [*completos da interface*](f-gly.md) de usuários.</span><span class="sxs-lookup"><span data-stu-id="09209-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="09209-108">Para obter informações sobre níveis de interface do usuário, consulte [níveis de interface de usuários](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="09209-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="09209-109">Publicada por</span><span class="sxs-lookup"><span data-stu-id="09209-109">Published By</span></span>

<span data-ttu-id="09209-110">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="09209-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="09209-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="09209-111">Argument</span></span>

<span data-ttu-id="09209-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="09209-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="09209-113">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="09209-113">Action on Subscribers</span></span>

<span data-ttu-id="09209-114">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="09209-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="09209-115">Usos comum</span><span class="sxs-lookup"><span data-stu-id="09209-115">Typical Use</span></span>

<span data-ttu-id="09209-116">Um [controle de texto](text-control.md) em uma caixa de diálogo sem janela restrita assina esse evento por meio da [tabela EventMappings](eventmapping-table.md) e usa o [atributo timecontinueing](timeremaining-control-attribute.md) para exibir o tempo restante.</span><span class="sxs-lookup"><span data-stu-id="09209-116">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md) and uses the [TimeRemaining attribute](timeremaining-control-attribute.md) to display the time remaining.</span></span>

<span data-ttu-id="09209-117">O mesmo controle de texto que assina para o timestart ControlEvent, também pode assinar o [ScriptInProgress ControlEvent,](scriptinprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="09209-117">The same text control that subscribes to the TimeRemaining ControlEvent can also subscribe to the [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md).</span></span> <span data-ttu-id="09209-118">Nesse caso, como a cadeia de caracteres de mensagem ScriptInProgress preliminar, ela é substituída pela cadeia de caracteres "tempo restante: XX minutos".</span><span class="sxs-lookup"><span data-stu-id="09209-118">In this case, as the preliminary ScriptInProgress message string, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



