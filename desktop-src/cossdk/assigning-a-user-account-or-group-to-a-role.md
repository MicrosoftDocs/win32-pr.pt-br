---
description: Você pode usar a ferramenta administrativa serviços de componentes para preencher uma função com contas de usuário ou grupos.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Atribuindo uma conta de usuário ou grupo a uma função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798460"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a><span data-ttu-id="f4177-103">Atribuindo uma conta de usuário ou grupo a uma função</span><span class="sxs-lookup"><span data-stu-id="f4177-103">Assigning a User Account or Group to a Role</span></span>

<span data-ttu-id="f4177-104">Você pode usar a ferramenta administrativa serviços de componentes para preencher uma função com contas de usuário ou grupos.</span><span class="sxs-lookup"><span data-stu-id="f4177-104">You can use the Component Services administrative tool to populate a role with user accounts or groups.</span></span> <span data-ttu-id="f4177-105">A maneira preferida de atribuir uma conta de usuário a uma função é atribuir a conta de usuário a um grupo e, em seguida, atribuir o grupo à função.</span><span class="sxs-lookup"><span data-stu-id="f4177-105">The preferred way to assign a user account to a role is to assign the user account to a group and then assign the group to the role.</span></span> <span data-ttu-id="f4177-106">Usar grupos para popular funções torna mais fácil gerenciar um grande número de usuários.</span><span class="sxs-lookup"><span data-stu-id="f4177-106">Using groups to populate roles makes it easier for you to manage large numbers of users.</span></span> <span data-ttu-id="f4177-107">Na ajuda online para a ferramenta administrativa Gerenciamento de computador, consulte o tópico "usuários e grupos locais" para obter mais informações sobre como criar grupos ou atribuir uma conta de usuário a um grupo.</span><span class="sxs-lookup"><span data-stu-id="f4177-107">In the online help for the Computer Management administrative tool, see the topic "Local Users and Groups" for more information about creating groups or assigning a user account to a group.</span></span>

> [!Note]  
> <span data-ttu-id="f4177-108">Para permitir que usuários de rede não autenticados executem um aplicativo COM+, as funções de aplicativo devem incluir o usuário anônimo.</span><span class="sxs-lookup"><span data-stu-id="f4177-108">To allow unauthenticated network users to run a COM+ application, the application roles must include the Anonymous user.</span></span> <span data-ttu-id="f4177-109">A partir do Windows Server 2003, por padrão, o usuário anônimo não está incluído no grupo Everyone.</span><span class="sxs-lookup"><span data-stu-id="f4177-109">Starting with Windows Server 2003, by default, the Anonymous user is not included in the Everyone group.</span></span>

 

<span data-ttu-id="f4177-110">Depois de atribuir a conta de usuário ao grupo do Windows apropriado, siga estas etapas para atribuir o grupo do Windows à função.</span><span class="sxs-lookup"><span data-stu-id="f4177-110">After you have assigned the user account to the appropriate Windows group, follow these steps to assign the Windows group to the role.</span></span>

<span data-ttu-id="f4177-111">**Para atribuir um grupo do Windows a uma função de segurança**</span><span class="sxs-lookup"><span data-stu-id="f4177-111">**To assign a Windows group to a security role**</span></span>

1.  <span data-ttu-id="f4177-112">Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ que contém a função à qual você deseja adicionar a conta de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="f4177-112">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="f4177-113">Expanda a exibição na árvore de console até que as funções do aplicativo fiquem visíveis.</span><span class="sxs-lookup"><span data-stu-id="f4177-113">Expand the view in the console tree until the application's roles are visible.</span></span>

2.  <span data-ttu-id="f4177-114">Localize a função à qual você deseja adicionar a conta de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="f4177-114">Locate the role to which you want to add the user account or group.</span></span>

    > [!Note]  
    > <span data-ttu-id="f4177-115">Se a função que você está procurando não estiver na pasta **funções** , a função não foi adicionada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f4177-115">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="f4177-116">Ele deve ser adicionado ao aplicativo pelo desenvolvedor antes que você possa atribuir contas de usuário à função.</span><span class="sxs-lookup"><span data-stu-id="f4177-116">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

     

3.  <span data-ttu-id="f4177-117">Clique com o botão direito do mouse na pasta **usuários** na função, aponte para **novo** e clique em **usuário**.</span><span class="sxs-lookup"><span data-stu-id="f4177-117">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

4.  <span data-ttu-id="f4177-118">Na janela **Selecionar usuários ou grupos** , no painel inferior, digite o nome totalmente qualificado do usuário ou grupo que você deseja adicionar.</span><span class="sxs-lookup"><span data-stu-id="f4177-118">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="f4177-119">Se você não souber o nome, clique no botão **avançado** e, em seguida, clique em **localizar agora** para exibir uma lista de usuários e grupos no domínio selecionado.</span><span class="sxs-lookup"><span data-stu-id="f4177-119">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="f4177-120">Selecione um usuário ou grupo na lista **nome (RDN)** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4177-120">Select a user or group from the **Name (RDN)** list, and click **OK**.</span></span>

5.  <span data-ttu-id="f4177-121">Para adicionar mais contas de usuário ou grupos, repita a etapa 4.</span><span class="sxs-lookup"><span data-stu-id="f4177-121">To add more user accounts or groups, repeat step 4.</span></span>

6.  <span data-ttu-id="f4177-122">Quando terminar de adicionar contas de usuário e grupos à função, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4177-122">When you have finished adding user accounts and groups to the role, click **OK**.</span></span>

<span data-ttu-id="f4177-123">Para cada conta de usuário ou grupo que você atribuiu à função, um ícone é exibido na pasta **usuários** .</span><span class="sxs-lookup"><span data-stu-id="f4177-123">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span> <span data-ttu-id="f4177-124">A nova associação de função entrará em vigor na próxima vez em que o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="f4177-124">The new role membership takes effect the next time the application is started.</span></span>

 

 



