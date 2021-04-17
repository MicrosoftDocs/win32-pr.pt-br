---
description: O instalador usa esse evento para exibir uma cadeia de caracteres informativa enquanto o script de execução da instalação está sendo compilado.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749575"
---
# <a name="scriptinprogress-controlevent"></a><span data-ttu-id="e7f99-103">ScriptInProgress ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="e7f99-103">ScriptInProgress ControlEvent</span></span>

<span data-ttu-id="e7f99-104">O instalador usa esse evento para exibir uma cadeia de caracteres informativa enquanto o script de execução da instalação está sendo compilado.</span><span class="sxs-lookup"><span data-stu-id="e7f99-104">The installer uses this event to display an informational string while the installation's execution script is being compiled.</span></span> <span data-ttu-id="e7f99-105">A cadeia de caracteres informativa pode ser exibida em uma caixa de diálogo por um [controle de texto](text-control.md) que assina esse ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="e7f99-105">The informational string can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="e7f99-106">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="e7f99-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="e7f99-107">Esse ControlEvent, pode ser manipulado por uma interface do usuário executada na [*interface da usuário básica*](b-gly.md), na [*IU reduzida*](r-gly.md)ou em níveis [*completos da interface*](f-gly.md) de usuários.</span><span class="sxs-lookup"><span data-stu-id="e7f99-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="e7f99-108">Para obter informações sobre níveis de interface do usuário, consulte [níveis de interface de usuários](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e7f99-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="e7f99-109">Publicada por</span><span class="sxs-lookup"><span data-stu-id="e7f99-109">Published By</span></span>

<span data-ttu-id="e7f99-110">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="e7f99-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="e7f99-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="e7f99-111">Argument</span></span>

<span data-ttu-id="e7f99-112">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="e7f99-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e7f99-113">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="e7f99-113">Action on Subscribers</span></span>

<span data-ttu-id="e7f99-114">Um [controle de texto](text-control.md) que se inscrever em ScriptInProgress exibirá a cadeia de caracteres de texto especificada na [tabela UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="e7f99-114">A [Text control](text-control.md) subscribing to ScriptInProgress will display text string specified in [UIText table](uitext-table.md).</span></span>

## <a name="typical-use"></a><span data-ttu-id="e7f99-115">Usos comum</span><span class="sxs-lookup"><span data-stu-id="e7f99-115">Typical Use</span></span>

<span data-ttu-id="e7f99-116">Enquanto o script de execução está sendo compilado, o instalador exibe um ProgressBar que indica o tempo restante antes do início da execução do script.</span><span class="sxs-lookup"><span data-stu-id="e7f99-116">While the execution script is being compiled, the installer displays a ProgressBar indicating the time remaining before the beginning of script execution.</span></span> <span data-ttu-id="e7f99-117">O autor do pacote pode exibir uma mensagem preliminar neste momento explicando o ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="e7f99-117">The package author can display a preliminary message at this time explaining the ProgressBar.</span></span> <span data-ttu-id="e7f99-118">Para exibir uma mensagem preliminar, inclua um [controle de texto](text-control.md) na mesma caixa de diálogo sem janela restrita que o ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="e7f99-118">To display a preliminary message, include a [Text control](text-control.md) on the same modeless dialog box as the ProgressBar.</span></span> <span data-ttu-id="e7f99-119">Especifique que esse controle de texto assine o ScriptInProgress ControlEvent, por meio da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="e7f99-119">Specify that this Text control subscribe to the ScriptInProgress ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="e7f99-120">Inclua uma entrada na [tabela UIText](uitext-table.md) com ScriptInProgress especificado no campo de chave.</span><span class="sxs-lookup"><span data-stu-id="e7f99-120">Include an entry in the [UIText table](uitext-table.md) with ScriptInProgress specified in the Key field.</span></span> <span data-ttu-id="e7f99-121">Especifique a mensagem preliminar como uma cadeia de texto no campo de texto da tabela UIText.</span><span class="sxs-lookup"><span data-stu-id="e7f99-121">Specify the preliminary message as a text string in the Text field of the UIText table.</span></span> <span data-ttu-id="e7f99-122">Em seguida, durante a compilação do script, o instalador exibirá essa cadeia de caracteres dentro do controle de texto.</span><span class="sxs-lookup"><span data-stu-id="e7f99-122">Then during script compilation, the installer will display this string within the text control.</span></span> <span data-ttu-id="e7f99-123">O texto exibido desaparece assim que a compilação do script é concluída.</span><span class="sxs-lookup"><span data-stu-id="e7f99-123">The displayed text disappears as soon as the script compilation is finished.</span></span>

<span data-ttu-id="e7f99-124">O mesmo controle de texto que assina o ScriptInProgress ControlEvent, também pode assinar o ControlEvent, de [permanência](timeremaining-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="e7f99-124">The same text control that subscribes to the ScriptInProgress ControlEvent can also subscribe to the [TimeRemaining ControlEvent](timeremaining-controlevent.md).</span></span> <span data-ttu-id="e7f99-125">Nesse caso, como o texto da cadeia de caracteres preliminar do ScriptInProgress desaparece, ele é substituído pela cadeia de caracteres "tempo restante: XX minutos".</span><span class="sxs-lookup"><span data-stu-id="e7f99-125">In this case, as text of the preliminary ScriptInProgress string disappears, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



