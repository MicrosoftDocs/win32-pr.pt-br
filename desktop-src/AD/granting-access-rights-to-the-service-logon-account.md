---
title: Concedendo direitos de acesso à conta de logon do serviço
description: Uma consideração principal da instalação de uma instância de serviço é garantir que o serviço instalado possa acessar os recursos necessários.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Concedendo direitos de acesso ao AD da conta de logon do serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105769120"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a><span data-ttu-id="cabe8-104">Concedendo direitos de acesso à conta de logon do serviço</span><span class="sxs-lookup"><span data-stu-id="cabe8-104">Granting Access Rights to the Service Logon Account</span></span>

<span data-ttu-id="cabe8-105">Uma consideração principal da instalação de uma instância de serviço é garantir que o serviço instalado possa acessar os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="cabe8-105">A primary consideration of installing a service instance is to ensure that the installed service can access the necessary resources.</span></span> <span data-ttu-id="cabe8-106">Para fazer isso, defina ACEs nos descritores de segurança de objetos que o serviço deve acessar.</span><span class="sxs-lookup"><span data-stu-id="cabe8-106">To do this, set ACEs in the security descriptors of objects that the service must access.</span></span> <span data-ttu-id="cabe8-107">Uma ACE pode conceder ou negar direitos de acesso a uma entidade de segurança especificada, como a conta de usuário de serviço ou a conta de computador para um serviço LocalSystem ou um grupo ao qual a conta do serviço pertence.</span><span class="sxs-lookup"><span data-stu-id="cabe8-107">An ACE can grant or deny access rights to a specified security principal, such as the service user account, or the computer account for a LocalSystem service, or a group to which the service's account belongs.</span></span> <span data-ttu-id="cabe8-108">Para obter mais informações sobre ACEs, descritores de segurança e controle de acesso, consulte [controlando o acesso a objetos no Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) e [controle de acesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="cabe8-108">For more information about ACEs, security descriptors, and access control, see [Controlling Access to objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="cabe8-109">Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE que permite ao serviço modificar seu ponto de conexão de serviço, consulte [habilitando a conta de serviço para acessar as propriedades do SCP](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="cabe8-109">For more information and a code example that can be used to set an ACE that enables the service to modify its service connection point, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>

<span data-ttu-id="cabe8-110">Em alguns casos, você deve adicionar sua conta de usuário de serviço como um membro de um ou mais grupos de segurança.</span><span class="sxs-lookup"><span data-stu-id="cabe8-110">In some cases, you must add your service user account as a member of one or more security groups.</span></span> <span data-ttu-id="cabe8-111">Por exemplo, se você criar um grupo de administradores para seu serviço, poderá fazer com que o serviço seja um membro do grupo.</span><span class="sxs-lookup"><span data-stu-id="cabe8-111">For example, if you create an administrators group for your service, you might make the service a member of the group.</span></span> <span data-ttu-id="cabe8-112">Você pode conceder direitos de acesso ao grupo em vez de concedê-los explicitamente para a conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="cabe8-112">You can then grant access rights to the group rather than granting them explicitly to the service account.</span></span> <span data-ttu-id="cabe8-113">Para obter mais informações sobre grupos de segurança, consulte [Managing groups](managing-groups.md).</span><span class="sxs-lookup"><span data-stu-id="cabe8-113">For more information about security groups, see [Managing Groups](managing-groups.md).</span></span>

 

 