---
title: Criando gráficos de filtro em aplicativos DRM-Enabled
description: Criando gráficos de filtro em aplicativos DRM-Enabled
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows SDK do formato de mídia, criando gráficos de filtro
- Windows SDK do formato de mídia, DirectShow
- Windows SDK do formato de mídia, aplicativos habilitados para DRM
- ASF (Advanced Systems Format), criando gráficos de filtro
- ASF (formato de sistemas avançados), criando gráficos de filtro
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), aplicativos habilitados para DRM
- ASF (formato de sistemas avançados), aplicativos habilitados para DRM
- DirectShow, criando gráficos de filtro
- DirectShow, aplicativos habilitados para DRM
- DRM (gerenciamento de direitos digitais), DirectShow
- DRM (gerenciamento de direitos digitais), DirectShow
- DRM (gerenciamento de direitos digitais), criando gráficos de filtro
- DRM (gerenciamento de direitos digitais), criando gráficos de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e7f411a52c0ce7c42410c7a901787c7f6d9d7089921019639cb3f5e708dff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447946"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>Criando gráficos de filtro em aplicativos DRM-Enabled

se seu aplicativo DirectShow dá suporte à reprodução de arquivos protegidos por DRM, em geral, você não deve usar o **renderfile** para criar o grafo de filtro porque não há como especificar quais direitos de DRM você está solicitando antes de o arquivo ser aberto. O leitor ASF do WM, por padrão, solicita apenas direitos de reprodução. O filtro não é adicionado ao grafo e, portanto, não é detectável por aplicativos, até que um arquivo seja aberto com êxito.

Para criar um grafo de reprodução habilitado para DRM usando o [leitor ASF do WM](wm-asf-reader-filter.md), você deve criar uma instância do filtro usando **CoCreateInstance**, adicioná-lo ao grafo de filtro usando **IGraphBuilder:: AddFilter**, configurá-lo e renderizar seus PINs de saída. Essa técnica é demonstrada no exemplo de PlayWndASF. Ao criar o grafo dessa forma, você já tem o ponteiro **IBaseFilter** que pode ser usado para chamar o **QueryService** para obter o **IWMDRMWriter**. no entanto, essa interface não estará disponível até que o Windows objeto de leitor do media Format SDK seja criado internamente pelo leitor ASF do WM. A primeira oportunidade que o aplicativo tem para definir direitos de DRM está em seu \_ manipulador de eventos WMT no \_ Rights \_ ex, como mostrado neste trecho de código:


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

 

 




