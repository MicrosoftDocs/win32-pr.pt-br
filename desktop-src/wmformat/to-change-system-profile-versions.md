---
title: Para alterar versões de perfil do sistema
description: Para alterar versões de perfil do sistema
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- perfis, sistema
- perfis do sistema, versões
- perfis do sistema, alterando versões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c963a142c879242b5e2ae734dedb4073a120a57a9121c3f3f95e5838c15110a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084259"
---
# <a name="to-change-system-profile-versions"></a>Para alterar versões de perfil do sistema

Sempre que você cria um objeto do gerenciador de perfil, ele analisará os perfis do sistema. Você pode iterar pelos perfis do sistema usando os métodos [**IWMProfileManager::GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**IWMProfileManager::LoadSystemProfile,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) mas o gerenciador de perfil contará e lista apenas os perfis de uma única versão por vez. Se você quiser usar esse método de localizar perfis do sistema, precisará garantir que o manger de perfil lida com a versão que você deseja. Use os métodos da interface [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) para definir e recuperar a versão do perfil do sistema usada pelo gerenciador de perfil.

As versões são especificadas usando os membros do tipo de [**enumeração WMT \_ VERSION.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) Se você definir a versão do perfil do sistema como WMT \_ VER \_ 9 0, a chamada terá êxito, mas a contagem de perfil do sistema \_ será zero. Isso porque nenhum perfil de sistema predefinido usa os codecs Windows Media Audio e Video 9 Series. Para obter mais informações sobre como atualizar perfis para usar os codecs mais novos, consulte [Reutilizando configurações de fluxo.](reusing-stream-configurations.md)

Se você carregar um perfil do sistema por seu identificador guid, não importa qual versão do perfil do sistema o gerenciador de perfil está usando. Para obter mais informações sobre como carregar perfis do sistema, [consulte Para carregar um perfil do sistema.](to-load-a-system-profile.md)

O código de exemplo a seguir mostra como definir e recuperar a versão do perfil do sistema. Este exemplo usa printf para a saída do console e requer que stdio.h seja incluído. Para obter mais informações sobre como usar esse código, [consulte Usando os exemplos de código](using-the-code-examples.md).


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

[**Usando perfis do sistema**](using-system-profiles.md)
</dt> </dl>

 

 




