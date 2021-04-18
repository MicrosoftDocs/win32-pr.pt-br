---
description: Algumas funções exigem privilégios especiais para serem executadas corretamente.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Executando com privilégios especiais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762910"
---
# <a name="running-with-special-privileges"></a><span data-ttu-id="f6dd5-103">Executando com privilégios especiais</span><span class="sxs-lookup"><span data-stu-id="f6dd5-103">Running with Special Privileges</span></span>

<span data-ttu-id="f6dd5-104">Algumas funções exigem [privilégios](/windows/desktop/SecAuthZ/privileges) especiais para serem executadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-104">Some functions require special [privileges](/windows/desktop/SecAuthZ/privileges) to run correctly.</span></span> <span data-ttu-id="f6dd5-105">Em alguns casos, a função só pode ser executada por determinados usuários ou por membros de determinados grupos.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-105">In some cases, the function can only be run by certain users or by members of certain groups.</span></span> <span data-ttu-id="f6dd5-106">O requisito mais comum é que o usuário seja um administrador local.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-106">The most common requirement is that the user be a local administrator.</span></span> <span data-ttu-id="f6dd5-107">Outras funções exigem que a conta do usuário tenha privilégios específicos habilitados.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-107">Other functions require the user's account to have specific privileges enabled.</span></span>

<span data-ttu-id="f6dd5-108">Para reduzir a possibilidade de código não autorizado ser capaz de obter controle, o sistema deve ser executado com o privilégio mínimo necessário.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-108">To reduce the possibility of unauthorized code being able to get control, the system should run with the least privilege necessary.</span></span> <span data-ttu-id="f6dd5-109">Os aplicativos que precisam chamar funções que exigem privilégios especiais podem deixar o sistema aberto para atacar por hackers.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-109">Applications that need to call functions that require special privileges can leave the system open to attack by hackers.</span></span> <span data-ttu-id="f6dd5-110">Esses aplicativos devem ser projetados para serem executados por curto período de tempo e devem informar o usuário das implicações de segurança envolvidas.</span><span class="sxs-lookup"><span data-stu-id="f6dd5-110">Such applications should be designed to run for short periods of time and should inform the user of the security implications involved.</span></span>

<span data-ttu-id="f6dd5-111">Para obter informações sobre como executar o como usuários diferentes e como habilitar privilégios em seu aplicativo, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="f6dd5-111">For information about how to run as different users and how to enable privileges in your application, see the following topics:</span></span><dl>

[<span data-ttu-id="f6dd5-112">Executando com privilégios de administrador</span><span class="sxs-lookup"><span data-stu-id="f6dd5-112">Running with Administrator Privileges</span></span>](running-with-administrator-privileges.md)  
[<span data-ttu-id="f6dd5-113">Solicitando credenciais ao usuário</span><span class="sxs-lookup"><span data-stu-id="f6dd5-113">Asking the User for Credentials</span></span>](asking-the-user-for-credentials.md)  
[<span data-ttu-id="f6dd5-114">Alterando privilégios em um token</span><span class="sxs-lookup"><span data-stu-id="f6dd5-114">Changing Privileges in a Token</span></span>](changing-privileges-in-a-token.md)  
[<span data-ttu-id="f6dd5-115">Atribuindo privilégios a uma conta</span><span class="sxs-lookup"><span data-stu-id="f6dd5-115">Assigning Privileges to an Account</span></span>](assigning-privileges-to-an-account.md)  
</dl>

 

 
