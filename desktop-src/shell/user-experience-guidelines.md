---
description: A principal responsabilidade de qualquer item do painel de controle é exibir uma janela que permite ao usuário exibir e manipular as configurações.
title: Diretrizes da Experiência do Usuário
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989088"
---
# <a name="user-experience-guidelines"></a><span data-ttu-id="ec1be-103">Diretrizes da Experiência do Usuário</span><span class="sxs-lookup"><span data-stu-id="ec1be-103">User Experience Guidelines</span></span>

<span data-ttu-id="ec1be-104">A principal responsabilidade de qualquer item do painel de controle é exibir uma janela que permite ao usuário exibir e manipular as configurações.</span><span class="sxs-lookup"><span data-stu-id="ec1be-104">The primary responsibility of any Control Panel item is to display a window that allows the user to view and manipulate settings.</span></span> <span data-ttu-id="ec1be-105">Consulte as [diretrizes UX (experiência do usuário dos painéis de controle)](../uxguide/winenv-ctrl-panels.md) para o comportamento e o design de itens do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="ec1be-105">See the [Control Panels user experience (UX) guidelines](../uxguide/winenv-ctrl-panels.md) for the behavior and design of Control Panel items.</span></span> <span data-ttu-id="ec1be-106">As diretrizes discutidas neste tópico mostram um método de fluxo de tarefas de organizar um item do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="ec1be-106">The guidelines discussed in that topic show a task flow method of organizing a Control Panel item.</span></span> <span data-ttu-id="ec1be-107">Isso coloca as configurações mais importantes em um home page.</span><span class="sxs-lookup"><span data-stu-id="ec1be-107">This places the most important settings on a home page.</span></span> <span data-ttu-id="ec1be-108">As configurações usadas com menos frequência são colocadas em páginas spoke ou acessadas de links em um painel lateral.</span><span class="sxs-lookup"><span data-stu-id="ec1be-108">Less frequently used settings are placed on spoke pages or accessed from links in a side pane.</span></span>

<span data-ttu-id="ec1be-109">O painel de controle inclui muitos itens que seguem essas diretrizes, como a facilidade de central de acesso e a central de rede e compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="ec1be-109">The Control Panel includes many items that follow these guidelines, such as Ease of Access Center and Network and Sharing Center.</span></span> <span data-ttu-id="ec1be-110">Outros itens do painel de controle usam o formato de folha de propriedades da caixa de diálogo com guias, como nas versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="ec1be-110">Other Control Panel items use the tabbed dialog property sheet format as in earlier versions of Windows.</span></span> <span data-ttu-id="ec1be-111">Os exemplos incluem o item do mouse e as opções da Internet.</span><span class="sxs-lookup"><span data-stu-id="ec1be-111">Examples include the Mouse item and Internet Options.</span></span> <span data-ttu-id="ec1be-112">O uso do formato de folha de propriedades deve ser descontinuado.</span><span class="sxs-lookup"><span data-stu-id="ec1be-112">Use of the property sheet format should be discontinued.</span></span> <span data-ttu-id="ec1be-113">Se você criar novos itens do painel de controle, siga as diretrizes de fluxo de tarefas.</span><span class="sxs-lookup"><span data-stu-id="ec1be-113">If you create new Control Panel items, you should follow the task flow guidelines.</span></span>

<span data-ttu-id="ec1be-114">No passado, os itens do painel de controle eram empacotados como arquivos. cpl.</span><span class="sxs-lookup"><span data-stu-id="ec1be-114">In the past, Control Panel items were packaged as .cpl files.</span></span> <span data-ttu-id="ec1be-115">Isso não é mais necessário.</span><span class="sxs-lookup"><span data-stu-id="ec1be-115">That is no longer necessary.</span></span> <span data-ttu-id="ec1be-116">Novos itens do painel de controle devem ser implementados como um arquivo. exe autônomo ou como uma opção de sinalizador de linha de comando para o arquivo executável principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ec1be-116">New Control Panel items should be implemented as a standalone .exe file or as a command-line flag option for the application's main executable file.</span></span>

> [!Note]  
> <span data-ttu-id="ec1be-117">Em sistemas de 64 bits, os itens do painel de controle de 32 bits são exibidos no painel de controle quando a opção de **pasta exibir itens do painel de controle de 32 bits** está selecionada.</span><span class="sxs-lookup"><span data-stu-id="ec1be-117">On 64-bit systems, 32-bit Control Panel items are displayed in the Control Panel when the **View 32-bit Control Panel Items folder** option is selected.</span></span> <span data-ttu-id="ec1be-118">Os itens de 32 bits devem estar localizados na pasta% SystemRoot% \\ SysWOW64 a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="ec1be-118">The 32-bit items must be located in the %SystemRoot%\\SysWOW64 folder to be displayed.</span></span> <span data-ttu-id="ec1be-119">Eles não exigem nenhum registro adicional.</span><span class="sxs-lookup"><span data-stu-id="ec1be-119">They do not require any further registration.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ec1be-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec1be-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec1be-121">Itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="ec1be-121">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="ec1be-122">Registrando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="ec1be-122">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="ec1be-123">Usando CPLApplet</span><span class="sxs-lookup"><span data-stu-id="ec1be-123">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="ec1be-124">Processamento de mensagens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="ec1be-124">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="ec1be-125">Executando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="ec1be-125">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="ec1be-126">Estendendo itens do painel de controle do sistema</span><span class="sxs-lookup"><span data-stu-id="ec1be-126">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="ec1be-127">Atribuindo categorias do painel de controle</span><span class="sxs-lookup"><span data-stu-id="ec1be-127">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="ec1be-128">Criando links de tarefas pesquisáveis para um item do painel de controle</span><span class="sxs-lookup"><span data-stu-id="ec1be-128">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="ec1be-129">Acessando o painel de controle no modo de segurança</span><span class="sxs-lookup"><span data-stu-id="ec1be-129">Accessing the Control Panel in Safe Mode</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



