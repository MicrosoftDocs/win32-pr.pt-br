---
description: Os seguintes elementos de API são usados com perfis de usuário.
title: Referência de perfis de usuário
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5d4c4f585eda66674059f402dbd73f106a3e4f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968190"
---
# <a name="user-profiles-reference"></a><span data-ttu-id="11b22-103">Referência de perfis de usuário</span><span class="sxs-lookup"><span data-stu-id="11b22-103">User Profiles Reference</span></span>

<span data-ttu-id="11b22-104">Os seguintes elementos de API são usados com perfis de usuário.</span><span class="sxs-lookup"><span data-stu-id="11b22-104">The following API elements are used with user profiles.</span></span>

## <a name="functions"></a><span data-ttu-id="11b22-105">Funções</span><span class="sxs-lookup"><span data-stu-id="11b22-105">Functions</span></span>



| <span data-ttu-id="11b22-106">Função</span><span class="sxs-lookup"><span data-stu-id="11b22-106">Function</span></span>                                                                   | <span data-ttu-id="11b22-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="11b22-107">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11b22-108">**CreateEnvironmentBlock**</span><span class="sxs-lookup"><span data-stu-id="11b22-108">**CreateEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | <span data-ttu-id="11b22-109">Recupera as variáveis de ambiente para o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="11b22-109">Retrieves the environment variables for the specified user.</span></span>                                                   |
| [<span data-ttu-id="11b22-110">**CreateProfile**</span><span class="sxs-lookup"><span data-stu-id="11b22-110">**CreateProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | <span data-ttu-id="11b22-111">Cria um novo perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="11b22-111">Creates a new user profile.</span></span> <span data-ttu-id="11b22-112">(Somente Windows Vista e posterior.)</span><span class="sxs-lookup"><span data-stu-id="11b22-112">(Windows Vista and later only.)</span></span>                                                   |
| [<span data-ttu-id="11b22-113">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="11b22-113">**DeleteProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | <span data-ttu-id="11b22-114">Exclui o perfil do usuário e todas as configurações relacionadas ao usuário do computador especificado.</span><span class="sxs-lookup"><span data-stu-id="11b22-114">Deletes the user profile and all user-related settings from the specified computer.</span></span>                           |
| [<span data-ttu-id="11b22-115">**DestroyEnvironmentBlock**</span><span class="sxs-lookup"><span data-stu-id="11b22-115">**DestroyEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | <span data-ttu-id="11b22-116">Libera as variáveis de ambiente criadas pela função [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) .</span><span class="sxs-lookup"><span data-stu-id="11b22-116">Frees environment variables created by the [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) function.</span></span> |
| [<span data-ttu-id="11b22-117">**ExpandEnvironmentStringsForUser**</span><span class="sxs-lookup"><span data-stu-id="11b22-117">**ExpandEnvironmentStringsForUser**</span></span>](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | <span data-ttu-id="11b22-118">Expande a cadeia de caracteres de origem usando o bloco de ambiente estabelecido para o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="11b22-118">Expands the source string by using the environment block established for the specified user.</span></span>                  |
| [<span data-ttu-id="11b22-119">**GetAllUsersProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="11b22-119">**GetAllUsersProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | <span data-ttu-id="11b22-120">Recupera o caminho para a raiz do perfil todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="11b22-120">Retrieves the path to the root of the All Users profile.</span></span>                                                      |
| [<span data-ttu-id="11b22-121">**GetDefaultUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="11b22-121">**GetDefaultUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | <span data-ttu-id="11b22-122">Recupera o caminho para a raiz do perfil de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="11b22-122">Retrieves the path to the root of the Default User profile.</span></span>                                                   |
| [<span data-ttu-id="11b22-123">**GetProfilesDirectory**</span><span class="sxs-lookup"><span data-stu-id="11b22-123">**GetProfilesDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | <span data-ttu-id="11b22-124">Recupera o caminho para o diretório raiz onde todos os perfis de usuário são armazenados.</span><span class="sxs-lookup"><span data-stu-id="11b22-124">Retrieves the path to the root directory where all user profiles are stored.</span></span>                                  |
| [<span data-ttu-id="11b22-125">**Getprofiletype**</span><span class="sxs-lookup"><span data-stu-id="11b22-125">**GetProfileType**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | <span data-ttu-id="11b22-126">Recupera o tipo de perfil carregado para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="11b22-126">Retrieves the type of profile loaded for the current user.</span></span>                                                    |
| [<span data-ttu-id="11b22-127">**GetUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="11b22-127">**GetUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | <span data-ttu-id="11b22-128">Recupera o caminho para o diretório raiz do perfil do usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="11b22-128">Retrieves the path to the root directory of the specified user's profile.</span></span>                                     |
| [<span data-ttu-id="11b22-129">**LoadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="11b22-129">**LoadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | <span data-ttu-id="11b22-130">Carrega o perfil do usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="11b22-130">Loads the specified user's profile.</span></span>                                                                           |
| [<span data-ttu-id="11b22-131">**UnloadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="11b22-131">**UnloadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | <span data-ttu-id="11b22-132">Descarrega o perfil de um usuário que foi carregado pela função [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="11b22-132">Unloads a user's profile that was loaded by the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span>          |



 

<span data-ttu-id="11b22-133">Não há suporte para a função [**CreateUserProfileEx**](createuserprofileex.md) .</span><span class="sxs-lookup"><span data-stu-id="11b22-133">The [**CreateUserProfileEx**](createuserprofileex.md) function is not supported.</span></span>

## <a name="structures"></a><span data-ttu-id="11b22-134">Estruturas</span><span class="sxs-lookup"><span data-stu-id="11b22-134">Structures</span></span>



| <span data-ttu-id="11b22-135">Estrutura</span><span class="sxs-lookup"><span data-stu-id="11b22-135">Structure</span></span>                          | <span data-ttu-id="11b22-136">Description</span><span class="sxs-lookup"><span data-stu-id="11b22-136">Description</span></span>                                |
|------------------------------------|--------------------------------------------|
| [<span data-ttu-id="11b22-137">**PROFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="11b22-137">**PROFILEINFO**</span></span>](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | <span data-ttu-id="11b22-138">Contém informações sobre um perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="11b22-138">Contains information about a user profile.</span></span> |



 

 

 



