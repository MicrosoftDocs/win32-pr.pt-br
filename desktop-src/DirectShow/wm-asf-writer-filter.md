---
description: Filtro de gravador ASF do WM
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: Filtro de gravador ASF do WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9281d09e609bd51bc0d0ab42291bd183e782df447e918d3c478e4e857063c21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650817"
---
# <a name="wm-asf-writer-filter-directshow"></a>Filtro de gravador ASF do WM (DirectShow)

o gravador ASF do WM é um filtro de wrapper para o objeto do gravador fornecido com o SDK do formato de™ de mídia Windows. O filtro aceita um número variável de fluxos de entrada e cria um arquivo ASF (Advanced Systems Format). O filtro manipula toda a compactação e a multiplexação (embora o mecanismo de compactação possa ser ignorado). Você pode usar o gravador ASF do WM em vários cenários, incluindo captura Audio-Video de vídeo digital (DV), recompactação de áudio e conversão de arquivos multimídia intercalados (AVI) ou MPEG para transmissão de rede. esse filtro fornece a única maneira de criar arquivos de vídeo do microsoft® Windows mídia™ áudio e Windows media no microsoft DirectShow.

Para obter mais informações, consulte [criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md).



| Rótulo | Valor |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **ISpecifyPropertyPages** além disso, o filtro expõe as seguintes interfaces SDK do formato de mídia Windows: **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**<br/> |
| Tipos de mídia de pino de entrada                    | Depende do perfil do ASF. Normalmente, os tipos de áudio e vídeo não compactados, embora o filtro aceite tipos compactados se corresponderem ao perfil do ASF.                                                                                                                                                                                                                                                                                                                                             |
| Interfaces de pino de entrada                     | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** além disso, o pin expõe a seguinte interface do SDK do formato de mídia Windows: **IWMStreamConfig2** (por meio de **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Tipos de mídia do pino de saída                   | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de pino de saída                    | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| CLSID do filtro                             | \_WMASFWRITER CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID de página de propriedades                      | \_ASFWRITERPROPERTIES CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Executável                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Categoria do filtro](filter-categories.md) | Não especificado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Comentários

o filtro requer o SDK (Software Development Kit) Windows Media Format e suas dependências subjacentes.

O número de Pins de entrada no filtro depende do perfil ou do identificador do perfil do fluxo do ASF.

Os Pins de entrada dão suporte a um método da interface **IAMStreamConfig** : [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Todos os outros métodos retornam E \_ NOTIMPL. Chame o método **GetFormat** para consultar o formato de compactação de destino do PIN, que é definido pelo perfil ASF atual. Use a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) para definir o perfil.

você pode usar a interface **IServiceProvider** do filtro para obter um ponteiro para a interface **IWMWriterAdvanced2** , que é definida no SDK do formato de mídia Windows. Você pode usar a interface **IWMWriterAdvanced2** para controlar o desentrelaçamento de vídeo quando o vídeo de origem é entrelaçado. Para definir o modo de desentrelaçamento, chame **IWMWriterAdvanced2:: SetInputSetting**. Para o parâmetro *dwInputNum* , use o índice de base zero do pino de entrada de vídeo, conforme enumerado pela interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .

O exemplo a seguir mostra como consultar essa interface:


```C++
// Assume that pAsfWriter is a valid IBaseFilter pointer.
IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = pAsfWriter->QueryInterface(
    IID_IServiceProvider, 
    (void**)&pProvider
    );
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(
        IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, 
        (void**)&pWMWA2
        );
    pProvider->Release();
    if (SUCCEEDED(hr))
    {
        // Use pWMWA2. (Not shown.)
        pWMWA2->Release();
    }
}
```



Os aplicativos não devem usar nenhum dos métodos **IWMWriterAdvanced** que a interface **IWMWriterAdvanced2** herda. Chamar qualquer um desses métodos pode interere com a operação do filtro.

O único modo de gravação de arquivos com suporte nesse filtro é a \_ substituição de arquivo am \_ . Consulte [**IFileSinkFilter2:: GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

quando o tempo de execução do SDK do formato de mídia do Windows envia \_ mensagens de STATUS WMT para o filtro de gravador ASF do WM, o filtro as encaminha como eventos de [**\_ \_ evento do EC WMT**](ec-wmt-event.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> </dl>

 

 




