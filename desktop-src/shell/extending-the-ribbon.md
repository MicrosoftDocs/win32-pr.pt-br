---
description: Saiba como estender a faixa de forma do Windows Explorer.
title: Estendendo a faixa de faixas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501412"
---
# <a name="extending-the-ribbon"></a><span data-ttu-id="97601-103">Estendendo a faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="97601-103">Extending the Ribbon</span></span>

<span data-ttu-id="97601-104">No Windows Explorer, a faixa de faixas ajuda a tornar mais fáceis e mais detectáveis as atividades comuns de gerenciamento de arquivos do usuário final, mas há alterações andamento para desenvolvedores de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="97601-104">In Windows Explorer, the Ribbon helps make common end-user file management activities easier and more discoverable, but there are changes afoot for app developers.</span></span> <span data-ttu-id="97601-105">Por exemplo, a antiga barra de comandos era extensível livremente, mas a faixa de faixas é mais restrita no momento.</span><span class="sxs-lookup"><span data-stu-id="97601-105">For example, the old command bar was freely extensible but the Ribbon is more restricted at this time.</span></span> <span data-ttu-id="97601-106">Além disso, a faixa de opção não é mostrada por padrão para todas as extensões de namespace, portanto, você precisa optar por obter a faixa de opção; caso contrário, você obterá a barra de comandos mais antiga.</span><span class="sxs-lookup"><span data-stu-id="97601-106">Also, the Ribbon is not shown by default for all namespace extensions, so you have to opt in to get the Ribbon; otherwise, you get the older command bar.</span></span>

<span data-ttu-id="97601-107">As ações disponíveis para os usuários na faixa de faixas se enquadram em três categorias de extensibilidade:</span><span class="sxs-lookup"><span data-stu-id="97601-107">Actions available to users on the Ribbon fall into three extensibility categories:</span></span>

-   <span data-ttu-id="97601-108">A extensibilidade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="97601-108">Extensibility is not needed.</span></span> <span data-ttu-id="97601-109">Exemplos: copiar, colar, excluir.</span><span class="sxs-lookup"><span data-stu-id="97601-109">Examples: Copy, Paste, Delete.</span></span> <span data-ttu-id="97601-110">O Windows lida com esses verbos para você.</span><span class="sxs-lookup"><span data-stu-id="97601-110">Windows handles these verbs for you.</span></span>
-   <span data-ttu-id="97601-111">A extensibilidade não é permitida no momento: exemplos: zip, sessão de fechamento e outras ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="97601-111">Extensibility is not currently allowed: Examples: Zip, Close Session, and other custom actions.</span></span> <span data-ttu-id="97601-112">Use o menu de contexto para abordar esses cenários.</span><span class="sxs-lookup"><span data-stu-id="97601-112">Use the context menu to cover these scenarios.</span></span>
-   <span data-ttu-id="97601-113">A extensibilidade é incorporada à própria ação.</span><span class="sxs-lookup"><span data-stu-id="97601-113">Extensibility is built into the action itself.</span></span> <span data-ttu-id="97601-114">Exemplos: Pesquisar, enviar por email, imprimir, novo item.</span><span class="sxs-lookup"><span data-stu-id="97601-114">Examples: Search, Email, Print, New Item.</span></span> <span data-ttu-id="97601-115">Você precisa se registrar para esses verbos para incluir seu aplicativo ou formato de arquivo na faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="97601-115">You need to register for these verbs to include your app or file format in the Ribbon .</span></span>

<span data-ttu-id="97601-116">Este documento descreve como você pode optar por obter a faixa de opção e como registrá-la para lidar com verbos de faixa de opção específicos.</span><span class="sxs-lookup"><span data-stu-id="97601-116">This document describes how you can opt-in to get the Ribbon, and how to register to handle specific Ribbon verbs.</span></span>

## <a name="opting-in-to-the-ribbon"></a><span data-ttu-id="97601-117">Optando pela faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="97601-117">Opting in to the Ribbon</span></span>

<span data-ttu-id="97601-118">Para aceitar a faixa de opção, sua implementação do [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) deve especificar a **\_ faixa** de opção do EP em [**IExplorerPaneVisibility:: getpanestate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) e retornar o EPS **\_ Force** \| **\_ padrão \_ em**.</span><span class="sxs-lookup"><span data-stu-id="97601-118">To opt in to the Ribbon, your [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) implementation should specify **EP\_Ribbon** in [**IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) and return **EPS\_FORCE** \| **EPS\_DEFAULT\_ON**.</span></span>

## <a name="extending-the-ribbon-for-file-extensions"></a><span data-ttu-id="97601-119">Estendendo a faixa de faixas para extensões de arquivo</span><span class="sxs-lookup"><span data-stu-id="97601-119">Extending the Ribbon for File Extensions</span></span>

<span data-ttu-id="97601-120">Esses botões de faixa de lista são extensíveis com base nas extensões de arquivo:</span><span class="sxs-lookup"><span data-stu-id="97601-120">These Ribbon buttons are extensible based on file extensions:</span></span>

-   <span data-ttu-id="97601-121"> Extrair Tudo</span><span class="sxs-lookup"><span data-stu-id="97601-121">Extract All</span></span>
-   <span data-ttu-id="97601-122">\|Gravação de montagem (um ISO)</span><span class="sxs-lookup"><span data-stu-id="97601-122">Mount \| Burn (an ISO)</span></span>
-   <span data-ttu-id="97601-123">Reproduzir \| reproduzir tudo \| Adicionar à lista de reprodução (verbo: enfileirar)</span><span class="sxs-lookup"><span data-stu-id="97601-123">Play \| Play All \| Add to Playlist (verb: Enqueue)</span></span>
-   <span data-ttu-id="97601-124">Aberto</span><span class="sxs-lookup"><span data-stu-id="97601-124">Open</span></span>
-   <span data-ttu-id="97601-125">Editar</span><span class="sxs-lookup"><span data-stu-id="97601-125">Edit</span></span>
-   <span data-ttu-id="97601-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="97601-126">Properties</span></span>

<span data-ttu-id="97601-127">Quando você se registra para lidar estaticamente com os verbos relevantes para novos tipos de arquivo, a faixa de faixas manipula os verbos adequadamente.</span><span class="sxs-lookup"><span data-stu-id="97601-127">When you register to statically handle the relevant verbs for new file types, the Ribbon handles the verbs appropriately.</span></span> <span data-ttu-id="97601-128">Você se registra exatamente como faria para verbos de menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="97601-128">You register just as you would for context menu verbs.</span></span> <span data-ttu-id="97601-129">Para obter mais informações sobre associações de arquivo e registro para verbos, consulte [verbos e associações de arquivo](fa-verbs.md) e [criando manipuladores de menu de atalho](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="97601-129">For more information about file associations and registering for verbs, see [Verbs and File Associations](fa-verbs.md) and [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="registering-as-a-default-handler-for-actionids"></a><span data-ttu-id="97601-130">Registrando como um manipulador padrão para ActionIds</span><span class="sxs-lookup"><span data-stu-id="97601-130">Registering as a Default Handler for ActionIds</span></span>

<span data-ttu-id="97601-131">Primeiro, Registre seu ProgId na subchave AssocActionId apropriada.</span><span class="sxs-lookup"><span data-stu-id="97601-131">First, register your ProgId under the appropriate AssocActionId subkey.</span></span> <span data-ttu-id="97601-132">Cada subchave AssocActionId representa um verbo ou uma ação que os usuários podem invocar na faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="97601-132">Each AssocActionId subkey represents a verb or action that users can invoke from the Ribbon.</span></span> <span data-ttu-id="97601-133">Neste exemplo, o aplicativo registra para o ActionID ZipSelection para estender o botão "extrair tudo" na faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="97601-133">In this example, the app registers for the ZipSelection ActionID to extend the "Extract All" button on the Ribbon.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

<span data-ttu-id="97601-134">Depois que o registro for concluído, você deverá se registrar para manipular protocolos da mesma forma como faria normalmente, conforme descrito em [programas padrão](default-programs.md).</span><span class="sxs-lookup"><span data-stu-id="97601-134">Once that registration is complete, you must then register to handle protocols just as you normally would, as described in [Default Programs](default-programs.md).</span></span>

 

 



