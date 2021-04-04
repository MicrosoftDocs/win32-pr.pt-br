---
description: O controle de acesso refere-se aos recursos de segurança que controlam quem pode acessar recursos no sistema operacional. Os aplicativos chamam funções de controle de acesso para definir quem pode acessar recursos específicos ou controlar o acesso aos recursos fornecidos pelo aplicativo.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Controle de acesso (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010898"
---
# <a name="access-control-authorization"></a><span data-ttu-id="7c645-104">Controle de acesso (autorização)</span><span class="sxs-lookup"><span data-stu-id="7c645-104">Access Control (Authorization)</span></span>

<span data-ttu-id="7c645-105">O controle de acesso refere-se aos recursos de segurança que controlam quem pode acessar recursos no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7c645-105">Access control refers to security features that control who can access resources in the operating system.</span></span> <span data-ttu-id="7c645-106">Os aplicativos chamam funções de controle de acesso para definir quem pode acessar recursos específicos ou controlar o acesso aos recursos fornecidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c645-106">Applications call access control functions to set who can access specific resources or control access to resources provided by the application.</span></span>

<span data-ttu-id="7c645-107">Esta visão geral descreve o modelo de segurança para controlar o acesso a objetos do Windows, como arquivos, e para controlar o acesso a funções administrativas, como definir a hora do sistema ou as ações do usuário de auditoria.</span><span class="sxs-lookup"><span data-stu-id="7c645-107">This overview describes the security model for controlling access to Windows objects, such as files, and for controlling access to administrative functions, such as setting the system time or auditing user actions.</span></span> <span data-ttu-id="7c645-108">O tópico [modelo de controle de acesso](access-control-model.md) fornece uma descrição de alto nível das partes do controle de acesso e como elas interagem entre si.</span><span class="sxs-lookup"><span data-stu-id="7c645-108">The [Access Control Model](access-control-model.md) topic provides a high-level description of the parts of access control and how they interact with each other.</span></span>

<span data-ttu-id="7c645-109">Os tópicos a seguir descrevem o controle de acesso:</span><span class="sxs-lookup"><span data-stu-id="7c645-109">The following topics describe access control:</span></span>

-   [<span data-ttu-id="7c645-110">Segurança em nível C2</span><span class="sxs-lookup"><span data-stu-id="7c645-110">C2-level Security</span></span>](c2-level-security.md)
-   [<span data-ttu-id="7c645-111">Modelo de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="7c645-111">Access Control Model</span></span>](access-control-model.md)
-   [<span data-ttu-id="7c645-112">Linguagem de definição do descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="7c645-112">Security Descriptor Definition Language</span></span>](security-descriptor-definition-language.md)
-   [<span data-ttu-id="7c645-113">Direitos</span><span class="sxs-lookup"><span data-stu-id="7c645-113">Privileges</span></span>](privileges.md)
-   [<span data-ttu-id="7c645-114">Geração de auditoria</span><span class="sxs-lookup"><span data-stu-id="7c645-114">Audit Generation</span></span>](audit-generation.md)
-   [<span data-ttu-id="7c645-115">Objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="7c645-115">Securable Objects</span></span>](securable-objects.md)
-   [<span data-ttu-id="7c645-116">Controle de acesso de baixo nível</span><span class="sxs-lookup"><span data-stu-id="7c645-116">Low-level Access Control</span></span>](low-level-access-control.md)

<span data-ttu-id="7c645-117">A seguir estão as tarefas comuns de controle de acesso:</span><span class="sxs-lookup"><span data-stu-id="7c645-117">The following are common access control tasks:</span></span>

-   [<span data-ttu-id="7c645-118">Como as DACLs controlam o acesso a um objeto</span><span class="sxs-lookup"><span data-stu-id="7c645-118">How DACLs Control Access to an Object</span></span>](how-dacls-control-access-to-an-object.md)
-   [<span data-ttu-id="7c645-119">Controlando a criação de objetos filho em C++</span><span class="sxs-lookup"><span data-stu-id="7c645-119">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="7c645-120">ACEs para controlar o acesso às propriedades de um objeto</span><span class="sxs-lookup"><span data-stu-id="7c645-120">ACEs to Control Access to an Object's Properties</span></span>](aces-to-control-access-to-an-object-s-properties.md)
-   [<span data-ttu-id="7c645-121">Solicitando direitos de acesso a um objeto</span><span class="sxs-lookup"><span data-stu-id="7c645-121">Requesting Access Rights to an Object</span></span>](requesting-access-rights-to-an-object.md)

<span data-ttu-id="7c645-122">Os tópicos a seguir fornecem código de exemplo para tarefas de controle de acesso:</span><span class="sxs-lookup"><span data-stu-id="7c645-122">The following topics provide example code for access control tasks:</span></span>

-   [<span data-ttu-id="7c645-123">Modificando as ACLs de um objeto em C++</span><span class="sxs-lookup"><span data-stu-id="7c645-123">Modifying the ACLs of an Object in C++</span></span>](modifying-the-acls-of-an-object-in-c--.md)
-   [<span data-ttu-id="7c645-124">Criando um descritor de segurança para um novo objeto em C++</span><span class="sxs-lookup"><span data-stu-id="7c645-124">Creating a Security Descriptor for a New Object in C++</span></span>](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [<span data-ttu-id="7c645-125">Controlando a criação de objetos filho em C++</span><span class="sxs-lookup"><span data-stu-id="7c645-125">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="7c645-126">Habilitando e desabilitando privilégios em C++</span><span class="sxs-lookup"><span data-stu-id="7c645-126">Enabling and Disabling Privileges in C++</span></span>](enabling-and-disabling-privileges-in-c--.md)
-   [<span data-ttu-id="7c645-127">Pesquisando um SID em um token de acesso em C++</span><span class="sxs-lookup"><span data-stu-id="7c645-127">Searching for a SID in an Access Token in C++</span></span>](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [<span data-ttu-id="7c645-128">Localizando o proprietário de um objeto de arquivo em C++</span><span class="sxs-lookup"><span data-stu-id="7c645-128">Finding the Owner of a File Object in C++</span></span>](finding-the-owner-of-a-file-object-in-c--.md)
-   [<span data-ttu-id="7c645-129">Tirando a propriedade do objeto em C++</span><span class="sxs-lookup"><span data-stu-id="7c645-129">Taking Object Ownership in C++</span></span>](taking-object-ownership-in-c--.md)
-   [<span data-ttu-id="7c645-130">Criando uma DACL</span><span class="sxs-lookup"><span data-stu-id="7c645-130">Creating a DACL</span></span>](/windows/desktop/SecBP/creating-a-dacl)

 

 
