---
description: Uma DACL nula concede acesso completo a qualquer usuário que a solicite. Uma DACL vazia é uma DACL corretamente alocada e inicializada que não contém entradas de controle de acesso. Uma DACL vazia não concede acesso ao objeto ao qual está atribuída.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACLs nulas e DACLs vazias (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c06942d7b2d188a74b7e3e307cf60d6740a4251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754129"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a><span data-ttu-id="4b084-105">DACLs nulas e DACLs vazias (autorização)</span><span class="sxs-lookup"><span data-stu-id="4b084-105">Null DACLs and Empty DACLs (Authorization)</span></span>

<span data-ttu-id="4b084-106">Se a DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) que pertence ao [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) de um objeto for definida como **NULL**, uma DACL nula será criada.</span><span class="sxs-lookup"><span data-stu-id="4b084-106">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that belongs to an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly) is set to **NULL**, a null DACL is created.</span></span> <span data-ttu-id="4b084-107">Uma DACL nula concede acesso completo a qualquer usuário que o solicita; a verificação de segurança normal não é executada em relação ao objeto.</span><span class="sxs-lookup"><span data-stu-id="4b084-107">A null DACL grants full access to any user that requests it; normal security checking is not performed with respect to the object.</span></span> <span data-ttu-id="4b084-108">Uma DACL nula não deve ser confundida com uma DACL vazia.</span><span class="sxs-lookup"><span data-stu-id="4b084-108">A null DACL should not be confused with an empty DACL.</span></span> <span data-ttu-id="4b084-109">Uma DACL vazia é uma DACL corretamente alocada e inicializada que não contém ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ).</span><span class="sxs-lookup"><span data-stu-id="4b084-109">An empty DACL is a properly allocated and initialized DACL that contains no [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs).</span></span> <span data-ttu-id="4b084-110">Uma DACL vazia não concede acesso ao objeto ao qual está atribuída.</span><span class="sxs-lookup"><span data-stu-id="4b084-110">An empty DACL grants no access to the object it is assigned to.</span></span>

<span data-ttu-id="4b084-111">Para obter um exemplo de como criar uma DACL, consulte [criando uma DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="4b084-111">For an example of how to create a DACL, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

 
