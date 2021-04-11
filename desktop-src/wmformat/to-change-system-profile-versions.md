---
title: Para alterar as versões do perfil do sistema
description: Para alterar as versões do perfil do sistema
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- perfis, sistema
- perfis de sistema, versões
- perfis do sistema, alterando versões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824e2b1cf4a43cef0e87daa461c6510a6672472d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293782"
---
# <a name="to-change-system-profile-versions"></a>Para alterar as versões do perfil do sistema

Sempre que você cria um objeto do Gerenciador de perfis, ele analisa os perfis de sistema. Você pode iterar pelos perfis de sistema usando os métodos [**IWMProfileManager:: GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**IWMProfileManager:: LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) , mas o Gerenciador de perfis contará e listará somente os perfis de uma única versão por vez. Se desejar usar esse método de localização de perfis de sistema, você precisará garantir que o Gerenciador de perfis lida com a versão desejada. Use os métodos da interface [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) para definir e recuperar a versão do perfil do sistema usada pelo Gerenciador de perfis.

As versões são especificadas usando os membros do tipo de enumeração de [**\_ versão WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) . Se você definir a versão do perfil do sistema como WMT \_ Ver \_ 9 \_ 0, a chamada terá sucesso, mas a contagem do perfil do sistema será zero. Isso ocorre porque nenhum perfil de sistema predefinido usa os codecs de áudio do Windows Media e vídeo 9 Series. Para obter mais informações sobre como atualizar perfis para usar os codecs mais recentes, consulte [reutilizando configurações de fluxo](reusing-stream-configurations.md).

Se você carregar um perfil do sistema por seu identificador GUID, não importa qual versão do perfil do sistema o Gerenciador de perfis está usando. Para obter mais informações sobre como carregar perfis de sistema, consulte [para carregar um perfil do sistema](to-load-a-system-profile.md).

O código de exemplo a seguir mostra como definir e recuperar a versão do perfil do sistema. Este exemplo usa printf para saída de console e requer que stdio. h seja incluído. Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).


```C++
int main(void)
{
    HRESULT hr = S_OK;

    IWMProfileManager*  pProfileMgr  = NULL;
    IWMProfileManager2* pProfileMgr2 = NULL;

    WMT_VERSION         profileVersion;

    // Initialize COM.
    hr = CoInitialize(NULL);
    if(FAILED(hr))
    {
        printf("Could not initialize COM.");
        return 0;
    }

    // Create a profile manager object.
    hr = WMCreateProfileManager(&pProfileMgr);
    if(FAILED(hr))
    {
        printf("Could not create a profile manager object.");
        return 0;
    }

    // Get the IWMProfileManager2 interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManager2, 
                                     (void**) &pProfileMgr2);
    if(FAILED(hr))
    {
        printf("Could not get the IWMProfileManager2 interface.");
        SAFE_RELEASE(pProfileMgr);
        return 0;
    }

    // Release the old interface.
    SAFE_RELEASE(pProfileMgr);

    // Get the current system profile version.
    hr = pProfileMgr2->GetSystemProfileVersion(&profileVersion);
    if(FAILED(hr))
    {
        printf("Could not retrieve profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }
    
    // Display the current version.
    printf("Current version: ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Set the system profile version to 8.
    profileVersion = WMT_VER_8_0;

    hr = pProfileMgr2->SetSystemProfileVersion(profileVersion);
    if(FAILED(hr))
    {
        printf("Could not change profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }

    // Print verification.
    printf("Successfully set version to ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Clean up.
    SAFE_RELEASE(pProfileMgr2);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando perfis de sistema**](using-system-profiles.md)
</dt> </dl>

 

 




