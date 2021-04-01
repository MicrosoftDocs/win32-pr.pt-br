---
description: Usando o DMOs no DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Usando o DMOs no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c90513649756a49067e523390292d4b44e1eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091739"
---
# <a name="using-dmos-in-directshow"></a>Usando o DMOs no DirectShow

Aplicativos baseados no DirectShow podem usar DMOs em um grafo de filtro, por meio do filtro de [invólucro do DMO](dmo-wrapper-filter.md) . Esse filtro agrega um DMO e manipula todos os detalhes do uso do DMO, como a passagem de dados de e para o DMO, a alocação de objetos [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) e assim por diante.

Como o DMO é agregado pelo filtro, o aplicativo pode consultar o filtro para todas as interfaces COM que o DMO expõe. No entanto, o aplicativo deve permitir que o filtro manipule todas as operações de streaming no DMO. Por exemplo, não defina os tipos de mídia, processe os buffers, libere o DMO, bloqueie o DMO, habilite ou desabilite o controle de qualidade ou defina otimizações de vídeo.

Se você souber o identificador de classe (CLSID) de um DMO específico que deseja usar, poderá inicializar o filtro de invólucro de DMO com esse DMO, da seguinte maneira:

1.  Chame **CoCreateInstance** para criar o filtro de invólucro do DMO.
2.  Consulte o filtro de invólucro do DMO para a interface [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Chame o método [**IDMOWrapperFilter:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) . Especifique o CLSID do DMO e o GUID da categoria do DMO. Para obter uma lista de categorias de DMO, consulte [GUIDs do DMO](dmo-guids.md).

O código a seguir mostra estas etapas:


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



A função [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera DMOs no registro. Essa função usa um conjunto diferente de GUIDs de categoria dos que são usados para filtros do DirectShow.

**Usando o enumerador de dispositivo do sistema com DMOs**

Em vez de criar diretamente um DMO, você pode usar o [enumerador de dispositivo do sistema](system-device-enumerator.md), que pode enumerar qualquer categoria de DMO com suporte do método **DMOEnum** . O enumerador de dispositivo do sistema também inclui DMOs quando enumera determinadas categorias de filtro do DirectShow. A tabela a seguir mostra o mapeamento entre as categorias de DMO e as categorias do DirectShow.



|                             |                                |
|-----------------------------|--------------------------------|
| Categoria de DMO                | Equivalente do DirectShow          |
| \_codificador de áudio DMOCATEGORY \_ | \_AUDIOCOMPRESSORCATEGORY CLSID |
| \_decodificador de áudio DMOCATEGORY \_ | \_LEGACYAMFILTERCATEGORY CLSID  |
| \_codificador de vídeo DMOCATEGORY \_ | \_VIDEOCOMPRESSORCATEGORY CLSID |
| \_decodificador de vídeo DMOCATEGORY \_ | \_LEGACYAMFILTERCATEGORY CLSID  |



 

O enumerador de dispositivo do sistema retorna uma lista de objetos moniker. Se o moniker representar um DMO, o método **IMoniker:: BindToObject** criará automaticamente o filtro de invólucro de DMO e o inicializará com esse DMO. Portanto, o fato de que um DMO está envolvido é transparente para o aplicativo. Para obter mais informações sobre como usar o enumerador de dispositivo do sistema, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).

**Limitações**

Há algumas limitações ao usar o DMOs no DirectShow:

-   O filtro de invólucro de DMO não dá suporte a DMOs com zero entradas, várias entradas ou zero saídas.
-   Todas as conexões de PIN no filtro de invólucro do DMO usam a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Os serviços de edição do DirectShow não dão suporte a transições ou efeitos baseados em DMO.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DMOs](using-dmos.md)
</dt> </dl>

 

 



