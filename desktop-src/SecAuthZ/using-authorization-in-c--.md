---
description: Use a API do Gerenciador de autorização para controlar o acesso aos recursos do aplicativo.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Usando a autorização em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753724"
---
# <a name="using-authorization-in-c"></a><span data-ttu-id="7c1e8-103">Usando a autorização em C++</span><span class="sxs-lookup"><span data-stu-id="7c1e8-103">Using Authorization in C++</span></span>

<span data-ttu-id="7c1e8-104">Você pode usar a API do Gerenciador de autorização para controlar o acesso aos recursos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-104">You can use the Authorization Manager API to control access to application resources.</span></span>

<span data-ttu-id="7c1e8-105">Se você tiver uma solução de controle de acesso com base nas [*listas de controle de acesso*](/windows/desktop/SecGloss/a-gly) (ACLs) e quiser evitar a conversão dessa solução para usar o Gerenciador de autorização, poderá continuar a usar ACLs para controlar o acesso aos recursos.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-105">If you have an existing access control solution based on [*access control lists*](/windows/desktop/SecGloss/a-gly) (ACLs) and want to avoid converting this solution to use Authorization Manager, you can continue to use ACLs to control access to resources.</span></span> <span data-ttu-id="7c1e8-106">Para obter informações sobre como controlar o acesso a recursos usando ACLs, consulte [definindo permissões com ACLs em c++](defining-permissions-with-acls-in-c--.md), [estabelecendo um contexto de cliente de um SID em c++](establishing-a-client-context-from-a-sid-in-c--.md)e [verificando o acesso de cliente com ACLs em c++](verifying-client-access-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="7c1e8-106">For information about controlling access to resources using ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md), [Establishing a Client Context from a SID in C++](establishing-a-client-context-from-a-sid-in-c--.md), and [Verifying Client Access with ACLs in C++](verifying-client-access-with-acls-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="7c1e8-107">Para grandes empresas, há uma compensação entre o desempenho e a sobrecarga administrativa.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-107">For large enterprises, there is a trade-off between administrative overhead and performance.</span></span> <span data-ttu-id="7c1e8-108">À medida que aumenta o número de recursos protegidos e os usuários, a administração das ACLs torna-se mais complicada.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-108">As the number of secured resources and users increases, the administration of ACLs becomes more complicated.</span></span> <span data-ttu-id="7c1e8-109">O desempenho não é afetado porque todas as informações necessárias sobre direitos de acesso são distribuídas para os recursos protegidos.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-109">Performance is not affected because all required information about access rights is distributed to the secured resources.</span></span> <span data-ttu-id="7c1e8-110">O desempenho do Gerenciador de autorização é afetado pelo dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-110">The performance of Authorization Manager is affected by scaling.</span></span>

 

<span data-ttu-id="7c1e8-111">Para obter informações sobre outras tarefas de autorização, consulte [tarefas de suporte para autorização em C++](supporting-tasks-for-authorization-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="7c1e8-111">For information about other authorization tasks, see [Supporting Tasks for Authorization in C++](supporting-tasks-for-authorization-in-c--.md).</span></span>



| <span data-ttu-id="7c1e8-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="7c1e8-112">Topic</span></span>                                                                                                                | <span data-ttu-id="7c1e8-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c1e8-113">Description</span></span>                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c1e8-114">Definindo permissões em C++</span><span class="sxs-lookup"><span data-stu-id="7c1e8-114">Defining Permissions in C++</span></span>](defining-permissions-in-c--.md)                                                       | <span data-ttu-id="7c1e8-115">Defina quais usuários têm acesso a quais recursos de aplicativo Criando um repositório de política de autorização.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-115">Define which users have access to which application resources by creating an authorization policy store.</span></span> |
| [<span data-ttu-id="7c1e8-116">Verificando o acesso do cliente a um recurso solicitado em C++</span><span class="sxs-lookup"><span data-stu-id="7c1e8-116">Verifying Client Access to a Requested Resource in C++</span></span>](verifying-client-access-to-a-requested-resource-in-c--.md) | <span data-ttu-id="7c1e8-117">Verifique se o cliente tem acesso a uma ou mais operações.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-117">Check whether the client has access to one or more operations.</span></span>                                           |
| [<span data-ttu-id="7c1e8-118">Delegando a definição de permissões em C++</span><span class="sxs-lookup"><span data-stu-id="7c1e8-118">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)                   | <span data-ttu-id="7c1e8-119">Delegar a administração de armazenamentos de diretiva de autorização armazenados no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7c1e8-119">Delegate the administration of authorization policy stores that are stored in Active Directory.</span></span>          |



 

 

 
