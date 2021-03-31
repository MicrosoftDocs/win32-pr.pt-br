---
title: Herança e delegação de administração
description: Descreve AD DS suporte para a herança de permissões na árvore de objetos e também herança específica de objeto.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- herança de administração e delegação Active Directory
- Active Directory Active Directory, herança de permissões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d76db80497b54e71c806f3ccff9df549f9b2c1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159316"
---
# <a name="inheritance-and-delegation-of-administration"></a><span data-ttu-id="86efe-105">Herança e delegação de administração</span><span class="sxs-lookup"><span data-stu-id="86efe-105">Inheritance and Delegation of Administration</span></span>

<span data-ttu-id="86efe-106">Active Directory Domain Services dá suporte à herança de permissões na árvore de objetos para permitir que as tarefas de administração sejam executadas em níveis mais altos na árvore.</span><span class="sxs-lookup"><span data-stu-id="86efe-106">Active Directory Domain Services supports the inheritance of permissions down the object tree to allow administration tasks to be performed at higher levels in the tree.</span></span> <span data-ttu-id="86efe-107">Isso permite que os administradores configurem permissões herdáveis em objetos próximos à raiz, como domínio e unidades organizacionais, e tenham essas permissões distribuídas a vários objetos na árvore.</span><span class="sxs-lookup"><span data-stu-id="86efe-107">This enables administrators to set up inheritable permissions on objects near the root, such as domain and organizational units, and have those permissions distributed to various objects in the tree.</span></span>

<span data-ttu-id="86efe-108">A herança pode ser definida em uma base por ACE.</span><span class="sxs-lookup"><span data-stu-id="86efe-108">Inheritance can be set on a per-ACE basis.</span></span> <span data-ttu-id="86efe-109">A tabela a seguir lista os sinalizadores que podem ser especificados no **AceFlags** para controlar a herança da Ace.</span><span class="sxs-lookup"><span data-stu-id="86efe-109">The following table lists flags that can be specified in the **AceFlags** to control inheritance of the ACE.</span></span>



| <span data-ttu-id="86efe-110">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="86efe-110">Flag</span></span>                                                     | <span data-ttu-id="86efe-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="86efe-111">Description</span></span>                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86efe-112">**\_ACE de \_ herança de ACEFLAG ADS \_**</span><span class="sxs-lookup"><span data-stu-id="86efe-112">**ADS\_ACEFLAG\_INHERIT\_ACE**</span></span><br/>                | <span data-ttu-id="86efe-113">Faz com que a ACE seja herdada na árvore.</span><span class="sxs-lookup"><span data-stu-id="86efe-113">Causes the ACE to be inherited down in the tree.</span></span><br/>                                                                                     |
| <span data-ttu-id="86efe-114">**ADS \_ ACEFLAG \_ não \_ propagar \_ a \_ Ace INHERIT**</span><span class="sxs-lookup"><span data-stu-id="86efe-114">**ADS\_ACEFLAG\_NO\_PROPAGATE\_INHERIT\_ACE**</span></span><br/> | <span data-ttu-id="86efe-115">Faz com que a ACE seja herdada apenas um nível na árvore.</span><span class="sxs-lookup"><span data-stu-id="86efe-115">Causes the ACE to be inherited down only one level in the tree.</span></span><br/>                                                                      |
| <span data-ttu-id="86efe-116">**os anúncios \_ ACEFLAG \_ herdam \_ apenas \_ Ace**</span><span class="sxs-lookup"><span data-stu-id="86efe-116">**ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE**</span></span><br/>          | <span data-ttu-id="86efe-117">Faz com que a ACE seja ignorada no objeto no qual ela está especificada, seja herdada somente e seja efetiva onde foi herdada.</span><span class="sxs-lookup"><span data-stu-id="86efe-117">Causes the ACE to be ignored on the object it is specified on, only be inherited down, and be effective where it has been inherited.</span></span><br/> |



 

<span data-ttu-id="86efe-118">Além de definir a herança, o Active Directory Domain Services dá suporte à herança específica do objeto.</span><span class="sxs-lookup"><span data-stu-id="86efe-118">In addition to setting inheritance, Active Directory Domain Services supports object-specific inheritance.</span></span> <span data-ttu-id="86efe-119">Isso permite que as ACEs herdáveis sejam herdadas para baixo na árvore, mas entram em vigor apenas em um tipo específico de objeto.</span><span class="sxs-lookup"><span data-stu-id="86efe-119">This allows the inheritable ACEs to be inherited down the tree, but be effective only on a specific type of object.</span></span> <span data-ttu-id="86efe-120">Isso é extremamente útil na delegação da administração.</span><span class="sxs-lookup"><span data-stu-id="86efe-120">This is extremely useful in delegating administration.</span></span> <span data-ttu-id="86efe-121">Por exemplo, isso pode ser usado para definir uma ACE herdável específica de objeto em uma unidade organizacional que permite que um grupo tenha controle total sobre todos os objetos de usuário na unidade organizacional, mas nada mais.</span><span class="sxs-lookup"><span data-stu-id="86efe-121">For example, this can be used to set an object-specific inheritable ACE at an organizational unit that enables a group to have full control on all user objects in the organizational unit, but nothing else.</span></span> <span data-ttu-id="86efe-122">Assim, o gerenciamento de usuários nessa unidade organizacional é delegado aos usuários nesse grupo.</span><span class="sxs-lookup"><span data-stu-id="86efe-122">Thereby, the management of users in that organizational unit gets delegated to the users in that group.</span></span>

### <a name="delegating-service-administration-with-security-groups"></a><span data-ttu-id="86efe-123">Delegando a administração do serviço com grupos de segurança</span><span class="sxs-lookup"><span data-stu-id="86efe-123">Delegating Service Administration with Security Groups</span></span>

<span data-ttu-id="86efe-124">Use grupos de segurança para definir e delegar funções administrativas associadas ao servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="86efe-124">Use Security groups to define and delegate administrative roles associated with your application server.</span></span> <span data-ttu-id="86efe-125">Por exemplo, seu serviço pode estar associado a um grupo Administradores de myatendimento.</span><span class="sxs-lookup"><span data-stu-id="86efe-125">For example, your service may be associated with a group MyService Administrators.</span></span> <span data-ttu-id="86efe-126">Os usuários identificados como administradores do MyService serão adicionados ao grupo de administradores do MyService.</span><span class="sxs-lookup"><span data-stu-id="86efe-126">Users who are identified as the MyService administrators will be added to MyService Administrators group.</span></span> <span data-ttu-id="86efe-127">O programa de instalação do MyService pode definir ACLs no diretório para habilitar os administradores de MyService permissões suficientes para ler/gravar atributos relacionados a MyService ou criar objetos específicos de MyService, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="86efe-127">The setup program for MyService can set ACLs on the directory to enable MyService Administrators sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

### <a name="roles-in-security-groups-for-computers-running-your-service"></a><span data-ttu-id="86efe-128">Funções em grupos de segurança para computadores que executam seu serviço</span><span class="sxs-lookup"><span data-stu-id="86efe-128">Roles in Security Groups for Computers Running Your Service</span></span>

<span data-ttu-id="86efe-129">Use grupos de segurança para definir o conjunto de computadores que recebem acesso aos objetos do serviço no diretório.</span><span class="sxs-lookup"><span data-stu-id="86efe-129">Use security groups to define the set of computers that are granted access to your service's objects in the directory.</span></span> <span data-ttu-id="86efe-130">Por exemplo, seu serviço pode estar associado a um grupo de servidores MyService.</span><span class="sxs-lookup"><span data-stu-id="86efe-130">For example, your service may be associated with a group MyService Servers.</span></span> <span data-ttu-id="86efe-131">Todos os computadores que executam o servidor MyService são adicionados ao grupo de servidores MyService e esse grupo pode receber acesso a partes do diretório em que os servidores de MyService precisam ler/gravar dados.</span><span class="sxs-lookup"><span data-stu-id="86efe-131">All computers running the MyService server are added to MyService Servers group and this group can then be given access to parts of the directory where MyService servers need to read/write data.</span></span> <span data-ttu-id="86efe-132">O programa de instalação do MyService pode definir ACLs no diretório para habilitar os servidores de MyService permissões suficientes para ler/gravar atributos relacionados a MyService ou criar objetos específicos de MyService, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="86efe-132">The setup program for MyService can set ACLs on the directory to enable MyService Servers sufficient permissions to read/write MyService-related attributes or create MyService-specific objects for example.</span></span>

 

 





