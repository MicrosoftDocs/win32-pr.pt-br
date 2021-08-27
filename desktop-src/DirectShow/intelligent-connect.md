---
description: Conexão inteligente
ms.assetid: 938ba1b0-822e-4871-8786-b7eeee243867
title: Conexão inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2248dc936076dfcad1b2ad934da4ef6a8b1e28a260ff75ebca3a63ec6356bf6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107696"
---
# <a name="intelligent-connect"></a>Conexão inteligente

o Intelligent Conexão é o mecanismo que o gerenciador de Graph de filtro usa para criar grafos de filtro. Ele consiste em vários algoritmos relacionados que selecionam filtros e os adiciona ao gráfico de filtro.

Leia este tópico se você estiver tendo problemas para criar um determinado grafo de filtro e desejar solucionar o problema, ou se estiver escrevendo seu próprio filtro e desejar disponibilizá-lo para a criação automática de gráficos.

o Conexão inteligente envolve os seguintes métodos [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) :

-   [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)
-   [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)
-   [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)
-   [**IGraphBuilder:: Conexão**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)

### <a name="igraphbuilderaddsourcefilter"></a>IGraphBuilder::AddSourceFilter

O método [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) adiciona um filtro de origem que pode renderizar um arquivo especificado. Em primeiro lugar, ele procura no registro e faz a correspondência com o protocolo (como `https://` ), a extensão de nome de arquivo ou um conjunto de *bytes de cheque* predeterminados, que são bytes em determinados deslocamentos no arquivo que correspondem a determinados padrões. Para obter detalhes, consulte [registrando um tipo de arquivo personalizado](registering-a-custom-file-type.md). Supondo que o método Localize um filtro de origem apropriado, ele cria uma instância desse filtro, adiciona-o ao grafo e chama o método [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) do filtro com o nome do arquivo.

### <a name="igraphbuilderrender"></a>IGraphBuilder:: render

O método [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) cria uma subseção de um grafo. Ele inicia de um PIN de saída não conectado e funciona downstream, adicionando novos filtros, conforme necessário. O filtro inicial já deve estar no grafo. Em cada etapa, o método **render** procura um filtro que possa se conectar ao filtro anterior. O fluxo pode ramificar se um filtro de conexão tiver vários Pins de saída. A pesquisa para quando cada fluxo tem um processador. Se o método **render** ficar preso, ele poderá fazer backup e tentar novamente usando um conjunto diferente de filtros.

Para conectar cada pino de saída, o método [**render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) faz o seguinte:

1.  se o pin der suporte à interface [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) , o gerenciador de Graph de filtro delegará todo o processo ao método [**IStreamBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-istreambuilder-render) do pin. Ao expor essa interface, o PIN assume a responsabilidade de criar o restante do grafo, até o renderizador. No entanto, poucos Pins dão suporte a essa interface.
2.  o filtro Graph Manager tenta usar filtros que são armazenados em cache na memória, se houver. durante o processo de Conexão inteligente, o filtro Graph gerenciador pode armazenar em cache filtros de etapas anteriores no processo. (além disso, consulte [criação dinâmica de Graph](dynamic-graph-building.md).)
3.  se o gráfico de filtro contiver qualquer filtro com pins de entrada desconectados, o filtro Graph Manager os tentará em seguida. Você pode forçar o método [**render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) a tentar um filtro específico adicionando esse filtro ao grafo antes de chamar **render**.
4.  a partir do Windows 7, DirectShow tem uma lista de filtros preferenciais para determinados subtipos de mídia. se houver um filtro preferencial para o tipo de mídia que está sendo processado, o filtro Graph Manager tentará esse filtro em seguida. Um aplicativo pode modificar a lista de filtros preferenciais usando a interface [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) . As alterações na lista afetam o processo atual do aplicativo e são descartadas após o término do processo.
5.  por fim, se nenhum filtro adequado for encontrado, o filtro Graph gerenciador pesquisará o registro, usando o método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) . Ele tenta corresponder os tipos de mídia preferenciais do pino de saída em relação aos tipos de mídia listados no registro.

    Cada filtro é registrado com um *mérito*, um valor numérico que indica como é preferível o filtro, em relação a outros filtros. O método [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) retorna filtros em ordem de mérito, com um mérito mínimo de **mérito \_ \_ não \_ use** + 1. Ele ignora filtros com um mérito de **mérito não \_ \_ \_ usa** ou menos. Os filtros também são agrupados em categorias, definidos pelo GUID. As categorias em si têm mérito, e o método **EnumMatchingFilters** ignora qualquer categoria com um mérito **de \_ mérito \_ não \_ usa** ou menos, mesmo que os filtros nessa categoria tenham valores de mérito mais altos.

    a partir do Windows 7, DirectShow tem uma lista de filtros bloqueados para determinados subtipos de mídia. o filtro Graph Manager ignora os filtros nesta lista. Um aplicativo pode modificar a lista de filtros bloqueados usando a interface [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) . As alterações feitas nessa lista afetam o processo atual do aplicativo e são descartadas após o término do processo.

Para resumir, o método [**render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) tenta filtros na seguinte ordem:

1.  Use [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder).
2.  Experimente os filtros em cache.
3.  Tente filtros no grafo.
4.  Windows 7 ou posterior: tente o filtro preferencial para o tipo de mídia, se houver.
5.  Pesquisar filtros no registro.

### <a name="igraphbuilderrenderfile"></a>IGraphBuilder:: RenderFile

O método [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) cria um grafo de reprodução padrão a partir de um nome de arquivo. Internamente, esse método usa [**AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para localizar o filtro de origem correto e [**renderizar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) para compilar o restante do grafo.

### <a name="igraphbuilderconnect"></a>IGraphBuilder:: Conexão

o método [**IGraphBuilder:: Conexão**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) conecta um pino de saída a um pin de entrada. Esse método adiciona filtros intermediários, se necessário, usando uma variação do algoritmo descrito para o método [**render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) :

1.  Tente uma conexão direta entre os filtros, sem filtros intermediários.
2.  Experimente os filtros em cache.
3.  Tente filtros no grafo.
4.  Windows 7 ou posterior: tente o filtro preferencial para o tipo de mídia, se houver.
5.  Pesquisar filtros no registro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtrar categorias](filter-categories.md)
</dt> <dt>

[Núcleo](merit.md)
</dt> <dt>

[simulando Graph compilando com GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[Criando o filtro Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



