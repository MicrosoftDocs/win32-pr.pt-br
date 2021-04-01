---
description: Em uma verificação de acesso, o sistema compara as informações de segurança no token de acesso de threads com relação às informações de segurança no descritor de segurança de objetos.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interação entre threads e objetos protegíveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829734"
---
# <a name="interaction-between-threads-and-securable-objects"></a><span data-ttu-id="8a2e6-103">Interação entre threads e objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="8a2e6-103">Interaction Between Threads and Securable Objects</span></span>

<span data-ttu-id="8a2e6-104">Quando um thread tenta usar um [objeto protegível](securable-objects.md), o sistema executa uma verificação de acesso antes de permitir que o thread prossiga.</span><span class="sxs-lookup"><span data-stu-id="8a2e6-104">When a thread attempts to use a [securable object](securable-objects.md), the system performs an access check before allowing the thread to proceed.</span></span> <span data-ttu-id="8a2e6-105">Em uma verificação de acesso, o sistema compara as informações de segurança no [*token de acesso*](/windows/desktop/SecGloss/a-gly) do thread com as informações de segurança no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)do objeto.</span><span class="sxs-lookup"><span data-stu-id="8a2e6-105">In an access check, the system compares the security information in the thread's [*access token*](/windows/desktop/SecGloss/a-gly) against the security information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

-   <span data-ttu-id="8a2e6-106">O token de acesso contém SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) que identificam o usuário associado ao thread.</span><span class="sxs-lookup"><span data-stu-id="8a2e6-106">The access token contains [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that identify the user associated with the thread.</span></span>
-   <span data-ttu-id="8a2e6-107">O descritor de segurança identifica o proprietário do objeto e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ).</span><span class="sxs-lookup"><span data-stu-id="8a2e6-107">The security descriptor identifies the object's owner and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL).</span></span> <span data-ttu-id="8a2e6-108">A DACL contém ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ), cada uma delas especificando os direitos de acesso permitidos ou negados a um usuário ou grupo específico.</span><span class="sxs-lookup"><span data-stu-id="8a2e6-108">The DACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), each of which specify the access rights allowed or denied to a specific user or group.</span></span>

<span data-ttu-id="8a2e6-109">O sistema verifica a DACL do objeto, procurando ACEs que se aplicam aos SIDs de usuário e grupo do token de acesso do thread.</span><span class="sxs-lookup"><span data-stu-id="8a2e6-109">The system checks the object's DACL, looking for ACEs that apply to the user and group SIDs from the thread's access token.</span></span> <span data-ttu-id="8a2e6-110">O sistema verifica cada ACE até que o acesso seja concedido ou negado ou até que não haja mais ACEs a serem verificadas.</span><span class="sxs-lookup"><span data-stu-id="8a2e6-110">The system checks each ACE until access is either granted or denied or until there are no more ACEs to check.</span></span> <span data-ttu-id="8a2e6-111">Concebível, uma ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) pode ter várias ACEs que se aplicam aos SIDs do token.</span><span class="sxs-lookup"><span data-stu-id="8a2e6-111">Conceivably, an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) could have several ACEs that apply to the token's SIDs.</span></span> <span data-ttu-id="8a2e6-112">E, se isso ocorrer, os direitos de acesso concedidos por cada ACE se acumulam.</span><span class="sxs-lookup"><span data-stu-id="8a2e6-112">And, if this occurs, the access rights granted by each ACE accumulate.</span></span> <span data-ttu-id="8a2e6-113">Por exemplo, se uma ACE conceder acesso de leitura a um grupo e outra ACE conceder acesso de gravação a um usuário que seja membro do grupo, o usuário poderá ter acesso de leitura e gravação ao objeto.</span><span class="sxs-lookup"><span data-stu-id="8a2e6-113">For example, if one ACE grants read access to a group and another ACE grants write access to a user who is a member of the group, the user can have both read and write access to the object.</span></span>

<span data-ttu-id="8a2e6-114">A ilustração a seguir mostra a relação entre esses blocos de informações de segurança:</span><span class="sxs-lookup"><span data-stu-id="8a2e6-114">The following illustration shows the relationship between these blocks of security information:</span></span>

![relações entre processos, Aces e DACLs](images/cssec-02.png)

 

 
