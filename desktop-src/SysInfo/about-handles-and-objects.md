---
description: O sistema usa objetos e identificadores para regular o acesso aos recursos do sistema por dois motivos principais.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Sobre identificadores e objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921834"
---
# <a name="about-handles-and-objects"></a><span data-ttu-id="b9530-103">Sobre identificadores e objetos</span><span class="sxs-lookup"><span data-stu-id="b9530-103">About Handles and Objects</span></span>

<span data-ttu-id="b9530-104">O sistema usa objetos e identificadores para regular o acesso aos recursos do sistema por dois motivos principais.</span><span class="sxs-lookup"><span data-stu-id="b9530-104">The system uses objects and handles to regulate access to system resources for two main reasons.</span></span> <span data-ttu-id="b9530-105">Primeiro, o uso de objetos garante que a Microsoft possa atualizar a funcionalidade do sistema, desde que a interface do objeto original seja mantida.</span><span class="sxs-lookup"><span data-stu-id="b9530-105">First, the use of objects ensures that Microsoft can update system functionality, as long as the original object interface is maintained.</span></span> <span data-ttu-id="b9530-106">Quando as versões subsequentes do sistema são liberadas, você pode usar o objeto atualizado com pouco ou nenhum trabalho adicional.</span><span class="sxs-lookup"><span data-stu-id="b9530-106">When subsequent versions of the system are released, you can use the updated object with little or no additional work.</span></span>

<span data-ttu-id="b9530-107">Em segundo lugar, o uso de objetos permite que você aproveite a segurança do Windows.</span><span class="sxs-lookup"><span data-stu-id="b9530-107">Secondly, the use of objects enables you to take advantage of Windows security.</span></span> <span data-ttu-id="b9530-108">Cada objeto tem sua própria lista de controle de acesso (ACL) que especifica as ações que um processo pode executar no objeto.</span><span class="sxs-lookup"><span data-stu-id="b9530-108">Each object has its own access-control list (ACL) that specifies the actions a process can perform on the object.</span></span> <span data-ttu-id="b9530-109">O sistema examina a ACL de um objeto cada vez que um aplicativo cria um identificador para o objeto.</span><span class="sxs-lookup"><span data-stu-id="b9530-109">The system examines an object's ACL each time an application creates a handle to the object.</span></span> <span data-ttu-id="b9530-110">Para mais informações, consulte [Controle de acesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="b9530-110">For more information, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

-   [<span data-ttu-id="b9530-111">Gerenciador de objetos</span><span class="sxs-lookup"><span data-stu-id="b9530-111">Object Manager</span></span>](object-manager.md)
-   [<span data-ttu-id="b9530-112">Interface de objeto</span><span class="sxs-lookup"><span data-stu-id="b9530-112">Object Interface</span></span>](object-interface.md)
-   [<span data-ttu-id="b9530-113">Namespaces de objeto</span><span class="sxs-lookup"><span data-stu-id="b9530-113">Object Namespaces</span></span>](/windows/desktop/Sync/object-namespaces)
-   [<span data-ttu-id="b9530-114">Limitações de identificador</span><span class="sxs-lookup"><span data-stu-id="b9530-114">Handle Limitations</span></span>](handle-limitations.md)
-   [<span data-ttu-id="b9530-115">Manipular herança</span><span class="sxs-lookup"><span data-stu-id="b9530-115">Handle Inheritance</span></span>](handle-inheritance.md)

 

 
