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
# <a name="to-load-a-system-profile"></a>Para carregar um perfil do sistema

Para fazer alterações em um perfil de sistema, você deve carregá-lo em um objeto de perfil. O Gerenciador de perfis fornece duas opções para carregar perfis de sistema: por identificador e por índice.

Um identificador de perfil do sistema é um valor de GUID atribuído ao perfil do sistema quando ele foi criado. Para obter uma lista das constantes de GUID associadas aos perfis de sistema da versão 8, consulte [perfis de sistema](system-profiles.md). Você pode encontrar as constantes de GUID para versões anteriores no arquivo de cabeçalho WMSysPrf. h. Para obter mais informações sobre esse e outros arquivos de cabeçalho incluídos no Windows Media Format SDK, consulte [arquivos de biblioteca e configurações do compilador](library-files-and-compiler-settings.md).

O código de exemplo a seguir demonstra como carregar um perfil do sistema usando o identificador de perfil do sistema. Para que esse código funcione, você deve incluir WMSysPrf. h e stdio. h. Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).


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



Se você não souber qual perfil deseja usar, poderá iterar por todos os perfis de sistema de uma versão específica usando os métodos [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) da interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Esses métodos lidam apenas com uma versão dos perfis do sistema de cada vez. Para obter mais informações sobre como alterar a versão do perfil do sistema, consulte [para alterar as versões do perfil do sistema](to-change-system-profile-versions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando perfis de sistema**](using-system-profiles.md)
</dt> </dl>

 

 




