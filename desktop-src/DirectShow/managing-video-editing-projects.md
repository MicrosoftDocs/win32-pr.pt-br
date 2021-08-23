---
description: Gerenciando projetos de edição de vídeo
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Gerenciando projetos de edição de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe226f4fdc43889daac8e978086c67bd81c5d8d822902e7c041bf500f2836fb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584446"
---
# <a name="managing-video-editing-projects"></a>Gerenciando projetos de edição de vídeo

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

As dicas a seguir ajudarão você a gerenciar projetos [no DirectShow Editing Services](directshow-editing-services.md).

Alterações na linha do tempo

-   Se você alterar a linha do tempo depois de criar o grafo de filtro, chame [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) novamente para recriar o front-end. Normalmente, isso não afeta o restante do grafo. Ocasionalmente, no entanto, o mecanismo de renderização precisa excluir todo o grafo antes de recriar o front-end. (Por exemplo, isso acontece se você adicionar ou remover um grupo.) O **método ConnectFrontEnd** retorna S \_ WARN \_ OUTPUTRESET para sinalizar que ele excluiu o grafo. Se isso acontecer, seu aplicativo deverá recriar a seção de renderização do grafo.
-   Para remover todos os objetos completamente da linha do tempo, chame o [**método IAMTimeline::ClearAllGroups.**](iamtimeline-clearallgroups.md)

**Limpeza**

-   Quando terminar de usar um mecanismo de renderização, chame o [**método IRenderEngine::ScrapIt.**](irenderengine-scrapit.md) Assim como acontece com qualquer objeto COM, certifique-se de liberar cada ponteiro de interface quando terminar de usá-lo.
-   O mecanismo de renderização não mantém uma contagem de referência na linha do tempo. Não libere a linha do tempo antes de terminar de usá-la e sempre chame **o ScrapIt** no mecanismo de renderização primeiro.
-   Se você liberar todas as referências a uma linha do tempo, não use nenhum dos objetos nessa linha do tempo, mesmo se você estiver mantendo contagens de referência sobre eles.

**Várias instâncias de linha do tempo**

-   Não mova objetos de linha do tempo entre linhas do tempo. Cada objeto em uma linha do tempo deve ser criado por essa linha do tempo. A linha do tempo contém um cache interno com informações sobre os objetos que ela cria; mover objetos de linha do tempo pode interromper o cache.
-   Nunca use a mesma instância de um mecanismo de renderização com mais de uma linha do tempo. O mecanismo de renderização contém um cache com informações sobre a linha do tempo. Várias linhas do tempo interromperão o cache e causarão resultados imprevisíveis. Se você precisar de duas linhas do tempo ativas, faça instâncias separadas de mecanismos de renderização para cada linha do tempo.
-   Uma linha do tempo pode usar mais de um mecanismo de renderização, mas não ao mesmo tempo. Exclua o mecanismo de renderização antigo antes de usar outro mecanismo de renderização. (Normalmente, você faria isso ao mudar do uso do mecanismo de renderização básico para versão prévia para o mecanismo de renderização inteligente para a escrita de arquivo.)

**Persistência**

-   O grafo de filtro não é persistente quando você salva o projeto em um arquivo XML. Portanto, você perde todas as informações relacionadas à recompactação inteligente, ao formato de compactação ou aos parâmetros de compactação. É critério do aplicativo restaurar esses parâmetros depois de carregar um projeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DirectShow de edição](using-directshow-editing-services.md)
</dt> </dl>

 

 



