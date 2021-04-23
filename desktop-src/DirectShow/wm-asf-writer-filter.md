---
description: Filtro de gravador ASF do WM
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: Filtro de gravador ASF do WM (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf09a99673b07e88198fd57b95a766ce821eb02
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909274"
---
# <a name="wm-asf-writer-filter-directshow"></a>Filtro de gravador ASF do WM (DirectShow)

O gravador ASF do WM é um filtro de wrapper para o objeto gravador fornecido com o SDK do Windows Media™ Format. O filtro aceita um número variável de fluxos de entrada e cria um arquivo ASF (Advanced Systems Format). O filtro manipula toda a compactação e a multiplexação (embora o mecanismo de compactação possa ser ignorado). Você pode usar o gravador ASF do WM em vários cenários, incluindo captura Audio-Video de vídeo digital (DV), recompactação de áudio e conversão de arquivos multimídia intercalados (AVI) ou MPEG para transmissão de rede. Esse filtro fornece a única maneira de criar arquivos de vídeo do Microsoft® Windows Media™ áudio e do Windows Media no Microsoft DirectShow.

Para obter mais informações, consulte [criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md).



| Label | Valor |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter), [**IConfigAsfWriter2**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream**, **IServiceProvider**, **ISpecifyPropertyPages** além disso, o filtro expõe as seguintes interfaces SDK do Windows Media Format: **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**<br/> |
| Tipos de mídia de pino de entrada                    | Depende do perfil do ASF. Normalmente, os tipos de áudio e vídeo não compactados, embora o filtro aceite tipos compactados se corresponderem ao perfil do ASF.                                                                                                                                                                                                                                                                                                                                             |
| Interfaces de pino de entrada                     | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** além disso, o PIN expõe a seguinte interface do SDK do Windows Media Format: **IWMStreamConfig2** (por meio de **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Tipos de mídia do pino de saída                   | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de pino de saída                    | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| CLSID do filtro                             | \_WMASFWRITER CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID de página de propriedades                      | \_ASFWRITERPROPERTIES CLSID                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Executável                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Núcleo](merit.md)                       | MÉRITO \_ \_ não \_ use                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Categoria do filtro](filter-categories.md) | Não especificado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Comentários

O filtro requer o SDK (Software Development Kit) do Windows Media Format e suas dependências subjacentes.

O número de Pins de entrada no filtro depende do perfil ou do identificador do perfil do fluxo do ASF.

Os Pins de entrada dão suporte a um método da interface **IAMStreamConfig** : [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Todos os outros métodos retornam E \_ NOTIMPL. Chame o método **GetFormat** para consultar o formato de compactação de destino do PIN, que é definido pelo perfil ASF atual. Use a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) para definir o perfil.

Você pode usar a interface **IServiceProvider** do filtro para obter um ponteiro para a interface **IWMWriterAdvanced2** , que é definida no Windows Media Format SDK. Você pode usar a interface **IWMWriterAdvanced2** para controlar o desentrelaçamento de vídeo quando o vídeo de origem é entrelaçado. Para definir o modo de desentrelaçamento, chame **IWMWriterAdvanced2:: SetInputSetting**. Para o parâmetro *dwInputNum* , use o índice de base zero do pino de entrada de vídeo, conforme enumerado pela interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .

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

Quando o tempo de execução do SDK do Windows Media Format envia \_ mensagens de status WMT para o filtro de gravador ASF do WM, o filtro as encaminha como eventos de [**\_ \_ evento do EC WMT**](ec-wmt-event.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 




