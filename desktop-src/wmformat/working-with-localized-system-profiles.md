---
title: Trabalhando com perfis de sistema localizados
description: Trabalhando com perfis de sistema localizados
ms.assetid: d911baf6-0731-4f02-9001-d04464a03f56
keywords:
- perfis, sistema
- perfis de sistema, localizados
- perfis de sistema, interface IWMProfileManagerLanguage
- perfis de sistema localizados, sobre
- IWMProfileManagerLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8c040d9804cd822b17e7caad8a8cfb5e5854c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105766281"
---
# <a name="working-with-localized-system-profiles"></a><span data-ttu-id="7ae75-108">Trabalhando com perfis de sistema localizados</span><span class="sxs-lookup"><span data-stu-id="7ae75-108">Working with Localized System Profiles</span></span>

<span data-ttu-id="7ae75-109">O Windows Media Format SDK inclui perfis de sistema com nomes e descrições em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="7ae75-109">The Windows Media Format SDK includes system profiles with names and descriptions in several languages.</span></span> <span data-ttu-id="7ae75-110">Os arquivos do perfil do sistema. prx localizados são instalados \[ na \] \\ pasta SDKRoot WMSDK \\ WMFSDK9 \\ LocalizedProfiles.</span><span class="sxs-lookup"><span data-stu-id="7ae75-110">The localized system profile .prx files are installed into the \[SDKRoot\]\\WMSDK\\WMFSDK9\\LocalizedProfiles folder.</span></span> <span data-ttu-id="7ae75-111">Para acessar um arquivo específico com os métodos **IWMProfileManagerLanguage** , você deve movê-lo para o diretório raiz do sistema junto com os outros arquivos de perfil do sistema.</span><span class="sxs-lookup"><span data-stu-id="7ae75-111">To access a particular file with the **IWMProfileManagerLanguage** methods, you must move it into the system root directory along with the other system profile files.</span></span> <span data-ttu-id="7ae75-112">Para obter uma lista dos arquivos de perfil do sistema localizados, consulte [perfis de sistema localizados](localized-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="7ae75-112">For a list of the localized system profile files, see [Localized System Profiles](localized-system-profiles.md).</span></span>

<span data-ttu-id="7ae75-113">Você pode definir ou recuperar o idioma do perfil do sistema usando os métodos da interface [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) .</span><span class="sxs-lookup"><span data-stu-id="7ae75-113">You can set or retrieve the system profile language using the methods of the [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) interface.</span></span> <span data-ttu-id="7ae75-114">O idioma é especificado como um valor de LANGid, que consiste em um identificador de idioma primário e um identificador de idioma secundário.</span><span class="sxs-lookup"><span data-stu-id="7ae75-114">The language is specified as a LANGID value, which consists of a primary language identifier and a secondary language identifier.</span></span> <span data-ttu-id="7ae75-115">O código a seguir demonstra como recuperar o idioma atual.</span><span class="sxs-lookup"><span data-stu-id="7ae75-115">The following code demonstrates how to retrieve the current language.</span></span> <span data-ttu-id="7ae75-116">O idioma padrão é inglês americano (0x409).</span><span class="sxs-lookup"><span data-stu-id="7ae75-116">The default language is U.S. English (0x409).</span></span> <span data-ttu-id="7ae75-117">Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="7ae75-117">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT GetCurrentSystemProfileLanguage(IMWProfilManager* pProfileMgr)
{
    HRESULT hr = S_OK;

    IWMProfileManagerLanguage* pProfileMgrLang = NULL;

    // Get the profile manager language interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManagerLanguage,
                                     (void **) &pProfileMgrLang);
    if(FAILED(hr))
    {
        printf("Couldn't get IWMProfileManagerLanguage.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    // Retrieve the current language (as a LANGID value)
    WORD wLangID = 0;
    hr = pProfileMgrLang->GetUserLanguageID(&wLangID);
    if(FAILED(hr))
    {
        printf("Could not get the current language.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    printf("The current language ID is 0x%X\n", wLangID);

    SAFE_RELEASE(pProfileMgrLang);
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="7ae75-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ae75-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ae75-119">**Usando perfis de sistema**</span><span class="sxs-lookup"><span data-stu-id="7ae75-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




