---
description: Para adicionar componentes à pasta componentes de um aplicativo COM+, você pode usar o assistente de instalação de componente COM+ ou arrastar arquivos. dll que contêm os componentes do Windows Explorer e soltá-los no aplicativo.
ms.assetid: 3cb0c24d-cd52-42ac-8b07-d8774698b90c
title: Instalando novos componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434bdb59c0a0e9c786bb3460a0cb1cbb6a1f50dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010228"
---
# <a name="installing-new-components"></a><span data-ttu-id="bd22c-103">Instalando novos componentes</span><span class="sxs-lookup"><span data-stu-id="bd22c-103">Installing New Components</span></span>

<span data-ttu-id="bd22c-104">Para adicionar componentes à pasta **componentes** de um aplicativo com+, você pode usar o assistente de instalação de componente com+ ou arrastar arquivos. dll que contêm os componentes do Windows Explorer e soltá-los no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd22c-104">To add components to the **Components** folder of a COM+ application, you can either use the COM+ Component Install Wizard or drag .dll files that contain the components from the Windows Explorer and drop them in the application.</span></span>

<span data-ttu-id="bd22c-105">Se você usar o assistente de instalação de componente COM+, poderá instalar um novo componente, que registra o componente no computador ou importar componentes que já foram registrados.</span><span class="sxs-lookup"><span data-stu-id="bd22c-105">If you use the COM+ Component Install Wizard, you can either install a new component, which registers the component on the computer, or import components that have already been registered.</span></span> <span data-ttu-id="bd22c-106">Os componentes podem ser adicionados a aplicativos vazios ou a aplicativos existentes.</span><span class="sxs-lookup"><span data-stu-id="bd22c-106">Components can be added to empty applications or existing applications.</span></span>

<span data-ttu-id="bd22c-107">**Para adicionar um componente a um aplicativo COM+**</span><span class="sxs-lookup"><span data-stu-id="bd22c-107">**To add a component to a COM+ application**</span></span>

1.  <span data-ttu-id="bd22c-108">Na árvore de console da ferramenta administrativa serviços de componentes, selecione o computador que hospeda o aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="bd22c-108">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="bd22c-109">Abra a pasta **aplicativos com+** para esse computador e selecione o aplicativo no qual você deseja instalar os componentes.</span><span class="sxs-lookup"><span data-stu-id="bd22c-109">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component(s).</span></span>

3.  <span data-ttu-id="bd22c-110">Abra a pasta do aplicativo e selecione **componentes**.</span><span class="sxs-lookup"><span data-stu-id="bd22c-110">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="bd22c-111">No menu **ação** , aponte para **novo** e clique em **componente**.</span><span class="sxs-lookup"><span data-stu-id="bd22c-111">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="bd22c-112">Você também pode clicar com o botão direito do mouse na pasta **componentes** , apontar para **novo** e clicar em **componente**.</span><span class="sxs-lookup"><span data-stu-id="bd22c-112">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="bd22c-113">Na página de **boas-vindas** do assistente de instalação do aplicativo com+, clique em **Avançar** e, na caixa de diálogo **importar ou instalar um componente** , clique em **instalar novos componentes** .</span><span class="sxs-lookup"><span data-stu-id="bd22c-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Install new components** .</span></span>

6.  <span data-ttu-id="bd22c-114">Na caixa de diálogo **instalar novos componentes** , clique em **Adicionar** para procurar o componente que você deseja adicionar.</span><span class="sxs-lookup"><span data-stu-id="bd22c-114">In the **Install new components** dialog box, click **Add** to browse for the component you want to add.</span></span>

7.  <span data-ttu-id="bd22c-115">Na caixa de diálogo **selecionar arquivos para instalar** , digite o nome do arquivo do componente a ser instalado ou selecione um nome de arquivo na lista exibida.</span><span class="sxs-lookup"><span data-stu-id="bd22c-115">In the **Select files to install** dialog box, type the filename of the component to install or select a filename from the displayed list.</span></span> <span data-ttu-id="bd22c-116">Clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="bd22c-116">Click **Open**.</span></span>

    <span data-ttu-id="bd22c-117">Depois de adicionar os arquivos, a caixa de diálogo **instalar novos componentes** exibe os arquivos que você adicionou e seus componentes associados.</span><span class="sxs-lookup"><span data-stu-id="bd22c-117">After you add the files, the **Install new components** dialog box displays the files you have added and their associated components.</span></span> <span data-ttu-id="bd22c-118">Se você marcar a caixa de seleção **detalhes** , verá mais informações sobre o conteúdo do arquivo e os componentes que foram encontrados.</span><span class="sxs-lookup"><span data-stu-id="bd22c-118">If you select the **Details** check box, you will see more information about file contents and the components that were found.</span></span>

    > [!Note]  
    > <span data-ttu-id="bd22c-119">Os componentes COM não configurados devem ter uma biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="bd22c-119">Unconfigured COM components must have a type library.</span></span> <span data-ttu-id="bd22c-120">Se COM+ não conseguir localizar a biblioteca de tipos do componente, seu componente não aparecerá na lista.</span><span class="sxs-lookup"><span data-stu-id="bd22c-120">If COM+ cannot find your component's type library, your component will not appear in the list.</span></span> <span data-ttu-id="bd22c-121">Você também pode remover um arquivo da lista **arquivos a serem instalados** selecionando-o e clicando em **remover**.</span><span class="sxs-lookup"><span data-stu-id="bd22c-121">You can also remove a file from the **Files to install** list by selecting it and clicking **Remove**.</span></span>

     

8.  <span data-ttu-id="bd22c-122">Clique em **Avançar** e em **concluir** para instalar o componente.</span><span class="sxs-lookup"><span data-stu-id="bd22c-122">Click **Next**, and then click **Finish** to install the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd22c-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd22c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd22c-124">Copiando componentes</span><span class="sxs-lookup"><span data-stu-id="bd22c-124">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="bd22c-125">Criando um novo aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="bd22c-125">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="bd22c-126">Excluindo um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="bd22c-126">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="bd22c-127">Importando componentes</span><span class="sxs-lookup"><span data-stu-id="bd22c-127">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="bd22c-128">Movendo componentes</span><span class="sxs-lookup"><span data-stu-id="bd22c-128">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="bd22c-129">Removendo um componente de um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="bd22c-129">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



