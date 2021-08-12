---
description: DMO Filtro wrapper
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: DMO Filtro wrapper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13383e7539f478327f1a904d60fcd069692180239e76bcfd48bcc090a068e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653036"
---
# <a name="dmo-wrapper-filter"></a>DMO Filtro wrapper

O DMO wrapper permite que um aplicativo DirectShow use um DMO de Mídia [DirectX](directx-media-objects.md) dentro de um grafo de filtro. O filtro envolve o DMO e lida com todos os detalhes do uso do DMO, como passar dados para e do DMO. Além disso, o filtro agrega o DMO, para que o aplicativo possa consultar o filtro para qualquer interface COM que o DMO expõe.



| Rótulo | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IDMOWrapperFilter,**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Tipos de mídia de pino de entrada                    | Consulte Comentários                                                                                                                                                                                                                                        |
| Interfaces de pino de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de mídia de pino de saída                   | Consulte Comentários                                                                                                                                                                                                                                        |
| Interfaces de pino de saída                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtrar CLSID                             | CLSID \_ DMOWrapperFilter                                                                                                                                                                                                                            |
| CLSID da página de propriedades                      | Nenhuma página de propriedades                                                                                                                                                                                                                                   |
| Executável                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Mérito](merit.md)                       | Consulte Comentários                                                                                                                                                                                                                                        |
| [Categoria de filtro](filter-categories.md) | Consulte Comentários                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Comentários

### <a name="limitations"></a>Limitações

O DMO Wrapper tem as seguintes limitações:

-   Ele não dá suporte a DMOs com zero entradas, várias entradas ou zero saídas. (Ele dá suporte a DMOs com uma entrada e várias saídas.)
-   Ele não dá suporte a transporte personalizado. Todo o transporte de dados é feito por meio da interface [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   Ele não usa a interface **IMediaObjectInPlace;** todo o processamento é feito usando [**métodos IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)

### <a name="pins"></a>Pins

Para cada fluxo de entrada no DMO, o filtro cria um pino de entrada correspondente. Para cada fluxo de saída, ele cria um pino de saída correspondente. Os tipos de mídia aos quais cada pino dá suporte dependem da DMO

### <a name="encoder-interfaces"></a>Interfaces do codificador

Se o DMO for um codificador de vídeo ou um codificador de áudio, o pino de saída exporá a interface [**IAMStreamConfig.**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) Se o DMO for um codificador de vídeo, o pino de saída também exporá a interface [**IAMVideoCompression.**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) Em ambos os casos, se o DMO dá suporte à interface , o pino delega ao DMO. Caso contrário, o pin fornece sua própria implementação.

### <a name="streaming"></a>Streaming

O filtro usa a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) para manipular todo o streaming. Ele não dá suporte a [**conexões IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) O filtro chama [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) no DMO somente quando recebe dados de upstream (incluindo notificações de fim de fluxo). Portanto, ele não dá suporte a DMOs com nenhum fluxo de entrada.

### <a name="seeking"></a>Procurando

Todas as solicitações de busca são passadas para o filtro upstream, por meio do primeiro pino de entrada no wrapper DMO. Para DMOs de várias saídas, isso significa que o filtro upstream pode receber várias solicitações de busca quando o aplicativo busca o grafo.

### <a name="merit"></a>Mérito

DirectShow atribui a todos os DMOs um valor padrão de **valor de VALOR \_ NORMAL** + 0x800. Esse valor se enquadra **entre VALOR \_ NORMAL** e **\_ PREFERENCIAL DE VALOR.** Os filtros de decodificador geralmente têm um valor de **valor de SEMPRE \_ NORMAL.** Portanto, o gerenciador de grafo de filtro geralmente selecionará um DMO decodificador em um filtro de decodificador. Para substituir o valor padrão, adicione uma entrada do Registro à chave do registro do DMO no CLSID RAIZ de \_ CLASSES \_ \\ HKEY. Inclua um **valor DWORD** chamado "Valor" cujo valor especifica o valor.

### <a name="category"></a>Categoria

O DMO wrapper não aparece sozinho em nenhuma categoria. Quando ele envolve um DMO, ele aparece na categoria DirectShow que corresponde à categoria do DMO, sob o nome do DMO.

### <a name="buffers"></a>Buffers

O DMO wrapper passa buffers de mídia para o DMO que expõem a interface [**IMediaBuffer.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer)

No Windows Vista ou posterior, os buffers de mídia também expõem a interface IServiceProvider. O DMO pode usar essa interface para obter um ponteiro para o exemplo de mídia associado ao buffer. Use o identificador de serviço **IID \_ IMediaSample.** Um vídeo DMO pode usar a interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) da amostra de mídia para definir sinalizadores de intercala no exemplo. O código a seguir mostra como obter o ponteiro para o exemplo de mídia:


```C++
IServiceProvider *pSp = NULL;
IMediaSample2 *pSample2 = NULL;
HRESULT hr = S_OK;

hr = pBuffer->QueryInterface(IID_IServiceProvider, (void**)&pSp);
if (SUCCEEDED(hr))
{
    hr = pSp->QueryService(
        IID_IMediaSample,  // Service identifier.
        IID_IMediaSample2, // Interface identifier.
        (void**)&pSample2
        );
    if (SUCCEEDED(hr))
    {
        // Set flags (not shown).
        pSample2->Release();
    }
    pSp->Release();
}
```



Para obter mais informações sobre sinalizadores de intercala por exemplo, consulte [**ESTRUTURA DE PROPRIEDADES AM \_ SAMPLE2 \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).

### <a name="quality-control"></a>Controle de qualidade

Se o DMO expõe a interface [**IDMOQualityControl,**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) o filtro converte chamadas [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) em seu pin de saída em [**chamadas IDMOQualityControl::SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) no DMO. O *parâmetro rtNow* **de SetNow** é calculado como a soma dos membros **TimeStamp** e **Late** da [**estrutura Quality.**](/windows/win32/api/strmif/ns-strmif-quality)

### <a name="using-the-fiter-in-graphedit"></a>Usando o Fiter no GraphEdit

No GraphEdit, o DMO wrapper não aparece sob seu próprio nome. Em vez disso, cada DMO registrado é listado na categoria de filtro apropriada. Quando você adiciona um DMO  por meio da caixa de diálogo Inserir Filtros, o GraphEdit cria o filtro wrapper DMO e o configura para usar esse DMO.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Objetos de mídia do DirectX](directx-media-objects.md)
</dt> </dl>

 

 
