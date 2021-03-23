---
title: Visão geral da Associação de recursos
description: A chave para a associação de recursos no DirectX 12 são os conceitos de um descritor, tabelas de descritores, heaps de descritores e uma assinatura de raiz.
ms.assetid: 92E100CA-822D-46B1-BD37-FF57C3FB703D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc7e78255c123777716eddb43d9443e19113b34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104874"
---
# <a name="resource-binding-overview"></a>Visão geral da Associação de recursos

A chave para a associação de recursos no DirectX 12 são os conceitos de um *descritor*, *tabelas de descritores*, *heaps de descritores* e uma *assinatura de raiz*.

-   [Recursos e pipeline de gráficos](#resources-and-the-graphics-pipeline)
-   [Tipos de recursos e exibições](#resource-types-and-views)
-   [Fluxo de controle de associação de recursos](#resource-binding-overview)
-   [Subalocação](#suballocation)
-   [Liberando recursos](#freeing-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="resources-and-the-graphics-pipeline"></a>Recursos e pipeline de gráficos

Os recursos do sombreador (como texturas, tabelas constantes, imagens, buffers e assim por diante) não são associados diretamente ao pipeline do sombreador; em vez disso, eles são referenciados por meio de um *descritor*. Um descritor é um objeto pequeno que contém informações sobre um recurso.

Os descritores são agrupados em tabelas de *descritores* de formulário. Cada tabela de descritores armazena informações sobre um intervalo de tipos de recursos. Há muitos tipos diferentes de recursos. Os recursos mais comuns são:

-   Exibições de buffer de constantes (CBVs)
-   Exibições de acesso não ordenado (UAVs)
-   Exibições de recursos do sombreador (SRVs)
-   Amostradores

Os descritores SRV, UAV e CBVs podem ser combinados na mesma tabela de descritores.

Os pipelines de computação e gráficos têm acesso aos recursos referenciando em tabelas de descritores por índice.

As tabelas de descritores são armazenadas em um *heap de descritor*. Os heaps de descritores idealmente conterão todos os descritores (em tabelas de descritores) para que um ou mais quadros sejam renderizados. Todos os recursos serão armazenados em heaps de modo de usuário.

Outro conceito é o de uma *assinatura raiz*. A assinatura raiz é uma Convenção de associação, definida pelo aplicativo, que é usada por sombreadores para localizar os recursos aos quais precisam de acesso. A assinatura raiz pode armazenar:

-   Índices para tabelas de descritores em um heap de descritor, em que o layout da tabela de descritores foi predefinido.
-   As constantes, portanto, os aplicativos podem ligar constantes definidas pelo usuário (conhecidas como *constantes raiz*) diretamente a sombreadores sem precisar passar por descritores e tabelas de descrição.
-   Um número muito pequeno de descritores diretamente dentro da assinatura raiz, como uma CBV (exibição de buffer constante) que muda por empate, poupando assim o aplicativo de precisar colocar esses descritores em um heap de descritor.

Em outras palavras, a assinatura raiz fornece otimizações de desempenho adequadas para pequenas quantidades de dados que são alteradas por empate.

O design do Direct3D 12 para associação o separa de outras tarefas, como gerenciamento de memória, gerenciamento de tempo de vida de objeto, rastreamento de estado e sincronização de memória (consulte [as diferenças no modelo de associação do Direct3D 11](binding-model.md)). A ligação do Direct3D 12 foi projetada para ser baixa sobrecarga e otimizada para as chamadas à API que são feitas com mais frequência. Ele também é escalonável em hardware de ponta a ponta e é escalonável do mais antigo (o pipeline Direct3D 11 mais linear) para as abordagens mais recentes (mais paralelas) à programação do mecanismo de gráficos.

## <a name="resource-types-and-views"></a>Tipos de recursos e exibições

Os tipos de recurso são os mesmos que o Direct3D 11, ou seja:

-   Texture1D e Texture1DArray
-   Texture2D e Texture2DArray, Texture2DMS, Texture2DMSArray
-   Texture3D
-   Buffers (digitados, estruturados e brutos)

As exibições de recursos são semelhantes, mas ligeiramente diferentes das exibições do Direct3D 11, do vértice e do buffer do índice foram adicionadas.

-   Modo de exibição de buffer constante (CBV)
-   Modo de exibição de acesso não ordenado (UAV)
-   Exibição de recurso de sombreador (SRV)
-   Amostradores
-   Renderizar exibição de destino (RTV)
-   Exibição de estêncil de profundidade (DSV)
-   IBV (exibição de buffer de índice)
-   Exibição de buffer de vértice (VBV)
-   Exibição de saída de fluxo (SOV)

Somente as quatro primeiras dessas exibições são realmente visíveis para os sombreadores, consulte [heaps de descritores visíveis do sombreador](shader-visible-descriptor-heaps.md) e [heaps de descritor visíveis sem sombreador](non-shader-visible-descriptor-heaps.md).

## <a name="resource-binding-flow-of-control"></a>Fluxo de controle de associação de recursos

Concentrando-se apenas nas assinaturas raiz, nos descritores raiz, nas constantes raiz, nas tabelas de descritores e nos heaps de descritores, o fluxo de lógica de renderização de um aplicativo deve ser semelhante ao seguinte:

-   Crie um ou mais objetos de assinatura raiz – um para cada configuração de ligação diferente que um aplicativo precisa.
-   Crie sombreadores e estado de pipeline com os objetos de assinatura raiz com os quais eles serão usados.
-   Crie um (ou, se necessário, mais) heaps de descritores que conterão todos os descritores SRV, UAV e CBV para cada quadro de renderização.
-   Inicialize os heaps de descritores com descriprs, onde possível para conjuntos de descritores que serão reutilizados em vários quadros.
-   Para cada quadro a ser renderizado:
    -   Para cada lista de comandos:
        -   Defina a assinatura raiz atual a ser usada (e altere se necessário durante o processamento – o que raramente é necessário).
        -   Atualize algumas constantes da assinatura raiz e/ou descritores de assinatura raiz para a nova exibição (como projeções do mundo/exibição).
        -   Para cada item a ser desenhado:
            -   Defina os novos descritores nos heaps do descritor conforme necessário para a renderização por objeto. Para heaps de descritores visíveis para sombreador, o aplicativo deve se certificar de usar o espaço de heap de descritor que ainda não está sendo referenciado pela renderização que poderia estar em trânsito – por exemplo, alocar espaço linearmente por meio do heap de descritor durante a renderização.
            -   Atualize a assinatura raiz com ponteiros para as regiões necessárias dos heaps de descritor. Por exemplo, uma tabela de descritores pode apontar para alguns descritores estáticos (inalteráveis) inicializados anteriormente, enquanto outra tabela de descritores pode apontar para alguns descriprs dinâmicos configurados para a renderização atual.
            -   Atualize algumas constantes de assinatura raiz e/ou descritores de assinatura raiz para renderização por item.
            -   Defina o estado do pipeline para o item a ser desenhado (somente se a alteração for necessária), compatível com a assinatura de raiz atualmente associada.
            -   Draw
        -   Repetir (próximo item)
    -   REPEAT (próxima lista de comandos)
    -   Estritamente quando a GPU termina com qualquer memória que não será mais usada, ela pode ser liberada. As referências de descritores a ele não precisam ser excluídas se a renderização adicional que usa esses descritores não for enviada. Portanto, a renderização subsequente pode apontar para outras áreas em heaps de descritor ou os descritores obsoletos podem ser substituídos por descritores válidos para reutilizar o espaço de heap do descritor.
-   Repetir (próximo quadro)

Observe que outros tipos de descritores, RTVs (exibições de destino de renderização), DSV (exibições de estêncil de profundidade), IBVs (exibições de buffer de índice), VBVs (exibições de buffer de vértice) e SOV (exibições de objeto do sombreador) são gerenciados de forma diferente. O driver manipula o controle de versão do conjunto de descritores associado para cada desenho durante a gravação da lista de comandos (semelhante à forma como as associações de assinatura raiz têm controle de versão do hardware/driver). Isso é diferente do conteúdo de heaps de descritores visíveis para sombreador, para os quais o aplicativo deve alocar manualmente por meio do heap, pois faz referência a descritores diferentes entre o desenho. O controle de versão do conteúdo de heap que está visível para sombreador é deixado para o aplicativo porque permite que os aplicativos façam coisas como os descritores de reutilização que não mudam ou usam grandes conjuntos estáticos de descritores e usam a indexação de sombreador (como por ID de material) para selecionar os descritores a serem usados a partir do heap de descrição ou usar combinações de técnicas para O hardware não está equipado para lidar com esse tipo de flexibilidade para os outros tipos de descritores (RTV, DSV, IBV, VBV, SOV).

## <a name="suballocation"></a>Subalocação

No Direct3D 12, o aplicativo tem controle de baixo nível sobre o gerenciamento de memória. Em versões anteriores do Direct3D, incluindo o Direct3D 11, haveria uma alocação por recurso. No Direct3D 12, o aplicativo pode usar a API para alocar um grande bloco de memória, maior do que qualquer objeto individual precisaria. Depois que isso for feito, o aplicativo poderá criar descritores para apontar para seções desse grande bloco de memória. Esse processo de decidir o que colocar onde (blocos menores dentro do bloco grande) é conhecido como *subalocação*. Habilitar o aplicativo para fazer isso pode produzir ganhos no uso eficiente da computação e da memória. Por exemplo, a renomeação de recursos é renderizada como obsoleta. Em vez disso, os aplicativos podem usar limites para determinar quando um recurso específico está sendo usado e quando não é por meio do isolamento nas execuções da lista de comandos, em que a lista de comandos requer o uso desse recurso específico.

## <a name="freeing-resources"></a>Liberando recursos

Antes que qualquer memória que tenha sido associada ao pipeline possa ser liberada, a GPU deve ser concluída com ela.

Aguardar a renderização de quadros provavelmente é a maneira mais grosseira de ter certeza de que a GPU foi concluída. Em um detalhamento mais detalhado, você pode usar novamente os limites — quando um comando é registrado em uma lista de comandos que você deseja controlar a conclusão, insira um limite imediatamente após ele. Em seguida, você pode fazer várias operações de sincronização com a cerca. Você envia um novo trabalho (listas de comandos) que aguarda até que um limite especificado tenha passado na GPU, o que indica que tudo antes de ser concluído ou que você pode solicitar que um evento de CPU seja gerado quando a cerca passada (que o aplicativo pode estar aguardando com um thread em suspensão). No Direct3D 11, isso era `EnqueueSetEvent` ().

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associação de recursos](resource-binding.md)
</dt> </dl>

 

 




