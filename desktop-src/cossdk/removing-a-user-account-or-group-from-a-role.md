---
description: Se os privilégios de usuários forem alterados ou se as funções forem adicionadas a um aplicativo, você poderá mover uma conta de uma função para outra função.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Removendo uma conta de usuário ou grupo de uma função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771659"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a><span data-ttu-id="759a9-103">Removendo uma conta de usuário ou grupo de uma função</span><span class="sxs-lookup"><span data-stu-id="759a9-103">Removing a User Account or Group from a Role</span></span>

<span data-ttu-id="759a9-104">Se os privilégios de um usuário forem alterados ou se as funções forem adicionadas a um aplicativo, você poderá mover uma conta de uma função para outra função.</span><span class="sxs-lookup"><span data-stu-id="759a9-104">If a user's privileges change or if roles are added to an application, you can move an account from one role to another role.</span></span> <span data-ttu-id="759a9-105">Para mover uma conta de usuário ou grupo de usuários de uma função para outra, você deve remover a conta de usuário ou grupo de sua função atual e, em seguida, atribuí-la à nova função.</span><span class="sxs-lookup"><span data-stu-id="759a9-105">To move a user account or group of users from one role to another, you must remove the user account or group from its current role and then assign it to the new role.</span></span>

<span data-ttu-id="759a9-106">**Para mover uma conta de usuário ou grupo de uma função para outra**</span><span class="sxs-lookup"><span data-stu-id="759a9-106">**To move a user account or group from one role to another**</span></span>

1.  <span data-ttu-id="759a9-107">Remova a conta de usuário ou grupo da função à qual ela não deve mais pertencer, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="759a9-107">Remove the user account or group from the role that it should no longer belong to, as follows:</span></span>

    1.  <span data-ttu-id="759a9-108">Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ que contém a função em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="759a9-108">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="759a9-109">Expanda a exibição na árvore de console até que os usuários da função fiquem visíveis.</span><span class="sxs-lookup"><span data-stu-id="759a9-109">Expand the view in the console tree until the users for the role are visible.</span></span>

    2.  <span data-ttu-id="759a9-110">Clique com o botão direito do mouse na conta de usuário ou grupo que você deseja remover e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="759a9-110">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

    3.  <span data-ttu-id="759a9-111">Quando solicitado pela caixa de diálogo **Confirmar exclusão de item** , clique em **Sim** para excluir a conta de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="759a9-111">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

    <span data-ttu-id="759a9-112">A conta de usuário ou o grupo que você removeu da função não aparece mais na pasta **usuários** .</span><span class="sxs-lookup"><span data-stu-id="759a9-112">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span>

2.  <span data-ttu-id="759a9-113">Atribua a conta de usuário ou grupo que você removeu para as funções às quais o usuário ou grupo deve ser atribuído, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="759a9-113">Assign the user account or group you have removed to the roles that the user or group should be assigned to, as follows:</span></span>

    1.  <span data-ttu-id="759a9-114">Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ que contém a função à qual você deseja adicionar a conta de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="759a9-114">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="759a9-115">Expanda a exibição na árvore de console até que as funções do aplicativo fiquem visíveis.</span><span class="sxs-lookup"><span data-stu-id="759a9-115">Expand the view in the console tree until the application's roles are visible.</span></span>

    2.  <span data-ttu-id="759a9-116">Localize a função à qual você deseja adicionar a conta de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="759a9-116">Locate the role to which you want to add the user account or group.</span></span>

        > [!Note]  
        > <span data-ttu-id="759a9-117">Se a função que você está procurando não estiver na pasta **funções** , a função não foi adicionada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="759a9-117">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="759a9-118">Ele deve ser adicionado ao aplicativo pelo desenvolvedor antes que você possa atribuir contas de usuário à função.</span><span class="sxs-lookup"><span data-stu-id="759a9-118">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

         

    3.  <span data-ttu-id="759a9-119">Clique com o botão direito do mouse na pasta **usuários** na função, aponte para **novo** e clique em **usuário**.</span><span class="sxs-lookup"><span data-stu-id="759a9-119">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

    4.  <span data-ttu-id="759a9-120">Na janela **Selecionar usuários ou grupos** , no painel inferior, digite o nome totalmente qualificado do usuário ou grupo que você deseja adicionar.</span><span class="sxs-lookup"><span data-stu-id="759a9-120">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="759a9-121">Se você não souber o nome, clique no botão **avançado** e, em seguida, clique em **localizar agora** para exibir uma lista de usuários e grupos no domínio selecionado.</span><span class="sxs-lookup"><span data-stu-id="759a9-121">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="759a9-122">Selecione um usuário ou grupo na lista **nome (RDN)** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="759a9-122">Select a user or group from the **Name (RDN)** list and click **OK**.</span></span>

    5.  <span data-ttu-id="759a9-123">Quando terminar de adicionar a conta de usuário ou grupo à função, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="759a9-123">When you have finished adding the user account or group to the role, click **OK**.</span></span>

    <span data-ttu-id="759a9-124">Para cada conta de usuário ou grupo que você atribuiu à função, um ícone é exibido na pasta **usuários** .</span><span class="sxs-lookup"><span data-stu-id="759a9-124">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span>

<span data-ttu-id="759a9-125">A associação de função alterada para a conta de usuário ou grupo entrará em vigor na próxima vez em que o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="759a9-125">The changed role membership for the user account or group takes effect the next time the application is started.</span></span>

 

 



