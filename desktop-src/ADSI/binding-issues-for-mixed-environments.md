---
title: Problemas de associação para ambientes mistos
description: Problemas de associação para ambientes mistos
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usando, problemas de associação para ambientes mistos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105756461"
---
# <a name="binding-issues-for-mixed-environments"></a><span data-ttu-id="ee9b1-104">Problemas de associação para ambientes mistos</span><span class="sxs-lookup"><span data-stu-id="ee9b1-104">Binding Issues for Mixed Environments</span></span>

<span data-ttu-id="ee9b1-105">Para ambientes nos quais o domínio que contém Active Directory tem uma relação de confiança com um domínio do Windows NT 4,0, pode haver um problema ao usar a associação sem servidor para associar a objetos Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ee9b1-105">For environments in which the domain that contains Active Directory has a trust relationship with a Windows NT 4.0 domain, there may be a problem with using serverless binding to bind to Active Directory objects.</span></span>

<span data-ttu-id="ee9b1-106">Em alguns ambientes de rede, as relações de confiança foram configuradas entre controladores de domínio que contêm Active Directory e servidores Windows NT 4,0 com a finalidade de permitir a autenticação entre domínios.</span><span class="sxs-lookup"><span data-stu-id="ee9b1-106">In some networking environments, trust relationships have been set up between domain controllers that contain Active Directory and Windows NT 4.0 servers for the purpose of allowing authentication between domains.</span></span> <span data-ttu-id="ee9b1-107">Nesses ambientes mistos, se um usuário, que é membro do Windows NT 4,0, o domínio tenta usar a associação sem servidor para se associar a um objeto de Active Directory em um domínio confiável, a ligação falhará e um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="ee9b1-107">In these mixed environments, if a user, who is a member of the Windows NT 4.0, domain attempts to use serverless binding to bind to an Active Directory object on a trusted domain, then the bind will fail and an error is returned.</span></span> <span data-ttu-id="ee9b1-108">Isso ocorre porque uma ligação sem servidor usa a função [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) para associar ao objeto em Active Directory, que depende do DNS adequado.</span><span class="sxs-lookup"><span data-stu-id="ee9b1-108">This is because a serverless bind uses the [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) function to bind to the object in Active Directory, which is dependent upon the proper DNS.</span></span>

<span data-ttu-id="ee9b1-109">Nesse cenário, o usuário do Windows NT deve fornecer o nome de um domínio específico ao qual associar.</span><span class="sxs-lookup"><span data-stu-id="ee9b1-109">In this scenario, the Windows NT user must provide the name of a specific domain to bind to.</span></span> <span data-ttu-id="ee9b1-110">A seguir, é mostrado um exemplo.</span><span class="sxs-lookup"><span data-stu-id="ee9b1-110">The following is an example.</span></span>

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 