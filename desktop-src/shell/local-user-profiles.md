---
description: O sistema cria automaticamente um perfil de usuário local para cada usuário quando o usuário faz logon no computador pela primeira vez. O sistema mantém automaticamente as configurações do ambiente de trabalho de cada usuário em um perfil de usuário no computador local.
title: Perfis de usuário local
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba330189b11875198ce40ffdb9dd34925e3adc4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968016"
---
# <a name="local-user-profiles"></a><span data-ttu-id="fad8d-104">Perfis de usuário local</span><span class="sxs-lookup"><span data-stu-id="fad8d-104">Local User Profiles</span></span>

<span data-ttu-id="fad8d-105">A segurança do Windows requer um perfil de usuário para cada conta de usuário em um computador.</span><span class="sxs-lookup"><span data-stu-id="fad8d-105">Windows security requires a user profile for each user account on a computer.</span></span> <span data-ttu-id="fad8d-106">O sistema cria automaticamente um *perfil de usuário local* para cada usuário quando o usuário faz logon no computador pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="fad8d-106">The system automatically creates a *local user profile* for each user when the user logs on to the computer for the first time.</span></span> <span data-ttu-id="fad8d-107">O sistema mantém automaticamente as configurações do ambiente de trabalho de cada usuário em um perfil de usuário no computador local.</span><span class="sxs-lookup"><span data-stu-id="fad8d-107">The system automatically maintains the settings for each user's work environment in a user profile on the local computer.</span></span>

<span data-ttu-id="fad8d-108">Windows Vista e posterior: os perfis de usuário são gerenciados por meio do item do painel de controle de **contas de usuário** .</span><span class="sxs-lookup"><span data-stu-id="fad8d-108">Windows Vista and later: User profiles are managed through the **User Accounts** control panel item.</span></span>

<span data-ttu-id="fad8d-109">Windows 2000 e Windows XP: para copiar ou excluir um perfil de usuário, selecione **sistema** no painel de controle, a guia **avançado** e, em seguida, o botão **configurações** na área **perfil do usuário** .</span><span class="sxs-lookup"><span data-stu-id="fad8d-109">Windows 2000 and Windows XP: To copy or delete a user profile, select **System** from the Control Panel, then the **Advanced** tab, and then the **Settings** button in the **User Profile** area.</span></span>

<span data-ttu-id="fad8d-110">O perfil do usuário não é carregado automaticamente quando o usuário faz logon usando a função [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) .</span><span class="sxs-lookup"><span data-stu-id="fad8d-110">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="fad8d-111">Para carregar um perfil de usuário programaticamente, use a função [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="fad8d-111">To load a user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="fad8d-112">Para descarregar um perfil de usuário carregado pelo **LoadUserProfile**, chame a função [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .</span><span class="sxs-lookup"><span data-stu-id="fad8d-112">To unload a user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
