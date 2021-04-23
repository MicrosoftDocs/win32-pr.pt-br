---
description: Filtro de invólucro de DMO
ms.assetid: ffa6234d-9040-4838-8f51-0cf87df40a5c
title: Filtro de invólucro de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29c5b86bdff4a215ec2ef5854d09a1f842dbf0e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908624"
---
# <a name="dmo-wrapper-filter"></a>Filtro de invólucro de DMO

O filtro de invólucro do DMO permite que um aplicativo do DirectShow use um [objeto de mídia do DirectX](directx-media-objects.md) (DMO) em um grafo de filtro. O filtro encapsula o DMO e manipula todos os detalhes do uso do DMO, como a passagem de dados de e para o DMO. Além disso, o filtro agrega o DMO, portanto, o aplicativo pode consultar o filtro para todas as interfaces COM que o DMO expõe.



| Label | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtrar interfaces                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter), [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)                                                                                                                       |
| Tipos de mídia de pino de entrada                    | Ver comentários                                                                                                                                                                                                                                        |
| Interfaces de pino de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipos de mídia do pino de saída                   | Ver comentários                                                                                                                                                                                                                                        |
| Interfaces de pino de saída                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID do filtro                             | \_DMOWRAPPERFILTER CLSID                                                                                                                                                                                                                            |
| CLSID de página de propriedades                      | Nenhuma página de propriedades                                                                                                                                                                                                                                   |
| Executável                               | Qasf.dll                                                                                                                                                                                                                                           |
| [Núcleo](merit.md)                       | Ver comentários                                                                                                                                                                                                                                        |
| [Categoria do filtro](filter-categories.md) | Ver comentários                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Comentários

### <a name="limitations"></a>Limitações

O invólucro de DMO tem as seguintes limitações:

-   Ele não dá suporte a DMOs com zero entradas, várias entradas ou zero saídas. (Ele dá suporte a DMOs com uma entrada e várias saídas.)
-   Ele não dá suporte a transportes personalizados. Todo o transporte de dados é feito por meio da interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Ele não usa a interface **IMediaObjectInPlace** ; todo o processamento é feito usando métodos [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .

### <a name="pins"></a>Pins

Para cada fluxo de entrada no DMO, o filtro cria um PIN de entrada correspondente. Para cada fluxo de saída, ele cria um pino de saída correspondente. Os tipos de mídia aos quais cada PIN dá suporte depende do DMO

### <a name="encoder-interfaces"></a>Interfaces do codificador

Se o DMO for um codificador de vídeo ou um codificador de áudio, o pino de saída exporá a interface [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) . Se o DMO for um codificador de vídeo, o PIN de saída também expõe a interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) . Em ambos os casos, se o DMO der suporte à interface, o PIN delegará para o DMO. Caso contrário, o PIN fornecerá sua própria implementação.

### <a name="streaming"></a>Streaming

O filtro usa a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) para lidar com todo o streaming. Ele não dá suporte a conexões [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . O filtro chama [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) no DMO somente quando recebe dados de upstream (incluindo notificações de fim de fluxo). Portanto, ele não dá suporte a DMOs com fluxos de entrada zero.

### <a name="seeking"></a>Atingir

Todas as solicitações de busca são passadas para o filtro upstream, por meio do primeiro PIN de entrada no wrapper DMO. Para DMOs de várias saídas, isso significa que o filtro upstream pode receber várias solicitações de busca quando o aplicativo procura o grafo.

### <a name="merit"></a>Núcleo

O DirectShow atribui a todos os DMOs um valor de mérito padrão de **mérito \_ normal** + 0x800. Esse valor cai entre o **mérito \_ normal** e o **mérito \_ preferido**. Os filtros de decodificador geralmente têm um valor de mérito **\_ normal**. Portanto, o Gerenciador de gráfico de filtro geralmente selecionará um decodificador de DMO em um filtro de decodificador. Para substituir o valor de mérito padrão, adicione uma entrada de registro à chave do registro do DMO em \_ classe HKEY \_ raiz \\ CLSID. Inclua um valor **DWORD** chamado "mérito" cujo valor especifique o mérito.

### <a name="category"></a>Categoria

O filtro de invólucro do DMO não aparece sozinho em nenhuma categoria. Quando ele encapsula um DMO, ele aparece na categoria do DirectShow que corresponde à categoria do DMO, sob o nome do DMO.

### <a name="buffers"></a>Buffers

O filtro de invólucro do DMO passa os buffers de mídia para o DMO, que expõem a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) .

No Windows Vista ou posterior, os buffers de mídia também expõem a interface IServiceProvider. O DMO pode usar essa interface para obter um ponteiro para o exemplo de mídia que está associado ao buffer. Use o IMediaSample de **IID \_** do identificador de serviço. Um vídeo DMO pode usar a interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) do exemplo de mídia para definir sinalizadores de entrelaçamento no exemplo. O código a seguir mostra como obter o ponteiro para o exemplo de mídia:


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



Para obter mais informações sobre sinalizadores de entrelaçamento por amostra, consulte a [**\_ estrutura de \_ Propriedades da am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties).

### <a name="quality-control"></a>Controle de qualidade

Se o DMO expõe a interface [**IDMOQualityControl**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-idmoqualitycontrol) , o filtro converte [**IQualityControl:: notificar**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) chamadas em seu pino de saída em [**IDMOQualityControl:: SetNow**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-idmoqualitycontrol-setnow) chamadas no DMO. O parâmetro *rtNow* de **SetNow** é calculado como a soma do **carimbo de data/hora** e dos membros **atrasados** da estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) .

### <a name="using-the-fiter-in-graphedit"></a>Usando o fiter no GraphEdit

No GraphEdit, o filtro de invólucro do DMO não aparece com seu próprio nome. Em vez disso, cada DMO registrado é listado na categoria de filtro apropriada. Quando você adiciona um DMO por meio da caixa de diálogo **Inserir filtros** , o GraphEdit cria o filtro de invólucro do DMO e o configura para usar esse DMO.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Objetos de mídia do DirectX](directx-media-objects.md)
</dt> </dl>

 

 
