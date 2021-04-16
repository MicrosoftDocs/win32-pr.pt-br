---
title: Itens recentes
description: A lista itens recentes é um painel no menu do aplicativo que exibe os itens usados mais recentemente (MRU) para um aplicativo.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104557726"
---
# <a name="recent-items"></a><span data-ttu-id="ae342-103">Itens recentes</span><span class="sxs-lookup"><span data-stu-id="ae342-103">Recent Items</span></span>

<span data-ttu-id="ae342-104">A lista itens recentes é um painel no [menu do aplicativo](windowsribbon-controls-applicationmenu.md) que exibe os itens usados mais recentemente (MRU) para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae342-104">The Recent Items list is a pane in the [Application Menu](windowsribbon-controls-applicationmenu.md) that displays the most recently used (MRU) items for an application.</span></span>

-   [<span data-ttu-id="ae342-105">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ae342-105">Details</span></span>](#details)
-   [<span data-ttu-id="ae342-106">Propriedades de itens recentes</span><span class="sxs-lookup"><span data-stu-id="ae342-106">Recent Items Properties</span></span>](#recent-items-properties)
-   [<span data-ttu-id="ae342-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae342-107">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="ae342-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae342-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="ae342-109">Detalhes</span><span class="sxs-lookup"><span data-stu-id="ae342-109">Details</span></span>

<span data-ttu-id="ae342-110">A captura de tela a seguir ilustra uma lista de itens recentes do WordPad para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ae342-110">The following screen shot illustrates a Recent Items list from WordPad for Windows 7).</span></span>

![captura de tela da lista de itens recentes na faixa de faixas do Microsoft Paint.](images/controls/recentitems.png)

<span data-ttu-id="ae342-112">O [menu do aplicativo](windowsribbon-controls-applicationmenu.md) pode ter no máximo uma lista [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) , representada por um elemento **ApplicationMenu. RecentItems** , para exibir documentos, imagens, filmes e outros projetos em que um usuário está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ae342-112">The [Application Menu](windowsribbon-controls-applicationmenu.md) can have at most one [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) list, represented by an **ApplicationMenu.RecentItems** element, for displaying recent documents, pictures, movies, and other projects a user has been working on.</span></span> <span data-ttu-id="ae342-113">O número de itens listados varia de zero até o número máximo especificado na marcação, com um valor padrão de dez.</span><span class="sxs-lookup"><span data-stu-id="ae342-113">The number of listed items ranges from zero to the maximum number specified in markup, with a default value of ten.</span></span> <span data-ttu-id="ae342-114">Os itens recentes são exibidos como uma lista numerada de cadeias de caracteres que indicam nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ae342-114">The recent items are displayed as a numbered list of strings indicating file names.</span></span> <span data-ttu-id="ae342-115">É recomendável que a propriedade [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) seja usada para fornecer o caminho completo para o local do arquivo, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae342-115">It is recommended that the [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) property be used to give the full path for the file location, as shown in the following screen shot .</span></span>

![captura de tela de uma lista de itens recentes em um menu de aplicativo.](images/overviews/applicationmenu-menurecentitems.png)

<span data-ttu-id="ae342-117">O elemento [**RecentItems**](windowsribbon-element-recentitems.md) tem um atributo *EnablePinning* que, se definido como `true` , exibe um ícone de pino à direita de cada item na lista, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae342-117">The [**RecentItems**](windowsribbon-element-recentitems.md) element has an *EnablePinning* attribute that, if set to `true`, displays a pin icon to the right of each item in the list, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="ae342-118">A fixação será habilitada por padrão se o atributo *EnablePinning* não for especificado.</span><span class="sxs-lookup"><span data-stu-id="ae342-118">Pinning is enabled by default if the *EnablePinning* attribute is not specified.</span></span>

 

![captura de tela de itens recentes fixando em um menu de aplicativo.](images/overviews/applicationmenu-menurecentitemspinned.png)

<span data-ttu-id="ae342-120">O algoritmo de fixação destina-se a impedir que os itens caiam na lista de **itens recentes** .</span><span class="sxs-lookup"><span data-stu-id="ae342-120">The pinning algorithm is intended to keep items from falling off the **Recent items** list.</span></span> <span data-ttu-id="ae342-121">O algoritmo produz o seguinte comportamento:</span><span class="sxs-lookup"><span data-stu-id="ae342-121">The algorithm produces the following behavior:</span></span>

-   <span data-ttu-id="ae342-122">Um novo item é sempre adicionado na parte superior da lista de **itens recentes** .</span><span class="sxs-lookup"><span data-stu-id="ae342-122">A new item is always added at the top of the **Recent items** list.</span></span>
-   <span data-ttu-id="ae342-123">Os itens serão movidos para baixo na lista ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="ae342-123">Items will move down in the list over time.</span></span> <span data-ttu-id="ae342-124">Quando a lista estiver cheia (atingir o número máximo de itens especificados na marcação), os itens mais antigos ficarão na parte inferior da lista à medida que novos itens forem adicionados à parte superior da lista.</span><span class="sxs-lookup"><span data-stu-id="ae342-124">Once the list is full (reaches the maximum number of items specified in markup), older items fall off the bottom of the list as new items are added to the top of the list.</span></span>
-   <span data-ttu-id="ae342-125">Se um item já aparecer em algum lugar na lista, mas for acessado novamente, ele voltará para o topo da lista.</span><span class="sxs-lookup"><span data-stu-id="ae342-125">If an item already appears somewhere in the list but is accessed again, it moves back to the top of the list.</span></span>
-   <span data-ttu-id="ae342-126">Se um item for fixado, ele ainda fará a viagem na lista, mas não cairá na parte inferior.</span><span class="sxs-lookup"><span data-stu-id="ae342-126">If an item is pinned, it will still travel down the list, but it will not fall off the bottom.</span></span> <span data-ttu-id="ae342-127">Em vez disso, quando a lista estiver cheia, o primeiro item desafixado acima do item fixado será desativado quando um novo item for adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="ae342-127">Instead, once the list is full, the first unpinned item above the pinned item will fall off when a new item is added to the list.</span></span>
-   <span data-ttu-id="ae342-128">Se o número de itens fixados atingir o número máximo de itens, nenhum novo item será adicionado à lista, até que ele seja desafixado.</span><span class="sxs-lookup"><span data-stu-id="ae342-128">If the number of pinned items ever reaches the maximum number of items, then no new items will get added to the list until an item is unpinned.</span></span>

## <a name="recent-items-properties"></a><span data-ttu-id="ae342-129">Propriedades de itens recentes</span><span class="sxs-lookup"><span data-stu-id="ae342-129">Recent Items Properties</span></span>

<span data-ttu-id="ae342-130">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle itens recentes.</span><span class="sxs-lookup"><span data-stu-id="ae342-130">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Recent Items control.</span></span>

<span data-ttu-id="ae342-131">Normalmente, uma propriedade Items recentes é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="ae342-131">Typically, a Recent Items property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="ae342-132">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="ae342-132">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="ae342-133">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="ae342-133">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="ae342-134">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="ae342-134">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="ae342-135">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="ae342-135">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="ae342-136">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle itens recentes.</span><span class="sxs-lookup"><span data-stu-id="ae342-136">The following table lists the property keys that are associated with the Recent Items control.</span></span>



| <span data-ttu-id="ae342-137">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="ae342-137">Property Key</span></span>                                                                       | <span data-ttu-id="ae342-138">Observações</span><span class="sxs-lookup"><span data-stu-id="ae342-138">Notes</span></span>                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="ae342-139">\_KeyTip PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="ae342-139">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)           | <span data-ttu-id="ae342-140">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="ae342-140">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="ae342-141">\_RecentItems PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="ae342-141">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md) | <span data-ttu-id="ae342-142">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="ae342-142">Can only be updated through invalidation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ae342-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae342-143">Remarks</span></span>

<span data-ttu-id="ae342-144">O método [IApplicationDocumentLists:: GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) pode ser usado para recuperar a lista MRU do shell do Windows para o aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="ae342-144">The [IApplicationDocumentLists::GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) method can be used to retrieve the Windows Shell MRU list for the Ribbon application.</span></span> <span data-ttu-id="ae342-145">O objeto recuperado por esse método pode então ser usado pelo aplicativo para criar os dados exigidos pela estrutura da faixa de faixas para preencher a lista de **itens recentes** do [menu do aplicativo](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="ae342-145">The object retrieved by this method can then be used by the application to create the data required by the Ribbon framework to populate the **Recent items** list of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

> [!Note]  
> <span data-ttu-id="ae342-146">Ao usar esse método, *ListType* deve ter o valor `ADLT_RECENT` .</span><span class="sxs-lookup"><span data-stu-id="ae342-146">When using this method, *listtype* should have the value `ADLT_RECENT`.</span></span>

 

<span data-ttu-id="ae342-147">Para obter um exemplo de como implementar uma lista de itens MRU em um aplicativo da estrutura da faixa de faixas, consulte o [exemplo HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="ae342-147">For an example of how to implement an MRU items list in a Ribbon framework application, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae342-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae342-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae342-149">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="ae342-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="ae342-150">**Elemento de marcação de itens recentes**</span><span class="sxs-lookup"><span data-stu-id="ae342-150">**Recent items markup element**</span></span>](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 