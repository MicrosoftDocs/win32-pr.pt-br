---
title: Estratégias de gerenciamento de memória
description: Um gerenciador de memória para Direct3D 12 pode ficar muito complicado rapidamente com todas as diferentes camadas de suporte, para adaptadores UMA ou discretos (não UM) e com uma variedade considerável de diferenças de arquitetura entre adaptadores de GPU. A estratégia recomendada para o gerenciamento de memória do Direct3D 12, descrita nesta seção, é \ 0034;classify, budget and stream \ 0034;.
ms.assetid: BC9894F7-D496-46F2-A5C3-C7CA31FD4BA8
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7797b933a759afd0ccfb959672e5c595cefa21712f3488e61b4f99b8a57b0893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123798"
---
# <a name="memory-management-strategies"></a>Estratégias de gerenciamento de memória

Um gerenciador de memória para Direct3D 12 pode ficar muito complicado rapidamente com todas as diferentes camadas de suporte, para adaptadores UMA ou discretos (não UM) e com uma variedade considerável de diferenças de arquitetura entre adaptadores de GPU.

A estratégia recomendada para o gerenciamento de memória do Direct3D 12, descrita nesta seção, é "classificar, orçamento e fluxo".

-   [Tipos de recursos](#resource-types)
-   [Orçamento de memória](#memory-budget)
-   [Estratégia de classificação](#classification-strategy)
-   [Tópicos relacionados](#related-topics)

## <a name="resource-types"></a>Tipos de recurso

O conceito básico de um "recurso confirmado" (criação de espaços de endereço físico e virtual inicializados na memória física gerenciada) tem sido conhecido desde o Direct3D 9, embora a VA (endereçamento virtual) e o endereçamento físico possam ser separados no Direct3D 12 para permitir que o aplicativo gerencie cuidadosamente a memória física.

Além dos recursos confirmados, o constructo de heap do Direct3D 12 permite dois outros tipos de recurso: "colocado" e "reservado". No Direct3D 11, um recurso "reservado" era conhecido como um "recurso lado a lado".

Os recursos reservados diferem dos recursos colocados, já que os recursos reservados têm seu próprio espaço de endereço virtual de GPU exclusivo. Isso permite uma grande alocação de espaço de VA na frente e, em seguida, permite o mapeamento de páginas va para determinadas seções do heap posteriormente e o aplicativo reconfigura a organização em tempo real. O espaço va é contíguo e pode ser mapeado de forma esparsa.

O recurso reservado pode ser feito para referenciar regiões no heap com chamadas à API, como [**UpdateTileMappings,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) e elas podem ser feitas residentes pelo aplicativo atualizando tabelas de página em tempo real. Quando um intervalo de VA é mapeado para NULL ou um heap não residente, essa parte do recurso é considerada não residente. Quando um intervalo de VA é mapeado para um heap residente, essa parte do recurso é considerada residente. Os heaps são residentes após a criação.

Os recursos colocados são um design muito mais simples, sendo simplesmente um ponteiro para uma determinada região de um heap (por exemplo, uma região de 1 Mb para uma textura em um heap de 5 Mb). As barreiras de alias permitem o uso de recursos colocados sobrepostos (consulte [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) e [**ResourceBapping).**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Os recursos reservados não estão disponíveis em todo o hardware do Direct3D 12 e os recursos colocados são um fallback razoável, embora os recursos colocados devem ser contíguos e não podem ser parcialmente residentes.

## <a name="memory-budget"></a>Orçamento de memória

No Direct3D 12, ao alocar um heap, você está criando o aspecto de memória física de um recurso confirmado. A opção de segmento de memória mais explícita está disponível no Direct3D 12 (escolhendo entre o vídeo e a memória do sistema). Os adaptadores UMA têm apenas um único segmento de memória, a memória do sistema.

As GPUs não são suportadas por falhas de página, portanto, os desenvolvedores devem estar cientes de que não superam a commit, especialmente para sistemas com apenas 1 Gb de memória do sistema. Se um aplicativo realizar uma confirmação em excesso, o sistema operacional usará o agendamento mais desa granulado de processos por sua demanda na memória física. O agendador congelará processos em primeiro plano e, essencialmente, a página de alguns deles, para fazer a página em um processo em segundo plano que deseja executar. A memória física disponível pode variar consideravelmente dependendo do que o usuário está fazendo em segundo plano (como executar um navegador ou assistir a um vídeo).

A API para orçamento de memória [**é QueryVideoMemoryInfo.**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) Para adaptadores discretos "local" é memória de vídeo, "não local" é memória do sistema. Para adaptadores UMA não locais é sempre zero. Uma pergunta de design é se o mecanismo gerenciará ambos os orçamentos ou apenas o orçamento local. Gerenciar apenas o orçamento local é mais simples, mas tem algumas advertências; por exemplo, digamos que haja um orçamento local máximo de 1 Gb, então todos os heaps virão desse 1 Gb em um sistema UMA e não haverá estouro na memória do sistema (claramente, como não há nenhum).

Como a memória gerenciada do Direct3D11 para aplicativos, os recursos não utilizados seriam essencialmente pageados.

Escolha as dimensões de recurso mais apropriadas. Considere se o tamanho de um recurso é apropriado para a situação em que o aplicativo está realmente em execução. Alguns usuários podem executar o aplicativo em uma janela ou com uma resolução de tela de 800 x 600.

## <a name="classification-strategy"></a>Estratégia de classificação

Para gerenciar recursos efetivamente em cenários de limite de memória, considere classificar os recursos da seguinte maneira:



| classificação      | Exemplos                                                                                         | Objetos e recursos de API                                                                                           | Notas de gerenciamento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crítico            | Interface do usuário do jogo                                                                                          | Alocador de comando, filas de comando, heaps de consulta, recursos e heaps de recursos.                                      | Esses elementos devem entrar em memória não pageável/sempre comprometida.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Dimensionado/ Opcional    | Modelos e texturas específicos ao nível, cadeias de permuta, caixas de céu, modelos de caracteres de jogador de primeira pessoa | Recursos e heaps. Os recursos comprometidos, mas também os recursos colocados e reservados, também podem funcionar.          | Integre o orçamento de residência de memória aos algoritmos de renderização. Escolha o nível apropriado de detalhes disponíveis e avalie novamente menos de uma vez por quadro. As técnicas incluem o uso de recursos de tamanho variável e o dimensionamento de cadeia de permuta.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| Recursos rea usados   | Buffers de sombra, recursos de renderização adiados, recursos de pós-processamento, caches de dados de iluminação    | Recursos e heaps. Sobreposição de recursos colocados em heaps e barreiras de alias.                                  | Reutilizar recursos grandes ou regiões de heap em um quadro para reduzir os requisitos de todo o quadro. Use a técnica de reutilização de memória intra-quadro. No Direct3D 11, os aplicativos só podiam reutilizar recursos com o mesmo tipo e dimensões potencialmente grandes o suficiente. Os heaps do Direct3D 12 permitem a sobreposição de recursos para reutilização muito mais simples e maior.<br/>                                                                                                                                                                                                                              |
| Recursos de streaming | Geometria e texturas de terra, mundo aberto                                                        | Recursos e heaps. Criação de thread livre, threads de CPU em segundo plano e listas e filas de comandos de cópia em segundo plano. | Residência parcial, normalmente baseada na visibilidade (usando a avaliação baseada em distância ou exibição) e reavaliação das necessidades de residência a cada quadro.<br/> A técnica de usar um gerenciamento de residência parcial por bloco e reutilização entre quadros está disponível quando o adaptador de GPU dá suporte a recursos reservados em heaps.<br/> Usando a técnica de usar a nova utilização de memória entre quadros, a residência parcial de sub-recursos pode ser realizada, mas é menos ideal. Os recursos colocados com heaps devem habilitar a reciclagem mais rápida, mas os recursos confirmados podem ser usados como um fallback.<br/> |



 

Quanto mais aplicativos gravitarem para os recursos de streaming na maior parte do trabalho, mais eles aproveitarão os recursos colocados e reservados, o que maximizará o re uso de memória entre essas quatro classificações. Quanto mais aplicativos são transmitidos, mais orçamento e priorizam a largura de banda.

Normalmente, com os mecanismos gráficos do Direct3D 12, é necessário seguir um orçamento mais diversificado e dinâmico e fazer isso mais estritamente do que no passado. Os melhores aplicativos localizarão todas as quatro categorias no orçamento dado ao processo, dimensionando o jogo do aplicativo móvel em segundo plano para orçamentos discretos de tela inteira. No entanto, muitos aplicativos provavelmente terão dificuldades ao começar com muitos tipos críticos de categoria de recursos. Os recursos habilitados para Direct3D 11 são criados anonimamente e ocupam o status crítico sem afetar o desempenho. No entanto, para o Direct3D 12, os desenvolvedores devem procurar recursos criados aleatoriamente em todo o mecanismo e middleware e atribuí-los a uma das outras categorias.

Outras áreas de problema são componentes de middleware, controles de usuário e streaming intra-quadro. Os componentes de middleware podem não ser expostos a um orçamento nem ter que trabalhar juntos. Componentes de middleware provavelmente podem expor recursos como técnicas de renderização; e o aplicativo pode contar com a exposição de configurações de middleware e mecanismo. Os desenvolvedores podem contar com o Direct3D 11 para fazer a paagem e obter a taxa de quadros correta. Em alguns casos, os aplicativos Direct3D 11 podem ter pajado o conteúdo dos recursos em cada quadro; e isso resultou em taxas de quadros aceitáveis para o usuário. A maioria dos mecanismos apenas transmite dados de recursos como uma atividade em segundo plano, em que não tem nenhum fallback normalmente para streaming intra-quadro de alta prioridade. Pedir que os mecanismos implementem isso esvaia alguns dos ganhos de sobrecarga de CPU que eles estão buscando movendo para o Direct3D 12. Os desenvolvedores de mecanismo podem considerar a possibilidade de transformar seus quadros em fases para fornecer mais oportunidades para rea usáveis recursos; e provavelmente funcionam com fornecedores de middleware para dar suporte a recursos colocados e heaps para reaplicação de memória intra-quadro.

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

 

