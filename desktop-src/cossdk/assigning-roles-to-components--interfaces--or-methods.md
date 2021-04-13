---
description: Atribuindo funções a componentes, interfaces ou métodos
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Atribuindo funções a componentes, interfaces ou métodos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370462"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a><span data-ttu-id="38df3-103">Atribuindo funções a componentes, interfaces ou métodos</span><span class="sxs-lookup"><span data-stu-id="38df3-103">Assigning Roles to Components, Interfaces, or Methods</span></span>

<span data-ttu-id="38df3-104">Você pode atribuir explicitamente uma função a qualquer item em um aplicativo COM+ que seja visível por meio da ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="38df3-104">You can explicitly assign a role to any item within a COM+ application that is visible through the Component Services administrative tool.</span></span> <span data-ttu-id="38df3-105">Isso garante que todos os usuários que são membros da função tenham acesso permitido a esse item e a quaisquer outros itens que ele contenha.</span><span class="sxs-lookup"><span data-stu-id="38df3-105">Doing so ensures that any users that are members of the role will be permitted access to that item and any other items that it contains.</span></span> <span data-ttu-id="38df3-106">Por exemplo, se você atribuir a função "leitores" a um componente, qualquer membro de "leitores" tem permissão para acessar esse componente e quaisquer interfaces e métodos que ele expõe.</span><span class="sxs-lookup"><span data-stu-id="38df3-106">For example, if you assign the role "Readers" to a component, any member of "Readers" is allowed access to that component and any interfaces and methods it exposes.</span></span> <span data-ttu-id="38df3-107">Os "leitores" aparecerão como uma função herdada para qualquer uma dessas interfaces e métodos.</span><span class="sxs-lookup"><span data-stu-id="38df3-107">"Readers" will show up as an Inherited role for any of those interfaces and methods.</span></span>

<span data-ttu-id="38df3-108">Um método só poderá ser acessado pelos chamadores se você atribuir uma função a ele, seja atribuindo explicitamente a função diretamente ao método ou atribuindo uma função à interface do método ou ao componente do método; nesse caso, a função será herdada pelo método.</span><span class="sxs-lookup"><span data-stu-id="38df3-108">A method is accessible to callers only if you assign a role to it, either by explicitly assigning the role directly to the method or by assigning a role to the method's interface or the method's component, in which case the role will be inherited by the method.</span></span> <span data-ttu-id="38df3-109">Se nenhuma função for atribuída e se as verificações de acesso estiverem habilitadas, todas as chamadas para o método falharão.</span><span class="sxs-lookup"><span data-stu-id="38df3-109">If no role is assigned and if access checks are enabled, all calls to the method will fail.</span></span>

<span data-ttu-id="38df3-110">Para poder atribuir uma função, você deve [defini](defining-roles-for-an-application.md) -la para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="38df3-110">Before you can assign a role, you must [define](defining-roles-for-an-application.md) it for the application.</span></span> <span data-ttu-id="38df3-111">Todas as funções definidas para o aplicativo aparecerão na janela **funções explicitamente definidas para os itens selecionados** na guia **segurança** para quaisquer componentes, métodos e interfaces dentro do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="38df3-111">All roles defined for the application will appear in the **Roles explicitly set for selected item(s)** window on the **Security** tab for any components, methods, and interfaces within the application.</span></span>

<span data-ttu-id="38df3-112">**Para atribuir funções a um componente, método ou interface**</span><span class="sxs-lookup"><span data-stu-id="38df3-112">**To assign roles to a component, method, or interface**</span></span>

1.  <span data-ttu-id="38df3-113">Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ para o qual a função foi definida.</span><span class="sxs-lookup"><span data-stu-id="38df3-113">In the console tree of the Component Services administrative tool, locate the COM+ application for which the role has been defined.</span></span> <span data-ttu-id="38df3-114">Expanda a árvore para exibir os componentes, as interfaces ou os métodos do aplicativo, dependendo do que você está atribuindo a função.</span><span class="sxs-lookup"><span data-stu-id="38df3-114">Expand the tree to view the application's components, interfaces, or methods, depending on what you are assigning the role to.</span></span>

2.  <span data-ttu-id="38df3-115">Clique com o botão direito do mouse no item ao qual você deseja atribuir a função e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="38df3-115">Right-click the item to which you want to assign the role, and then click **Properties**.</span></span>

3.  <span data-ttu-id="38df3-116">Na caixa de diálogo Propriedades, clique na guia **segurança** .</span><span class="sxs-lookup"><span data-stu-id="38df3-116">In the properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="38df3-117">Na caixa **funções explicitamente definidas para Item (ns) selecionado (s)** , selecione as funções que você deseja atribuir ao item.</span><span class="sxs-lookup"><span data-stu-id="38df3-117">In the **Roles explicitly set for selected item(s)** box, select the roles that you want to assign to the item.</span></span>

5.  <span data-ttu-id="38df3-118">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="38df3-118">Click **OK**.</span></span>

<span data-ttu-id="38df3-119">Todas as funções que você definir explicitamente para um item serão herdadas por itens de nível inferior que ele contém e aparecerão na janela **funções herdadas por item (ns) selecionado (s)** para esses itens.</span><span class="sxs-lookup"><span data-stu-id="38df3-119">Any roles that you have explicitly set for an item will be inherited by any lower-level items it contains and will show up in the **Roles inherited by selected item(s)** window for those items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38df3-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38df3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38df3-121">Configurando a segurança do Role-Based</span><span class="sxs-lookup"><span data-stu-id="38df3-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="38df3-122">Definindo funções para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="38df3-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="38df3-123">Habilitando verificações de acesso para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="38df3-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="38df3-124">Habilitando verificações de acesso no nível do componente</span><span class="sxs-lookup"><span data-stu-id="38df3-124">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="38df3-125">Configurando um nível de segurança para verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="38df3-125">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



