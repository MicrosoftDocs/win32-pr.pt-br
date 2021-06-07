---
title: Filtro do Wm ASF Writer (Windows Media Format SDK 11)
description: Saiba mais sobre o filtro Wm ASF Writer.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, Wm ASF Writer
- DirectShow, Wm ASF Writer
- Filtros QASF, Wm ASF Writer
- WM ASF Writer,about
- AsF (Advanced Systems Format), WM ASF Writer
- ASF (Formato de Sistemas Avançados), Wm ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fbd6e36a8178f6ebd1943cdaac214597e0ba4e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444697"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>Filtro do Wm ASF Writer (Windows Media Format SDK 11)

O filtro Wm ASF Writer aceita um número variável de fluxos de entrada e cria um arquivo ASF. O filtro lida com toda a compactação e multiplexação (embora o mecanismo de compactação possa ser ignorado). Você pode usar o filtro gravador WM ASF em vários cenários, incluindo captura de DV (vídeo digital), re Audio-Video compactação de áudio e conversão de arquivos de mídia digital INTERcalados (AVI) ou MPEG para streaming de rede. Esse filtro fornece a única maneira de criar arquivos de Áudio de Mídia do Microsoft Windows e vídeo de mídia do Windows no DirectShow.

Para obter mais informações, consulte [Criando arquivos ASF no DirectShow.](creating-asf-files-in-directshow.md)

A tabela a seguir contém informações sobre o filtro Wm ASF Writer, como as interfaces e tipos de mídia aos quais ele dá suporte.



| Informações de filtro                       |  Tipos                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro      | **IAMFilterMiscFlags,** **IBaseFilter,** **IConfigAsfWriter,** **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2** |
| Tipos de mídia de pino de entrada  | Dependendo do perfil. Normalmente, tipos descompactados, como Áudio MEDIATYPE ou Vídeo MEDIATYPE, embora os tipos compactados possam ser aceitos se corresponderem \_ \_ ao perfil                                                   |
| Interfaces de pino de entrada   | **IPin,** **IMemInputPin,** **IAMStreamConfig,** **IServiceProvider,** **IAMWMBufferPass,** **IWMStreamConfig2** (por **meio de IServiceProvider**)                                                                         |
| Tipos de mídia de pino de saída | Não aplicável                                                                                                                                                                                                          |
| Interfaces de pino de saída  | Não aplicável                                                                                                                                                                                                          |
| Filtrar CLSID           | CLSID \_ WMAsfWriter                                                                                                                                                                                                      |
| CLSID da página de propriedades    | CLSID \_ WMAsfWriterProperties                                                                                                                                                                                            |
| Executável             | Qasf.dll                                                                                                                                                                                                                |
| Mérito                  | NÃO USE O NÃO \_ \_ USO \_ DE LIMITED                                                                                                                                                                                                     |
| Categoria de filtro        | Não especificado                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Comentários

O número de pinos de entrada no filtro depende do perfil passado para o filtro. Um pino do tipo de mídia apropriado é criado para cada fluxo definido no perfil.

Os pinos de entrada suportam um método da interface **IAMStreamConfig:** **IAMStreamConfig::GetFormat**. Todos os outros métodos retornam E \_ NOTIMPL. Chame o **método GetFormat** para consultar o formato de compactação de destino do pino, que é definido pelo perfil atual. Use a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) para definir o perfil.

A interface **IServiceProvider** do filtro permite que os aplicativos recuperem a interface [**IWMWriterAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) que é definida no SDK do Windows Media Format. A interface **IWMWriterAdvanced2** controla [*a*](wmformat-glossary.md) desintervalação de vídeo e é útil se a entrada for uma fonte entrelaçada, como DV (vídeo digital). Use os **métodos GetInputSetting** **e SetInputSetting** para controlar a desintercalação. Não é recomendável que os clientes usem qualquer um dos outros métodos nessa interface. Essa interface só poderá ser obtida depois que o filtro tiver sido adicionado ao grafo de filtro. O exemplo a seguir mostra como consultar essa interface:


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

[**Referência de QASF do DirectShow**](directshow-qasf-reference.md)
</dt> </dl>

 

 
