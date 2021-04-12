---
title: Para carregar um perfil do sistema
description: Para carregar um perfil do sistema
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- perfis, sistema
- perfis de sistema, carregando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e745cb2fed32d650a22febef827ed7662f4448
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365570"
---
# <a name="to-load-a-system-profile"></a><span data-ttu-id="6263d-105">Para carregar um perfil do sistema</span><span class="sxs-lookup"><span data-stu-id="6263d-105">To Load a System Profile</span></span>

<span data-ttu-id="6263d-106">Para fazer alterações em um perfil de sistema, você deve carregá-lo em um objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="6263d-106">To make changes to a system profile, you must load it into a profile object.</span></span> <span data-ttu-id="6263d-107">O Gerenciador de perfis fornece duas opções para carregar perfis de sistema: por identificador e por índice.</span><span class="sxs-lookup"><span data-stu-id="6263d-107">The profile manager provides two options for loading system profiles: by identifier, and by index.</span></span>

<span data-ttu-id="6263d-108">Um identificador de perfil do sistema é um valor de GUID atribuído ao perfil do sistema quando ele foi criado.</span><span class="sxs-lookup"><span data-stu-id="6263d-108">A system profile identifier is a GUID value assigned to the system profile when it was created.</span></span> <span data-ttu-id="6263d-109">Para obter uma lista das constantes de GUID associadas aos perfis de sistema da versão 8, consulte [perfis de sistema](system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6263d-109">For a list of the GUID constants associated with the version 8 system profiles, see [System Profiles](system-profiles.md).</span></span> <span data-ttu-id="6263d-110">Você pode encontrar as constantes de GUID para versões anteriores no arquivo de cabeçalho WMSysPrf. h.</span><span class="sxs-lookup"><span data-stu-id="6263d-110">You can find the GUID constants for previous versions in the header file WMSysPrf.h.</span></span> <span data-ttu-id="6263d-111">Para obter mais informações sobre esse e outros arquivos de cabeçalho incluídos no Windows Media Format SDK, consulte [arquivos de biblioteca e configurações do compilador](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="6263d-111">For more information about this and other header files included with the Windows Media Format SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

<span data-ttu-id="6263d-112">O código de exemplo a seguir demonstra como carregar um perfil do sistema usando o identificador de perfil do sistema.</span><span class="sxs-lookup"><span data-stu-id="6263d-112">The following example code demonstrates how to load a system profile using the system profile identifier.</span></span> <span data-ttu-id="6263d-113">Para que esse código funcione, você deve incluir WMSysPrf. h e stdio. h.</span><span class="sxs-lookup"><span data-stu-id="6263d-113">For this code to work, you must include WMSysPrf.h and stdio.h.</span></span> <span data-ttu-id="6263d-114">Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="6263d-114">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
IWMProfileManager* pProfileMgr = NULL;
IWMProfile*        pProfile    = NULL;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager.
hr = WMCreateProfileManager(&pProfileMgr);

// Retrieve the data for the general-purpose broadband video profile.
hr = pProfileMgr->LoadProfileByID(WMProfile_V80_100Video, &pProfile);

// TODO: Perform whatever customizations are needed. For details about
// editing profiles, see Using Custom Profiles.

// Clean up.
pProfile->Release();
pProfile = NULL;
pProfileMgr->Release();
pProfileMgr = NULL;
```



<span data-ttu-id="6263d-115">Se você não souber qual perfil deseja usar, poderá iterar por todos os perfis de sistema de uma versão específica usando os métodos [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) da interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="6263d-115">If you do not know which profile you want to use, you can iterate through all of the system profiles of a particular version using the [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="6263d-116">Esses métodos lidam apenas com uma versão dos perfis do sistema de cada vez.</span><span class="sxs-lookup"><span data-stu-id="6263d-116">These methods only deal with one version of the system profiles at a time.</span></span> <span data-ttu-id="6263d-117">Para obter mais informações sobre como alterar a versão do perfil do sistema, consulte [para alterar as versões do perfil do sistema](to-change-system-profile-versions.md).</span><span class="sxs-lookup"><span data-stu-id="6263d-117">For more information about changing the system profile version, see [To Change System Profile Versions](to-change-system-profile-versions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6263d-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6263d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6263d-119">**Usando perfis de sistema**</span><span class="sxs-lookup"><span data-stu-id="6263d-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




