---
title: Estratégias de gerenciamento de memória
description: Um Gerenciador de memória para o Direct3D 12 poderia ficar muito complicado com todas as diferentes camadas de suporte, para adaptadores de uma ou discretos (não de uma) e com uma variedade considerável de diferenças de arquitetura entre os adaptadores de GPU. A estratégia recomendada para o gerenciamento de memória do Direct3D 12, descrita nesta seção, é \ 0034; classificar, orçamento e fluxo \ 0034;.
ms.assetid: BC9894F7-D496-46F2-A5C3-C7CA31FD4BA8
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dad04055a5acdeeeaead3a56f0bd04e64aa90fe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548261"
---
# <a name="memory-management-strategies"></a>Estratégias de gerenciamento de memória

Um Gerenciador de memória para o Direct3D 12 poderia ficar muito complicado com todas as diferentes camadas de suporte, para adaptadores de uma ou discretos (não de uma) e com uma variedade considerável de diferenças de arquitetura entre os adaptadores de GPU.

A estratégia recomendada para o gerenciamento de memória do Direct3D 12, descrita nesta seção, é "classificar, orçamento e fluxo".

-   [Tipos de recursos](#resource-types)
-   [Orçamento de memória](#memory-budget)
-   [Estratégia de classificação](#classification-strategy)
-   [Tópicos relacionados](#related-topics)

## <a name="resource-types"></a>Tipos de recurso

O conceito básico de "recurso confirmado" (criando espaços de endereços virtuais e físicos inicializados na memória física gerenciada) já existe desde o Direct3D 9, embora o endereçamento virtual (VA) e o endereçamento físico possam ser separados no Direct3D 12 para permitir que o aplicativo gerencie cuidadosamente a memória física.

Além dos recursos confirmados, a construção de heap do Direct3D 12 permite dois outros tipos de recurso: "posicionado" e "reservado". No Direct3D 11, um recurso "reservado" era conhecido como "recurso ao lado".

Os recursos reservados diferem dos recursos inseridos, pois os recursos reservados têm seu próprio espaço de endereço virtual de GPU exclusivo. Isso permite uma grande alocação do espaço de VA de antecedência e, em seguida, habilita o mapeamento de páginas de VA para determinadas seções do heap posteriormente, e o aplicativo reconfigura a organização em tempo real. O espaço de VA é contíguo e pode ser mapeado de forma grosseira para.

O recurso reservado pode ser feito para referenciar regiões no heap com chamadas à API, como [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) , e podem se tornar residentes pelo aplicativo atualizando tabelas de páginas dinamicamente. Quando um intervalo de VA é mapeado para nulo ou para um heap não residente, essa parte do recurso é considerada não-residente. Quando um intervalo de VA é mapeado para um heap residente, essa parte do recurso é considerada residente. Os heaps são residentes após a criação.

Os recursos inseridos são um design muito mais simples, sendo simplesmente um ponteiro para uma determinada região de um heap (por exemplo, uma região de 1Mb para uma textura em um heap de 5 MB). As barreiras de alias permitem o uso de recursos inseridos sobrepostos (consulte [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) e [**ResourceBarrier**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)).

Os recursos reservados não estão disponíveis em todos os hardwares do Direct3D 12, e os recursos colocados são um fallback razoável, embora os recursos inseridos devam ser contíguos e não possam ser parcialmente residentes.

## <a name="memory-budget"></a>Orçamento de memória

No Direct3D 12, ao alocar um heap, você está criando o aspecto de memória física de um recurso confirmado. Uma opção de segmento de memória mais explícita está disponível no Direct3D 12 (escolhendo entre vídeo e memória do sistema). Os adaptadores de um só têm um único segmento de memória, a memória do sistema.

As GPUs não dão suporte à falha de página, de modo que os desenvolvedores devem estar atentos de que não estão excedendo a confirmação, especialmente em sistemas, digamos com apenas 1 GB de memória do sistema. Se um aplicativo efetuar a confirmação, o sistema operacional usará o agendamento refinado de processos mais esparsos por sua demanda na memória física. O Agendador congelará processos em primeiro plano e, essencialmente, paginará um pouco, a fim de paginar um processo em segundo plano que deseja executar. A memória física disponível pode variar consideravelmente dependendo do que o usuário está fazendo em segundo plano (como executar um navegador ou assistir a um vídeo).

A API para o orçamento de memória é [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo). Para adaptadores discretos "local" é a memória de vídeo, "não local" é a memória do sistema. Para adaptadores de uma não local é sempre zero. Uma pergunta de design é se o mecanismo gerenciará orçamentos ou apenas o orçamento local. Gerenciar apenas o orçamento local é mais simples, mas tem algumas limitações; por exemplo, digamos que haja um orçamento local máximo de 1 GB, todos os heaps serão provenientes de 1 GB em um sistema de uma e não haverá estouro na memória do sistema (claramente, pois não há nenhum).

Desde a Direct3D11 de memória gerenciada para aplicativos, os recursos não utilizados essencialmente seriam paginados.

Escolha as dimensões de recurso mais apropriadas. Considere se o tamanho de um recurso é apropriado para a situação na qual o aplicativo está realmente sendo executado. Alguns usuários podem executar o aplicativo em uma janela ou com uma resolução de tela de 800x600.

## <a name="classification-strategy"></a>Estratégia de classificação

Para gerenciar recursos com eficiência em cenários de limite de memória, considere classificar os recursos no seguinte:



| classificação      | Exemplos                                                                                         | Objetos e recursos de API                                                                                           | Notas de gerenciamento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crítico            | Interface do usuário do jogo                                                                                          | Alocador de comando, filas de comando, heaps de consulta, recursos e heaps de recursos.                                      | Esses elementos devem ficar em memória não paginável/sempre confirmada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Escalado/opcional    | Modelos e texturas específicos de nível, cadeias de permuta, caixas céu, modelos de caractere de jogador de primeira pessoa | Recursos e heaps. Os recursos confirmados, mas também os recursos colocados e reservados podem funcionar também.          | Integre o orçamento de residência de memória nos algoritmos de renderização. Escolha o nível apropriado de detalhes disponíveis e reavalie menos de uma vez por quadro. As técnicas incluem o uso de recursos de tamanho variável e dimensionamento da cadeia de permuta.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| Recursos reutilizados   | Buffers de sombra, recursos de renderização adiados, recursos de pós-processamento, caches de dados de iluminação    | Recursos e heaps. Sobreposição de recursos posicionados em heaps e barreiras de alias.                                  | Reutilize os recursos grandes ou regiões de heap dentro de um quadro para reduzir os requisitos para todo o quadro. Use a técnica de reutilização de memória dentro do quadro. No Direct3D 11, os aplicativos podiam reutilizar recursos com o mesmo tipo e dimensões possivelmente grandes o suficiente. Os heaps do Direct3D 12 permitem a sobreposição de recursos para uma reutilização muito mais simples e maior.<br/>                                                                                                                                                                                                                              |
| Recursos de streaming | Terrenos, texturas e geometrias do Open World                                                        | Recursos e heaps. Criação de thread livre, threads de CPU em segundo plano e filas e listas de comandos de cópia em segundo plano. | Residência parcial, normalmente baseada na visibilidade (usando a exibição frustum ou avaliação baseada em distância) e reavaliar a residência precisa de cada quadro.<br/> A técnica de usar um gerenciamento de residência parcial por bloco e a reutilização entre quadros está disponível quando o adaptador de GPU dá suporte a recursos reservados dentro de heaps.<br/> Usando a técnica de uso da reutilização de memória entre quadros, a residência parcial de subrecurso pode ser realizada, mas é menos adequada. Os recursos inseridos com heaps devem permitir reciclagem mais rápida, mas os recursos confirmados podem ser usados como um fallback.<br/> |



 

Quanto mais aplicativos gravitam ao streaming de recursos para a maior parte do trabalho, mais eles aproveitarão os recursos colocados e reservados, o que maximizará a reutilização da memória entre essas quatro classificações. Quanto mais aplicativos forem transmitidos, mais eles terão orçamento e priorizarão a largura de banda.

Normalmente, com os mecanismos gráficos do Direct3D 12, é necessário respeitar um orçamento mais diversificado e dinâmico e fazê-lo mais estritamente do que fazia no passado. Os melhores aplicativos localizarão todas as quatro categorias no orçamento fornecido ao processo, dimensionando o jogo para o aplicativo móvel em segundo plano para orçamentos discretos em tela inteira. Mas, muitos aplicativos provavelmente terão dificuldades ao iniciar com muitos tipos críticos de categoria de recursos. Os recursos habilitados para Direct3D 11 são criados anonimamente e ocupam o status crítico sem afetar o desempenho. No entanto, para o Direct3D 12, os desenvolvedores devem procurar por recursos criados aleatoriamente em todo o mecanismo e middleware e atribuí-los novamente a uma das outras categorias.

Outras áreas problemáticas são componentes de middleware, controles de usuário e streaming intra-frame. Os componentes de middleware podem não ser expostos a um orçamento, nem devem trabalhar juntos. Os componentes de middleware provavelmente poderiam expor recursos como técnicas de renderização; e o aplicativo poderia depender de expor as configurações de middleware e de mecanismo. Os desenvolvedores poderiam contar com o Direct3D 11 para fazer a paginação e atingir a taxa de quadros correta. Em alguns casos, os aplicativos do Direct3D 11 podem ter sido paginando o conteúdo dos recursos dentro e fora de cada quadro; e isso resultou em taxas de quadros aceitáveis para o usuário. A maioria dos mecanismos só transmite dados de recursos como uma atividade em segundo plano, em que ele não tem nenhum fallback normal para streaming de alta prioridade dentro do quadro. Solicitar que os mecanismos implementem que erode alguns dos ganhos de sobrecarga da CPU que eles buscam ao migrar para o Direct3D 12. Os desenvolvedores de mecanismos podem considerar separar seus quadros em fases para fornecer mais oportunidades para recursos reutilizáveis; e, provavelmente, trabalhar com fornecedores de middleware para dar suporte a recursos e heaps posicionados para reutilização de memória intra-frame.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
</dt> <dt>

[**CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)
</dt> <dt>

[Guia de programação do Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Gerenciamento de memória](memory-management.md)
</dt> <dt>

[Associação de recursos](resource-binding.md)
</dt> </dl>

 

