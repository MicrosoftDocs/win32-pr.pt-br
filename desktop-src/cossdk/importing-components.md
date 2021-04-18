---
description: Você pode usar a ferramenta administrativa serviços de componentes para importar para componentes específicos de aplicativos que já foram registrados em seu computador como componentes COM no registro do Windows.
ms.assetid: 5310e08a-5146-41f8-ae65-8467b921abd4
title: Importando componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1b67d944e9b8880b3edd0583569155fffecb23b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456953"
---
# <a name="importing-components"></a><span data-ttu-id="ce993-103">Importando componentes</span><span class="sxs-lookup"><span data-stu-id="ce993-103">Importing Components</span></span>

<span data-ttu-id="ce993-104">Você pode usar a ferramenta administrativa serviços de componentes para importar para componentes específicos de aplicativos que já foram registrados em seu computador como componentes COM no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="ce993-104">You can use the Component Services administrative tool to import into applications specific components that have already been registered on your computer as COM components in the Windows registry.</span></span> <span data-ttu-id="ce993-105">A importação de um componente não instala as informações de interface ou método necessárias para definir propriedades de interface ou para configurar o acesso ao componente de um cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="ce993-105">Importing a component does not install the interface or method information required to set interface properties or to configure access to the component from a remote client.</span></span> <span data-ttu-id="ce993-106">Portanto, se possível, você deve instalar o em vez de importar componentes não configurados.</span><span class="sxs-lookup"><span data-stu-id="ce993-106">Therefore, if possible, you should install rather than import unconfigured components.</span></span>

> [!Note]  
> <span data-ttu-id="ce993-107">Ao importar um componente para um aplicativo COM+, o COM+ não preenche as informações de interface e de método do componente.</span><span class="sxs-lookup"><span data-stu-id="ce993-107">When importing a component into a COM+ application, COM+ does not populate interface and method information for the component.</span></span> <span data-ttu-id="ce993-108">Durante a exportação de um proxy de aplicativo, o COM+ não fornecerá informações de marshaling (bibliotecas de tipo ou proxy/stubs) para algumas ou todas as interfaces.</span><span class="sxs-lookup"><span data-stu-id="ce993-108">During the export of an application proxy, COM+ will not provide marshaling information (type libraries or proxy/stubs) for some or all of the interfaces.</span></span> <span data-ttu-id="ce993-109">A exportação de proxies de aplicativo que contêm componentes importados falhará ou fará com que um aviso seja emitido.</span><span class="sxs-lookup"><span data-stu-id="ce993-109">Exporting application proxies that contain imported components will fail or cause a warning to be issued.</span></span>

 

<span data-ttu-id="ce993-110">**Para importar um componente para um aplicativo COM+**</span><span class="sxs-lookup"><span data-stu-id="ce993-110">**To import a component into a COM+ application**</span></span>

1.  <span data-ttu-id="ce993-111">Na árvore de console da ferramenta administrativa serviços de componentes, selecione o computador que hospeda o aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="ce993-111">In the console tree of the Component Services administrative tool, select the computer hosting the COM+ application.</span></span>

2.  <span data-ttu-id="ce993-112">Abra a pasta **aplicativos com+** para esse computador e selecione o aplicativo no qual você deseja instalar o componente.</span><span class="sxs-lookup"><span data-stu-id="ce993-112">Open the **COM+ Applications** folder for that computer, and select the application in which you want to install the component.</span></span>

3.  <span data-ttu-id="ce993-113">Abra a pasta do aplicativo e selecione **componentes**.</span><span class="sxs-lookup"><span data-stu-id="ce993-113">Open the application folder and select **Components**.</span></span>

4.  <span data-ttu-id="ce993-114">No menu **ação** , aponte para **novo** e clique em **componente**.</span><span class="sxs-lookup"><span data-stu-id="ce993-114">On the **Action** menu, point to **New**, and then click **Component**.</span></span> <span data-ttu-id="ce993-115">Você também pode clicar com o botão direito do mouse na pasta **componentes** , apontar para **novo** e clicar em **componente**.</span><span class="sxs-lookup"><span data-stu-id="ce993-115">You can also right-click the **Components** folder, point to **New**, and then click **Component**.</span></span>

5.  <span data-ttu-id="ce993-116">Na página de **boas-vindas** do assistente de instalação do aplicativo com+, clique em **Avançar** e, na caixa de diálogo **importar ou instalar um componente** , clique em **importar componente (s) que já está registrado**.</span><span class="sxs-lookup"><span data-stu-id="ce993-116">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Import or Install a Component** dialog box, click **Import component(s) that are already registered**.</span></span>

6.  <span data-ttu-id="ce993-117">Na caixa de diálogo **escolher componentes a serem importados** , marque a caixa de seleção **detalhes** para ver informações completas sobre os componentes que já estão registrados.</span><span class="sxs-lookup"><span data-stu-id="ce993-117">In the **Choose Components to Import** dialog box, select the **Details** check box to see complete information about the components that are already registered.</span></span> <span data-ttu-id="ce993-118">Selecione os componentes que você deseja importar da lista exibida e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="ce993-118">Select the component(s) you want to import from the displayed list, and click **Next**.</span></span>

7.  <span data-ttu-id="ce993-119">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="ce993-119">Click **Finish**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce993-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce993-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce993-121">Copiando componentes</span><span class="sxs-lookup"><span data-stu-id="ce993-121">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="ce993-122">Criando um novo aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="ce993-122">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="ce993-123">Excluindo um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="ce993-123">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="ce993-124">Instalando novos componentes</span><span class="sxs-lookup"><span data-stu-id="ce993-124">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="ce993-125">Movendo componentes</span><span class="sxs-lookup"><span data-stu-id="ce993-125">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="ce993-126">Removendo um componente de um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="ce993-126">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



