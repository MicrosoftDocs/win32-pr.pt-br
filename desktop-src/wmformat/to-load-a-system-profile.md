---
title: Para carregar um perfil do sistema
description: Para carregar um perfil do sistema
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- perfis, sistema
- perfis do sistema, carregando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becd98903921b81ce1eaf7d2317659c7760bb99c4e55e07efe336719d5d34ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807476"
---
# <a name="to-load-a-system-profile"></a>Para carregar um perfil do sistema

Para fazer alterações em um perfil do sistema, você deve carregá-lo em um objeto de perfil. O gerenciador de perfil fornece duas opções para carregar perfis do sistema: por identificador e por índice.

Um identificador de perfil do sistema é um valor GUID atribuído ao perfil do sistema quando ele foi criado. Para ver uma lista das constantes GUID associadas aos perfis de sistema da versão 8, consulte [Perfis do sistema.](system-profiles.md) Você pode encontrar as constantes guid para versões anteriores no arquivo de header WMSysPrf.h. Para obter mais informações sobre esse e outros arquivos de header incluídos no SDK Windows Media Format, consulte Arquivos de biblioteca e [compilador Configurações](library-files-and-compiler-settings.md).

O código de exemplo a seguir demonstra como carregar um perfil do sistema usando o identificador de perfil do sistema. Para que esse código funcione, você deve incluir WMSysPrf.h e stdio.h. Para obter mais informações sobre como usar esse código, [consulte Usando os exemplos de código](using-the-code-examples.md).


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



Se você não sabe qual perfil deseja usar, poderá iterar por todos os perfis do sistema de uma versão específica usando os métodos [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) da interface [**IWMProfileManager.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) Esses métodos lidam apenas com uma versão dos perfis de sistema por vez. Para obter mais informações sobre como alterar a versão do perfil do sistema, consulte [To Change System Profile Versions](to-change-system-profile-versions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando perfis do sistema**](using-system-profiles.md)
</dt> </dl>

 

 




