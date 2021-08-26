---
description: Usando DMOs no DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Usando DMOs no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d056d22e5e9b42795cbe95ce676ac293605453200e0a691d4f0d00374e94cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078646"
---
# <a name="using-dmos-in-directshow"></a>Usando DMOs no DirectShow

aplicativos baseados em DirectShow podem usar DMOs em um grafo de filtro, por meio do filtro de [invólucro de DMO](dmo-wrapper-filter.md) . esse filtro agrega um DMO e manipula todos os detalhes do uso do DMO, como a passagem de dados de e para o DMO, a alocação de objetos [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) e assim por diante.

como o DMO é agregado pelo filtro, o aplicativo pode consultar o filtro para qualquer interface COM que o DMO exponha. No entanto, o aplicativo deve permitir que o filtro manipule todas as operações de streaming no DMO. por exemplo, não defina os tipos de mídia, processe os buffers, libere o DMO, bloqueie o DMO, habilite ou desabilite o controle de qualidade ou defina otimizações de vídeo.

se você souber o identificador de classe (CLSID) de um DMO específico que deseja usar, poderá inicializar o filtro de invólucro de DMO com esse DMO, da seguinte maneira:

1.  chame **CoCreateInstance** para criar o filtro de invólucro de DMO.
2.  consulte o filtro de invólucro de DMO para a interface [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Chame o método [**IDMOWrapperFilter:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) . especifique o CLSID do DMO e o GUID da categoria do DMO. para obter uma lista de categorias de DMO, consulte [guids de DMO](dmo-guids.md).

O código a seguir mostra essas etapas:


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



A função [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera DMOs no registro. essa função usa um conjunto diferente de guids de categoria daqueles usados para filtros de DirectShow.

**Usando o enumerador de dispositivo do sistema com DMOs**

em vez de criar um DMO diretamente, você pode usar o [enumerador de dispositivo do sistema](system-device-enumerator.md), que pode enumerar qualquer categoria de DMO que tenha suporte do método **DMOEnum** . o enumerador de dispositivo do sistema também inclui DMOs quando enumera determinadas categorias de filtro de DirectShow. a tabela a seguir mostra o mapeamento entre categorias de DMO e DirectShow categorias.



| Rótulo | Valor |
|-----------------------------|--------------------------------|
| DMO Categorias                | DirectShow Equivalente          |
| \_codificador de áudio DMOCATEGORY \_ | \_AUDIOCOMPRESSORCATEGORY CLSID |
| \_decodificador de áudio DMOCATEGORY \_ | \_LEGACYAMFILTERCATEGORY CLSID  |
| \_codificador de vídeo DMOCATEGORY \_ | \_VIDEOCOMPRESSORCATEGORY CLSID |
| \_decodificador de vídeo DMOCATEGORY \_ | \_LEGACYAMFILTERCATEGORY CLSID  |



 

O enumerador de dispositivo do sistema retorna uma lista de objetos moniker. se o moniker representar um DMO, o método **IMoniker:: BindToObject** criará automaticamente o filtro de Wrapper de DMO e o inicializará com esse DMO. portanto, o fato de que um DMO está envolvido é transparente para o aplicativo. Para obter mais informações sobre como usar o enumerador de dispositivo do sistema, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).

**Limitações**

Há algumas limitações ao usar o DMOs no DirectShow:

-   o filtro de invólucro de DMO não dá suporte a DMOs com zero entradas, várias entradas ou zero saídas.
-   todas as conexões de pin no filtro de invólucro de DMO usam a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   DirectShow os serviços de edição não dão suporte a efeitos ou transições baseados em DMO.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DMOs](using-dmos.md)
</dt> </dl>

 

 



