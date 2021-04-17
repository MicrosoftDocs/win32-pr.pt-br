---
description: Criando um novo aplicativo COM+
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Criando um novo aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762356"
---
# <a name="creating-a-new-com-application"></a><span data-ttu-id="a1314-103">Criando um novo aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="a1314-103">Creating a New COM+ Application</span></span>

<span data-ttu-id="a1314-104">A criação de um novo aplicativo COM+ requer duas etapas básicas, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a1314-104">Creating a new COM+ application requires two basic steps, as follows:</span></span>

-   <span data-ttu-id="a1314-105">Criando um aplicativo COM+ vazio (descrito abaixo).</span><span class="sxs-lookup"><span data-stu-id="a1314-105">Creating an empty COM+ application (described below).</span></span>
-   <span data-ttu-id="a1314-106">Adicionando componentes ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1314-106">Adding components to the application.</span></span> <span data-ttu-id="a1314-107">(Consulte [instalando novos componentes](installing-new-components.md) e [importando componentes](importing-components.md).)</span><span class="sxs-lookup"><span data-stu-id="a1314-107">(See [Installing New Components](installing-new-components.md) and [Importing Components](importing-components.md).)</span></span>

<span data-ttu-id="a1314-108">**Para criar um aplicativo COM+ vazio**</span><span class="sxs-lookup"><span data-stu-id="a1314-108">**To create an empty COM+ application**</span></span>

1.  <span data-ttu-id="a1314-109">Na árvore de console da ferramenta administrativa serviços de componentes, selecione o computador no qual você deseja criar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1314-109">In the console tree of the Component Services administrative tool, select the computer on which you want to create an application.</span></span>

2.  <span data-ttu-id="a1314-110">Selecione a pasta **aplicativos com+** para esse computador.</span><span class="sxs-lookup"><span data-stu-id="a1314-110">Select the **COM+ Applications** folder for that computer.</span></span>

3.  <span data-ttu-id="a1314-111">No menu **ação** , aponte para **novo** e clique em **aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="a1314-111">On the **Action** menu, point to **New**, and then click **Application**.</span></span> <span data-ttu-id="a1314-112">Você também pode clicar com o botão direito do mouse na pasta **aplicativos com+** , apontar para **novo** e clicar em **aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="a1314-112">You can also right-click the **COM+ Applications** folder, point to **New**, and then click **Application**.</span></span>

4.  <span data-ttu-id="a1314-113">Na página de **boas-vindas** do assistente de instalação do aplicativo com+, clique em **Avançar** e, na caixa de diálogo **instalar ou criar um novo aplicativo** , clique em **criar um aplicativo vazio**.</span><span class="sxs-lookup"><span data-stu-id="a1314-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Install or Create a New Application** dialog box, click **Create an empty application**.</span></span>

5.  <span data-ttu-id="a1314-114">Na caixa fornecida, digite um nome para o novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1314-114">In the box provided, type a name for the new application.</span></span> <span data-ttu-id="a1314-115">(Observe que os seguintes caracteres especiais não podem ser usados em um nome de aplicativo: \\ ,/, ~,!, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ , ', ", >, <,.,?,: e;.) Em **tipo de ativação**, clique em **aplicativo de biblioteca** ou **aplicativo de servidor**.</span><span class="sxs-lookup"><span data-stu-id="a1314-115">(Note that the following special characters cannot be used in an application name: \\, /, ~, !, @, \#, %, ^, &, \*, (, ), \|, }, {, \], \[, ', ", >, <, ., ?, :, and ;.) Under **Activation type**, click **Library application** or **Server application**.</span></span> <span data-ttu-id="a1314-116">Clique em **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="a1314-116">Click **Next**.</span></span>

    > [!Note]  
    > <span data-ttu-id="a1314-117">Um aplicativo de servidor é executado em seu próprio processo.</span><span class="sxs-lookup"><span data-stu-id="a1314-117">A server application runs in its own process.</span></span> <span data-ttu-id="a1314-118">Os aplicativos de servidor podem dar suporte a todos os serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="a1314-118">Server applications can support all COM+ services.</span></span> <span data-ttu-id="a1314-119">Um aplicativo de biblioteca é executado no processo do cliente que o cria.</span><span class="sxs-lookup"><span data-stu-id="a1314-119">A library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="a1314-120">Os aplicativos de biblioteca podem usar a segurança baseada em função, mas não dão suporte a acesso remoto ou a componentes na fila.</span><span class="sxs-lookup"><span data-stu-id="a1314-120">Library applications can use role-based security but do not support remote access or queued components.</span></span>

     

6.  <span data-ttu-id="a1314-121">Na caixa de diálogo **definir identidade do aplicativo** , escolha uma identidade sob a qual o aplicativo será executado.</span><span class="sxs-lookup"><span data-stu-id="a1314-121">In the **Set Application Identity** dialog box, choose an identity under which the application will run.</span></span> <span data-ttu-id="a1314-122">Se você selecionar **este usuário**, digite o nome de usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="a1314-122">If you select **This user**, type the user name and password.</span></span> <span data-ttu-id="a1314-123">Você também deve digitar a senha novamente na caixa **Confirmar senha** .</span><span class="sxs-lookup"><span data-stu-id="a1314-123">You must also retype the password in the **Confirm password** box.</span></span> <span data-ttu-id="a1314-124">Clique em **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="a1314-124">Click **Next**.</span></span> <span data-ttu-id="a1314-125">(A seleção padrão de identidade do aplicativo é **usuário interativo**.</span><span class="sxs-lookup"><span data-stu-id="a1314-125">(The default selection for application identity is **Interactive User**.</span></span> <span data-ttu-id="a1314-126">O usuário interativo é o usuário conectado ao computador do servidor em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="a1314-126">The interactive user is the user logged on to the server computer at any given time.</span></span> <span data-ttu-id="a1314-127">Você pode selecionar um usuário diferente selecionando **esse usuário** e inserindo um usuário ou grupo específico.)</span><span class="sxs-lookup"><span data-stu-id="a1314-127">You can select a different user by selecting **This user** and entering a specific user or group.)</span></span>

    > [!Note]  
    > <span data-ttu-id="a1314-128">A caixa de diálogo **definir identidade do aplicativo** será exibida somente se você tiver selecionado **aplicativo de servidor** para o tipo de ativação do novo aplicativo na caixa de diálogo anterior do assistente de instalação de aplicativo com.</span><span class="sxs-lookup"><span data-stu-id="a1314-128">The **Set Application Identity** dialog box appears only if you selected **Server application** for the new application's activation type in the COM Application Install Wizard's preceding dialog box.</span></span> <span data-ttu-id="a1314-129">A propriedade Identity não é usada para aplicativos de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a1314-129">The identity property is not used for library applications.</span></span>

     

7.  <span data-ttu-id="a1314-130">Na caixa de diálogo **adicionar funções de aplicativo** , adicione as funções que você deseja associar ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1314-130">In the **Add Application Roles** dialog box, add any roles you want to associate with the application.</span></span> <span data-ttu-id="a1314-131">Por padrão, somente a função **CreatorOwner** é definida.</span><span class="sxs-lookup"><span data-stu-id="a1314-131">By default, only the **CreatorOwner** role is defined.</span></span> <span data-ttu-id="a1314-132">Para obter informações sobre funções, consulte [Administração de segurança baseada em funções](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="a1314-132">For information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

8.  <span data-ttu-id="a1314-133">Na caixa de diálogo **Adicionar usuários às funções** , preencha cada função que você criou na última etapa com os usuários, grupos ou entidades de segurança internas às quais você deseja conceder os privilégios associados a essa função.</span><span class="sxs-lookup"><span data-stu-id="a1314-133">In the **Add Users to Roles** dialog box, populate each role you created in the last step with the users, groups, or built-in security principals to which you want to grant the privileges associated with that role.</span></span> <span data-ttu-id="a1314-134">Por padrão, o usuário interativo é colocado na função **CreatorOwner** .</span><span class="sxs-lookup"><span data-stu-id="a1314-134">By default, the interactive user is placed in the **CreatorOwner** role.</span></span>

9.  <span data-ttu-id="a1314-135">Clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="a1314-135">Click **Finish**.</span></span>

<span data-ttu-id="a1314-136">O novo aplicativo agora será exibido na pasta **aplicativos com+** na árvore de console da ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="a1314-136">The new application will now be displayed under the **COM+ Applications** folder in the console tree of the Component Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="a1314-137">A partir do Windows Server 2003, as verificações de acesso são habilitadas por padrão ao criar um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="a1314-137">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="a1314-138">Em versões anteriores, as verificações de acesso foram desabilitadas por padrão no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1314-138">In previous versions, access checks were disabled by default at the application level.</span></span> <span data-ttu-id="a1314-139">O resultado é que, por padrão, o acesso a um aplicativo COM+ é permitido somente para usuários que estão nas funções associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1314-139">The result is that by default, access to a COM+ application is allowed only to users that are in the roles associated with the application.</span></span> <span data-ttu-id="a1314-140">(Consulte [Administração de segurança baseada em funções](role-based-security-administration.md).) Como alternativa, você pode permitir o acesso a todos os usuários desabilitando as verificações de acesso em um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="a1314-140">(See [Role-Based Security Administration](role-based-security-administration.md).) Alternatively, you can allow access to all users by disabling access checks on a COM+ application.</span></span> <span data-ttu-id="a1314-141">(Consulte [habilitando verificações de acesso para um aplicativo](enabling-access-checks-for-an-application.md).)</span><span class="sxs-lookup"><span data-stu-id="a1314-141">(See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md).)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a1314-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1314-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1314-143">Copiando componentes</span><span class="sxs-lookup"><span data-stu-id="a1314-143">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="a1314-144">Excluindo um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="a1314-144">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="a1314-145">Importando componentes</span><span class="sxs-lookup"><span data-stu-id="a1314-145">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="a1314-146">Instalando novos componentes</span><span class="sxs-lookup"><span data-stu-id="a1314-146">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="a1314-147">Movendo componentes</span><span class="sxs-lookup"><span data-stu-id="a1314-147">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="a1314-148">Removendo um componente de um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="a1314-148">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



