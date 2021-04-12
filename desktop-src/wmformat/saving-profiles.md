---
title: Salvando perfis
description: Salvando perfis
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- SDK do Windows Media Format, salvando perfis
- SDK do Windows Media Format, salvamento de perfil
- perfis, salvando
- perfis, interface IWMProfileManager
- IWMProfileManager, salvando perfis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276b002f0b7f98de2e84f2c27a4f52bde25726bb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365540"
---
# <a name="saving-profiles"></a><span data-ttu-id="6e414-108">Salvando perfis</span><span class="sxs-lookup"><span data-stu-id="6e414-108">Saving Profiles</span></span>

<span data-ttu-id="6e414-109">Você pode usar o método [**IWMProfileManager:: SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) para salvar o conteúdo de um objeto de perfil em uma cadeia de caracteres formatada com XML.</span><span class="sxs-lookup"><span data-stu-id="6e414-109">You can use the [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) method to save the contents of a profile object to a string formatted with XML.</span></span> <span data-ttu-id="6e414-110">Nenhum método é fornecido para armazenar a cadeia de caracteres do perfil em um arquivo; Você pode usar as rotinas de e/s de arquivo de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="6e414-110">No methods are provided to store the profile string to a file; you can use the file I/O routines of your choice.</span></span>

> [!Note]  
> <span data-ttu-id="6e414-111">Você nunca deve alterar a cadeia de caracteres do perfil gravada em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="6e414-111">You should never alter the profile string written to a file.</span></span> <span data-ttu-id="6e414-112">As alterações que você deseja fazer em um perfil devem ser feitas programaticamente.</span><span class="sxs-lookup"><span data-stu-id="6e414-112">Any changes you want to make to a profile should be made programmatically.</span></span> <span data-ttu-id="6e414-113">Alterar valores em um arquivo. prx pode causar resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="6e414-113">Changing values in a .prx file can cause unpredictable results.</span></span>

 

<span data-ttu-id="6e414-114">O exemplo a seguir é uma função para salvar um perfil em um arquivo usando e/s de arquivo em estilo C padrão.</span><span class="sxs-lookup"><span data-stu-id="6e414-114">The following example is a function to save a profile to a file using standard C-style file I/O.</span></span> <span data-ttu-id="6e414-115">Para compilar um aplicativo que usa este exemplo, você deve incluir STDIO. h em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="6e414-115">To compile an application that uses this example, you must include stdio.h in your project.</span></span>


```C++
HRESULT ProfileToFile(IWMProfileManager* pProfileMgr, 
                      IWMProfile* pProfile)
{
    HRESULT hr = S_OK;

    FILE*   pFile;
    
    WCHAR*  pwszProfileString = NULL;
    DWORD   cchProfileString = 0;

    // Save the profile to a string.
    // First, retrieve the size of the string required.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  NULL, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not get the profile string size.");
        return hr;
    }

    // Allocate memory to hold the string.
    pwszProfileString = new WCHAR[cchProfileString];

    if(pwszProfileString == NULL)
    {
        printf("Could not allocate memory for the profile string.");
        return E_OUTOFMEMORY;
    }

    // Retrieve the string.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  pwszProfileString, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not save the profile string.");
        return hr;
    }

    // Create the output file.
    pFile = fopen("MyProfile.prx", "w");

    // Write the profile string to the file.
    fprintf(pFile, "%S\n", pwszProfileString);

    // Close the file.
    fclose(pFile);

    delete[] pwszProfileString;

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="6e414-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e414-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e414-117">**Trabalhando com perfis**</span><span class="sxs-lookup"><span data-stu-id="6e414-117">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




