---
description: selecionando um decodificador em serviços de edição DirectShow
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: selecionando um decodificador em serviços de edição DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcff63d44918a189f49e11527fe6fef35d108b7f20c1dadefa0a045e2c895b0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341266"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a>selecionando um decodificador em serviços de edição DirectShow

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

quando os [serviços de edição de DirectShow](directshow-editing-services.md) (DES) renderizam um projeto de edição de vídeo, o mecanismo de renderização seleciona automaticamente os decodificadores necessários. Isso pode acontecer dentro do método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) ou, mais dinamicamente, durante a renderização.

Um usuário pode instalar vários decodificadores que são capazes de decodificar um arquivo específico. quando vários decodificadores estão disponíveis, o DES usa o algoritmo de [Conexão inteligente](intelligent-connect.md) para selecionar o decodificador.

Não há como o aplicativo especificar diretamente qual decodificador usar. No entanto, você pode escolher o decodificador indiretamente por meio da interface de retorno de chamada [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) . Ao implementar essa interface em seu aplicativo, você pode receber notificações durante o processo de criação de grafo e rejeitar determinados filtros do grafo.

Comece implementando uma classe que expõe a interface [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) :


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



em seguida, crie uma instância do filtro Graph Manager e registre sua classe para receber notificações de retorno de chamada:


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



em seguida, crie o mecanismo de renderização e chame o método [**IRenderEngine:: SetFilterGraph**](irenderengine-setfiltergraph.md) com um ponteiro para o filtro Graph Manager. isso garante que o mecanismo de renderização não crie seu próprio filtro Graph Manager, mas, em vez disso, usa a instância que você configurou para retornos de chamada.


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



quando o projeto é renderizado, o método [**IAMGraphBuilderCallback:: SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) do aplicativo é chamado imediatamente antes de o filtro Graph Manager criar um novo filtro. O método **SelectedFilter** recebe um ponteiro para uma interface **IMoniker** que representa um moniker para o filtro. Examine o moniker e, se você decidir rejeitar o filtro, retorne um código de falha do método **SelectedFilter** .

A parte difícil é identificar quais monikers representam decodificadores — e, em particular, quais monikers representam os decodificadores que você deseja rejeitar. Uma solução é a seguinte:

-   Antes de renderizar o projeto, use o método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) para criar uma lista de filtros que são registrados como aceitando o tipo de entrada desejado. Para tipos de compactação de vídeo ou áudio, essa lista deve ser mapeada para um conjunto de decodificadores.
-   O método **EnumMatchingFilters** retorna uma coleção de monikers. Para cada moniker na coleção, obtenha a propriedade **DisplayName** , conforme descrito em [usando o mapeador de filtro](using-the-filter-mapper.md).
-   Armazene uma lista dos nomes de exibição, mas omita o nome de exibição que corresponde ao filtro que você deseja usar para decodificação. Os nomes de exibição dos filtros de software têm o seguinte formato:

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    onde

    ```C++
    CategoryGUID
    ```

    

    é o GUID da categoria de filtro e

    ```C++
    FilterCLSID
    ```

    

    é o CLSID do filtro. Para DMOs, o formato é o mesmo, mas é alterado `sw` para `dmo` .

    Agora, a lista contém nomes de exibição para cada filtro que gera o tipo de mídia desejado, mas não é seu filtro preferido.

-   No método **SelectedFilter** , obtenha a propriedade **DisplayName** no moniker proposto e verifique-a na lista armazenada. Se o nome de exibição corresponder a uma entrada na lista, rejeite esse filtro. Caso contrário, aceite-o retornando S \_ OK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um Project](rendering-a-project.md)
</dt> </dl>

 

 



