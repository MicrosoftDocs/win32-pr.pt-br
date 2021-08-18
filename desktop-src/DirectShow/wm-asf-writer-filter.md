---
description: Filtro do Wm ASF Writer
ms.assetid: 1b12f65f-8d77-4d38-aad9-92bb15cc0426
title: Filtro do Wm ASF Writer (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9281d09e609bd51bc0d0ab42291bd183e782df447e918d3c478e4e857063c21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650817"
---
# <a name="wm-asf-writer-filter-directshow"></a>Filtro do Wm ASF Writer (DirectShow)

O Wm ASF Writer é um filtro wrapper para o objeto writer fornecido com o SDK Windows Media™ Format. O filtro aceita um número variável de fluxos de entrada e cria um arquivo ASF (Advanced Systems Format). O filtro lida com toda a compactação e multiplexação (embora o mecanismo de compactação possa ser ignorado). Você pode usar o Gravador do WM ASF em vários cenários, incluindo captura de DV (vídeo digital), re Audio-Video compactação de áudio e conversão de arquivos de multimídia INTERcalados (AVI) ou MPEG para streaming de rede. Esse filtro fornece a única maneira de criar arquivos microsoft® Windows Media™ Audio e Windows Media Video no Microsoft DirectShow.

Para obter mais informações, consulte [Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md).



| Rótulo | Valor |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IConfigAsfWriter,**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) [**IConfigAsfWriter2,**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2) [**IFileSinkFilter2,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2) [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), **IPersistStream,** **IServiceProvider**, **ISpecifyPropertyPages** Além disso Windows, o filtro expõe as seguintes interfaces do SDK de formato de mídia: **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**<br/> |
| Tipos de mídia de pino de entrada                    | Depende do perfil do ASF. Normalmente, tipos de áudio e vídeo descompactados, embora o filtro aceite tipos compactados se eles corresponderem ao perfil ASF.                                                                                                                                                                                                                                                                                                                                             |
| Interfaces de pino de entrada                     | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass), [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), **IServiceProvider** Além disso, o pino expõe a seguinte interface do SDK de Formato de Mídia do Windows: **IWMStreamConfig2** (por meio de **IServiceProvider**)<br/>                                                                                                                                                                                 |
| Tipos de mídia de pino de saída                   | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Interfaces de pino de saída                    | Não aplicável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Filtrar CLSID                             | CLSID \_ WMAsfWriter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CLSID da página de propriedades                      | CLSID \_ AsfWriterProperties                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Executável                               | Qasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Mérito](merit.md)                       | NÃO USE O NÃO \_ \_ USO \_ DE LIMITED                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [Categoria de filtro](filter-categories.md) | Não especificado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Comentários

O filtro requer o Windows SDK (Kit de Desenvolvimento de Software de Formato de Mídia) e suas dependências subjacentes.

O número de pinos de entrada no filtro depende do identificador de perfil ou perfil do fluxo ASF.

Os pinos de entrada suportam um método da interface **IAMStreamConfig:** [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat). Todos os outros métodos retornam E \_ NOTIMPL. Chame o **método GetFormat** para consultar o formato de compactação de destino do pino, que é definido pelo perfil ASF atual. Use a interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) para definir o perfil.

Você pode usar a interface **IServiceProvider** do filtro para obter um ponteiro para a interface **IWMWriterAdvanced2,** que é definida no SDK Windows Formato de Mídia. Você pode usar a interface **IWMWriterAdvanced2** para controlar a desintervalação de vídeo quando o vídeo de origem é entrelaçado. Para definir o modo de desintervalo, chame **IWMWriterAdvanced2::SetInputSetting.** Para o *parâmetro dwInputNum,* use o índice baseado em zero do pino de entrada de vídeo, conforme enumerado pela interface [**IEnumPins.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins)

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



Os aplicativos não devem usar nenhum dos métodos **IWMWriterAdvanced** herdados pela interface **IWMWriterAdvanced2.** Chamar qualquer um desses métodos pode intercalá-los com a operação do filtro.

O único modo de escrita de arquivo com suporte por esse filtro é AM \_ FILE \_ OVERWRITE. Consulte [**IFileSinkFilter2::GetMode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter2-getmode).

Quando o runtime do SDK de Formato de Mídia Windows envia mensagens DE STATUS do WMT para o filtro Wm ASF Writer, o filtro as encaminha como eventos \_ [**EC \_ WMT \_ EVENT.**](ec-wmt-event.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




