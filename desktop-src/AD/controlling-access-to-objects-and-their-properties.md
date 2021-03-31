---
title: Controlando o acesso a objetos e suas propriedades
description: Para controlar o acesso a objetos de aplicativo, trabalhe com o descritor de segurança de objeto e, especificamente, com a DACL (lista de controle de acesso discricionário) e sua lista de ACEs (entradas de controle de acesso).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- AD de objeto, controlando o acesso ao
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159267"
---
# <a name="controlling-access-to-objects-and-their-properties"></a><span data-ttu-id="3536a-104">Controlando o acesso a objetos e suas propriedades</span><span class="sxs-lookup"><span data-stu-id="3536a-104">Controlling Access to Objects and Their Properties</span></span>

<span data-ttu-id="3536a-105">Para controlar o acesso a objetos de aplicativo, trabalhe com o descritor de segurança de objeto e, especificamente, com a DACL (lista de controle de acesso discricionário) e sua lista de ACEs (entradas de controle de acesso).</span><span class="sxs-lookup"><span data-stu-id="3536a-105">To control access to application objects, work with the object security descriptor, and specifically, with the discretionary access-control list (DACL) and its list of access-control entries (ACEs).</span></span>

<span data-ttu-id="3536a-106">Quando um objeto é criado, ele recebe um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="3536a-106">When an object is created, it receives a security descriptor.</span></span> <span data-ttu-id="3536a-107">Para obter mais informações e uma descrição das regras que o sistema usa para criar a DACL para um novo objeto, consulte [como descritores de segurança são definidos em novos objetos de diretório](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3536a-107">For more information, and a description of the rules that the system uses to create the DACL for a new object, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span> <span data-ttu-id="3536a-108">Essas regras revelam que você pode:</span><span class="sxs-lookup"><span data-stu-id="3536a-108">These rules reveal that you can:</span></span>

-   <span data-ttu-id="3536a-109">Crie um novo descritor de segurança e anexe-o ao objeto no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="3536a-109">Create a new security descriptor and attach it to the object at creation time.</span></span> <span data-ttu-id="3536a-110">Para obter mais informações, consulte [criando um descritor de segurança para um novo objeto de diretório](creating-a-security-descriptor-for-a-new-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="3536a-110">For more information, see [Creating a Security Descriptor for a New Directory Object](creating-a-security-descriptor-for-a-new-directory-object.md).</span></span>
-   <span data-ttu-id="3536a-111">Aplique uma ACE herdável, em qualquer ponto da hierarquia de diretório, de modo que uma ACE seja herdada por objetos na árvore.</span><span class="sxs-lookup"><span data-stu-id="3536a-111">Apply an inheritable ACE, at any point in the directory hierarchy, such that an ACE is inherited by objects down the tree.</span></span> <span data-ttu-id="3536a-112">Um objeto pode herdar uma ACE de seu contêiner pai.</span><span class="sxs-lookup"><span data-stu-id="3536a-112">An object can inherit an ACE from its parent container.</span></span> <span data-ttu-id="3536a-113">Para obter mais informações, consulte [herança e delegação de administração](inheritance-and-delegation-of-administration.md).</span><span class="sxs-lookup"><span data-stu-id="3536a-113">For more information, see [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md).</span></span>
-   <span data-ttu-id="3536a-114">Especifique uma ACE na DACL padrão no esquema, se você tiver os direitos de acesso necessários.</span><span class="sxs-lookup"><span data-stu-id="3536a-114">Specify an ACE in the default DACL in the schema, if you have the necessary access rights.</span></span> <span data-ttu-id="3536a-115">Cada definição de classe de objeto no esquema inclui um descritor de segurança padrão que pode ter uma DACL padrão.</span><span class="sxs-lookup"><span data-stu-id="3536a-115">Every object class definition in the schema includes a default security descriptor that can have a default DACL.</span></span> <span data-ttu-id="3536a-116">Para obter mais informações, consulte [descritor de segurança padrão](default-security-descriptor.md).</span><span class="sxs-lookup"><span data-stu-id="3536a-116">For more information, see [Default Security Descriptor](default-security-descriptor.md).</span></span>

<span data-ttu-id="3536a-117">Além disso, a DACL de um objeto existente pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="3536a-117">In addition the DACL of an existing object can be modified.</span></span> <span data-ttu-id="3536a-118">Você pode:</span><span class="sxs-lookup"><span data-stu-id="3536a-118">You can:</span></span>

-   <span data-ttu-id="3536a-119">Substitua a DACL por uma nova.</span><span class="sxs-lookup"><span data-stu-id="3536a-119">Replace the DACL with a new one.</span></span>
-   <span data-ttu-id="3536a-120">Leia a DACL existente, modifique-a e aplique a DACL modificada.</span><span class="sxs-lookup"><span data-stu-id="3536a-120">Read the existing DACL, modify it, and apply the modified DACL.</span></span> <span data-ttu-id="3536a-121">Para obter mais informações, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="3536a-121">For more information, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="3536a-122">A lista a seguir descreve a função mais importante de uma ACE no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="3536a-122">The following list describes the most important function of an ACE in Active Directory Domain Services.</span></span> <span data-ttu-id="3536a-123">Com uma ACE, você pode:</span><span class="sxs-lookup"><span data-stu-id="3536a-123">With an ACE, you can:</span></span>

-   <span data-ttu-id="3536a-124">Controle quem pode executar operações específicas em um objeto.</span><span class="sxs-lookup"><span data-stu-id="3536a-124">Control who can perform specific operations on an object.</span></span>
-   <span data-ttu-id="3536a-125">Controle quem tem acesso a uma propriedade específica ou a um conjunto de propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="3536a-125">Control who has access to a specific property, or set of properties, of an object.</span></span>
-   <span data-ttu-id="3536a-126">Controle quem pode criar objetos filho em um contêiner, incluindo quem pode criar um tipo específico de objeto filho.</span><span class="sxs-lookup"><span data-stu-id="3536a-126">Control who can create child objects in a container, including who can create a specific type of child object.</span></span>
-   <span data-ttu-id="3536a-127">Defina controle privado-direitos de acesso para um tipo de objeto e controle quem pode executar as operações protegidas pelos direitos particulares.</span><span class="sxs-lookup"><span data-stu-id="3536a-127">Define private control-access rights for an object type and control who can perform the operations protected by the private rights.</span></span>
-   <span data-ttu-id="3536a-128">Aplique uma ACE a um objeto de contêiner na raiz de uma subárvore de diretório, de modo que as proteções possam ser herdadas automaticamente por todos os objetos filho na árvore.</span><span class="sxs-lookup"><span data-stu-id="3536a-128">Apply an ACE to a container object at the root of a directory subtree, such that the protections can be inherited automatically by all child objects down the tree.</span></span>
-   <span data-ttu-id="3536a-129">Aplicar uma ACE que é herdada automaticamente por um tipo específico de objeto filho em uma subárvore.</span><span class="sxs-lookup"><span data-stu-id="3536a-129">Apply an ACE that is inherited automatically by a specific type of child object in a subtree.</span></span>
-   <span data-ttu-id="3536a-130">Crie uma ACE que conceda direitos a um grupo de segurança, e não a um único usuário.</span><span class="sxs-lookup"><span data-stu-id="3536a-130">Create an ACE that grants rights to a security group, rather than to a single user.</span></span>
-   <span data-ttu-id="3536a-131">Aplique uma ACE a Política de Grupo objetos para controlar as contas e os computadores afetados pela política.</span><span class="sxs-lookup"><span data-stu-id="3536a-131">Apply an ACE to Group Policy Objects to control the accounts and computers affected by the policy.</span></span>

 

 




