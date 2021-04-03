---
title: Usando tipos de exclusão mútua personalizada
description: Usando tipos de exclusão mútua personalizada
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- exclusão mútua, interface IWMMutualExclusion
- exclusão mútua, tipos personalizados
- perfis, tipos de exclusão mútua personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084354"
---
# <a name="using-custom-mutual-exclusion-types"></a>Usando tipos de exclusão mútua personalizada

Você pode usar objetos de exclusão mútua em um perfil para atender às necessidades de cenários personalizados. Ao passar o valor de GUID CLSID \_ WMMUTEX \_ desconhecido para [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), você informa ao objeto de exclusão mútua que está usando um cenário personalizado.

Você deve controlar manualmente a seleção de fluxo ao ler um arquivo com um valor de exclusão mútua personalizado. O objeto leitor usará o primeiro fluxo que você adicionar à exclusão mútua como padrão.

Use as etapas a seguir para criar um objeto de exclusão mútua personalizada e adicioná-lo a um perfil:

1.  Crie um Gerenciador de perfis chamando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Inicie o com um perfil existente ou crie um totalmente novo.
    -   Se você estiver usando um perfil existente, chame um dos métodos de carga da interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Em seguida, pule para a etapa 4.
    -   Se você estiver criando um perfil totalmente novo, chame [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).
3.  Adicione fluxos ao novo perfil chamando [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream). Configure os fluxos conforme necessário usando os métodos de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig). Você também pode chamar **QueryInterface** para acessar outras interfaces no objeto de configuração de fluxo.

    **CreateNewStream** cria apenas um objeto de configuração de fluxo e não afeta o perfil. Depois que um fluxo é configurado corretamente, você deve chamar [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para adicionar o fluxo ao perfil.

4.  Crie um objeto de exclusão mútua chamando [**IWMProfile:: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).
5.  Adicione os fluxos desejados ao objeto de exclusão mútua chamando [**IWMStreamList:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (disponível diretamente de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), que herda de [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).
6.  Defina o tipo de exclusão mútua para personalizado chamando [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype). Passe o CLSID \_ WMMUTEX \_ desconhecido como o tipo Guid.
7.  Adicione o objeto de exclusão mútua configurado ao perfil chamando [**IWMProfile:: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interface IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Interface IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**Interface IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[**Usando a exclusão mútua**](using-mutual-exclusion.md)
</dt> <dt>

[**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




