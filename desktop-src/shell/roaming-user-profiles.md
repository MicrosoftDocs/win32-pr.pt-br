---
description: Se um computador estiver executando o Windows 2000 Server ou posterior em uma rede, os usuários poderão armazenar seus perfis no servidor. Esses perfis são chamados de perfis de usuário de roaming.
title: Perfis de usuário em roaming
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967997"
---
# <a name="roaming-user-profiles"></a><span data-ttu-id="e51b5-104">Perfis de usuário em roaming</span><span class="sxs-lookup"><span data-stu-id="e51b5-104">Roaming User Profiles</span></span>

<span data-ttu-id="e51b5-105">Se um computador estiver executando o Windows 2000 Server ou posterior em uma rede, os usuários poderão armazenar seus perfis no servidor.</span><span class="sxs-lookup"><span data-stu-id="e51b5-105">If a computer is running Windows 2000 Server or later on a network, users can store their profiles on the server.</span></span> <span data-ttu-id="e51b5-106">Esses perfis são chamados de *perfis de usuário de roaming*.</span><span class="sxs-lookup"><span data-stu-id="e51b5-106">These profiles are called *roaming user profiles*.</span></span>

<span data-ttu-id="e51b5-107">Os perfis de usuário de roaming têm as seguintes vantagens:</span><span class="sxs-lookup"><span data-stu-id="e51b5-107">Roaming user profiles have the following advantages:</span></span>

-   <span data-ttu-id="e51b5-108">Disponibilidade automática de recursos.</span><span class="sxs-lookup"><span data-stu-id="e51b5-108">Automatic resource availability.</span></span> <span data-ttu-id="e51b5-109">O perfil exclusivo de um usuário fica automaticamente disponível quando ele faz logon em qualquer computador na rede.</span><span class="sxs-lookup"><span data-stu-id="e51b5-109">A user's unique profile is automatically available when he or she logs on to any computer on the network.</span></span> <span data-ttu-id="e51b5-110">Os usuários não precisam criar um perfil em cada computador que usam em uma rede.</span><span class="sxs-lookup"><span data-stu-id="e51b5-110">Users do not need to create a profile on each computer they use on a network.</span></span>
-   <span data-ttu-id="e51b5-111">Substituição e backup simplificados do computador.</span><span class="sxs-lookup"><span data-stu-id="e51b5-111">Simplified computer replacement and backup.</span></span> <span data-ttu-id="e51b5-112">Quando o computador de um usuário deve ser substituído, ele pode ser substituído facilmente, pois todas as informações de perfil do usuário são mantidas separadamente na rede, independentemente de um computador individual.</span><span class="sxs-lookup"><span data-stu-id="e51b5-112">When a user's computer must be replaced, it can be replaced easily because all of the user's profile information is maintained separately on the network, independent of an individual computer.</span></span> <span data-ttu-id="e51b5-113">Quando o usuário faz logon no novo computador pela primeira vez, a cópia de servidor do perfil do usuário é copiada para o novo computador.</span><span class="sxs-lookup"><span data-stu-id="e51b5-113">When the user logs on to the new computer for the first time, the server copy of the user's profile is copied to the new computer.</span></span>

<span data-ttu-id="e51b5-114">O perfil do usuário não é carregado automaticamente quando o usuário faz logon usando a função [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) .</span><span class="sxs-lookup"><span data-stu-id="e51b5-114">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="e51b5-115">Para carregar um perfil de usuário móvel programaticamente, use a função [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="e51b5-115">To load a roaming user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="e51b5-116">Para descarregar um perfil de usuário móvel carregado por **LoadUserProfile**, chame a função [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .</span><span class="sxs-lookup"><span data-stu-id="e51b5-116">To unload a roaming user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
