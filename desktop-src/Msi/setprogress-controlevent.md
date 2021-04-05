---
description: O instalador usa o evento setProgress para publicar informações sobre o progresso da instalação.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: ControlEvent, de reprogress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922133"
---
# <a name="setprogress-controlevent"></a><span data-ttu-id="b91b0-103">ControlEvent, de reprogress</span><span class="sxs-lookup"><span data-stu-id="b91b0-103">SetProgress ControlEvent</span></span>

<span data-ttu-id="b91b0-104">O instalador usa o evento setProgress para publicar informações sobre o progresso da instalação.</span><span class="sxs-lookup"><span data-stu-id="b91b0-104">The installer uses the SetProgress event to publish information on the installation's progress.</span></span> <span data-ttu-id="b91b0-105">Um [controle ProgressBar](progressbar-control.md) ou um [controle de mensagem](billboard-control.md) deve assinar o evento por meio da [tabela EventMappings](eventmapping-table.md) , nomeando a ação cujo progresso está sendo indicado.</span><span class="sxs-lookup"><span data-stu-id="b91b0-105">A [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) should subscribe to the event via the [EventMapping table](eventmapping-table.md) by naming the Action whose progress is being indicated.</span></span> <span data-ttu-id="b91b0-106">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b91b0-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="b91b0-107">Esse ControlEvent, pode ser manipulado por uma interface do usuário executada na [*interface da usuário básica*](b-gly.md), na [*IU reduzida*](r-gly.md)ou em níveis [*completos da interface*](f-gly.md) de usuários.</span><span class="sxs-lookup"><span data-stu-id="b91b0-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="b91b0-108">Para obter informações sobre níveis de interface do usuário, consulte [níveis de interface de usuários](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b91b0-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="b91b0-109">Publicada por</span><span class="sxs-lookup"><span data-stu-id="b91b0-109">Published By</span></span>

<span data-ttu-id="b91b0-110">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="b91b0-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="b91b0-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="b91b0-111">Argument</span></span>

<span data-ttu-id="b91b0-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b91b0-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b91b0-113">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="b91b0-113">Action on Subscribers</span></span>

<span data-ttu-id="b91b0-114">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b91b0-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b91b0-115">Usos comum</span><span class="sxs-lookup"><span data-stu-id="b91b0-115">Typical Use</span></span>

<span data-ttu-id="b91b0-116">Um controle [ProgressBar](progressbar-control.md) em uma caixa de diálogo sem janela restrita assina esse evento usando o atributo [Progress](progress-control-attribute.md) para receber as informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="b91b0-116">A [ProgressBar](progressbar-control.md) control on a modeless dialog box subscribes to this event using the [Progress](progress-control-attribute.md) attribute to receive the progress information.</span></span>

 

 



