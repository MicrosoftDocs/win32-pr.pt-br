---
title: Usando tipos de exclusão mútua personalizados
description: Usando tipos de exclusão mútua personalizados
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- exclusão mútua, interface IWMMutualExclusion
- exclusão mútua, tipos personalizados
- perfis, tipos de exclusão mútua personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7162b8d0588031e934e55425af03cd0d2e8d0a58524b19251521ec2ab6848094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845074"
---
# <a name="using-custom-mutual-exclusion-types"></a>Usando tipos de exclusão mútua personalizados

Você pode usar objetos de exclusão mútua em um perfil para atender às necessidades de cenários personalizados. Ao passar o valor GUID CLSID \_ WMMUTEX \_ Unknown para [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), você informa ao objeto de exclusão mútua que está usando um cenário personalizado.

Você deve controlar manualmente a seleção de fluxo ao ler um arquivo com um valor de exclusão mútua personalizado. O objeto leitor usará o primeiro fluxo que você adicionar à exclusão mútua como o padrão.

Use as etapas a seguir para criar um objeto de exclusão mútua personalizado e adicioná-lo a um perfil:

1.  Crie um gerenciador de perfil chamando [**a função WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
2.  Comece com um perfil existente ou crie um totalmente novo.
    -   Se você estiver usando um perfil existente, chame um dos métodos de carregamento da interface [**IWMProfileManager.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) Em seguida, pule para a etapa 4.
    -   Se você estiver criando um perfil totalmente novo, chame [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).
3.  Adicione fluxos ao novo perfil chamando [**IWMProfile::CreateNewStream.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream) Configure os fluxos conforme necessário usando os métodos de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig). Você também pode chamar **QueryInterface** para acessar outras interfaces no objeto de configuração de fluxo.

    **CreateNewStream** cria apenas um objeto de configuração de fluxo e não afeta o perfil. Depois que um fluxo estiver configurado corretamente, você deverá chamar [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para adicionar o fluxo ao perfil.

4.  Crie um objeto de exclusão mútua chamando [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).
5.  Adicione os fluxos desejados ao objeto de exclusão mútua chamando [**IWMStreamList::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (disponível diretamente de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), que herda de [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).
6.  De definir o tipo de exclusão mútua como personalizado chamando [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype). Passe CLSID \_ WMMUTEX \_ Unknown como o GUID do tipo.
7.  Adicione o objeto de exclusão mútua configurado ao perfil chamando [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMMutualExclusion Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**IWMProfile Interface**](iwmprofile.md)
</dt> <dt>

[**IWMProfileManager Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**IWMStreamConfig Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**IWMStreamList Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[**Usando a exclusão mútua**](using-mutual-exclusion.md)
</dt> <dt>

[**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




