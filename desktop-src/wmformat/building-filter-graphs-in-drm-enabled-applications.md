---
title: Criando gráficos de filtro em aplicativos DRM-Enabled
description: Criando gráficos de filtro em aplicativos DRM-Enabled
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- SDK do Windows Media Format, criando gráficos de filtro
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, aplicativos habilitados para DRM
- ASF (Advanced Systems Format), criando gráficos de filtro
- ASF (formato de sistemas avançados), criando gráficos de filtro
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), aplicativos habilitados para DRM
- ASF (formato de sistemas avançados), aplicativos habilitados para DRM
- DirectShow, criando gráficos de filtro
- Aplicativos habilitados para DRM e DirectShow
- DRM (gerenciamento de direitos digitais), DirectShow
- DRM (gerenciamento de direitos digitais), DirectShow
- DRM (gerenciamento de direitos digitais), criando gráficos de filtro
- DRM (gerenciamento de direitos digitais), criando gráficos de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944037a00c208e1427d3d19aa6c9dc0a352ec5fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293791"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>Criando gráficos de filtro em aplicativos DRM-Enabled

Se seu aplicativo do DirectShow der suporte à reprodução de arquivos protegidos por DRM, em geral, você não deve usar o **RenderFile** para criar o grafo de filtro porque não há como especificar quais direitos de DRM você está solicitando antes de o arquivo ser aberto. O leitor ASF do WM, por padrão, solicita apenas direitos de reprodução. O filtro não é adicionado ao grafo e, portanto, não é detectável por aplicativos, até que um arquivo seja aberto com êxito.

Para criar um grafo de reprodução habilitado para DRM usando o [leitor ASF do WM](wm-asf-reader-filter.md), você deve criar uma instância do filtro usando **CoCreateInstance**, adicioná-lo ao grafo de filtro usando **IGraphBuilder:: AddFilter**, configurá-lo e renderizar seus PINs de saída. Essa técnica é demonstrada no exemplo de PlayWndASF. Ao criar o grafo dessa forma, você já tem o ponteiro **IBaseFilter** que pode ser usado para chamar o **QueryService** para obter o **IWMDRMWriter**. No entanto, essa interface não estará disponível até que o objeto leitor do Windows Media Format SDK seja criado internamente pelo leitor ASF do WM. A primeira oportunidade que o aplicativo tem para definir direitos de DRM está em seu \_ manipulador de eventos WMT no \_ Rights \_ ex, como mostrado neste trecho de código:


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




