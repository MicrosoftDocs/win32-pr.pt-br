---
description: Você determina uma política de segurança para um aplicativo definindo os privilégios de segurança que ele requer.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definindo funções para um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813704"
---
# <a name="defining-roles-for-an-application"></a><span data-ttu-id="cadeb-103">Definindo funções para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="cadeb-103">Defining Roles for an Application</span></span>

<span data-ttu-id="cadeb-104">Você determina uma política de segurança para um aplicativo definindo os privilégios de segurança que ele requer.</span><span class="sxs-lookup"><span data-stu-id="cadeb-104">You determine a security policy for an application by defining the security privileges that it requires.</span></span> <span data-ttu-id="cadeb-105">Para fazer isso, você declara um nível simbólico de privilégio como uma função, ou seja, define a função para o aplicativo — e, em seguida, [atribui a função](assigning-roles-to-components--interfaces--or-methods.md) a recursos específicos dentro do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cadeb-105">To do this you declare a symbolic level of privilege as a role—that is, define the role for the application—and then [assign the role](assigning-roles-to-components--interfaces--or-methods.md) to specific resources within the application.</span></span> <span data-ttu-id="cadeb-106">Esse design é atendido quando o aplicativo é implantado e os administradores do sistema preenchem a função com usuários reais e grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="cadeb-106">This design is fulfilled when the application is deployed and system administrators populate the role with actual users and user groups.</span></span> <span data-ttu-id="cadeb-107">Para obter mais detalhes, consulte [Administração de segurança baseada em funções](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="cadeb-107">For greater detail, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

<span data-ttu-id="cadeb-108">**Para adicionar uma função a um aplicativo**</span><span class="sxs-lookup"><span data-stu-id="cadeb-108">**To add a role to an application**</span></span>

1.  <span data-ttu-id="cadeb-109">Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ ao qual você deseja adicionar a função.</span><span class="sxs-lookup"><span data-stu-id="cadeb-109">In the console tree of the Component Services administrative tool, locate the COM+ application to which you want to add the role.</span></span> <span data-ttu-id="cadeb-110">Expanda a árvore para exibir as pastas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cadeb-110">Expand the tree to view the folders for the application.</span></span>

2.  <span data-ttu-id="cadeb-111">Clique com o botão direito do mouse na pasta **funções** do aplicativo, aponte para **novo** e clique em **função**.</span><span class="sxs-lookup"><span data-stu-id="cadeb-111">Right-click the **Roles** folder for the application, point to **New**, and then click **Role**.</span></span>

3.  <span data-ttu-id="cadeb-112">Na caixa de diálogo **função**, digite o nome da nova função na caixa fornecida.</span><span class="sxs-lookup"><span data-stu-id="cadeb-112">In the **Role** dialog box, type the name of the new role in the box provided.</span></span>

4.  <span data-ttu-id="cadeb-113">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="cadeb-113">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="cadeb-114">Depois de adicionar funções ao aplicativo, você deve ter certeza de atribuir as funções aos componentes, às interfaces e aos métodos apropriados.</span><span class="sxs-lookup"><span data-stu-id="cadeb-114">After adding roles to the application, you must be sure to assign the roles to the appropriate components, interfaces, and methods.</span></span> <span data-ttu-id="cadeb-115">Caso contrário, se a segurança baseada em funções tiver sido escolhida e habilitada e se as funções tiverem sido adicionadas, mas não atribuídas, todas as chamadas para o aplicativo falharão.</span><span class="sxs-lookup"><span data-stu-id="cadeb-115">Otherwise, if role-based security has been chosen and enabled and if roles have been added but not assigned, all calls to the application will fail.</span></span> <span data-ttu-id="cadeb-116">Para obter mais informações, consulte [atribuindo funções a componentes, interfaces ou métodos](assigning-roles-to-components--interfaces--or-methods.md).</span><span class="sxs-lookup"><span data-stu-id="cadeb-116">For more information, see [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cadeb-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cadeb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cadeb-118">Atribuindo funções a componentes, interfaces ou métodos</span><span class="sxs-lookup"><span data-stu-id="cadeb-118">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="cadeb-119">Configurando a segurança do Role-Based</span><span class="sxs-lookup"><span data-stu-id="cadeb-119">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="cadeb-120">Habilitando verificações de acesso para um aplicativo</span><span class="sxs-lookup"><span data-stu-id="cadeb-120">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="cadeb-121">Habilitando verificações de acesso no nível do componente</span><span class="sxs-lookup"><span data-stu-id="cadeb-121">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="cadeb-122">Configurando um nível de segurança para verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="cadeb-122">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



