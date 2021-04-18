---
title: Filtro de gravador ASF do WM (SDK do Windows Media Format 11)
description: Filtro de gravador ASF do WM
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- SDK do Windows Media Format, gravador ASF do WM
- DirectShow, gravador ASF do WM
- Filtros do QASF, gravador ASF do WM
- Gravador ASF do WM, sobre
- ASF (Advanced Systems Format), gravador ASF do WM
- ASF (formato de sistemas avançados), gravador ASF do WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0de34bcf4b4047673f832d78f40377f98e94d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105760105"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>Filtro de gravador ASF do WM (SDK do Windows Media Format 11)

O filtro do gravador ASF do WM aceita um número variável de fluxos de entrada e cria um arquivo ASF. O filtro manipula toda a compactação e a multiplexação (embora o mecanismo de compactação possa ser ignorado). Você pode usar o filtro do gravador ASF do WM em vários cenários, incluindo captura Audio-Video de vídeo digital (DV), recompactação de áudio e conversão de arquivos de mídia digital intercalados (AVI) ou MPEG para streaming de rede. Esse filtro fornece a única maneira de criar arquivos de vídeo do Windows Media e áudio do Microsoft Windows no DirectShow.

Para obter mais informações, consulte [criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md).

A tabela a seguir contém informações sobre o filtro de gravador ASF do WM, como as interfaces e os tipos de mídia aos quais ele dá suporte.



|                        |                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces      | **IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2** |
| Tipos de mídia de pino de entrada  | Dependente do perfil. Normalmente, tipos descompactados como \_ vídeo de áudio de MediaType ou MediaType \_ , embora tipos compactados possam ser aceitos se corresponderem ao perfil                                                   |
| Interfaces de pino de entrada   | **IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (por meio de **IServiceProvider**)                                                                         |
| Tipos de mídia do pino de saída | Não aplicável                                                                                                                                                                                                          |
| Interfaces de pino de saída  | Não aplicável                                                                                                                                                                                                          |
| CLSID do filtro           | \_WMASFWRITER CLSID                                                                                                                                                                                                      |
| CLSID de página de propriedades    | \_WMASFWRITERPROPERTIES CLSID                                                                                                                                                                                            |
| Executável             | Qasf.dll                                                                                                                                                                                                                |
| Núcleo                  | MÉRITO \_ \_ não \_ use                                                                                                                                                                                                     |
| Categoria do filtro        | Não especificado                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Comentários

O número de Pins de entrada no filtro depende do perfil que é passado para o filtro. Um PIN do tipo de mídia apropriado é criado para cada fluxo definido no perfil.

Os Pins de entrada dão suporte a um método da interface **IAMStreamConfig** : **IAMStreamConfig:: GetFormat**. Todos os outros métodos retornam E \_ NOTIMPL. Chame o método **GetFormat** para consultar o formato de compactação de destino do PIN, que é definido pelo perfil atual. Use a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) para definir o perfil.

A interface **IServiceProvider** do filtro permite que os aplicativos recuperem a interface [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , que é definida no SDK do Windows Media Format. A interface **IWMWriterAdvanced2** controla o desentrelaçamento de vídeo e será útil se a entrada for uma fonte [*entrelaçada*](wmformat-glossary.md) , como DV (Digital Video). Use os métodos **GetInputSetting** e **SetInputSetting** para controlar o desentrelaçamento. Não é recomendável que os clientes usem qualquer um dos outros métodos nessa interface. Essa interface só pode ser obtida depois que o filtro tiver sido adicionado ao grafo de filtro. O exemplo a seguir mostra como consultar essa interface:


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência do QASF do DirectShow**](directshow-qasf-reference.md)
</dt> </dl>

 

 
