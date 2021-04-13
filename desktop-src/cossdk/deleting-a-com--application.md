---
description: À medida que os aplicativos existentes forem desatualizados ou não estiverem mais sendo usados, talvez seja necessário removê-los.
ms.assetid: 5cce94c9-8eff-40b9-946d-a57749da073d
title: Excluindo um aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da685e5a7ae7590fcc247caa765d49dc34d076e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370456"
---
# <a name="deleting-a-com-application"></a><span data-ttu-id="a171c-103">Excluindo um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="a171c-103">Deleting a COM+ Application</span></span>

<span data-ttu-id="a171c-104">À medida que os aplicativos existentes forem desatualizados ou não estiverem mais sendo usados, talvez seja necessário removê-los.</span><span class="sxs-lookup"><span data-stu-id="a171c-104">As existing applications become dated or are no longer being used, you may need to remove them.</span></span>

<span data-ttu-id="a171c-105">**Para excluir um aplicativo COM+**</span><span class="sxs-lookup"><span data-stu-id="a171c-105">**To delete a COM+ application**</span></span>

1.  <span data-ttu-id="a171c-106">Na árvore de console da ferramenta administrativa serviços de componentes, selecione o computador para o qual você deseja excluir um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a171c-106">In the console tree of the Component Services administrative tool, select the computer for which you want to delete an application.</span></span>

2.  <span data-ttu-id="a171c-107">Abra a pasta **aplicativos com+** do computador especificado para exibir todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a171c-107">Open the **COM+ Applications** folder for the specified computer to display all the applications.</span></span>

3.  <span data-ttu-id="a171c-108">Selecione o aplicativo que você deseja remover.</span><span class="sxs-lookup"><span data-stu-id="a171c-108">Select the application you want to remove.</span></span>

4.  <span data-ttu-id="a171c-109">Se você selecionou um aplicativo de servidor, desligue o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a171c-109">If you selected a server application, shut down the application.</span></span> <span data-ttu-id="a171c-110">Você pode desligar um aplicativo selecionando-o na ferramenta administrativa serviços de componentes, clicando com o botão direito do mouse e, em seguida, clicando em **desligar**.</span><span class="sxs-lookup"><span data-stu-id="a171c-110">You can shut down an application by selecting it in the Component Services administrative tool, right-clicking, and then clicking **Shut down**.</span></span> <span data-ttu-id="a171c-111">Se você selecionou um aplicativo de biblioteca, verifique se todos os processos que estão usando este aplicativo de biblioteca atualmente estão desligados.</span><span class="sxs-lookup"><span data-stu-id="a171c-111">If you selected a library application, make sure that all processes currently using this library application are shut down.</span></span>

5.  <span data-ttu-id="a171c-112">No menu **ação** , clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="a171c-112">On the **Action** menu, click **Delete**.</span></span> <span data-ttu-id="a171c-113">Você também pode clicar com o botão direito do mouse no nome do aplicativo e clicar em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="a171c-113">You can also right-click the application name and then click **Delete**.</span></span> <span data-ttu-id="a171c-114">Você também pode excluir um aplicativo selecionando-o na ferramenta administrativa serviços de componentes e pressionando a tecla **delete** , ou pode selecionar o aplicativo, clicar com o botão direito do mouse e, em seguida, clicar em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="a171c-114">You can also delete an application by selecting it in the Component Services administrative tool and pressing the **Delete** key, or you can select the application, right-click, and then click **Delete**.</span></span>

6.  <span data-ttu-id="a171c-115">Clique em **Sim** quando for solicitado a confirmar sua ação.</span><span class="sxs-lookup"><span data-stu-id="a171c-115">Click **Yes** when prompted to confirm your action.</span></span>

<span data-ttu-id="a171c-116">Além disso, se um aplicativo de servidor ou proxy de aplicativo tiver sido instalado em um computador usando Windows Installer (conforme descrito em "Instalando aplicativos COM+" no guia de administração de serviços de componentes), você poderá excluí-lo por meio do utilitário adicionar/remover programas no painel de controle do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a171c-116">In addition, if a server application or application proxy has been installed on a computer using Windows Installer (as described in "Installing COM+ Applications" in the Component Services Administration Guide), you can delete it through the Add/Remove Programs utility in the Microsoft Windows Control Panel.</span></span> <span data-ttu-id="a171c-117">Ou você pode excluir um aplicativo de servidor instalado ou proxy de aplicativo usando a sintaxe de linha de comando Windows Installer:</span><span class="sxs-lookup"><span data-stu-id="a171c-117">Or you can delete an installed server application or application proxy by using the Windows Installer command line syntax:</span></span>

<span data-ttu-id="a171c-118">**msiexec-x** *nome do aplicativo \_ \* \* *. msi**</span><span class="sxs-lookup"><span data-stu-id="a171c-118">**msiexec -x** *application\_name\*\*\*.msi*\*</span></span>

<span data-ttu-id="a171c-119">Esses métodos são especialmente úteis para excluir aplicativos COM+ em computadores cliente que não executam a ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="a171c-119">These methods are especially useful for deleting COM+ applications on client machines that are not running the Component Services administrative tool.</span></span>

<span data-ttu-id="a171c-120">Excluir o aplicativo também exclui todos os componentes contidos no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a171c-120">Deleting the application also deletes any components contained in the application.</span></span> <span data-ttu-id="a171c-121">Se esses componentes dependerem de recursos adicionais (conexões de banco de dados, arquivos de data ou de texto, configuração de raiz virtual do IIS e assim por diante), esses recursos deverão ser removidos por meio de mecanismos diferentes da ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="a171c-121">If these components depend on additional resources (database connections, data or text files, IIS virtual root configuration, and so on), these resources must be removed through mechanisms other than the Component Services administrative tool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a171c-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a171c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a171c-123">Copiando componentes</span><span class="sxs-lookup"><span data-stu-id="a171c-123">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="a171c-124">Criando um novo aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="a171c-124">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)
</dt> <dt>

[<span data-ttu-id="a171c-125">Importando componentes</span><span class="sxs-lookup"><span data-stu-id="a171c-125">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="a171c-126">Instalando novos componentes</span><span class="sxs-lookup"><span data-stu-id="a171c-126">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="a171c-127">Movendo componentes</span><span class="sxs-lookup"><span data-stu-id="a171c-127">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="a171c-128">Removendo um componente de um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="a171c-128">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



