---
title: Gerenciando usuários
description: As contas de usuário são criadas e armazenadas como objetos no Active Directory Domain Services.
ms.assetid: 57c83e4d-2d9f-4f22-97e2-27e2d277f014
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, Gerenciando usuários
- AD de usuários
- usuários AD, Gerenciando usuários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1105132c6836e108a416331b2f4a6ad666c03d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822266"
---
# <a name="managing-users"></a><span data-ttu-id="9d13a-106">Gerenciando usuários</span><span class="sxs-lookup"><span data-stu-id="9d13a-106">Managing Users</span></span>

<span data-ttu-id="9d13a-107">As contas de usuário são criadas e armazenadas como objetos no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9d13a-107">User accounts are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="9d13a-108">Esses objetos de usuário representam usuários e computadores.</span><span class="sxs-lookup"><span data-stu-id="9d13a-108">These user objects represent users and computers.</span></span> <span data-ttu-id="9d13a-109">Esta seção define o que os usuários são e como eles são usados e explica como gerenciar programaticamente os usuários no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9d13a-109">This section defines what users are and how they are used, and explains how to programmatically manage users in Active Directory Domain Services.</span></span> <span data-ttu-id="9d13a-110">Esta seção aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="9d13a-110">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="9d13a-111">Usuários no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="9d13a-111">Users in Active Directory Domain Services</span></span>](users-in-active-directory-domain-services.md)
-   [<span data-ttu-id="9d13a-112">Entidades de segurança</span><span class="sxs-lookup"><span data-stu-id="9d13a-112">Security Principals</span></span>](security-principals.md)
-   [<span data-ttu-id="9d13a-113">O que é um usuário?</span><span class="sxs-lookup"><span data-stu-id="9d13a-113">What is a User?</span></span>](what-is-a-user.md)
-   [<span data-ttu-id="9d13a-114">Código de exemplo para associação ao contêiner de usuários</span><span class="sxs-lookup"><span data-stu-id="9d13a-114">Example Code for Binding to the Users Container</span></span>](example-code-for-binding-to-the-users-container.md)
-   [<span data-ttu-id="9d13a-115">Atributos de objeto de usuário</span><span class="sxs-lookup"><span data-stu-id="9d13a-115">User Object Attributes</span></span>](user-object-attributes.md)
-   [<span data-ttu-id="9d13a-116">Criando um usuário</span><span class="sxs-lookup"><span data-stu-id="9d13a-116">Creating a User</span></span>](creating-a-user.md)
-   <span data-ttu-id="9d13a-117">Excluindo um usuário.</span><span class="sxs-lookup"><span data-stu-id="9d13a-117">Deleting a user.</span></span> <span data-ttu-id="9d13a-118">Um usuário é excluído na mesma forma que qualquer outro objeto em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9d13a-118">A user is deleted in the same was as any other object in Active Directory Domain Services.</span></span> <span data-ttu-id="9d13a-119">Para obter mais informações sobre como excluir objetos, consulte [criando e excluindo objetos no Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="9d13a-119">For more information about deleting objects, see [Creating and Deleting Objects in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span></span>
-   [<span data-ttu-id="9d13a-120">Enumerando usuários</span><span class="sxs-lookup"><span data-stu-id="9d13a-120">Enumerating Users</span></span>](enumerating-users.md)
-   [<span data-ttu-id="9d13a-121">Consultando usuários</span><span class="sxs-lookup"><span data-stu-id="9d13a-121">Querying for Users</span></span>](querying-for-users.md)
-   <span data-ttu-id="9d13a-122">Movendo usuários.</span><span class="sxs-lookup"><span data-stu-id="9d13a-122">Moving users.</span></span> <span data-ttu-id="9d13a-123">Um usuário é movido da mesma forma que qualquer outro objeto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9d13a-123">A user is moved in the same was as any other Active Directory object.</span></span> <span data-ttu-id="9d13a-124">Para obter mais informações sobre como mover objetos Active Directory, consulte [movendo objetos](moving-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9d13a-124">For more information about moving Active Directory objects, see [Moving Objects](moving-objects.md).</span></span>
-   [<span data-ttu-id="9d13a-125">Gerenciando usuários em servidores membros e no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9d13a-125">Managing Users on Member Servers and Windows 2000 Professional</span></span>](managing-users-on-member-servers-and-windows-2000-professional.md)

 

 




