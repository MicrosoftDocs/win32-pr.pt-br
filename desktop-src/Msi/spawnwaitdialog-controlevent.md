---
description: O ControlEvent, SpawnWaitDialog aciona a caixa de diálogo especificada pela coluna Argument da tabela ControlEvent,, se a expressão na coluna condição for avaliada como FALSE.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921015"
---
# <a name="spawnwaitdialog-controlevent"></a><span data-ttu-id="4795e-103">SpawnWaitDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="4795e-103">SpawnWaitDialog ControlEvent</span></span>

<span data-ttu-id="4795e-104">O ControlEvent, SpawnWaitDialog aciona a caixa de diálogo especificada pela coluna Argument da [tabela ControlEvent,](controlevent-table.md), se a expressão na coluna condição for avaliada como false.</span><span class="sxs-lookup"><span data-stu-id="4795e-104">The SpawnWaitDialog ControlEvent triggers the dialog box specified by the Argument column of the [ControlEvent table](controlevent-table.md), if the expression in the Condition column evaluates as FALSE.</span></span> <span data-ttu-id="4795e-105">A caixa de diálogo permanece ativa por enquanto a expressão condicional permanece falsa e é removida assim que a condição é avaliada como TRUE.</span><span class="sxs-lookup"><span data-stu-id="4795e-105">The dialog box remains up for as long as the conditional expression remains FALSE and is removed as soon as the condition evaluates TRUE.</span></span>

<span data-ttu-id="4795e-106">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="4795e-106">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="4795e-107">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="4795e-107">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="4795e-108">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="4795e-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="4795e-109">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4795e-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="4795e-110">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="4795e-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="4795e-111">Publicada por</span><span class="sxs-lookup"><span data-stu-id="4795e-111">Published By</span></span>

<span data-ttu-id="4795e-112">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="4795e-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="4795e-113">Argumento</span><span class="sxs-lookup"><span data-stu-id="4795e-113">Argument</span></span>

<span data-ttu-id="4795e-114">Uma caixa de diálogo na [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="4795e-114">A dialog box in the [Dialog table](dialog-table.md).</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="4795e-115">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="4795e-115">Action on Subscribers</span></span>

<span data-ttu-id="4795e-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4795e-116">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="4795e-117">Usos comum</span><span class="sxs-lookup"><span data-stu-id="4795e-117">Typical Use</span></span>

<span data-ttu-id="4795e-118">O SpawnWaitDialog ControlEvent, pode ser usado para aguardar qualquer tarefa em segundo plano a conclusão do que pode ser testada usando uma expressão condicional, como o estado de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="4795e-118">The SpawnWaitDialog ControlEvent can be used to wait for any background task the completion of which can be tested using a conditional expression such as the state of a property.</span></span> <span data-ttu-id="4795e-119">Para obter um exemplo de como usar o SpawnWaitDialog ControlEvent,, consulte a seção [criando uma condicional "Aguarde...". Caixa de mensagem](authoring-a-conditional-please-wait-------message-box.md).</span><span class="sxs-lookup"><span data-stu-id="4795e-119">For an example of using the SpawnWaitDialog ControlEvent, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

 

 



