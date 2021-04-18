---
description: Gerenciando projetos de edição de vídeo
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Gerenciando projetos de edição de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105756608"
---
# <a name="managing-video-editing-projects"></a>Gerenciando projetos de edição de vídeo

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

As dicas a seguir ajudarão você a gerenciar projetos nos [serviços de edição do DirectShow](directshow-editing-services.md).

Alterações na linha do tempo

-   Se você alterar a linha do tempo depois de criar o grafo de filtro, chame [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) novamente para recriar o front-end. Normalmente, isso não afeta o restante do grafo. Ocasionalmente, no entanto, o mecanismo de renderização precisa excluir o grafo inteiro antes de recompilar o front-end. (Por exemplo, isso acontece se você adicionar ou remover um grupo.) O método **ConnectFrontEnd** retorna S \_ \_ OUTPUTRESET warn para sinalizar que excluiu o grafo. Se isso acontecer, seu aplicativo deverá recriar a seção de renderização do grafo.
-   Para remover completamente todos os objetos da linha do tempo, chame o método [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) .

**Limpeza**

-   Quando você terminar de usar um mecanismo de renderização, chame o método [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) . Como com qualquer objeto COM, certifique-se de liberar todos os ponteiros de interface quando terminar de usá-lo.
-   O mecanismo de renderização não mantém uma contagem de referência na linha do tempo. Não libere a linha do tempo antes de terminar de usá-la e sempre chame **ScrapIt** no mecanismo de processamento primeiro.
-   Se você liberar todas as referências a uma linha do tempo, não use nenhum dos objetos nessa linha do tempo, mesmo se você estiver mantendo contagens de referência neles.

**Várias instâncias da linha do tempo**

-   Não mova objetos do cronograma entre as linhas do tempo. Cada objeto em uma linha do tempo deve ser criado por essa linha do tempo. A linha do tempo contém um cache interno com informações sobre os objetos que ele cria; mover objetos de linha do tempo pode interromper o cache.
-   Nunca use a mesma instância de um mecanismo de renderização com mais de uma linha do tempo. O mecanismo de renderização mantém um cache com informações sobre a linha do tempo. Várias linhas do tempo interromperão o cache e causarão resultados imprevisíveis. Se você precisar de duas linhas do tempo ativas, faça instâncias separadas de mecanismos de renderização para cada linha do cronograma.
-   Uma linha do tempo pode usar mais de um mecanismo de renderização, mas não ao mesmo tempo. Exclua o mecanismo de processamento antigo antes de usar outro mecanismo de renderização. (Normalmente, você faria isso quando alternar de usando o mecanismo de renderização básico para visualização para o mecanismo de processamento inteligente para gravação de arquivo.)

**Persistência**

-   O grafo de filtro não é persistente quando você salva o projeto em um arquivo XML. Portanto, você perde todas as informações relacionadas à recompactação inteligente, ao formato de compactação ou aos parâmetros de compactação. Cabe ao aplicativo restaurar esses parâmetros depois de carregar um projeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando os serviços de edição do DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



