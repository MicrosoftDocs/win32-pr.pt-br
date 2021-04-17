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
# <a name="working-with-localized-system-profiles"></a>Trabalhando com perfis de sistema localizados

O Windows Media Format SDK inclui perfis de sistema com nomes e descrições em vários idiomas. Os arquivos do perfil do sistema. prx localizados são instalados \[ na \] \\ pasta SDKRoot WMSDK \\ WMFSDK9 \\ LocalizedProfiles. Para acessar um arquivo específico com os métodos **IWMProfileManagerLanguage** , você deve movê-lo para o diretório raiz do sistema junto com os outros arquivos de perfil do sistema. Para obter uma lista dos arquivos de perfil do sistema localizados, consulte [perfis de sistema localizados](localized-system-profiles.md).

Você pode definir ou recuperar o idioma do perfil do sistema usando os métodos da interface [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) . O idioma é especificado como um valor de LANGid, que consiste em um identificador de idioma primário e um identificador de idioma secundário. O código a seguir demonstra como recuperar o idioma atual. O idioma padrão é inglês americano (0x409). Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando perfis de sistema**](using-system-profiles.md)
</dt> </dl>

 

 




