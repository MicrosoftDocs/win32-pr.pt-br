---
title: Gerenciando usuários
description: Saiba mais sobre como gerenciar usuários. As contas de usuário são criadas e armazenadas como objetos Active Directory Domain Services.
ms.assetid: 57c83e4d-2d9f-4f22-97e2-27e2d277f014
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, gerenciando usuários
- AD de usuários
- usuários do AD, gerenciando usuários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8154dc9d062b86d10b0df6418b5b4cbb79b44d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395311"
---
# <a name="managing-users"></a><span data-ttu-id="c7e07-107">Gerenciando usuários</span><span class="sxs-lookup"><span data-stu-id="c7e07-107">Managing Users</span></span>

<span data-ttu-id="c7e07-108">As contas de usuário são criadas e armazenadas como objetos Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c7e07-108">User accounts are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="c7e07-109">Esses objetos de usuário representam usuários e computadores.</span><span class="sxs-lookup"><span data-stu-id="c7e07-109">These user objects represent users and computers.</span></span> <span data-ttu-id="c7e07-110">Esta seção define o que são os usuários e como eles são usados e explica como gerenciar usuários programaticamente Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c7e07-110">This section defines what users are and how they are used, and explains how to programmatically manage users in Active Directory Domain Services.</span></span> <span data-ttu-id="c7e07-111">Esta seção discute os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="c7e07-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="c7e07-112">Usuários no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c7e07-112">Users in Active Directory Domain Services</span></span>](users-in-active-directory-domain-services.md)
-   [<span data-ttu-id="c7e07-113">Entidades de segurança</span><span class="sxs-lookup"><span data-stu-id="c7e07-113">Security Principals</span></span>](security-principals.md)
-   [<span data-ttu-id="c7e07-114">O que é um usuário?</span><span class="sxs-lookup"><span data-stu-id="c7e07-114">What is a User?</span></span>](what-is-a-user.md)
-   [<span data-ttu-id="c7e07-115">Código de exemplo para associação ao contêiner usuários</span><span class="sxs-lookup"><span data-stu-id="c7e07-115">Example Code for Binding to the Users Container</span></span>](example-code-for-binding-to-the-users-container.md)
-   [<span data-ttu-id="c7e07-116">Atributos de objeto de usuário</span><span class="sxs-lookup"><span data-stu-id="c7e07-116">User Object Attributes</span></span>](user-object-attributes.md)
-   [<span data-ttu-id="c7e07-117">Criando um usuário</span><span class="sxs-lookup"><span data-stu-id="c7e07-117">Creating a User</span></span>](creating-a-user.md)
-   <span data-ttu-id="c7e07-118">Excluindo um usuário.</span><span class="sxs-lookup"><span data-stu-id="c7e07-118">Deleting a user.</span></span> <span data-ttu-id="c7e07-119">Um usuário é excluído da mesma forma que qualquer outro objeto no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c7e07-119">A user is deleted in the same was as any other object in Active Directory Domain Services.</span></span> <span data-ttu-id="c7e07-120">Para obter mais informações sobre como excluir objetos, consulte [Criando e excluindo objetos no Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="c7e07-120">For more information about deleting objects, see [Creating and Deleting Objects in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span></span>
-   [<span data-ttu-id="c7e07-121">Enumerando usuários</span><span class="sxs-lookup"><span data-stu-id="c7e07-121">Enumerating Users</span></span>](enumerating-users.md)
-   [<span data-ttu-id="c7e07-122">Consultando usuários</span><span class="sxs-lookup"><span data-stu-id="c7e07-122">Querying for Users</span></span>](querying-for-users.md)
-   <span data-ttu-id="c7e07-123">Mover usuários.</span><span class="sxs-lookup"><span data-stu-id="c7e07-123">Moving users.</span></span> <span data-ttu-id="c7e07-124">Um usuário é movido da mesma forma que qualquer outro objeto do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c7e07-124">A user is moved in the same was as any other Active Directory object.</span></span> <span data-ttu-id="c7e07-125">Para obter mais informações sobre como mover objetos do Active Directory, consulte [Movendo objetos](moving-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c7e07-125">For more information about moving Active Directory objects, see [Moving Objects](moving-objects.md).</span></span>
-   [<span data-ttu-id="c7e07-126">Gerenciando usuários em servidores membros e Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c7e07-126">Managing Users on Member Servers and Windows 2000 Professional</span></span>](managing-users-on-member-servers-and-windows-2000-professional.md)

 

 




