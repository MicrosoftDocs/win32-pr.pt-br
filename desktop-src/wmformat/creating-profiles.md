---
title: Criando perfis
description: Criando perfis
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- SDK do Windows Media Format, perfis
- perfis, criando
- perfis, interface IWMProfileManager
- IWMProfileManager, criando perfis
- perfis, função WMCreateProfileManager
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007083"
---
# <a name="creating-profiles"></a>Criando perfis

Em muitos casos, você desejará criar um perfil vazio para configurar suas necessidades. Em outros casos, é mais fácil editar um perfil existente, como um perfil do sistema. Para obter mais informações sobre como usar perfis de sistema, consulte [usando perfis de sistema](using-system-profiles.md).

A criação de um perfil vazio, pronto para configuração, requer um objeto do Gerenciador de perfis. Para obter a interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) de um objeto do Gerenciador de perfis, chame a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .

Para criar um perfil vazio, chame [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile). Quando você cria um perfil vazio, a única coisa que você especifica é a versão do SDK do Windows Media Format com a qual o perfil está em conformidade. A menos que você tenha uma necessidade específica de usar uma versão anterior, você sempre deve usar a versão mais recente. A versão determina a estrutura do perfil; as versões anteriores não davam suporte a algumas propriedades.

O código de exemplo a seguir mostra como criar um novo perfil. Para compilar esse código em seu aplicativo, inclua stdio. h. Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interface IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

 




