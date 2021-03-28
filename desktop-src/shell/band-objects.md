---
description: A barra do Explorer foi introduzida com o Microsoft Internet Explorer 4,0 para fornecer uma área de exibição adjacente ao painel do navegador.
title: Criar Barras personalizadas do Explorer, Faixas de ferramentas e Faixas da área de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104550296"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a><span data-ttu-id="a441e-103">Criando barras personalizadas do Explorer, faixas de ferramentas e faixas de escrivaninha</span><span class="sxs-lookup"><span data-stu-id="a441e-103">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</span></span>

<span data-ttu-id="a441e-104">A barra do Explorer foi introduzida com o Microsoft Internet Explorer 4,0 para fornecer uma área de exibição adjacente ao painel do navegador.</span><span class="sxs-lookup"><span data-stu-id="a441e-104">The Explorer Bar was introduced with Microsoft Internet Explorer 4.0 to provide a display area adjacent to the browser pane.</span></span> <span data-ttu-id="a441e-105">Ele é basicamente uma janela filho dentro da janela do Windows Internet Explorer e pode ser usado para exibir informações e interagir com o usuário praticamente da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="a441e-105">It is basically a child window within the Windows Internet Explorer window, and it can be used to display information and interact with the user in much the same way.</span></span> <span data-ttu-id="a441e-106">As barras do Explorer são exibidas com mais frequência como um painel vertical no lado esquerdo do painel do navegador.</span><span class="sxs-lookup"><span data-stu-id="a441e-106">Explorer Bars are most commonly displayed as a vertical pane on the left side of the browser pane.</span></span> <span data-ttu-id="a441e-107">No entanto, uma barra do Explorer também pode ser exibida horizontalmente, abaixo do painel do navegador.</span><span class="sxs-lookup"><span data-stu-id="a441e-107">However, an Explorer Bar can also be displayed horizontally, below the browser pane.</span></span>

![Captura de tela que mostra as barras verticais e horizontais do Explorer.](images/expl1.jpg)

<span data-ttu-id="a441e-109">Há uma ampla variedade de usos possíveis para a barra do Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-109">There is a wide range of possible uses for the Explorer Bar.</span></span> <span data-ttu-id="a441e-110">Os usuários podem selecionar a opção que desejam ver de várias maneiras diferentes, incluindo selecioná-la no submenu **barra do Explorer** do menu **Exibir** ou clicar em um botão da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a441e-110">Users can select which option they want to see in several different ways, including selecting it from the **Explorer Bar** submenu of the **View** menu, or clicking a toolbar button.</span></span> <span data-ttu-id="a441e-111">O Internet Explorer fornece várias barras padrão do Explorer, incluindo favoritos e pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a441e-111">Internet Explorer provides several standard Explorer Bars, including Favorites and Search.</span></span>

<span data-ttu-id="a441e-112">Uma das maneiras que você pode personalizar o Internet Explorer é adicionando uma barra personalizada do Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-112">One of the ways you can customize Internet Explorer is by adding a custom Explorer Bar.</span></span> <span data-ttu-id="a441e-113">Quando implementado e registrado, ele será adicionado ao submenu **barra do Explorer** do menu **Exibir** .</span><span class="sxs-lookup"><span data-stu-id="a441e-113">When implemented and registered, it will be added to the **Explorer Bar** submenu of the **View** menu.</span></span> <span data-ttu-id="a441e-114">Quando selecionado pelo usuário, a área de exibição da barra do Explorer pode ser usada para exibir informações e tomar a entrada do usuário praticamente da mesma forma que uma janela normal.</span><span class="sxs-lookup"><span data-stu-id="a441e-114">When selected by the user, the Explorer Bar's display area can then be used to display information and take user input in much the same way as a normal window.</span></span>

![captura de tela das barras do Gerenciador](images/expl2.jpg)

<span data-ttu-id="a441e-116">Para criar uma barra personalizada do Explorer, você deve implementar e registrar um *objeto Band*.</span><span class="sxs-lookup"><span data-stu-id="a441e-116">To create a custom Explorer Bar, you must implement and register a *band object*.</span></span> <span data-ttu-id="a441e-117">Os objetos de banda foram introduzidos com a versão 4,71 do Shell e fornecem recursos semelhantes aos de janelas normais.</span><span class="sxs-lookup"><span data-stu-id="a441e-117">Band objects were introduced with version 4.71 of the Shell and provide capabilities similar to those of normal windows.</span></span> <span data-ttu-id="a441e-118">No entanto, como eles são objetos de Component Object Model (COM) e contidos pelo Internet Explorer ou pelo shell, eles são implementados de maneira um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="a441e-118">However, because they are Component Object Model (COM) objects and contained by either Internet Explorer or the Shell, they are implemented somewhat differently.</span></span> <span data-ttu-id="a441e-119">Objetos de banda simples foram usados para criar as barras do Gerenciador de amostras exibidas no primeiro elemento gráfico.</span><span class="sxs-lookup"><span data-stu-id="a441e-119">Simple band objects were used to create the sample Explorer Bars displayed in the first graphic.</span></span> <span data-ttu-id="a441e-120">A implementação do exemplo de barra vertical do Explorer será discutida detalhadamente em uma seção posterior.</span><span class="sxs-lookup"><span data-stu-id="a441e-120">The implementation of the vertical Explorer Bar sample will be discussed in detail in a later section.</span></span>

## <a name="tool-bands"></a><span data-ttu-id="a441e-121">Faixas de ferramentas</span><span class="sxs-lookup"><span data-stu-id="a441e-121">Tool Bands</span></span>

<span data-ttu-id="a441e-122">Uma *faixa de ferramentas* é um objeto de banda que foi introduzido com o Microsoft Internet Explorer 5 para dar suporte ao recurso de barra de ferramentas de rádio do Windows.</span><span class="sxs-lookup"><span data-stu-id="a441e-122">A *tool band* is a band object that was introduced with Microsoft Internet Explorer 5 to support the Windows radio toolbar feature.</span></span> <span data-ttu-id="a441e-123">A barra de ferramentas do Internet Explorer é, na verdade, um [controle rebar](../controls/rebar-controls.md) que contém vários [controles ToolBar](../controls/toolbar-control-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a441e-123">The Internet Explorer toolbar is actually a [rebar control](../controls/rebar-controls.md) that contains several [toolbar controls](../controls/toolbar-control-reference.md).</span></span> <span data-ttu-id="a441e-124">Ao criar uma faixa de ferramentas, você pode adicionar uma banda a esse controle rebar.</span><span class="sxs-lookup"><span data-stu-id="a441e-124">By creating a tool band, you can add a band to that rebar control.</span></span> <span data-ttu-id="a441e-125">No entanto, como as barras do Explorer, uma faixa de ferramenta é uma janela de uso geral.</span><span class="sxs-lookup"><span data-stu-id="a441e-125">However, like Explorer Bars, a tool band is a general purpose window.</span></span>

![captura de tela de faixas de ferramentas](images/toolband1.jpg)

<span data-ttu-id="a441e-127">Os usuários exibem uma barra de ferramentas selecionando-o no submenu **barras de ferramentas** do menu **Exibir** ou no menu de atalho exibido ao clicar com o botão direito do mouse na área da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a441e-127">Users display a toolbar by selecting it from the **Toolbars** submenu of the **View** menu or from the shortcut menu that is displayed by right-clicking the toolbar area.</span></span>

## <a name="desk-bands"></a><span data-ttu-id="a441e-128">Faixas de escrivaninha</span><span class="sxs-lookup"><span data-stu-id="a441e-128">Desk Bands</span></span>

<span data-ttu-id="a441e-129">Os objetos de banda também podem ser usados para criar *faixas de escrivaninha*.</span><span class="sxs-lookup"><span data-stu-id="a441e-129">Band objects can also be used to create *desk bands*.</span></span> <span data-ttu-id="a441e-130">Embora sua implementação básica seja semelhante às barras do Explorer, as faixas de escrivaninha não estão relacionadas ao Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-130">While their basic implementation is similar to Explorer Bars, desk bands are unrelated to Internet Explorer.</span></span> <span data-ttu-id="a441e-131">Uma banda de mesa é basicamente uma maneira de criar uma janela encaixáveis na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a441e-131">A desk band is basically a way to create a dockable window on the desktop.</span></span> <span data-ttu-id="a441e-132">O usuário seleciona-o clicando com o botão direito do mouse na barra de tarefas e selecionando-o no submenu **barras de ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="a441e-132">The user selects it by right-clicking the taskbar and selecting it from the **Toolbars** submenu.</span></span>

![Captura de tela que mostra uma faixa de exemplo de escrivaninha.](images/desk2.png)

<span data-ttu-id="a441e-134">Inicialmente, as faixas de escrivaninha são encaixadas na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a441e-134">Initially, desk bands are docked on the taskbar.</span></span>

![Captura de tela que mostra as faixas de escrivaninha encaixadas na barra de tarefas.](images/desk1.jpg)

<span data-ttu-id="a441e-136">Em seguida, o usuário pode arrastar a faixa de escrivaninha para a área de trabalho e ela será exibida como uma janela normal.</span><span class="sxs-lookup"><span data-stu-id="a441e-136">The user can then drag the desk band to the desktop, and it will appear as a normal window.</span></span>

![captura de tela de faixas de escrivaninha](images/desk3.png)

## <a name="implementing-band-objects"></a><span data-ttu-id="a441e-138">Implementando objetos de banda</span><span class="sxs-lookup"><span data-stu-id="a441e-138">Implementing Band Objects</span></span>

<span data-ttu-id="a441e-139">Os tópicos a seguir são discutidos.</span><span class="sxs-lookup"><span data-stu-id="a441e-139">The following topics are discussed.</span></span>

-   [<span data-ttu-id="a441e-140">Noções básicas do objeto Band</span><span class="sxs-lookup"><span data-stu-id="a441e-140">Band Object Basics</span></span>](#band-object-basics)
-   [<span data-ttu-id="a441e-141">Registro de banda</span><span class="sxs-lookup"><span data-stu-id="a441e-141">Band Registration</span></span>](#band-registration)
-   [<span data-ttu-id="a441e-142">Um exemplo simples de uma barra personalizada do Explorer</span><span class="sxs-lookup"><span data-stu-id="a441e-142">A Simple Example of a Custom Explorer Bar</span></span>](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a><span data-ttu-id="a441e-143">Noções básicas do objeto Band</span><span class="sxs-lookup"><span data-stu-id="a441e-143">Band Object Basics</span></span>

<span data-ttu-id="a441e-144">Embora eles possam ser usados de forma muito semelhante às janelas normais, os objetos de banda são objetos COM que existem dentro de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="a441e-144">Although they can be used much like normal windows, band objects are COM objects that exist within a container.</span></span> <span data-ttu-id="a441e-145">As barras do Explorer são contidas pelo Internet Explorer, e as faixas de escrivaninha são contidas pelo shell.</span><span class="sxs-lookup"><span data-stu-id="a441e-145">Explorer Bars are contained by Internet Explorer, and desk bands are contained by the Shell.</span></span> <span data-ttu-id="a441e-146">Embora eles atendam a funções diferentes, sua implementação básica é muito semelhante.</span><span class="sxs-lookup"><span data-stu-id="a441e-146">While they serve different functions, their basic implementation is very similar.</span></span> <span data-ttu-id="a441e-147">A principal diferença é em como o objeto Band é registrado, o que, por sua vez, controla o tipo de objeto e seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="a441e-147">The primary difference is in how the band object is registered, which in turn controls the type of object and its container.</span></span> <span data-ttu-id="a441e-148">Esta seção aborda esses aspectos da implementação que são comuns a todos os objetos de banda.</span><span class="sxs-lookup"><span data-stu-id="a441e-148">This section discusses those aspects of implementation that are common to all band objects.</span></span> <span data-ttu-id="a441e-149">Consulte [um exemplo simples de uma barra personalizada do Explorer](#a-simple-example-of-a-custom-explorer-bar) para obter detalhes adicionais de implementação.</span><span class="sxs-lookup"><span data-stu-id="a441e-149">See [A Simple Example of a Custom Explorer Bar](#a-simple-example-of-a-custom-explorer-bar) for additional implementation details.</span></span>

<span data-ttu-id="a441e-150">Além de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), todos os objetos de banda devem implementar as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="a441e-150">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), all band objects must implement the following interfaces.</span></span>

-   [<span data-ttu-id="a441e-151">**IDeskBand**</span><span class="sxs-lookup"><span data-stu-id="a441e-151">**IDeskBand**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [<span data-ttu-id="a441e-152">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="a441e-152">**IObjectWithSite**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [<span data-ttu-id="a441e-153">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="a441e-153">**IPersistStream**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersiststream)

<span data-ttu-id="a441e-154">Além de registrar seu identificador de classe (CLSID), os objetos da barra do Gerenciador e da faixa de escrivaninha também devem ser registrados para a categoria de componente apropriada.</span><span class="sxs-lookup"><span data-stu-id="a441e-154">In addition to registering their class identifier (CLSID), the Explorer Bar and desk band objects must also be registered for the appropriate component category.</span></span> <span data-ttu-id="a441e-155">O registro da categoria de componente determina o tipo de objeto e seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="a441e-155">Registering the component category determines the object type and its container.</span></span> <span data-ttu-id="a441e-156">As bandas de ferramenta usam um procedimento de registro diferente e não têm um identificador de categoria (CATID).</span><span class="sxs-lookup"><span data-stu-id="a441e-156">Tool bands use a different registration procedure and do not have a category identifier (CATID).</span></span> <span data-ttu-id="a441e-157">Os CATIDs para os três objetos de banda que os exigem são:</span><span class="sxs-lookup"><span data-stu-id="a441e-157">The CATIDs for the three band objects that require them are:</span></span>



| <span data-ttu-id="a441e-158">Tipo de banda</span><span class="sxs-lookup"><span data-stu-id="a441e-158">Band Type</span></span>               | <span data-ttu-id="a441e-159">Categoria do componente</span><span class="sxs-lookup"><span data-stu-id="a441e-159">Component Category</span></span> |
|-------------------------|--------------------|
| <span data-ttu-id="a441e-160">Barra vertical do Explorer</span><span class="sxs-lookup"><span data-stu-id="a441e-160">Vertical Explorer Bar</span></span>   | <span data-ttu-id="a441e-161">InfoBand de CATID \_</span><span class="sxs-lookup"><span data-stu-id="a441e-161">CATID\_InfoBand</span></span>    |
| <span data-ttu-id="a441e-162">Barra horizontal do Gerenciador</span><span class="sxs-lookup"><span data-stu-id="a441e-162">Horizontal Explorer Bar</span></span> | <span data-ttu-id="a441e-163">CommBand de CATID \_</span><span class="sxs-lookup"><span data-stu-id="a441e-163">CATID\_CommBand</span></span>    |
| <span data-ttu-id="a441e-164">Faixa de escrivaninha</span><span class="sxs-lookup"><span data-stu-id="a441e-164">Desk Band</span></span>               | <span data-ttu-id="a441e-165">DeskBand de CATID \_</span><span class="sxs-lookup"><span data-stu-id="a441e-165">CATID\_DeskBand</span></span>    |



 

<span data-ttu-id="a441e-166">Consulte [registro de banda](#band-registration) para obter mais informações sobre como registrar objetos de banda.</span><span class="sxs-lookup"><span data-stu-id="a441e-166">See [Band Registration](#band-registration) for further discussion of how to register band objects.</span></span>

<span data-ttu-id="a441e-167">Se o objeto Band for aceitar a entrada do usuário, ele também deverá implementar [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span><span class="sxs-lookup"><span data-stu-id="a441e-167">If the band object is to accept user input, it must also implement [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span></span> <span data-ttu-id="a441e-168">Para adicionar itens ao menu de atalho para as faixas de barra ou escrivaninha do Explorer, o objeto de faixa deve exportar [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="a441e-168">To add items to the shortcut menu for Explorer Bar or desk bands, the band object must export [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="a441e-169">As faixas de ferramentas não dão suporte a menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="a441e-169">Tool bands do not support shortcut menus.</span></span>

<span data-ttu-id="a441e-170">Como os objetos de banda implementam uma janela filho, eles também devem implementar um procedimento de janela para lidar com as mensagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="a441e-170">Because band objects implement a child window, they must also implement a window procedure to handle Windows messaging.</span></span>

<span data-ttu-id="a441e-171">Os objetos de banda podem enviar comandos para seu contêiner por meio da interface [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a441e-171">Band objects can send commands to their container through the container's [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) interface.</span></span> <span data-ttu-id="a441e-172">Para obter o ponteiro de interface, chame o método [**IInputObjectSite:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) do contêiner e solicite \_ IOleCommandTarget de IID.</span><span class="sxs-lookup"><span data-stu-id="a441e-172">To obtain the interface pointer, call the container's [**IInputObjectSite::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method and ask for IID\_IOleCommandTarget.</span></span> <span data-ttu-id="a441e-173">Em seguida, você envia comandos para o contêiner com [**IOleCommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span><span class="sxs-lookup"><span data-stu-id="a441e-173">You then send commands to the container with [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span></span> <span data-ttu-id="a441e-174">O grupo de comandos é CGID \_ DeskBand.</span><span class="sxs-lookup"><span data-stu-id="a441e-174">The command group is CGID\_DeskBand.</span></span> <span data-ttu-id="a441e-175">Quando o método [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) de um objeto Band é chamado, o contêiner usa o parâmetro *dwBandID* para atribuir o objeto Band um identificador que é usado para três dos comandos.</span><span class="sxs-lookup"><span data-stu-id="a441e-175">When a band object's [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) method is called, the container uses the *dwBandID* parameter to assign the band object an identifier that is used for three of the commands.</span></span> <span data-ttu-id="a441e-176">Há suporte para as IDs de comando de quatro **IOleCommandTarget:: exec** .</span><span class="sxs-lookup"><span data-stu-id="a441e-176">Four **IOleCommandTarget::Exec** command IDs are supported.</span></span>

-   <span data-ttu-id="a441e-177">\_BANDINFOCHANGED DBID</span><span class="sxs-lookup"><span data-stu-id="a441e-177">DBID\_BANDINFOCHANGED</span></span>

    <span data-ttu-id="a441e-178">As informações da banda foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="a441e-178">The band's information has changed.</span></span> <span data-ttu-id="a441e-179">Defina o parâmetro *pvaIn* para o identificador de banda que foi recebido na chamada mais recente para [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="a441e-179">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="a441e-180">O contêiner chamará o método **IDeskBand:: GetBandInfo** do objeto Band para solicitar as informações atualizadas.</span><span class="sxs-lookup"><span data-stu-id="a441e-180">The container will call the band object's **IDeskBand::GetBandInfo** method to request the updated information.</span></span>

-   <span data-ttu-id="a441e-181">\_MAXIMIZEBAND DBID</span><span class="sxs-lookup"><span data-stu-id="a441e-181">DBID\_MAXIMIZEBAND</span></span>

    <span data-ttu-id="a441e-182">Maximize a banda.</span><span class="sxs-lookup"><span data-stu-id="a441e-182">Maximize the band.</span></span> <span data-ttu-id="a441e-183">Defina o parâmetro *pvaIn* para o identificador de banda que foi recebido na chamada mais recente para [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="a441e-183">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span>

-   <span data-ttu-id="a441e-184">DBID \_ somente</span><span class="sxs-lookup"><span data-stu-id="a441e-184">DBID\_SHOWONLY</span></span>

    <span data-ttu-id="a441e-185">Ativar ou desativar outras faixas no contêiner.</span><span class="sxs-lookup"><span data-stu-id="a441e-185">Turn other bands in the container on or off.</span></span> <span data-ttu-id="a441e-186">Defina o parâmetro *pvaIn* para o tipo de VT \_ desconhecido com um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a441e-186">Set the *pvaIn* parameter to the VT\_UNKNOWN type with one of the following values:</span></span>

    

    | <span data-ttu-id="a441e-187">Valor</span><span class="sxs-lookup"><span data-stu-id="a441e-187">Value</span></span> | <span data-ttu-id="a441e-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="a441e-188">Description</span></span>                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="a441e-189">pUnk</span><span class="sxs-lookup"><span data-stu-id="a441e-189">pUnk</span></span>  | <span data-ttu-id="a441e-190">Um ponteiro para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do objeto de banda.</span><span class="sxs-lookup"><span data-stu-id="a441e-190">A pointer to the band object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a441e-191">Todas as outras faixas de escrivaninha ficarão ocultas.</span><span class="sxs-lookup"><span data-stu-id="a441e-191">All other desk bands will be hidden.</span></span> |
    | <span data-ttu-id="a441e-192">0</span><span class="sxs-lookup"><span data-stu-id="a441e-192">0</span></span>     | <span data-ttu-id="a441e-193">Ocultar todas as faixas de escrivaninha.</span><span class="sxs-lookup"><span data-stu-id="a441e-193">Hide all desk bands.</span></span>                                                                                        |
    | <span data-ttu-id="a441e-194">1</span><span class="sxs-lookup"><span data-stu-id="a441e-194">1</span></span>     | <span data-ttu-id="a441e-195">Mostrar todas as faixas de escrivaninha.</span><span class="sxs-lookup"><span data-stu-id="a441e-195">Show all desk bands.</span></span>                                                                                        |

    

     

-   <span data-ttu-id="a441e-196">\_PUSHCHEVRON DBID</span><span class="sxs-lookup"><span data-stu-id="a441e-196">DBID\_PUSHCHEVRON</span></span>

    <span data-ttu-id="a441e-197">[Versão 5](versions.md).</span><span class="sxs-lookup"><span data-stu-id="a441e-197">[Version 5](versions.md).</span></span> <span data-ttu-id="a441e-198">Exiba um menu de divisa.</span><span class="sxs-lookup"><span data-stu-id="a441e-198">Display a chevron menu.</span></span> <span data-ttu-id="a441e-199">O contêiner envia uma [**mensagem \_ PUSHCHEVRON RB**](../controls/rb-pushchevron.md) e o objeto Band recebe uma notificação [RBN \_ CHEVRONPUSHED](../controls/rbn-chevronpushed.md) que solicita que ele exiba o menu de divisa.</span><span class="sxs-lookup"><span data-stu-id="a441e-199">The container sends an [**RB\_PUSHCHEVRON**](../controls/rb-pushchevron.md) message, and the band object receives an [RBN\_CHEVRONPUSHED](../controls/rbn-chevronpushed.md) notification that prompts it to display the chevron menu.</span></span> <span data-ttu-id="a441e-200">Defina o parâmetro *nCmdExecOpt* do método [**IOleCommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) como o identificador de banda recebido na chamada mais recente para [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="a441e-200">Set the [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) method's *nCmdExecOpt* parameter to the band identifier received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="a441e-201">Defina o parâmetro *pvaIn* do método **IOleCommandTarget:: exec** como o \_ tipo VT i4 com um valor definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a441e-201">Set the **IOleCommandTarget::Exec** method's *pvaIn* parameter to the VT\_I4 type with an application-defined value.</span></span> <span data-ttu-id="a441e-202">Ele passa de volta para o objeto Band como o valor *lAppValue* da \_ notificação RBN CHEVRONPUSHED.</span><span class="sxs-lookup"><span data-stu-id="a441e-202">It passes back to the band object as the *lAppValue* value of the RBN\_CHEVRONPUSHED notification.</span></span>

### <a name="band-registration"></a><span data-ttu-id="a441e-203">Registro de banda</span><span class="sxs-lookup"><span data-stu-id="a441e-203">Band Registration</span></span>

<span data-ttu-id="a441e-204">Um objeto de banda deve ser registrado como um servidor em processo OLE que dá suporte ao Threading Apartment.</span><span class="sxs-lookup"><span data-stu-id="a441e-204">A band object must be registered as an OLE in-process server that supports apartment threading.</span></span> <span data-ttu-id="a441e-205">O valor padrão para o servidor é uma cadeia de caracteres de texto de menu.</span><span class="sxs-lookup"><span data-stu-id="a441e-205">The default value for the server is a menu text string.</span></span> <span data-ttu-id="a441e-206">Para barras do Explorer, ele aparecerá no submenu **barra do Explorer** do menu **Exibir** do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-206">For Explorer Bars, it will appear in the **Explorer Bar** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="a441e-207">Para as faixas de ferramentas, ela aparecerá no submenu **barras de ferramentas** do menu **Exibir** do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-207">For tool bands, it will appear in the **Toolbars** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="a441e-208">Para faixas de escrivaninha, ela aparecerá no submenu **barras de ferramentas** do menu de atalho da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a441e-208">For desk bands, it will appear in the **Toolbars** submenu of the taskbar's shortcut menu.</span></span> <span data-ttu-id="a441e-209">Assim como os recursos de menu, colocar um e comercial (&) na frente de uma letra fará com que ele seja sublinhado e habilite atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="a441e-209">As with menu resources, placing an ampersand (&) in front of a letter will cause it to be underlined and enable keyboard shortcuts.</span></span> <span data-ttu-id="a441e-210">Por exemplo, a cadeia de menu para a barra vertical do Explorer mostrada no primeiro elemento gráfico é "exemplo &barra vertical do Explorer".</span><span class="sxs-lookup"><span data-stu-id="a441e-210">For example, the menu string for the vertical Explorer Bar shown in the first graphic is "Sample &Vertical Explorer Bar".</span></span>

<span data-ttu-id="a441e-211">Inicialmente, o Internet Explorer recupera uma enumeração dos objetos de barra do Gerenciador registrados do registro usando as categorias de componente.</span><span class="sxs-lookup"><span data-stu-id="a441e-211">Initially, Internet Explorer retrieves an enumeration of the registered Explorer Bar objects from the registry using the component categories.</span></span> <span data-ttu-id="a441e-212">Para aumentar o desempenho, ele armazena em cache essa enumeração, fazendo com que as barras do Explorer adicionadas subsequentemente sejam ignoradas.</span><span class="sxs-lookup"><span data-stu-id="a441e-212">To increase performance, it then caches this enumeration, causing subsequently added Explorer Bars to be overlooked.</span></span> <span data-ttu-id="a441e-213">Para forçar o Windows Internet Explorer a recriar o cache e reconhecer uma nova barra do Explorer, exclua as seguintes chaves do registro durante o registro da nova barra do Explorer:</span><span class="sxs-lookup"><span data-stu-id="a441e-213">To force Windows Internet Explorer to rebuild the cache and recognize a new Explorer Bar, delete the following registry keys during the registration of the new Explorer Bar:</span></span>

<span data-ttu-id="a441e-214">**HKEY \_ Software do \_ usuário atual** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Descartado** \\ , categorias de componente de **instalação** do \\  \\ **C000 {00021493-0000-0000-000000000046}** \\ **enum**</span><span class="sxs-lookup"><span data-stu-id="a441e-214">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021493-0000-0000-C000-000000000046}**\\**Enum**</span></span>

<span data-ttu-id="a441e-215">**HKEY \_ Software do \_ usuário atual** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Descartado** \\ , categorias de componente de **instalação** do \\  \\ **C000 {00021494-0000-0000-000000000046}** \\ **enum**</span><span class="sxs-lookup"><span data-stu-id="a441e-215">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021494-0000-0000-C000-000000000046}**\\**Enum**</span></span>

> [!Note]  
> <span data-ttu-id="a441e-216">Como um cache da barra do Explorer é criado para cada usuário, o aplicativo de instalação pode precisar enumerar todos os hives do registro do usuário ou adicionar um stub por usuário para ser executado quando o usuário fizer logon pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="a441e-216">Because an Explorer Bar cache is created for each user, your setup application may need to enumerate all the user registry hives or add a per-user stub to run when the user first logs on.</span></span>

 

<span data-ttu-id="a441e-217">Em geral, a entrada de registro básica para um objeto de banda será exibida da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="a441e-217">In general, the basic registry entry for a band object will appear as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

<span data-ttu-id="a441e-218">As faixas de ferramentas também devem ter o CLSID do seu objeto registrado no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-218">Tool bands must also have their object's CLSID registered with Internet Explorer.</span></span> <span data-ttu-id="a441e-219">Para fazer isso, atribua um valor em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **barra de ferramentas** chamado com o GUID CLSID do objeto de faixa de ferramenta, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="a441e-219">To do this, assign a value under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Internet Explorer**\\**Toolbar** named with the tool band object's CLSID GUID as shown here.</span></span> <span data-ttu-id="a441e-220">Seu valor de dados é ignorado, portanto, o tipo de valor não é importante.</span><span class="sxs-lookup"><span data-stu-id="a441e-220">Its data value is ignored, so the value type is unimportant.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

<span data-ttu-id="a441e-221">Há vários valores opcionais que também podem ser adicionados ao registro.</span><span class="sxs-lookup"><span data-stu-id="a441e-221">There are several optional values that can also be added to the registry.</span></span> <span data-ttu-id="a441e-222">Por exemplo, o valor a seguir será necessário se você quiser usar a barra do Explorer para exibir HTML o valor mostrado não é um exemplo, mas o valor real que deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="a441e-222">For instance, the following value is necessary if you want to use the Explorer Bar to display HTML The value shown is not an example, but the actual value that should be used.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

<span data-ttu-id="a441e-223">Usado em conjunto com o valor mostrado acima, o valor opcional a seguir também será necessário se você quiser usar a barra do Explorer para exibir HTML.</span><span class="sxs-lookup"><span data-stu-id="a441e-223">Used in conjunction with the value shown above, the following optional value is also necessary if you want to use the Explorer Bar to display HTML.</span></span> <span data-ttu-id="a441e-224">Esse valor deve ser definido como o local do arquivo que contém o conteúdo HTML da barra do Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-224">This value should be set to the location of the file that contains the HTML content for the Explorer Bar.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

<span data-ttu-id="a441e-225">Outro valor opcional define a largura ou a altura padrão da barra do Explorer, dependendo se ela é vertical ou horizontal, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a441e-225">Another optional value defines the default width or height of the Explorer Bar, depending on whether it is vertical or horizontal, respectively.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

<span data-ttu-id="a441e-226">O valor de barras deve ser definido como a largura ou altura da barra.</span><span class="sxs-lookup"><span data-stu-id="a441e-226">The BarSize value should be set to the width or height of the bar.</span></span> <span data-ttu-id="a441e-227">O valor requer oito bytes e é colocado no registro como um valor binário.</span><span class="sxs-lookup"><span data-stu-id="a441e-227">The value requires eight bytes and is placed in the registry as a binary value.</span></span> <span data-ttu-id="a441e-228">Os primeiros quatro bytes especificam o tamanho em pixels, em formato hexadecimal, a partir do byte mais à esquerda.</span><span class="sxs-lookup"><span data-stu-id="a441e-228">The first four bytes specify the size in pixels, in hexadecimal format, starting from the leftmost byte.</span></span> <span data-ttu-id="a441e-229">Os últimos quatro bytes são reservados e devem ser definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="a441e-229">The last four bytes are reserved and should be set to zero.</span></span>

<span data-ttu-id="a441e-230">Por exemplo, as entradas de registro completas para uma barra do Explorer com capacidade para HTML com uma largura padrão de pixels de 291 (0x123) são mostradas aqui.</span><span class="sxs-lookup"><span data-stu-id="a441e-230">As an example, the full registry entries for an HTML-capable Explorer Bar with a default width of 291 (0x123) pixels are shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

<span data-ttu-id="a441e-231">Você pode manipular o registro do CATID de um objeto de banda programaticamente.</span><span class="sxs-lookup"><span data-stu-id="a441e-231">You can handle registration of a band object's CATID programmatically.</span></span> <span data-ttu-id="a441e-232">Crie um objeto do Gerenciador de categorias de componente (CLSID \_ StdComponentCategoriesMgr) e solicite um ponteiro para sua interface [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) .</span><span class="sxs-lookup"><span data-stu-id="a441e-232">Create a component categories manager object (CLSID\_StdComponentCategoriesMgr) and request a pointer to its [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) interface.</span></span> <span data-ttu-id="a441e-233">Passe o CLSID e o CATID do objeto de banda para [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span><span class="sxs-lookup"><span data-stu-id="a441e-233">Pass the band object's CLSID and CATID to [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span></span>

### <a name="a-simple-example-of-a-custom-explorer-bar"></a><span data-ttu-id="a441e-234">Um exemplo simples de uma barra personalizada do Explorer</span><span class="sxs-lookup"><span data-stu-id="a441e-234">A Simple Example of a Custom Explorer Bar</span></span>

<span data-ttu-id="a441e-235">Este exemplo percorre a implementação da barra vertical do Explorer de exemplo mostrada na introdução.</span><span class="sxs-lookup"><span data-stu-id="a441e-235">This example goes through the implementation of the sample vertical Explorer Bar shown in the introduction.</span></span>

<span data-ttu-id="a441e-236">O procedimento básico para criar uma barra personalizada do Explorer é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="a441e-236">The basic procedure for creating a custom Explorer Bar is as follows.</span></span>

1.  <span data-ttu-id="a441e-237">[Implemente as funções necessárias para a dll](#dll-functions).</span><span class="sxs-lookup"><span data-stu-id="a441e-237">[Implement the functions needed by the DLL](#dll-functions).</span></span>
2.  [<span data-ttu-id="a441e-238">Implemente as interfaces COM necessárias.</span><span class="sxs-lookup"><span data-stu-id="a441e-238">Implement the required COM interfaces.</span></span>](#required-interface-implementations)
3.  [<span data-ttu-id="a441e-239">Implemente as interfaces COM opcionais desejadas.</span><span class="sxs-lookup"><span data-stu-id="a441e-239">Implement any desired optional COM interfaces.</span></span>](#optional-interface-implementations)
4.  [<span data-ttu-id="a441e-240">Registre o CLSID do objeto e, se necessário, a categoria do componente.</span><span class="sxs-lookup"><span data-stu-id="a441e-240">Register the object's CLSID and, if required, component category.</span></span>](#clsid-registration)
5.  <span data-ttu-id="a441e-241">Crie uma janela filho do Internet Explorer, dimensionada para caber na região de exibição da barra do Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-241">Create a child window of Internet Explorer, sized to fit the Explorer Bar's display region.</span></span>
6.  [<span data-ttu-id="a441e-242">Use a janela filho para exibir informações e interagir com o usuário.</span><span class="sxs-lookup"><span data-stu-id="a441e-242">Use the child window to display information and interact with the user.</span></span>](#the-window-procedure)

<span data-ttu-id="a441e-243">A implementação muito simples usada na amostra da barra do Gerenciador poderia ser realmente usada para qualquer tipo de barra do Explorer ou uma faixa de escrivaninha, simplesmente registrando-a para a categoria de componente apropriada.</span><span class="sxs-lookup"><span data-stu-id="a441e-243">The very simple implementation used in the Explorer Bar sample could actually be used for either type of Explorer Bar, or a desk band, by simply registering it for the appropriate component category.</span></span> <span data-ttu-id="a441e-244">Implementações mais sofisticadas precisarão ser personalizadas para a região de exibição e o contêiner de cada tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="a441e-244">More sophisticated implementations will need to be customized for each object type's display region and container.</span></span> <span data-ttu-id="a441e-245">No entanto, grande parte dessa personalização pode ser realizada com o código de exemplo e sua extensão, aplicando técnicas familiares de programação do Windows à janela filho.</span><span class="sxs-lookup"><span data-stu-id="a441e-245">However, much of this customization can be accomplished by taking the sample code and extending it by applying familiar Windows programming techniques to the child window.</span></span> <span data-ttu-id="a441e-246">Por exemplo, você pode adicionar controles para interação do usuário ou gráficos para uma exibição mais rica.</span><span class="sxs-lookup"><span data-stu-id="a441e-246">For example, you can add controls for user interaction, or graphics for a richer display.</span></span>

### <a name="dll-functions"></a><span data-ttu-id="a441e-247">Funções de DLL</span><span class="sxs-lookup"><span data-stu-id="a441e-247">DLL Functions</span></span>

<span data-ttu-id="a441e-248">Todos os três objetos são empacotados em uma única DLL, que expõe as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="a441e-248">All three objects are packaged in a single DLL, which exposes the following functions.</span></span>

-   [<span data-ttu-id="a441e-249">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="a441e-249">**DllMain**</span></span>](../dlls/dllmain.md)
-   [<span data-ttu-id="a441e-250">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="a441e-250">**DllCanUnloadNow**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [<span data-ttu-id="a441e-251">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="a441e-251">**DllGetClassObject**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [<span data-ttu-id="a441e-252">**DllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="a441e-252">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

<span data-ttu-id="a441e-253">As três primeiras funções são implementações padrão e não serão discutidas aqui.</span><span class="sxs-lookup"><span data-stu-id="a441e-253">The first three functions are standard implementations and will not be discussed here.</span></span> <span data-ttu-id="a441e-254">A implementação da fábrica de classes também é padrão.</span><span class="sxs-lookup"><span data-stu-id="a441e-254">The Class Factory implementation is also standard.</span></span>

### <a name="required-interface-implementations"></a><span data-ttu-id="a441e-255">Implementações de interface necessárias</span><span class="sxs-lookup"><span data-stu-id="a441e-255">Required Interface Implementations</span></span>

<span data-ttu-id="a441e-256">O exemplo de barra vertical do Explorer implementa as quatro interfaces necessárias: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)e [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) como parte da classe CExplorerBar.</span><span class="sxs-lookup"><span data-stu-id="a441e-256">The vertical Explorer Bar sample implements the four required interfaces: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream), and [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) as part of the CExplorerBar class.</span></span> <span data-ttu-id="a441e-257">As implementações do Construtor, destruidor e **IUnknown** são simples e não serão discutidas aqui.</span><span class="sxs-lookup"><span data-stu-id="a441e-257">The constructor, destructor, and **IUnknown** implementations are straightforward, and will not be discussed here.</span></span> <span data-ttu-id="a441e-258">Consulte o código de exemplo para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="a441e-258">See the sample code for details.</span></span>

<span data-ttu-id="a441e-259">As interfaces a seguir são discutidas em detalhes.</span><span class="sxs-lookup"><span data-stu-id="a441e-259">The following interfaces are discussed in detail.</span></span>

-   [<span data-ttu-id="a441e-260">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="a441e-260">IObjectWithSite</span></span>](#iobjectwithsite)
-   [<span data-ttu-id="a441e-261">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="a441e-261">IPersistStream</span></span>](#ipersiststream)
-   [<span data-ttu-id="a441e-262">IDeskBand</span><span class="sxs-lookup"><span data-stu-id="a441e-262">IDeskBand</span></span>](#ideskband)

### <a name="iobjectwithsite"></a><span data-ttu-id="a441e-263">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="a441e-263">IObjectWithSite</span></span>

<span data-ttu-id="a441e-264">Quando o usuário seleciona uma barra do Explorer, o contêiner chama o método [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) do objeto de banda correspondente.</span><span class="sxs-lookup"><span data-stu-id="a441e-264">When the user selects an Explorer Bar, the container calls the corresponding band object's [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) method.</span></span> <span data-ttu-id="a441e-265">O parâmetro *punkSite* será definido como o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do site.</span><span class="sxs-lookup"><span data-stu-id="a441e-265">The *punkSite* parameter will be set to the site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="a441e-266">Em geral, uma implementação de [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) deve executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="a441e-266">In general, a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) implementation should perform the following steps:</span></span>

1.  <span data-ttu-id="a441e-267">Libere qualquer ponteiro de site que esteja sendo mantido no momento.</span><span class="sxs-lookup"><span data-stu-id="a441e-267">Release any site pointer that is currently being held.</span></span>
2.  <span data-ttu-id="a441e-268">Se o ponteiro passado para [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) for definido como **NULL**, a banda será removida.</span><span class="sxs-lookup"><span data-stu-id="a441e-268">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is set to **NULL**, the band is being removed.</span></span> <span data-ttu-id="a441e-269">**SetSite** pode retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a441e-269">**SetSite** can return S\_OK.</span></span>
3.  <span data-ttu-id="a441e-270">Se o ponteiro passado para [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) for não **nulo**, um novo site será definido.</span><span class="sxs-lookup"><span data-stu-id="a441e-270">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is non-**NULL**, a new site is being set.</span></span> <span data-ttu-id="a441e-271">**SetSite** deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a441e-271">**SetSite** should do the following:</span></span>
    1.  <span data-ttu-id="a441e-272">Chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no site para sua interface [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) .</span><span class="sxs-lookup"><span data-stu-id="a441e-272">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) interface.</span></span>
    2.  <span data-ttu-id="a441e-273">Chame [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) para obter o identificador da janela pai.</span><span class="sxs-lookup"><span data-stu-id="a441e-273">Call [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) to obtain the parent window's handle.</span></span> <span data-ttu-id="a441e-274">Salve o identificador para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="a441e-274">Save the handle for later use.</span></span> <span data-ttu-id="a441e-275">Libere [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) se não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="a441e-275">Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) if it is no longer needed.</span></span>
    3.  <span data-ttu-id="a441e-276">Crie a janela do objeto de banda como um filho da janela obtida na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="a441e-276">Create the band object's window as a child of the window obtained in the previous step.</span></span> <span data-ttu-id="a441e-277">Não a crie como uma janela visível.</span><span class="sxs-lookup"><span data-stu-id="a441e-277">Do not create it as a visible window.</span></span>
    4.  <span data-ttu-id="a441e-278">Se o objeto Band implementar [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no site para sua interface [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) .</span><span class="sxs-lookup"><span data-stu-id="a441e-278">If the band object implements [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) interface.</span></span> <span data-ttu-id="a441e-279">Armazene o ponteiro para esta interface para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="a441e-279">Store the pointer to this interface for use later.</span></span>
    5.  <span data-ttu-id="a441e-280">Se todas as etapas forem bem-sucedidas, retorne as S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a441e-280">If all steps are successful, return S\_OK.</span></span> <span data-ttu-id="a441e-281">Caso contrário, retorne o código de erro definido por OLE indicando o que falhou.</span><span class="sxs-lookup"><span data-stu-id="a441e-281">If not, return the OLE-defined error code indicating what failed.</span></span>

<span data-ttu-id="a441e-282">O exemplo da barra do Explorer implementa [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="a441e-282">The Explorer Bar sample implements [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) in the following way.</span></span> <span data-ttu-id="a441e-283">No código m a seguir, *\_ pSite* é uma variável de membro particular que contém o ponteiro [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) e *m \_ hwndParent* mantém a alça da janela pai.</span><span class="sxs-lookup"><span data-stu-id="a441e-283">In the following code *m\_pSite* is a private member variable that holds the [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) pointer and *m\_hwndParent* holds the parent window's handle.</span></span> <span data-ttu-id="a441e-284">Neste exemplo, a criação de janela também é tratada.</span><span class="sxs-lookup"><span data-stu-id="a441e-284">In this sample, window creation is also handled.</span></span> <span data-ttu-id="a441e-285">Se a janela não existir, esse método criará a janela da barra do Explorer como um filho de tamanho adequado da janela pai obtida por **SetSite**.</span><span class="sxs-lookup"><span data-stu-id="a441e-285">If the window does not exist, this method creates the Explorer Bar's window as an appropriately sized child of the parent window obtained by **SetSite**.</span></span> <span data-ttu-id="a441e-286">O identificador da janela filho é armazenado na *\_ HWND do m*.</span><span class="sxs-lookup"><span data-stu-id="a441e-286">The child window's handle is stored in *m\_hwnd*.</span></span>


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



<span data-ttu-id="a441e-287">A implementação do [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) de exemplo simplesmente encapsula uma chamada para o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) do site, usando o ponteiro do site salvo por [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span><span class="sxs-lookup"><span data-stu-id="a441e-287">The sample's [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) implementation simply wraps a call to the site's [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, using the site pointer saved by [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span></span>


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a><span data-ttu-id="a441e-288">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="a441e-288">IPersistStream</span></span>

<span data-ttu-id="a441e-289">O Internet Explorer chamará a interface [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) da barra do Explorer para permitir que a barra do Explorer carregue ou salve dados persistentes.</span><span class="sxs-lookup"><span data-stu-id="a441e-289">Internet Explorer will call the Explorer Bar's [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to allow the Explorer Bar to load or save persistent data.</span></span> <span data-ttu-id="a441e-290">Se não houver dados persistentes, os métodos ainda devem retornar um código de êxito.</span><span class="sxs-lookup"><span data-stu-id="a441e-290">If there is no persistent data, the methods must still return a success code.</span></span> <span data-ttu-id="a441e-291">A interface **IPersistStream** herda de [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), portanto, cinco métodos devem ser implementados.</span><span class="sxs-lookup"><span data-stu-id="a441e-291">The **IPersistStream** interface inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), so five methods must be implemented.</span></span>

-   [<span data-ttu-id="a441e-292">**IPersist:: GetClassID**</span><span class="sxs-lookup"><span data-stu-id="a441e-292">**IPersist::GetClassID**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [<span data-ttu-id="a441e-293">**IPersistStream:: IsDirty**</span><span class="sxs-lookup"><span data-stu-id="a441e-293">**IPersistStream::IsDirty**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [<span data-ttu-id="a441e-294">**IPersistStream:: Load**</span><span class="sxs-lookup"><span data-stu-id="a441e-294">**IPersistStream::Load**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [<span data-ttu-id="a441e-295">**IPersistStream:: Save**</span><span class="sxs-lookup"><span data-stu-id="a441e-295">**IPersistStream::Save**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [<span data-ttu-id="a441e-296">**IPersistStream:: GetSizeMax**</span><span class="sxs-lookup"><span data-stu-id="a441e-296">**IPersistStream::GetSizeMax**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

<span data-ttu-id="a441e-297">A amostra da barra do Gerenciador não usa nenhum dado persistente e tem apenas uma implementação mínima de [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="a441e-297">The Explorer Bar sample does not use any persistent data and has only a minimal implementation of [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="a441e-298">[**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) retorna o CLSID do objeto (CLSID \_ SampleExplorerBar) e o resto retorna S \_ OK, s \_ false ou E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a441e-298">[**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) returns the object's CLSID (CLSID\_SampleExplorerBar), and the remainder return either S\_OK, S\_FALSE, or E\_NOTIMPL.</span></span>

### <a name="ideskband"></a><span data-ttu-id="a441e-299">IDeskBand</span><span class="sxs-lookup"><span data-stu-id="a441e-299">IDeskBand</span></span>

<span data-ttu-id="a441e-300">A interface [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) é específica para objetos de banda.</span><span class="sxs-lookup"><span data-stu-id="a441e-300">The [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) interface is specific to band objects.</span></span> <span data-ttu-id="a441e-301">Além de seu único método, ele herda de [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), que por sua vez herda de [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span><span class="sxs-lookup"><span data-stu-id="a441e-301">In addition to its one method, it inherits from [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), which in turn inherits from [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span></span>

<span data-ttu-id="a441e-302">Há dois métodos [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) : [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) e [**IOleWindow:: ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span><span class="sxs-lookup"><span data-stu-id="a441e-302">There are two [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) methods: [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) and [**IOleWindow::ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span></span> <span data-ttu-id="a441e-303">A implementação de exemplo da barra do Explorer de **GetWindow** retorna o identificador da janela filho da barra do Explorer, *m \_ hWnd*.</span><span class="sxs-lookup"><span data-stu-id="a441e-303">The Explorer Bar sample's implementation of **GetWindow** returns the Explorer Bar's child window handle, *m\_hwnd*.</span></span> <span data-ttu-id="a441e-304">A ajuda contextual não está implementada, portanto **ContextSensitiveHelp** retorna **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="a441e-304">Context-sensitive Help is not implemented, so **ContextSensitiveHelp** returns **E\_NOTIMPL**.</span></span>

<span data-ttu-id="a441e-305">A interface [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) tem três métodos.</span><span class="sxs-lookup"><span data-stu-id="a441e-305">The [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface has three methods.</span></span>

-   [<span data-ttu-id="a441e-306">**IDockingWindow::ShowDW**</span><span class="sxs-lookup"><span data-stu-id="a441e-306">**IDockingWindow::ShowDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [<span data-ttu-id="a441e-307">**IDockingWindow::CloseDW**</span><span class="sxs-lookup"><span data-stu-id="a441e-307">**IDockingWindow::CloseDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [<span data-ttu-id="a441e-308">**IDockingWindow::ResizeBorderDW**</span><span class="sxs-lookup"><span data-stu-id="a441e-308">**IDockingWindow::ResizeBorderDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

<span data-ttu-id="a441e-309">O método [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) não é usado com nenhum tipo de objeto Band e sempre deve retornar e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a441e-309">The [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) method is not used with any type of band object and should always return E\_NOTIMPL.</span></span> <span data-ttu-id="a441e-310">O método [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) mostra ou oculta a janela da barra do Explorer, dependendo do valor de seu parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a441e-310">The [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) method either shows or hides the Explorer Bar's window, depending on the value of its parameter.</span></span>


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



<span data-ttu-id="a441e-311">O método [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) destrói a janela da barra do Gerenciador.</span><span class="sxs-lookup"><span data-stu-id="a441e-311">The [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) method destroys the Explorer Bar's window.</span></span>


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



<span data-ttu-id="a441e-312">O método restante, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), é específico para **IDeskBand**.</span><span class="sxs-lookup"><span data-stu-id="a441e-312">The remaining method, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), is specific to **IDeskBand**.</span></span> <span data-ttu-id="a441e-313">O Internet Explorer usa-o para especificar o identificador e o modo de exibição da barra do Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-313">Internet Explorer uses it to specify the Explorer Bar's identifier and viewing mode.</span></span> <span data-ttu-id="a441e-314">O Internet Explorer também pode solicitar uma ou mais partes de informações da barra do Explorer preenchendo o membro **dwMask** da estrutura [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) que é passada como o terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a441e-314">Internet Explorer also may request one or more pieces of information from the Explorer Bar by filling the **dwMask** member of the [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) structure that is passed as the third parameter.</span></span> <span data-ttu-id="a441e-315">**GetBandInfo** deve armazenar o identificador e o modo de exibição e preencher a estrutura **DESKBANDINFO** com os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="a441e-315">**GetBandInfo** should store the identifier and viewing mode and fill the **DESKBANDINFO** structure with the requested data.</span></span> <span data-ttu-id="a441e-316">O exemplo da barra do Explorer implementa **GetBandInfo** conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a441e-316">The Explorer Bar sample implements **GetBandInfo** as shown in the following code example.</span></span>


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a><span data-ttu-id="a441e-317">Implementações de interface opcional</span><span class="sxs-lookup"><span data-stu-id="a441e-317">Optional Interface Implementations</span></span>

<span data-ttu-id="a441e-318">Há duas interfaces que não são necessárias, mas que podem ser úteis para implementar: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) e [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="a441e-318">There are two interfaces that are not required, but that may be useful to implement: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) and [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="a441e-319">O exemplo da barra do Gerenciador implementa **IInputObject**.</span><span class="sxs-lookup"><span data-stu-id="a441e-319">The Explorer Bar sample implements **IInputObject**.</span></span> <span data-ttu-id="a441e-320">Consulte a documentação para obter informações sobre como implementar o **IContextMenu**.</span><span class="sxs-lookup"><span data-stu-id="a441e-320">Refer to the documentation for information on how to implement **IContextMenu**.</span></span>

### <a name="iinputobject"></a><span data-ttu-id="a441e-321">IInputObject</span><span class="sxs-lookup"><span data-stu-id="a441e-321">IInputObject</span></span>

<span data-ttu-id="a441e-322">A interface [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) deve ser implementada se um objeto Band aceitar entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="a441e-322">The [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) interface must be implemented if a band object accepts user input.</span></span> <span data-ttu-id="a441e-323">O Internet Explorer implementa [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) e usa o **IInputObject** para manter o foco de entrada do usuário adequado quando ele tem mais de uma janela contida.</span><span class="sxs-lookup"><span data-stu-id="a441e-323">Internet Explorer implements [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) and uses **IInputObject** to maintain proper user input focus when it has more than one contained window.</span></span> <span data-ttu-id="a441e-324">Há três métodos que precisam ser implementados por uma barra do Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-324">There are three methods that need to be implemented by an Explorer Bar.</span></span>

-   [<span data-ttu-id="a441e-325">**IInputObject::UIActivateIO**</span><span class="sxs-lookup"><span data-stu-id="a441e-325">**IInputObject::UIActivateIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [<span data-ttu-id="a441e-326">**IInputObject::HasFocusIO**</span><span class="sxs-lookup"><span data-stu-id="a441e-326">**IInputObject::HasFocusIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [<span data-ttu-id="a441e-327">**IInputObject::TranslateAcceleratorIO**</span><span class="sxs-lookup"><span data-stu-id="a441e-327">**IInputObject::TranslateAcceleratorIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

<span data-ttu-id="a441e-328">O Internet Explorer chama [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) para informar à barra do Explorer que está sendo ativada ou desativada.</span><span class="sxs-lookup"><span data-stu-id="a441e-328">Internet Explorer calls [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) to inform the Explorer Bar that it is being activated or deactivated.</span></span> <span data-ttu-id="a441e-329">Quando ativado, o exemplo da barra do Explorer chama [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) para definir o foco para sua janela.</span><span class="sxs-lookup"><span data-stu-id="a441e-329">When activated, the Explorer Bar sample calls [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) to set the focus to its window.</span></span>

<span data-ttu-id="a441e-330">O Internet Explorer chama [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) quando está tentando determinar qual janela tem o foco.</span><span class="sxs-lookup"><span data-stu-id="a441e-330">Internet Explorer calls [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) when it is attempting to determine which window has focus.</span></span> <span data-ttu-id="a441e-331">Se a janela da barra do Explorer ou um de seus descendentes tiver foco, **HasFocusIO** deverá retornar s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a441e-331">If the Explorer Bar's window or one of its descendants has focus, **HasFocusIO** should return S\_OK.</span></span> <span data-ttu-id="a441e-332">Caso contrário, ele deve retornar S \_ false.</span><span class="sxs-lookup"><span data-stu-id="a441e-332">If not, it should return S\_FALSE.</span></span>

<span data-ttu-id="a441e-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) permite que o objeto processe aceleradores de teclado.</span><span class="sxs-lookup"><span data-stu-id="a441e-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) allows the object to process keyboard accelerators.</span></span> <span data-ttu-id="a441e-334">A amostra da barra do Gerenciador não implementa esse método, portanto, retorna S \_ false.</span><span class="sxs-lookup"><span data-stu-id="a441e-334">The Explorer Bar sample does not implement this method, so it returns S\_FALSE.</span></span>

<span data-ttu-id="a441e-335">A implementação da barra de exemplo do [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="a441e-335">The sample bar's implementation of [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) is as follows.</span></span>


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a><span data-ttu-id="a441e-336">Registro de CLSID</span><span class="sxs-lookup"><span data-stu-id="a441e-336">CLSID Registration</span></span>

<span data-ttu-id="a441e-337">Assim como acontece com todos os objetos COM, o CLSID da barra do Explorer deve ser registrado.</span><span class="sxs-lookup"><span data-stu-id="a441e-337">As with all COM objects, the Explorer Bar's CLSID must be registered.</span></span> <span data-ttu-id="a441e-338">Para que o objeto funcione corretamente com o Internet Explorer, ele também deve ser registrado para a categoria de componente apropriada (CATID \_ InfoBand).</span><span class="sxs-lookup"><span data-stu-id="a441e-338">For the object to function properly with Internet Explorer, it must also be registered for the appropriate component category (CATID\_InfoBand).</span></span> <span data-ttu-id="a441e-339">A seção de código relevante para a barra do Gerenciador é mostrada no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a441e-339">The relevant code section for the Explorer Bar is shown in the following code example.</span></span>


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="a441e-340">O registro de objetos de banda no exemplo usa procedimentos COM normais.</span><span class="sxs-lookup"><span data-stu-id="a441e-340">Registration of band objects in the sample uses normal COM procedures.</span></span>

<span data-ttu-id="a441e-341">Além do CLSID, o servidor de objeto de banda também deve ser registrado para uma ou mais categorias de componente.</span><span class="sxs-lookup"><span data-stu-id="a441e-341">In addition to the CLSID, the band object server must also be registered for one or more component categories.</span></span> <span data-ttu-id="a441e-342">Essa é, na verdade, a principal diferença na implementação entre as amostras de barra vertical e horizontal do Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-342">This is actually the main difference in implementation between the vertical and horizontal Explorer Bar samples.</span></span> <span data-ttu-id="a441e-343">Esse processo é tratado pela criação de um objeto do Gerenciador de categorias de componente (CLSID \_ StdComponentCategoriesMgr) e usando o método [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) para registrar o servidor de objeto de banda.</span><span class="sxs-lookup"><span data-stu-id="a441e-343">This process is handled by creating a component categories manager object (CLSID\_StdComponentCategoriesMgr) and using the [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) method to register the band object server.</span></span> <span data-ttu-id="a441e-344">Neste exemplo, o registro de categoria de componente é manipulado passando o CLSID de exemplo da barra do Explorer e o CATID para uma função particular —**RegisterComCat**— conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a441e-344">In this example, component category registration is handled by passing the Explorer Bar sample's CLSID and CATID to a private function—**RegisterComCat**—as shown in the following code example.</span></span>


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a><span data-ttu-id="a441e-345">O procedimento de janela</span><span class="sxs-lookup"><span data-stu-id="a441e-345">The Window Procedure</span></span>

<span data-ttu-id="a441e-346">Como um objeto Band usa uma janela filho para sua exibição, ele deve implementar um procedimento de janela para manipular mensagens do Windows.</span><span class="sxs-lookup"><span data-stu-id="a441e-346">Because a band object uses a child window for its display, it must implement a window procedure to handle Windows messaging.</span></span> <span data-ttu-id="a441e-347">O exemplo de banda tem funcionalidade mínima, portanto, seu procedimento de janela manipula apenas cinco mensagens:</span><span class="sxs-lookup"><span data-stu-id="a441e-347">The band sample has minimal functionality, so its window procedure only handles five messages:</span></span>

-   [<span data-ttu-id="a441e-348">**NCCREATE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a441e-348">**WM\_NCCREATE**</span></span>](../winmsg/wm-nccreate.md)
-   [<span data-ttu-id="a441e-349">**pintura do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a441e-349">**WM\_PAINT**</span></span>](../gdi/wm-paint.md)
-   [<span data-ttu-id="a441e-350">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a441e-350">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)
-   [<span data-ttu-id="a441e-351">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="a441e-351">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)
-   [<span data-ttu-id="a441e-352">**KILLFOCUS do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a441e-352">**WM\_KILLFOCUS**</span></span>](../inputdev/wm-killfocus.md)

<span data-ttu-id="a441e-353">O procedimento pode ser facilmente expandido para acomodar mensagens adicionais para dar suporte a mais recursos.</span><span class="sxs-lookup"><span data-stu-id="a441e-353">The procedure can easily be expanded to accommodate additional messages to support more features.</span></span>


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



<span data-ttu-id="a441e-354">O manipulador de comandos do WM \_ simplesmente retorna zero.</span><span class="sxs-lookup"><span data-stu-id="a441e-354">The WM\_COMMAND handler simply returns zero.</span></span> <span data-ttu-id="a441e-355">O manipulador de pintura do WM \_ cria a exibição de texto simples mostrada no exemplo da barra do Explorer na introdução.</span><span class="sxs-lookup"><span data-stu-id="a441e-355">The WM\_PAINT handler creates the simple text display shown in the Explorer Bar example in the introduction.</span></span>


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="a441e-356">Os \_ manipuladores do WM SETFOCUS e do WM KILLFOCUS informam \_ o site de uma alteração de foco chamando o método [**IInputObjectSite:: OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) do site.</span><span class="sxs-lookup"><span data-stu-id="a441e-356">The WM\_SETFOCUS and WM\_KILLFOCUS handlers inform the site of a focus change by calling the site's [**IInputObjectSite::OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) method.</span></span>


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



<span data-ttu-id="a441e-357">Os objetos de banda fornecem uma maneira flexível e eficiente de estender os recursos do Internet Explorer Criando barras personalizadas do Explorer.</span><span class="sxs-lookup"><span data-stu-id="a441e-357">Band objects provide a flexible and powerful way to extend the capabilities of Internet Explorer by creating custom Explorer Bars.</span></span> <span data-ttu-id="a441e-358">A implementação de uma banda de mesa permite que você estenda os recursos das janelas normais.</span><span class="sxs-lookup"><span data-stu-id="a441e-358">Implementing a desk band enables you to extend the capabilities of normal windows.</span></span> <span data-ttu-id="a441e-359">Embora alguma programação COM seja necessária, ela finalmente serve para fornecer uma janela filho para a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="a441e-359">Although some COM programming is required, it ultimately serves to provide a child window for your user interface.</span></span> <span data-ttu-id="a441e-360">A partir daí, a maior parte da implementação pode usar técnicas de programação familiares do Windows.</span><span class="sxs-lookup"><span data-stu-id="a441e-360">From there, the bulk of the implementation can use familiar Windows programming techniques.</span></span> <span data-ttu-id="a441e-361">Embora o exemplo discutido aqui tenha apenas uma funcionalidade limitada, ele ilustra todos os recursos necessários de um objeto de banda e pode ser prontamente estendido para criar uma interface de usuário exclusiva e poderosa.</span><span class="sxs-lookup"><span data-stu-id="a441e-361">While the example discussed here has only limited functionality, it illustrates all the necessary features of a band object and it can be readily extended to create a unique and powerful user interface.</span></span>

 

 
