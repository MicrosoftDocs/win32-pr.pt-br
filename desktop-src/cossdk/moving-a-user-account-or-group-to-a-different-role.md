---
description: Você pode remover contas de usuário ou grupos de uma função quando os usuários ou membros dos grupos não devem mais receber acesso aos recursos do aplicativo aos quais a função está atribuída.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Movendo uma conta de usuário ou grupo para uma função diferente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2401d792066212269d4eaa4eb11eadfef6e2d73e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089499"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a><span data-ttu-id="f9bba-103">Movendo uma conta de usuário ou grupo para uma função diferente</span><span class="sxs-lookup"><span data-stu-id="f9bba-103">Moving a User Account or Group to a Different Role</span></span>

<span data-ttu-id="f9bba-104">Você pode remover contas de usuário ou grupos de uma função quando os usuários ou membros dos grupos não devem mais receber acesso aos recursos do aplicativo aos quais a função está atribuída.</span><span class="sxs-lookup"><span data-stu-id="f9bba-104">You can remove user accounts or groups from a role when the users or members of the groups should no longer be given access to the application resources to which the role is assigned.</span></span>

<span data-ttu-id="f9bba-105">**Para remover uma conta de usuário ou grupo de uma função**</span><span class="sxs-lookup"><span data-stu-id="f9bba-105">**To remove a user account or group from a role**</span></span>

1.  <span data-ttu-id="f9bba-106">Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ que contém a função em que você está interessado.</span><span class="sxs-lookup"><span data-stu-id="f9bba-106">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="f9bba-107">Expanda a exibição na árvore de console até que os usuários da função fiquem visíveis.</span><span class="sxs-lookup"><span data-stu-id="f9bba-107">Expand the view in the console tree until the users for the role are visible.</span></span>

2.  <span data-ttu-id="f9bba-108">Clique com o botão direito do mouse na conta de usuário ou grupo que você deseja remover e clique em **excluir**.</span><span class="sxs-lookup"><span data-stu-id="f9bba-108">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

3.  <span data-ttu-id="f9bba-109">Quando solicitado pela caixa de diálogo **Confirmar exclusão de item** , clique em **Sim** para excluir a conta de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="f9bba-109">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

<span data-ttu-id="f9bba-110">A conta de usuário ou o grupo que você removeu da função não aparece mais na pasta **usuários** .</span><span class="sxs-lookup"><span data-stu-id="f9bba-110">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span> <span data-ttu-id="f9bba-111">A nova associação de função entrará em vigor na próxima vez em que o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="f9bba-111">The new role membership takes effect the next time the application is started.</span></span> <span data-ttu-id="f9bba-112">Se você tiver feito alterações no **aplicativo do sistema**, deverá reiniciar o computador para que as alterações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="f9bba-112">If you have made changes to the **System Application**, you must restart the computer for the changes to take effect.</span></span>

 

 



