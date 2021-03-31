---
title: Como a segurança afeta as operações no Active Directory Domain Services
description: Active Directory Domain Services usar o controle de acesso para conceder ou negar acesso a objetos, propriedades e operações com base na identidade do usuário que está executando a tentativa de acesso.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Efeitos de segurança em Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be628acd1709985aeaa9539bfa527de674732ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822271"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a><span data-ttu-id="6d316-104">Como a segurança afeta as operações no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="6d316-104">How Security Affects Operations in Active Directory Domain Services</span></span>

<span data-ttu-id="6d316-105">Active Directory Domain Services usar o controle de acesso para conceder ou negar acesso a objetos, propriedades e operações com base na identidade do usuário que está executando a tentativa de acesso.</span><span class="sxs-lookup"><span data-stu-id="6d316-105">Active Directory Domain Services use access control to grant or deny access to objects, properties, and operations based on the identity of the user performing the access attempt.</span></span> <span data-ttu-id="6d316-106">Quando seu aplicativo é associado ao diretório, ele é associado a credenciais de usuário específicas.</span><span class="sxs-lookup"><span data-stu-id="6d316-106">When your application binds to the directory, it binds with specific user credentials.</span></span> <span data-ttu-id="6d316-107">Quando autenticado, essas credenciais determinam o contexto de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6d316-107">When authenticated, these credentials determine your application's security context.</span></span> <span data-ttu-id="6d316-108">Independentemente de as credenciais serem aquelas do usuário conectado, um usuário especificado, uma conta de serviço, uma conta de computador ou um usuário não autenticado (convidado/todos), o servidor de Active Directory verifica o direito do usuário de acessar um objeto antes que qualquer operação seja executada nesse objeto.</span><span class="sxs-lookup"><span data-stu-id="6d316-108">Regardless of whether the credentials are those of the logged-on user, a specified user, a service account, a computer account, or an unauthenticated user (Guest/Everyone), the Active Directory server verifies the user's right to access an object before any operation is performed on that object.</span></span> <span data-ttu-id="6d316-109">O usuário pode, ou não, ter acesso a um objeto específico, seus filhos, suas propriedades ou operações nesse objeto, o que significa que seu aplicativo deve lidar com os possíveis erros causados pelo acesso negado.</span><span class="sxs-lookup"><span data-stu-id="6d316-109">The user may, or may not, have access to a particular object, its children, its properties, or operations on that object, which means that your application must handle the potential errors caused by denied access.</span></span>

<span data-ttu-id="6d316-110">Para obter mais informações sobre contextos de segurança e os efeitos do controle de acesso em várias operações, consulte:</span><span class="sxs-lookup"><span data-stu-id="6d316-110">For more information about security contexts and the effects of access control on various operations, see:</span></span>

-   [<span data-ttu-id="6d316-111">Controle de acesso e operações de leitura</span><span class="sxs-lookup"><span data-stu-id="6d316-111">Access Control and Read Operations</span></span>](access-control-and-read-operations.md)
-   [<span data-ttu-id="6d316-112">Controle de acesso e operações de gravação</span><span class="sxs-lookup"><span data-stu-id="6d316-112">Access Control and Write Operations</span></span>](access-control-and-write-operations.md)
-   [<span data-ttu-id="6d316-113">Controle de acesso e criação de objeto</span><span class="sxs-lookup"><span data-stu-id="6d316-113">Access Control and Object Creation</span></span>](access-control-and-object-creation.md)
-   [<span data-ttu-id="6d316-114">Exclusão de controle de acesso e objeto</span><span class="sxs-lookup"><span data-stu-id="6d316-114">Access Control and Object Deletion</span></span>](access-control-and-object-deletion.md)

 

 




