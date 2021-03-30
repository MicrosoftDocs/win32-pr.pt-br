---
description: Assim como o sistema usa descritores de segurança para controlar o acesso a objetos protegíveis, um servidor pode usar descritores de segurança para controlar o acesso a seus objetos privados. Para obter mais informações sobre o modelo de segurança do Windows, consulte modelo de controle de acesso.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Controle de acesso baseado em ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662052"
---
# <a name="acl-based-access-control"></a><span data-ttu-id="cdb10-104">Controle de acesso baseado em ACL</span><span class="sxs-lookup"><span data-stu-id="cdb10-104">ACL-based Access Control</span></span>

<span data-ttu-id="cdb10-105">Assim como o sistema usa [descritores de segurança](security-descriptors.md) para controlar o acesso a objetos protegíveis, um servidor pode usar descritores de segurança para controlar o acesso a seus objetos privados.</span><span class="sxs-lookup"><span data-stu-id="cdb10-105">Just as the system uses [security descriptors](security-descriptors.md) to control access to securable objects, a server can use security descriptors to control access to its private objects.</span></span> <span data-ttu-id="cdb10-106">Para obter mais informações sobre o modelo de segurança do Windows, consulte [modelo de controle de acesso](access-control-model.md).</span><span class="sxs-lookup"><span data-stu-id="cdb10-106">For more information about the Windows security model, see [Access Control Model](access-control-model.md).</span></span>

<span data-ttu-id="cdb10-107">Um servidor protegido pode [criar um descritor de segurança](security-descriptors-for-private-objects.md) com uma DACL que especifica os tipos de acesso permitidos para vários dos [confiáveis](trustees.md).</span><span class="sxs-lookup"><span data-stu-id="cdb10-107">A protected server can [create a security descriptor](security-descriptors-for-private-objects.md) with a DACL that specifies the types of access allowed for various [trustees](trustees.md).</span></span> <span data-ttu-id="cdb10-108">Em um caso simples, o servidor pode criar um único descritor de segurança para [controlar o acesso a todos os dados e funcionalidades do servidor](checking-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="cdb10-108">In a simple case, the server could create a single security descriptor to [control access to all of the server's data and functionality](checking-access-to-private-objects.md).</span></span> <span data-ttu-id="cdb10-109">Para uma granularidade mais refinada de proteção, o servidor pode criar descritores de segurança para cada um de seus objetos privados ou para diferentes tipos de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="cdb10-109">For a finer granularity of protection, the server could create security descriptors for each of its private objects, or for different types of functionality.</span></span>

<span data-ttu-id="cdb10-110">Por exemplo, quando um cliente solicita que o servidor crie um novo objeto em um banco de dados, o servidor pode criar um descritor de segurança para o novo objeto privado.</span><span class="sxs-lookup"><span data-stu-id="cdb10-110">For example, when a client asks the server to create a new object in a database, the server could create a security descriptor for the new private object.</span></span> <span data-ttu-id="cdb10-111">O servidor poderia então armazenar o descritor de segurança com o objeto particular no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cdb10-111">The server could then store the security descriptor with the private object in the database.</span></span> <span data-ttu-id="cdb10-112">Quando um cliente tenta acessar o objeto, o servidor recupera o descritor de segurança para verificar os direitos de acesso do cliente.</span><span class="sxs-lookup"><span data-stu-id="cdb10-112">When a client tries to access the object, the server retrieves the security descriptor to check the client's access rights.</span></span> <span data-ttu-id="cdb10-113">É importante observar que não há nada em um descritor de segurança que o associe com o objeto ou a funcionalidade que ele está protegendo.</span><span class="sxs-lookup"><span data-stu-id="cdb10-113">It is important to note that there is nothing in a security descriptor that associates it with the object or functionality it is protecting.</span></span> <span data-ttu-id="cdb10-114">Em vez disso, cabe ao servidor protegido manter a associação.</span><span class="sxs-lookup"><span data-stu-id="cdb10-114">Instead, it is up to the protected server to maintain the association.</span></span>

<span data-ttu-id="cdb10-115">O acesso ao objeto particular também pode ser auditado.</span><span class="sxs-lookup"><span data-stu-id="cdb10-115">Access to the private object can also be audited.</span></span> <span data-ttu-id="cdb10-116">Consulte [auditoria de acesso a objetos privados](auditing-access-to-private-objects.md) para obter uma descrição disso.</span><span class="sxs-lookup"><span data-stu-id="cdb10-116">Refer to [Auditing Access to Private Objects](auditing-access-to-private-objects.md) for a description of this.</span></span>

 

 



