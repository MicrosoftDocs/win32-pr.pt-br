---
title: Migrando para o Windows Ribbon Framework
description: Um aplicativo que se baseia em menus, barras de ferramentas e caixas de diálogo tradicionais pode ser migrado para a interface do usuário rica, dinâmica e controlada por contexto do sistema de comando da estrutura da faixa de ferramentas do Windows.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Faixa de-se do Windows, migrando para o
- Faixa de faixas, migrando para o
- migrando para a faixa de para do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74822781f891815c6eb30d9e15a7f7efaa983fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454184"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a><span data-ttu-id="d86e6-106">Migrando para o Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="d86e6-106">Migrating to the Windows Ribbon Framework</span></span>

<span data-ttu-id="d86e6-107">Um aplicativo que se baseia em menus, barras de ferramentas e caixas de diálogo tradicionais pode ser migrado para a interface do usuário rica, dinâmica e controlada por contexto do sistema de comando da estrutura da faixa de ferramentas do Windows.</span><span class="sxs-lookup"><span data-stu-id="d86e6-107">An application that relies on traditional menus, toolbars, and dialogs can be migrated to the rich, dynamic, and context-driven UI of the Windows Ribbon framework Command system.</span></span> <span data-ttu-id="d86e6-108">Essa é uma maneira fácil e eficaz de modernizar e revitalize o aplicativo ao mesmo tempo em que também melhora a acessibilidade, a usabilidade e a capacidade de descoberta de sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="d86e6-108">This is an easy and effective way to modernize and revitalize the application while also improving the accessibility, usability, and discoverability of its functionality.</span></span>

## <a name="introduction"></a><span data-ttu-id="d86e6-109">Introdução</span><span class="sxs-lookup"><span data-stu-id="d86e6-109">Introduction</span></span>

<span data-ttu-id="d86e6-110">Em geral, a migração de um aplicativo existente para a estrutura da faixa de opções envolve o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d86e6-110">In general, migrating an existing application to the Ribbon framework involves the following:</span></span>

-   <span data-ttu-id="d86e6-111">Criar uma organização de controle e layout da faixa de opção que expõe a funcionalidade do aplicativo existente e é flexível o suficiente para dar suporte à nova funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="d86e6-111">Designing a Ribbon layout and control organization that exposes the functionality of the existing application and is flexible enough to support new functionality.</span></span>
-   <span data-ttu-id="d86e6-112">Adaptando o código do aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="d86e6-112">Adapting the code of the existing application.</span></span>
-   <span data-ttu-id="d86e6-113">Migrar recursos de aplicativo (cadeias de caracteres e imagens) existentes para a estrutura da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d86e6-113">Migrating existing application resources (strings and images) to the Ribbon framework.</span></span>

> [!Note]  
> <span data-ttu-id="d86e6-114">As [diretrizes de experiência do usuário da faixa](https://msdn.microsoft.com/library/cc872782.aspx) de ver devem ser revisadas para determinar se o aplicativo é um candidato adequado para uma interface do usuário da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d86e6-114">The [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed to determine if the application is a suitable candidate for a Ribbon UI.</span></span>

 

## <a name="design-the-ribbon-layout"></a><span data-ttu-id="d86e6-115">Criar o layout da faixa de opção</span><span class="sxs-lookup"><span data-stu-id="d86e6-115">Design the Ribbon Layout</span></span>

<span data-ttu-id="d86e6-116">Possíveis designs de interface do usuário da faixa de opção e layouts de controle podem ser identificados executando estas etapas:</span><span class="sxs-lookup"><span data-stu-id="d86e6-116">Potential Ribbon UI designs and control layouts can be identified by performing these steps:</span></span>

1.  <span data-ttu-id="d86e6-117">Fazendo o inventário de todas as funcionalidades existentes.</span><span class="sxs-lookup"><span data-stu-id="d86e6-117">Taking inventory of all existing functionality.</span></span>
2.  <span data-ttu-id="d86e6-118">Convertendo essa funcionalidade em comandos da faixa de das.</span><span class="sxs-lookup"><span data-stu-id="d86e6-118">Translating this functionality into Ribbon Commands.</span></span>
3.  <span data-ttu-id="d86e6-119">Organizando os comandos em grupos lógicos.</span><span class="sxs-lookup"><span data-stu-id="d86e6-119">Organizing the Commands into logical groups.</span></span>

### <a name="take-inventory"></a><span data-ttu-id="d86e6-120">Fazer inventário</span><span class="sxs-lookup"><span data-stu-id="d86e6-120">Take Inventory</span></span>

<span data-ttu-id="d86e6-121">Na estrutura da faixa de visão, a funcionalidade exposta por um aplicativo que manipula o estado ou a exibição de um espaço de trabalho ou documento é considerada um comando.</span><span class="sxs-lookup"><span data-stu-id="d86e6-121">In the Ribbon framework, the functionality exposed by an application that manipulates the state or the view of a workspace or document is considered a command.</span></span> <span data-ttu-id="d86e6-122">O que constitui um comando pode variar e depende da natureza e do domínio do aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="d86e6-122">What constitutes a command may vary and depends on the nature and domain of the existing application.</span></span>

<span data-ttu-id="d86e6-123">A tabela a seguir lista um conjunto de comandos básicos para um aplicativo de edição de texto hipotético:</span><span class="sxs-lookup"><span data-stu-id="d86e6-123">The following table lists a set of basic commands for a hypothetical text editing application:</span></span>



| <span data-ttu-id="d86e6-124">Símbolo</span><span class="sxs-lookup"><span data-stu-id="d86e6-124">Symbol</span></span>           | <span data-ttu-id="d86e6-125">ID</span><span class="sxs-lookup"><span data-stu-id="d86e6-125">ID</span></span>     | <span data-ttu-id="d86e6-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="d86e6-126">Description</span></span>               |
|------------------|--------|---------------------------|
| <span data-ttu-id="d86e6-127">\_novo arquivo de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-127">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="d86e6-128">0xE100</span><span class="sxs-lookup"><span data-stu-id="d86e6-128">0xE100</span></span> | <span data-ttu-id="d86e6-129">Novo documento</span><span class="sxs-lookup"><span data-stu-id="d86e6-129">New document</span></span>              |
| <span data-ttu-id="d86e6-130">\_salvar arquivo de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-130">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="d86e6-131">0xE103</span><span class="sxs-lookup"><span data-stu-id="d86e6-131">0xE103</span></span> | <span data-ttu-id="d86e6-132">Salvar documento</span><span class="sxs-lookup"><span data-stu-id="d86e6-132">Save document</span></span>             |
| <span data-ttu-id="d86e6-133">\_salvar arquivo de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-133">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="d86e6-134">0xE104</span><span class="sxs-lookup"><span data-stu-id="d86e6-134">0xE104</span></span> | <span data-ttu-id="d86e6-135">Salvar como... '</span><span class="sxs-lookup"><span data-stu-id="d86e6-135">Save As... (dialog)</span></span>       |
| <span data-ttu-id="d86e6-136">arquivo de ID \_ \_ aberto</span><span class="sxs-lookup"><span data-stu-id="d86e6-136">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="d86e6-137">0xE101</span><span class="sxs-lookup"><span data-stu-id="d86e6-137">0xE101</span></span> | <span data-ttu-id="d86e6-138">Abrir... '</span><span class="sxs-lookup"><span data-stu-id="d86e6-138">Open... (dialog)</span></span>          |
| <span data-ttu-id="d86e6-139">\_saída do arquivo de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-139">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="d86e6-140">0xE102</span><span class="sxs-lookup"><span data-stu-id="d86e6-140">0xE102</span></span> | <span data-ttu-id="d86e6-141">Sair do aplicativo</span><span class="sxs-lookup"><span data-stu-id="d86e6-141">Exit the application</span></span>      |
| <span data-ttu-id="d86e6-142">\_desfazer edição de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-142">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="d86e6-143">0xE12B</span><span class="sxs-lookup"><span data-stu-id="d86e6-143">0xE12B</span></span> | <span data-ttu-id="d86e6-144">Desfazer</span><span class="sxs-lookup"><span data-stu-id="d86e6-144">Undo</span></span>                      |
| <span data-ttu-id="d86e6-145">edição de ID \_ \_ recortada</span><span class="sxs-lookup"><span data-stu-id="d86e6-145">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="d86e6-146">0xE123</span><span class="sxs-lookup"><span data-stu-id="d86e6-146">0xE123</span></span> | <span data-ttu-id="d86e6-147">Recortar texto selecionado</span><span class="sxs-lookup"><span data-stu-id="d86e6-147">Cut selected text</span></span>         |
| <span data-ttu-id="d86e6-148">ID \_ Editar \_ cópia</span><span class="sxs-lookup"><span data-stu-id="d86e6-148">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="d86e6-149">0xE122</span><span class="sxs-lookup"><span data-stu-id="d86e6-149">0xE122</span></span> | <span data-ttu-id="d86e6-150">Copiar texto selecionado</span><span class="sxs-lookup"><span data-stu-id="d86e6-150">Copy selected text</span></span>        |
| <span data-ttu-id="d86e6-151">\_Editar \_ colar ID</span><span class="sxs-lookup"><span data-stu-id="d86e6-151">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="d86e6-152">0xE125</span><span class="sxs-lookup"><span data-stu-id="d86e6-152">0xE125</span></span> | <span data-ttu-id="d86e6-153">Colar texto da área de transferência</span><span class="sxs-lookup"><span data-stu-id="d86e6-153">Paste text from clipboard</span></span> |
| <span data-ttu-id="d86e6-154">edição de ID \_ \_ limpar</span><span class="sxs-lookup"><span data-stu-id="d86e6-154">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="d86e6-155">0xE120</span><span class="sxs-lookup"><span data-stu-id="d86e6-155">0xE120</span></span> | <span data-ttu-id="d86e6-156">Excluir texto selecionado</span><span class="sxs-lookup"><span data-stu-id="d86e6-156">Delete selected text</span></span>      |
| <span data-ttu-id="d86e6-157">\_zoom da exibição de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-157">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="d86e6-158">1242</span><span class="sxs-lookup"><span data-stu-id="d86e6-158">1242</span></span>   | <span data-ttu-id="d86e6-159">Aplicar zoom... '</span><span class="sxs-lookup"><span data-stu-id="d86e6-159">Zoom... (dialog)</span></span>          |



 

<span data-ttu-id="d86e6-160">Olhe além dos menus e barras de ferramentas existentes ao criar um inventário de comandos.</span><span class="sxs-lookup"><span data-stu-id="d86e6-160">Look beyond existing menus and toolbars when building an inventory of commands.</span></span> <span data-ttu-id="d86e6-161">Considere todas as maneiras como um usuário pode interagir com o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d86e6-161">Consider all the ways a user can interact with the workspace.</span></span> <span data-ttu-id="d86e6-162">Embora nem todos os comandos sejam adequados para inclusão na faixa de faixas, esse exercício pode expor comandos que foram anteriormente obscurecidos por camadas de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="d86e6-162">Even though not every command is suitable for inclusion in the Ribbon, this exercise may very well expose commands that were previously obscured by layers of UI.</span></span>

### <a name="translate"></a><span data-ttu-id="d86e6-163">Translate</span><span class="sxs-lookup"><span data-stu-id="d86e6-163">Translate</span></span>

<span data-ttu-id="d86e6-164">Nem todos os comandos precisam ser representados na interface do usuário da faixa de para.</span><span class="sxs-lookup"><span data-stu-id="d86e6-164">Not every command needs to be represented in the Ribbon UI.</span></span> <span data-ttu-id="d86e6-165">Por exemplo, inserir texto, alterar uma seleção, rolar ou mover o ponto de inserção com o mouse tudo qualificado como comandos no editor de texto hipotético, no entanto, eles não são adequados para expor em uma barra de comandos, pois cada um envolve uma interação direta com a interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d86e6-165">For example, entering text, changing a selection, scrolling, or moving the insertion-point with the mouse all qualify as commands in the hypothetical text editor, however, these are not suitable to expose in a command bar as each involves a direct interaction with the UI of the application.</span></span>

<span data-ttu-id="d86e6-166">Por outro lado, algumas funcionalidades podem não ser consideradas como um comando no sentido tradicional.</span><span class="sxs-lookup"><span data-stu-id="d86e6-166">Conversely, some functionality may not be thought of as a command in the traditional sense.</span></span> <span data-ttu-id="d86e6-167">Por exemplo, em vez de ser ocultado em uma caixa de diálogo, os ajustes de margem da página da impressora podem ser representados na faixa de bits como um grupo de controles Spinner em uma guia contextual ou no [modo de aplicativo](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="d86e6-167">For example, instead of being buried in a dialog box, printer page-margin adjustments could be represented in the Ribbon as a group of Spinner controls in a contextual tab or [application mode](ribbon-applicationmodes.md).</span></span>

> [!Note]  
> <span data-ttu-id="d86e6-168">Anote a ID numérica que pode ser atribuída a cada comando.</span><span class="sxs-lookup"><span data-stu-id="d86e6-168">Make note of the numeric ID that may be assigned to each command.</span></span> <span data-ttu-id="d86e6-169">Algumas estruturas de interface do usuário, como MFC (MFC), definem IDs para comandos como o menu arquivo e editar (0xE100 para 0xE200).</span><span class="sxs-lookup"><span data-stu-id="d86e6-169">Some UI frameworks, such as Microsoft Foundation Classes (MFC), define IDs for commands such as the file and edit menu (0xE100 to 0xE200).</span></span>

 

### <a name="organize"></a><span data-ttu-id="d86e6-170">Organizar</span><span class="sxs-lookup"><span data-stu-id="d86e6-170">Organize</span></span>

<span data-ttu-id="d86e6-171">Antes de tentar organizar o inventário de comandos, as [diretrizes de experiência do usuário da faixa](https://msdn.microsoft.com/library/cc872782.aspx) de opções devem ser examinadas para obter as práticas recomendadas ao implementar uma interface do usuário da faixa.</span><span class="sxs-lookup"><span data-stu-id="d86e6-171">Before attempting to organize the command inventory, the [Ribbon User Experience Guidelines](https://msdn.microsoft.com/library/cc872782.aspx) should be reviewed for best practices when implementing a Ribbon UI.</span></span>

<span data-ttu-id="d86e6-172">Em geral, as seguintes regras podem ser aplicadas à organização de comando da faixa de opções:</span><span class="sxs-lookup"><span data-stu-id="d86e6-172">In general, the following rules can be applied to Ribbon Command organization:</span></span>

-   <span data-ttu-id="d86e6-173">Os comandos que operam no arquivo ou o aplicativo geral provavelmente pertencem ao [menu do aplicativo](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="d86e6-173">Commands that operate on the file or the overall application most likely belong in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="d86e6-174">Comandos usados com frequência, como recortar, copiar e colar (como no exemplo do editor de texto) normalmente são colocados em uma guia página inicial padrão. Em aplicativos mais complexos, eles podem estar duplicados em outro lugar na interface do usuário da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d86e6-174">Frequently used Commands such as Cut, Copy, and Paste (as in the text editor example) are typically placed on a default home tab. In more complex applications, they may be duplicated elsewhere in the Ribbon UI.</span></span>
-   <span data-ttu-id="d86e6-175">Os comandos importantes ou frequentemente usados podem garantir a inclusão padrão na [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="d86e6-175">Important or frequently used Commands might warrant default inclusion in the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="d86e6-176">A estrutura da faixa de visão também fornece controles ContextMenu e Minibarra por meio da exibição ContextPopup.</span><span class="sxs-lookup"><span data-stu-id="d86e6-176">The Ribbon framework also provides ContextMenu and MiniToolbar controls through the ContextPopup View.</span></span> <span data-ttu-id="d86e6-177">Esses recursos não são obrigatórios, mas se seu aplicativo tiver um ou mais menus de contexto existentes, a migração dos comandos que eles contêm poderá permitir a reutilização da base de código existente com associação automática a recursos existentes.</span><span class="sxs-lookup"><span data-stu-id="d86e6-177">These features are not mandatory, but if your application has one or more existing context menus then migrating the commands they contain may allow the reuse of the existing codebase with automatic binding to existing resources.</span></span>

<span data-ttu-id="d86e6-178">Como cada aplicativo é diferente, leia as diretrizes e tente aplicá-los à extensão mais completa possível.</span><span class="sxs-lookup"><span data-stu-id="d86e6-178">Because every application is different, read the guidelines and try to apply them to the fullest extent possible.</span></span> <span data-ttu-id="d86e6-179">Uma das metas da estrutura da faixa de faixas é fornecer uma experiência do usuário familiar e consistente, e esse objetivo será mais atingível se os designs de novos aplicativos espelharem os aplicativos da faixa de das faixas de uma forma mais bem possível.</span><span class="sxs-lookup"><span data-stu-id="d86e6-179">One of the goals of the Ribbon framework is to provide a familiar, consistent user experience and this goal will be more achievable if designs for new applications mirror existing Ribbon applications as much as possible.</span></span>

## <a name="adapt-your-code"></a><span data-ttu-id="d86e6-180">Adapte seu código</span><span class="sxs-lookup"><span data-stu-id="d86e6-180">Adapt Your Code</span></span>

<span data-ttu-id="d86e6-181">Depois que os comandos da faixa de faixas forem identificados e organizados em agrupamentos lógicos, o número de etapas envolvidas na incorporação da estrutura da faixa de das faixas ao código do aplicativo existente dependerá da complexidade do aplicativo original.</span><span class="sxs-lookup"><span data-stu-id="d86e6-181">Once the Ribbon Commands have been identified and organized into logical groupings, the number of steps involved when incorporating the Ribbon framework into existing application code depends on the complexity of the original application.</span></span> <span data-ttu-id="d86e6-182">Em geral, há três etapas básicas:</span><span class="sxs-lookup"><span data-stu-id="d86e6-182">In general, there are three basic steps:</span></span>

-   <span data-ttu-id="d86e6-183">Crie a marcação da faixa de opção com base na organização de comandos e na especificação de layout.</span><span class="sxs-lookup"><span data-stu-id="d86e6-183">Create the Ribbon markup based on the Command organization and layout specification.</span></span>
-   <span data-ttu-id="d86e6-184">Substitua o menu herdado e a funcionalidade da barra de ferramentas com a funcionalidade da faixa de</span><span class="sxs-lookup"><span data-stu-id="d86e6-184">Replace legacy menu and toolbar functionality with Ribbon functionality.</span></span>
-   <span data-ttu-id="d86e6-185">Implemente um adaptador IUICommandHandler.</span><span class="sxs-lookup"><span data-stu-id="d86e6-185">Implement an IUICommandHandler adapter.</span></span>

### <a name="create-the-markup"></a><span data-ttu-id="d86e6-186">Criar a marcação</span><span class="sxs-lookup"><span data-stu-id="d86e6-186">Create The Markup</span></span>

<span data-ttu-id="d86e6-187">A lista de comandos, bem como sua organização e layout, são declarados por meio do arquivo de marcação da faixa de opção que é consumido pelo [compilador de marcação da faixa](windowsribbon-intentcl.md)de lista.</span><span class="sxs-lookup"><span data-stu-id="d86e6-187">The list of commands as well as their organization and layout are declared through the Ribbon markup file which is consumed by the [Ribbon markup compiler](windowsribbon-intentcl.md).</span></span>

> [!Note]  
> <span data-ttu-id="d86e6-188">Muitas das etapas necessárias para adaptar um aplicativo existente são semelhantes às necessárias para iniciar um novo aplicativo da faixa de tipos.</span><span class="sxs-lookup"><span data-stu-id="d86e6-188">Many of the steps required to adapt an existing application are similar to those required to start a new Ribbon application.</span></span> <span data-ttu-id="d86e6-189">Para obter mais informações, consulte o tutorial [criando um aplicativo da faixa de Ribbon](windowsribbon-stepbystep.md) para um novo aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d86e6-189">For more information, see the [Creating a Ribbon Application](windowsribbon-stepbystep.md) tutorial for a new Ribbon application walkthrough.</span></span>

 

<span data-ttu-id="d86e6-190">Há duas seções principais para a marcação da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d86e6-190">There are two primary sections to the Ribbon markup.</span></span> <span data-ttu-id="d86e6-191">A primeira seção é um manifesto de comandos e seus recursos associados (cadeias de caracteres e imagens).</span><span class="sxs-lookup"><span data-stu-id="d86e6-191">The first section is a manifest of Commands and their associated resources (strings and images).</span></span> <span data-ttu-id="d86e6-192">A segunda seção especifica a estrutura e o posicionamento dos controles na faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d86e6-192">The second section specifies the structure and placement of controls on the Ribbon.</span></span>

<span data-ttu-id="d86e6-193">A marcação para o editor de texto simples pode ser semelhante ao exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d86e6-193">The markup for the simple text editor might look something like the following example:</span></span>

> [!Note]  
> <span data-ttu-id="d86e6-194">Os recursos de imagem e de cadeia de caracteres são abordados posteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="d86e6-194">Image and string resources are covered later in this article.</span></span>

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



<span data-ttu-id="d86e6-195">Para evitar a redefinição de símbolos que são definidos por uma estrutura de interface do usuário, como o MFC, o exemplo anterior usa nomes de símbolo ligeiramente diferentes para cada comando (arquivo de ID \_ \_ novo versus ID \_ cmd \_ novo).</span><span class="sxs-lookup"><span data-stu-id="d86e6-195">To avoid redefining symbols that are defined by a UI framework such as MFC, the previous example uses slightly different symbol names for each Command (ID\_FILE\_NEW versus ID\_CMD\_NEW).</span></span> <span data-ttu-id="d86e6-196">No entanto, a ID numérica atribuída a cada comando deve permanecer a mesma.</span><span class="sxs-lookup"><span data-stu-id="d86e6-196">However, the numeric ID assigned to each Command must remain the same.</span></span>

<span data-ttu-id="d86e6-197">Para integrar o arquivo de marcação em um aplicativo, configure uma etapa de compilação personalizada para executar o compilador de marcação da faixa de UICC.exe.</span><span class="sxs-lookup"><span data-stu-id="d86e6-197">To integrate the markup file into an application, configure a custom build step to run the Ribbon markup compiler, UICC.exe.</span></span> <span data-ttu-id="d86e6-198">Os arquivos de cabeçalho e de recurso resultantes são então incorporados ao projeto existente.</span><span class="sxs-lookup"><span data-stu-id="d86e6-198">The resulting header and resource files are then incorporated into the existing project.</span></span> <span data-ttu-id="d86e6-199">Se o aplicativo de faixa de opções do editor de texto de exemplo for denominado "RibbonPad", uma linha de comando de compilação personalizada semelhante à seguinte será necessária:</span><span class="sxs-lookup"><span data-stu-id="d86e6-199">If the example text editor Ribbon application is named "RibbonPad", a custom-build command line similar to the following is required:</span></span>


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



<span data-ttu-id="d86e6-200">O compilador de marcação cria um arquivo binário, um arquivo de cabeçalho (H) e um arquivo de recurso (RC).</span><span class="sxs-lookup"><span data-stu-id="d86e6-200">The markup compiler creates a binary file, a header (H) file and a resource (RC) file.</span></span> <span data-ttu-id="d86e6-201">Como o aplicativo existente provavelmente tem um arquivo RC existente, inclua os arquivos H e RC gerados nesse arquivo RC, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d86e6-201">Because the existing application likely has an existing RC file, include the generated H and RC files in that RC file, as shown in the following example:</span></span>


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a><span data-ttu-id="d86e6-202">Substituir menus herdados e barras de ferramentas</span><span class="sxs-lookup"><span data-stu-id="d86e6-202">Replace Legacy Menus and Toolbars</span></span>

<span data-ttu-id="d86e6-203">Substituir menus e barras de ferramentas padrão por uma faixa de opções em um aplicativo herdado requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d86e6-203">Replacing standard menus and toolbars with a ribbon in a legacy application requires the following:</span></span>

1.  <span data-ttu-id="d86e6-204">Remova as referências de recurso de barra de ferramentas e de menu do arquivo de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d86e6-204">Remove toolbar and menu resource references from the application's resource file.</span></span>
2.  <span data-ttu-id="d86e6-205">Excluir toda a barra de ferramentas e o código de inicialização da barra de menus.</span><span class="sxs-lookup"><span data-stu-id="d86e6-205">Delete all toolbar and menu bar initialization code.</span></span>
3.  <span data-ttu-id="d86e6-206">Exclui qualquer código usado para anexar uma barra de ferramentas ou barra de menus à janela de nível superior do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d86e6-206">Delete any code used to attach a toolbar or menu bar to the top-level window of the application.</span></span>
4.  <span data-ttu-id="d86e6-207">Crie uma instância da estrutura da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d86e6-207">Instantiate the Ribbon framework.</span></span>
5.  <span data-ttu-id="d86e6-208">Anexe a faixa de bits à janela de nível superior do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d86e6-208">Attach the ribbon to the top-level window of the application.</span></span>
6.  <span data-ttu-id="d86e6-209">Carregar a marcação compilada.</span><span class="sxs-lookup"><span data-stu-id="d86e6-209">Load the compiled markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d86e6-210">As tabelas de atalho de teclado e barra de status existentes devem ser preservadas, pois a estrutura da faixa de faixas não substitui esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d86e6-210">Existing status bar and keyboard shortcut tables should be preserved as the Ribbon framework does not replace these features.</span></span>

 

<span data-ttu-id="d86e6-211">O exemplo a seguir demonstra como inicializar a estrutura usando [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span><span class="sxs-lookup"><span data-stu-id="d86e6-211">The following example demonstrates how to initialize the framework using [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):</span></span>


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



<span data-ttu-id="d86e6-212">O exemplo a seguir demonstra como usar [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) para carregar a marcação compilada:</span><span class="sxs-lookup"><span data-stu-id="d86e6-212">The following example demonstrates how to use [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to load the compiled markup:</span></span>


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



<span data-ttu-id="d86e6-213">A classe CApplication, mencionada acima, deve implementar um par de interfaces COM (Component Object Model) definidas pela estrutura da faixa de opções: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) e [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span><span class="sxs-lookup"><span data-stu-id="d86e6-213">The CApplication class, referred to above, must implement a pair of Component Object Model (COM) interfaces defined by the Ribbon framework: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) and [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).</span></span>

<span data-ttu-id="d86e6-214">O [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) fornece a interface de retorno de chamada principal entre a estrutura e o aplicativo (por exemplo, a altura da faixa de faixas é comunicada por meio de [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)), enquanto os retornos de chamada para comandos individuais são fornecidos em resposta a [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span><span class="sxs-lookup"><span data-stu-id="d86e6-214">[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) provides the main callback interface between the framework and the application (for example, the height of the ribbon is communicated through [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)) while the callbacks for individual Commands are provided in response to [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).</span></span>

<span data-ttu-id="d86e6-215">**Dica:** Algumas estruturas de aplicativo, como MFC, exigem que a altura da barra de faixa de faixas seja levada em conta ao renderizar o espaço de documento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d86e6-215">**Tip:** Some application frameworks, such as MFC, require that the height of the ribbon bar be taken into account when rendering the document space of the application.</span></span> <span data-ttu-id="d86e6-216">Nesses casos, a adição de uma janela oculta para sobrepor a barra da faixa de faixas e forçar o espaço do documento para a altura desejada é necessária.</span><span class="sxs-lookup"><span data-stu-id="d86e6-216">In these cases, the addition of a hidden window to overlay the ribbon bar and force the document space to the desired height is necessary.</span></span> <span data-ttu-id="d86e6-217">Para obter um exemplo dessa abordagem, em que uma função de layout é chamada com base na altura da faixa de opção retornada pelo método [**IUIRibbon:: GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) , consulte o [exemplo HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="d86e6-217">For an example of this approach, where a layout function is called based on the ribbon height returned by the [**IUIRibbon::GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) method, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

<span data-ttu-id="d86e6-218">O exemplo de código a seguir demonstra uma implementação [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) :</span><span class="sxs-lookup"><span data-stu-id="d86e6-218">The following code example demonstrates an [**IUIApplication::OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) implementation:</span></span>


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a><span data-ttu-id="d86e6-219">Implementar um adaptador IUICommandHandler</span><span class="sxs-lookup"><span data-stu-id="d86e6-219">Implement an IUICommandHandler Adapter</span></span>

<span data-ttu-id="d86e6-220">Dependendo do design do aplicativo original, pode ser mais fácil ter várias implementações de manipulador de comandos ou um único manipulador de comando de ponte que invoque a lógica de comando de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="d86e6-220">Depending on the design of the original application, it may be easier to have multiple Command handler implementations, or a single bridging Command handler that invokes the existing-application command logic.</span></span> <span data-ttu-id="d86e6-221">Muitos aplicativos usam \_ mensagens de comando do WM para essa finalidade, em que é suficiente fornecer um único manipulador de comandos de finalidade única que simplesmente encaminhe \_ as mensagens de comando do WM para a janela de nível superior.</span><span class="sxs-lookup"><span data-stu-id="d86e6-221">Many applications use WM\_COMMAND messages for this purpose where it is sufficient to provide a single, all-purpose command handler that simply forwards WM\_COMMAND messages to the top-level window.</span></span>

<span data-ttu-id="d86e6-222">No entanto, essa abordagem requer tratamento especial para comandos como **Exit** ou **Close**.</span><span class="sxs-lookup"><span data-stu-id="d86e6-222">However, this approach requires special handling for Commands such as **Exit** or **Close**.</span></span> <span data-ttu-id="d86e6-223">Como a faixa de opções não pode ser destruída enquanto está processando uma mensagem de janela, a mensagem de fechamento do WM \_ deve ser postada no thread da interface do usuário do aplicativo e não deve ser processada de forma síncrona, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d86e6-223">Because the Ribbon cannot be destroyed while it's processing a window message, the WM\_CLOSE message should be posted to the UI thread of the application and should not be processed synchronously, as shown in the following example:</span></span>


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a><span data-ttu-id="d86e6-224">Migrando recursos</span><span class="sxs-lookup"><span data-stu-id="d86e6-224">Migrating Resources</span></span>

<span data-ttu-id="d86e6-225">Quando o manifesto de comandos tiver sido definido, a estrutura da faixa de faixas foi declarada e o código do aplicativo adaptado para hospedar a estrutura da faixa de faixas, a etapa final é a especificação dos recursos de cadeia de caracteres e de imagem para cada comando.</span><span class="sxs-lookup"><span data-stu-id="d86e6-225">When the manifest of commands has been defined, the structure of the Ribbon has been declared, and the application code adapted to host the Ribbon framework, the final step is the specification of string and image resources for each Command.</span></span>

> [!Note]  
> <span data-ttu-id="d86e6-226">Os recursos de cadeia de caracteres e de imagem normalmente são fornecidos no arquivo de marcação.</span><span class="sxs-lookup"><span data-stu-id="d86e6-226">String and image resources are typically provided in the markup file.</span></span> <span data-ttu-id="d86e6-227">No entanto, eles podem ser gerados ou substituídos programaticamente implementando o método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="d86e6-227">However, they can be generated or replaced programmatically by implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

 

### <a name="string-resources"></a><span data-ttu-id="d86e6-228">Recursos de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="d86e6-228">String Resources</span></span>

<span data-ttu-id="d86e6-229">[**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) é a propriedade de cadeia de caracteres mais comum definida para um comando.</span><span class="sxs-lookup"><span data-stu-id="d86e6-229">[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) is the most common string property defined for a Command.</span></span> <span data-ttu-id="d86e6-230">Eles são renderizados como rótulos de texto para guias, grupos e controles individuais.</span><span class="sxs-lookup"><span data-stu-id="d86e6-230">These are rendered as the text labels for tabs, groups, and individual controls.</span></span> <span data-ttu-id="d86e6-231">Uma cadeia de caracteres de rótulo de um item de menu herdado geralmente pode ser reutilizada para um **Command. LabelTitle** sem muita edição.</span><span class="sxs-lookup"><span data-stu-id="d86e6-231">A label string from a legacy menu item can typically be re-used for a **Command.LabelTitle** without much editing.</span></span>

<span data-ttu-id="d86e6-232">No entanto, as seguintes convenções foram alteradas com o advento da faixa de opções:</span><span class="sxs-lookup"><span data-stu-id="d86e6-232">However, the following conventions have changed with the advent of the Ribbon:</span></span>

-   <span data-ttu-id="d86e6-233">O sufixo de reticências (...), usado para indicar um comando de inicialização de caixa de diálogo, não é mais necessário.</span><span class="sxs-lookup"><span data-stu-id="d86e6-233">The ellipsis (...) suffix, used to indicate a dialog-launching command, is no longer necessary.</span></span>
-   <span data-ttu-id="d86e6-234">O e comercial (&) ainda pode ser usado para indicar um atalho de teclado para um comando que aparece em um menu, mas a propriedade [**Command. KeyTip**](windowsribbon-element-command-keytip.md) com suporte da estrutura atende a uma finalidade semelhante.</span><span class="sxs-lookup"><span data-stu-id="d86e6-234">The ampersand (&) can still be used to indicate a keyboard-shortcut for a Command that appears in a menu, but the [**Command.Keytip**](windowsribbon-element-command-keytip.md) property supported by the framework fulfills a similar purpose.</span></span>

<span data-ttu-id="d86e6-235">Referindo-se ao exemplo do editor de texto, as seguintes cadeias de caracteres para LabelTitle e KeyTip podem ser especificadas:</span><span class="sxs-lookup"><span data-stu-id="d86e6-235">Referring back to the text editor example, the following strings for LabelTitle and Keytip could be specified:</span></span>



| <span data-ttu-id="d86e6-236">Símbolo</span><span class="sxs-lookup"><span data-stu-id="d86e6-236">Symbol</span></span>           | <span data-ttu-id="d86e6-237">Cadeia de caracteres original</span><span class="sxs-lookup"><span data-stu-id="d86e6-237">Original string</span></span> | <span data-ttu-id="d86e6-238">Cadeia de caracteres LabelTitle</span><span class="sxs-lookup"><span data-stu-id="d86e6-238">LabelTitle string</span></span> | <span data-ttu-id="d86e6-239">Cadeia de caracteres KeyTip</span><span class="sxs-lookup"><span data-stu-id="d86e6-239">Keytip string</span></span> |
|------------------|-----------------|-------------------|---------------|
| <span data-ttu-id="d86e6-240">\_novo arquivo de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-240">ID\_FILE\_NEW</span></span>    | <span data-ttu-id="d86e6-241">&novo</span><span class="sxs-lookup"><span data-stu-id="d86e6-241">&New</span></span>            | <span data-ttu-id="d86e6-242">&novo</span><span class="sxs-lookup"><span data-stu-id="d86e6-242">&New</span></span>              | <span data-ttu-id="d86e6-243">N</span><span class="sxs-lookup"><span data-stu-id="d86e6-243">N</span></span>             |
| <span data-ttu-id="d86e6-244">\_salvar arquivo de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-244">ID\_FILE\_SAVE</span></span>   | <span data-ttu-id="d86e6-245">&salvar</span><span class="sxs-lookup"><span data-stu-id="d86e6-245">&Save</span></span>           | <span data-ttu-id="d86e6-246">&salvar</span><span class="sxs-lookup"><span data-stu-id="d86e6-246">&Save</span></span>             | <span data-ttu-id="d86e6-247">S</span><span class="sxs-lookup"><span data-stu-id="d86e6-247">S</span></span>             |
| <span data-ttu-id="d86e6-248">\_salvar arquivo de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-248">ID\_FILE\_SAVEAS</span></span> | <span data-ttu-id="d86e6-249">Salvar &como...</span><span class="sxs-lookup"><span data-stu-id="d86e6-249">Save &As…</span></span>       | <span data-ttu-id="d86e6-250">Salvar &como</span><span class="sxs-lookup"><span data-stu-id="d86e6-250">Save &as</span></span>          | <span data-ttu-id="d86e6-251">Um</span><span class="sxs-lookup"><span data-stu-id="d86e6-251">A</span></span>             |
| <span data-ttu-id="d86e6-252">arquivo de ID \_ \_ aberto</span><span class="sxs-lookup"><span data-stu-id="d86e6-252">ID\_FILE\_OPEN</span></span>   | <span data-ttu-id="d86e6-253">&abrir...</span><span class="sxs-lookup"><span data-stu-id="d86e6-253">&Open…</span></span>          | <span data-ttu-id="d86e6-254">&amp;Open</span><span class="sxs-lookup"><span data-stu-id="d86e6-254">&Open</span></span>             | <span data-ttu-id="d86e6-255">O</span><span class="sxs-lookup"><span data-stu-id="d86e6-255">O</span></span>             |
| <span data-ttu-id="d86e6-256">\_saída do arquivo de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-256">ID\_FILE\_EXIT</span></span>   | <span data-ttu-id="d86e6-257">Sa&ir</span><span class="sxs-lookup"><span data-stu-id="d86e6-257">E&xit</span></span>           | <span data-ttu-id="d86e6-258">Sa&ir</span><span class="sxs-lookup"><span data-stu-id="d86e6-258">E&xit</span></span>             | <span data-ttu-id="d86e6-259">X</span><span class="sxs-lookup"><span data-stu-id="d86e6-259">X</span></span>             |
| <span data-ttu-id="d86e6-260">\_desfazer edição de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-260">ID\_EDIT\_UNDO</span></span>   | <span data-ttu-id="d86e6-261">&desfazer</span><span class="sxs-lookup"><span data-stu-id="d86e6-261">&Undo</span></span>           | <span data-ttu-id="d86e6-262">Desfazer</span><span class="sxs-lookup"><span data-stu-id="d86e6-262">Undo</span></span>              | <span data-ttu-id="d86e6-263">Z</span><span class="sxs-lookup"><span data-stu-id="d86e6-263">Z</span></span>             |
| <span data-ttu-id="d86e6-264">edição de ID \_ \_ recortada</span><span class="sxs-lookup"><span data-stu-id="d86e6-264">ID\_EDIT\_CUT</span></span>    | <span data-ttu-id="d86e6-265">Cu&t</span><span class="sxs-lookup"><span data-stu-id="d86e6-265">Cu&t</span></span>            | <span data-ttu-id="d86e6-266">Cu&t</span><span class="sxs-lookup"><span data-stu-id="d86e6-266">Cu&t</span></span>              | <span data-ttu-id="d86e6-267">X</span><span class="sxs-lookup"><span data-stu-id="d86e6-267">X</span></span>             |
| <span data-ttu-id="d86e6-268">ID \_ Editar \_ cópia</span><span class="sxs-lookup"><span data-stu-id="d86e6-268">ID\_EDIT\_COPY</span></span>   | <span data-ttu-id="d86e6-269">&cópia</span><span class="sxs-lookup"><span data-stu-id="d86e6-269">&Copy</span></span>           | <span data-ttu-id="d86e6-270">&cópia</span><span class="sxs-lookup"><span data-stu-id="d86e6-270">&Copy</span></span>             | <span data-ttu-id="d86e6-271">C</span><span class="sxs-lookup"><span data-stu-id="d86e6-271">C</span></span>             |
| <span data-ttu-id="d86e6-272">\_Editar \_ colar ID</span><span class="sxs-lookup"><span data-stu-id="d86e6-272">ID\_EDIT\_PASTE</span></span>  | <span data-ttu-id="d86e6-273">Colar &</span><span class="sxs-lookup"><span data-stu-id="d86e6-273">&Paste</span></span>          | <span data-ttu-id="d86e6-274">Colar &</span><span class="sxs-lookup"><span data-stu-id="d86e6-274">&Paste</span></span>            | <span data-ttu-id="d86e6-275">V</span><span class="sxs-lookup"><span data-stu-id="d86e6-275">V</span></span>             |
| <span data-ttu-id="d86e6-276">edição de ID \_ \_ limpar</span><span class="sxs-lookup"><span data-stu-id="d86e6-276">ID\_EDIT\_CLEAR</span></span>  | <span data-ttu-id="d86e6-277">&excluir</span><span class="sxs-lookup"><span data-stu-id="d86e6-277">&Delete</span></span>         | <span data-ttu-id="d86e6-278">&excluir</span><span class="sxs-lookup"><span data-stu-id="d86e6-278">&Delete</span></span>           | <span data-ttu-id="d86e6-279">D</span><span class="sxs-lookup"><span data-stu-id="d86e6-279">D</span></span>             |
| <span data-ttu-id="d86e6-280">\_zoom da exibição de ID \_</span><span class="sxs-lookup"><span data-stu-id="d86e6-280">ID\_VIEW\_ZOOM</span></span>   | <span data-ttu-id="d86e6-281">&zoom...</span><span class="sxs-lookup"><span data-stu-id="d86e6-281">&Zoom…</span></span>          | <span data-ttu-id="d86e6-282">Zoom</span><span class="sxs-lookup"><span data-stu-id="d86e6-282">Zoom</span></span>              | <span data-ttu-id="d86e6-283">Z</span><span class="sxs-lookup"><span data-stu-id="d86e6-283">Z</span></span>             |



 

<span data-ttu-id="d86e6-284">A seguir está uma lista de outras propriedades de cadeia de caracteres que devem ser definidas na maioria dos comandos:</span><span class="sxs-lookup"><span data-stu-id="d86e6-284">The following is a list of other string properties which should be set on most Commands:</span></span>

-   [<span data-ttu-id="d86e6-285">**Comando. LabelDescription**</span><span class="sxs-lookup"><span data-stu-id="d86e6-285">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)
-   [<span data-ttu-id="d86e6-286">**Comando. TooltipTitle**</span><span class="sxs-lookup"><span data-stu-id="d86e6-286">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)
-   [<span data-ttu-id="d86e6-287">**Comando. TooltipDescription**</span><span class="sxs-lookup"><span data-stu-id="d86e6-287">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)

<span data-ttu-id="d86e6-288">Guias, grupos e outros recursos da interface do usuário da faixa de tipos agora podem ser declarados com todos os recursos de cadeia de caracteres e imagem especificados.</span><span class="sxs-lookup"><span data-stu-id="d86e6-288">Tabs, Groups, and other Ribbon UI features can now be declared with all string and image resources specified.</span></span>

<span data-ttu-id="d86e6-289">O exemplo de marcação de faixa de opções a seguir demonstra vários recursos de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="d86e6-289">The following Ribbon markup example demonstrates various string resources:</span></span>


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a><span data-ttu-id="d86e6-290">Recursos de imagem</span><span class="sxs-lookup"><span data-stu-id="d86e6-290">Image Resources</span></span>

<span data-ttu-id="d86e6-291">A estrutura da faixa de ferramentas dá suporte a formatos de imagem que fornecem uma aparência muito mais rica do que os formatos de imagem com suporte no menu anterior e nos componentes da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d86e6-291">The Ribbon framework supports image formats that provide a much richer look and feel than the image formats supported by previous menu and toolbar components.</span></span>

<span data-ttu-id="d86e6-292">Para o Windows 8 e posterior, a estrutura da faixa de opções dá suporte aos seguintes formatos de gráficos: arquivos BMP (bitmap ARGB) de 32 bits e arquivos PNG (Portable Network Graphics) com transparência.</span><span class="sxs-lookup"><span data-stu-id="d86e6-292">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="d86e6-293">Para o Windows 7 e versões anteriores, os recursos de imagem devem estar em conformidade com o formato gráfico BMP padrão usado no Windows.</span><span class="sxs-lookup"><span data-stu-id="d86e6-293">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="d86e6-294">Os arquivos de imagem existentes podem ser convertidos em qualquer formato.</span><span class="sxs-lookup"><span data-stu-id="d86e6-294">Existing image files can be converted to either format.</span></span> <span data-ttu-id="d86e6-295">No entanto, os resultados podem ser menos satisfatórios se os arquivos de imagem não oferecerem suporte à suavização e transparência.</span><span class="sxs-lookup"><span data-stu-id="d86e6-295">However, the results may be less than satisfactory if the image files do not support antialiasing and transparency.</span></span>

 

<span data-ttu-id="d86e6-296">Não é possível especificar um único tamanho padrão para recursos de imagem na estrutura da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="d86e6-296">It is not possible to specify a single default size for image resources in the Ribbon framework.</span></span> <span data-ttu-id="d86e6-297">No entanto, para dar suporte ao [layout adaptável](windowsribbon-templates.md) de controles, as imagens podem ser especificadas em dois tamanhos (grandes e pequenas).</span><span class="sxs-lookup"><span data-stu-id="d86e6-297">However, to support [adaptive layout](windowsribbon-templates.md) of controls, images can be specified in two sizes (large and small) .</span></span> <span data-ttu-id="d86e6-298">Todas as imagens na estrutura da faixa de opção são dimensionadas de acordo com a resolução de pontos por polegada (DPI) da exibição com o tamanho exato renderizado dependente dessa configuração de DPI.</span><span class="sxs-lookup"><span data-stu-id="d86e6-298">All images in the Ribbon framework are scaled according to the dots per inch (dpi) resolution of the display with the exact rendered size dependent on this dpi setting.</span></span> <span data-ttu-id="d86e6-299">Consulte [especificando recursos de imagem da faixa](windowsribbon-imageformats.md) de visualização para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d86e6-299">See [Specifying Ribbon Image Resources](windowsribbon-imageformats.md) for more information.</span></span>

<span data-ttu-id="d86e6-300">O exemplo a seguir demonstra como um conjunto de imagens específicas de DPI é referenciado na marcação:</span><span class="sxs-lookup"><span data-stu-id="d86e6-300">The following example demonstrates how a set of dpi-specific images are referenced in markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="d86e6-301">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d86e6-301">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d86e6-302">Especificando recursos de imagem da faixa de uma</span><span class="sxs-lookup"><span data-stu-id="d86e6-302">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 