---
description: Filtros de senha
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtros de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171666"
---
# <a name="password-filters"></a><span data-ttu-id="15864-103">Filtros de senha</span><span class="sxs-lookup"><span data-stu-id="15864-103">Password Filters</span></span>

<span data-ttu-id="15864-104">Os filtros de senha fornecem uma maneira de implementar a política de senha e a notificação de alteração.</span><span class="sxs-lookup"><span data-stu-id="15864-104">Password filters provide a way for you to implement password policy and change notification.</span></span>

<span data-ttu-id="15864-105">Quando uma solicitação de alteração de senha é feita, a [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) chama os filtros de senha registrados no sistema.</span><span class="sxs-lookup"><span data-stu-id="15864-105">When a password change request is made, the [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) calls the password filters registered on the system.</span></span> <span data-ttu-id="15864-106">Cada filtro de senha é chamado duas vezes: primeiro para validar a nova senha e, depois que todos os filtros tiverem validado a nova senha, para notificar os filtros de que a alteração foi feita.</span><span class="sxs-lookup"><span data-stu-id="15864-106">Each password filter is called twice: first to validate the new password and then, after all filters have validated the new password, to notify the filters that the change has been made.</span></span> <span data-ttu-id="15864-107">A ilustração a seguir mostra este processo.</span><span class="sxs-lookup"><span data-stu-id="15864-107">The following illustration shows this process.</span></span>

![solicitação de alteração de senha](images/pswdfilte.png)

<span data-ttu-id="15864-109">A notificação de alteração de senha é usada para sincronizar as alterações de senha para bancos de dados de conta externa.</span><span class="sxs-lookup"><span data-stu-id="15864-109">Password change notification is used to synchronize password changes to foreign account databases.</span></span>

<span data-ttu-id="15864-110">Os filtros de senha são usados para impor a política de senha.</span><span class="sxs-lookup"><span data-stu-id="15864-110">Password filters are used to enforce password policy.</span></span> <span data-ttu-id="15864-111">Os filtros validam novas senhas e indicam se a nova senha está em conformidade com a política de senha implementada.</span><span class="sxs-lookup"><span data-stu-id="15864-111">Filters validate new passwords and indicate whether the new password conforms to the implemented password policy.</span></span>

<span data-ttu-id="15864-112">Para obter uma visão geral do uso de filtros de senha, consulte [usando filtros de senha](using-password-filters.md).</span><span class="sxs-lookup"><span data-stu-id="15864-112">For an overview of using password filters, see [Using Password Filters](using-password-filters.md).</span></span>

<span data-ttu-id="15864-113">Para obter uma lista de funções de filtro de senha, consulte [funções de filtro de senha](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="15864-113">For a list of password filter functions, see [Password Filter Functions](management-functions.md).</span></span>

<span data-ttu-id="15864-114">Os tópicos a seguir fornecem mais informações sobre filtros de senha:</span><span class="sxs-lookup"><span data-stu-id="15864-114">The following topics provide more information about password filters:</span></span>

-   [<span data-ttu-id="15864-115">Considerações sobre programação de filtro de senha</span><span class="sxs-lookup"><span data-stu-id="15864-115">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
-   [<span data-ttu-id="15864-116">Imposição de senha forte e Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="15864-116">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)

 

 
