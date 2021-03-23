---
title: Alterações importantes do Direct3D 11 para o Direct3D 12
description: O Direct3D 12 representa um desvio significativo do modelo de programação do Direct3D 11. O Direct3D 12 permite que os aplicativos fiquem mais próximos do hardware do que nunca.
ms.assetid: CE5066C9-7EA6-437D-9EB0-AACFB6CFAD9E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be891d71d6c1f3a12d8d5aac3ec46785207ed31
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548218"
---
# <a name="important-changes-from-direct3d-11-to-direct3d-12"></a>Alterações importantes do Direct3D 11 para o Direct3D 12

O Direct3D 12 representa um desvio significativo do modelo de programação do Direct3D 11. O Direct3D 12 permite que os aplicativos fiquem mais próximos do hardware do que nunca. Ao se aproximar do hardware, o Direct3D 12 é mais rápido e mais eficiente. Mas, a desvantagem de seu aplicativo ter aumentado a velocidade e a eficiência com o Direct3D 12 é que você é responsável por mais tarefas do que era com o Direct3D 11.

-   [Sincronização explícita](#explicit-synchronization)
-   [Gerenciamento de residência de memória física](#physical-memory-residency-management)
-   [Objetos de estado do pipeline](#pipeline-state-objects)
-   [Listas de comandos e pacotes](#command-lists-and-bundles)
-   [Heaps e tabelas do descritor](#descriptor-heaps-and-tables)
-   [Portando do Direct3D 11](#porting-from-direct3d-11)
-   [Tópicos relacionados](#related-topics)

O Direct3D 12 é um retorno para programação de baixo nível; Ele oferece mais controle sobre os elementos gráficos de seus jogos e aplicativos introduzindo esses novos recursos: objetos para representar o estado geral do pipeline, listas de comandos e pacotes para envio de trabalho e heaps e tabelas de descritores para acesso aos recursos.

Seu aplicativo aumentou a velocidade e a eficiência com o Direct3D 12, mas você é responsável por mais tarefas do que era com o Direct3D 11.

## <a name="explicit-synchronization"></a>Sincronização explícita

-   No Direct3D 12, a sincronização de GPU de CPU agora é a responsabilidade explícita do aplicativo e não é mais implicitamente executada pelo tempo de execução, como no Direct3D 11. Esse fato também significa que nenhuma verificação automática de riscos de pipeline é executada pelo Direct3D 12; Portanto, novamente essa é a responsabilidade dos aplicativos.
-   No Direct3D 12, os aplicativos são responsáveis por atualizações de dados de pipeline. Ou seja, o padrão "mapear/bloquear-descartar" no Direct3D 11 deve ser executado manualmente no Direct3D 12. No Direct3D 11, se a GPU ainda estiver usando o buffer quando você chamar [**ID3D11DeviceContext:: map**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map) com [**\_ descarte de \_ gravação \_ de mapa D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_map), o tempo de execução retornará um ponteiro para uma nova região de memória em vez dos dados de buffer antigos. Isso permite que a GPU continue usando os dados antigos enquanto o aplicativo coloca os dados no novo buffer. Nenhum gerenciamento de memória adicional é necessário no aplicativo; o buffer antigo é reutilizado ou destruído automaticamente quando a GPU é concluída com ele.
-   No Direct3D 12, todas as atualizações dinâmicas (incluindo buffers de constantes, buffers de vértice dinâmicos, texturas dinâmicas e assim por diante) são explicitamente controladas pelo aplicativo. Essas atualizações dinâmicas incluem todos os limites ou buffers de GPU necessários. O aplicativo é responsável por manter a memória disponível até que ela não seja mais necessária.
-   O Direct3D 12 usa a contagem de referência de estilo COM apenas para os tempos de vida de interfaces (usando o modelo de referência fraca do Direct3D ligado ao tempo de vida do dispositivo). Todos os tempos de vida de memória de recursos e de descrição são o único responsável pelo aplicativo a ser mantido durante a duração apropriada e não são contados como referência. O Direct3D 11 usa a contagem de referência para gerenciar os tempos de vida de dependências de interface também.

## <a name="physical-memory-residency-management"></a>Gerenciamento de residência de memória física

Um aplicativo Direct3D 12 deve impedir as condições de corrida entre várias filas, vários adaptadores e os threads de CPU. O D3D12 não sincroniza mais a CPU e a GPU nem oferece suporte a mecanismos convenientes de renomeação de recursos ou de vários buffers. Os limites devem ser usados para evitar que várias unidades de processamento substituam a memória excessiva antes que outra unidade de processamento termine de usá-la.

O aplicativo Direct3D 12 deve garantir que os dados estejam residentes na memória enquanto a GPU lê. A memória usada por cada objeto torna-se residente durante a criação do objeto. Os aplicativos que chamam esses métodos devem usar limites para garantir que a GPU não acesse objetos que foram removidos.

As barreiras de recursos são outro tipo de sincronização necessária, usadas para sincronizar as transições de recurso e de subrecurso em um nível muito granular.

Consulte [Gerenciamento de memória no Direct3D 12](memory-management.md).

## <a name="pipeline-state-objects"></a>Objetos de estado do pipeline

O Direct3D 11 permite a manipulação do estado do pipeline por meio de um grande conjunto de objetos independentes. Por exemplo, o estado do assembler de entrada, o estado do sombreador de pixel, o estado do rasterizador e o estado de fusão de saída podem ser modificados independentemente. Esse design fornece uma representação conveniente e relativamente de alto nível do pipeline de gráficos, mas não utiliza os recursos do hardware moderno, principalmente porque os vários Estados geralmente são interdependentes. Por exemplo, muitas GPUs combinam o sombreador de pixel e o estado de fusão de saída em uma única representação de hardware. Mas como a API do Direct3D 11 permite que esses estágios de pipeline sejam definidos separadamente, o driver de vídeo não pode resolver problemas de estado do pipeline até que o estado seja finalizado, o que não é até o momento do desenho. Esse esquema atrasa a configuração do estado do hardware, o que significa sobrecarga extra e menos chamadas de desenho máximas por quadro.

O Direct3D 12 trata desse esquema, unificando grande parte do estado do pipeline em PSOs (objetos de estado de pipeline) imutáveis, que são finalizados após a criação. Hardware e drivers podem então converter imediatamente o PSO em quaisquer instruções e Estados nativos de hardware necessários para executar o trabalho de GPU. Você ainda pode alterar dinamicamente qual PSO está em uso, mas para fazer isso, o hardware precisa apenas copiar a quantidade mínima de Estado previamente computado diretamente para os registros de hardware, em vez de computar o estado do hardware em tempo real. Usando PSOs, a sobrecarga de chamada de desenho é reduzida de forma significativa e muitas outras chamadas de desenho podem ocorrer por quadro. Para obter mais informações sobre o PSOs, consulte [Gerenciando o estado do pipeline de gráficos no Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="command-lists-and-bundles"></a>Listas de comandos e pacotes

No Direct3D 11, todo o envio de trabalho é feito por meio do [contexto imediato](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render), que representa um único fluxo de comandos que vão para a GPU. Para obter o dimensionamento multithread, os jogos também têm [contextos adiados](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render) disponíveis para eles. Contextos adiados no Direct3D 11 não são mapeados perfeitamente para hardware, portanto, relativamente pouco trabalho pode ser feito neles.

O Direct3D 12 introduz um novo modelo de envio de trabalho com base em listas de comandos que contêm todo o necessário de informações necessárias para executar uma carga de trabalhos específica na GPU. Cada nova lista de comandos contém informações como qual PSO usar, quais recursos de textura e buffer são necessários e os argumentos para todas as chamadas de desenho. Como cada lista de comandos é independente e não herda nenhum estado, o driver pode pré-testar previamente todos os comandos de GPU necessários antes e em uma maneira de thread livre. O único processo serial necessário é o envio final de listas de comandos para a GPU por meio da fila de comandos.

Além das listas de comandos, o Direct3D 12 também introduz um segundo nível de trabalho de computação prévia: *grupos*. Ao contrário das listas de comandos, que são completamente independentes e são normalmente construídas, enviadas uma vez e descartadas, os grupos fornecem uma forma de herança de estado que permite a reutilização. Por exemplo, se um jogo quiser desenhar dois modelos de caractere com texturas diferentes, uma abordagem será registrar uma lista de comandos com dois conjuntos de chamadas de desenho idênticas. Mas outra abordagem é "registrar" um pacote que desenha um único modelo de caractere e, em seguida, "reproduzir" o pacote duas vezes na lista de comandos usando diferentes recursos. No último caso, o driver de vídeo só precisa computar as instruções apropriadas uma vez e criar a lista de comandos é basicamente uma quantidade de duas chamadas de função de baixo custo.

Para obter mais informações sobre listas de comandos e pacotes, consulte [envio de trabalho no Direct3D 12](command-queues-and-command-lists.md).

## <a name="descriptor-heaps-and-tables"></a>Heaps e tabelas do descritor

A associação de recursos no Direct3D 11 é altamente abstrata e conveniente, mas deixa muitos recursos de hardware modernos subutilizados. No Direct3D 11, os jogos criam objetos de *exibição* de recursos e associam essas exibições a vários *Slots* em vários estágios de sombreador no pipeline. Os sombreadores, por sua vez, lêem dados desses slots de ligação explícitos, que são corrigidos no momento do empate. Esse modelo significa que sempre que um jogo for desenhado usando recursos diferentes, ele deverá reassociar diferentes modos de exibição a Slots diferentes e chamar o Draw novamente. Esse caso também representa a sobrecarga que pode ser eliminada por meio da utilização completa dos recursos de hardware modernos.

O Direct3D 12 altera o modelo de associação para corresponder ao hardware moderno e melhora significativamente o desempenho. Em vez de exigir exibições de recursos autônomos e mapeamento explícito para slots, o Direct3D 12 fornece um heap de descritor no qual os jogos criam seus diversos modos de exibição de recursos. Esse esquema fornece um mecanismo para a GPU gravar diretamente a descrição do recurso nativo do hardware (descritor) na memória ativa. Para declarar quais recursos devem ser usados pelo pipeline para uma chamada de desenho particular, os jogos especificam uma ou mais tabelas de descritores que representam subintervalos do heap de descritor completo. Como o heap de descritor já foi populado com os dados apropriados de descritor específicos de hardware, a alteração de tabelas de descritores é uma operação de custo extremamente baixo.

Além do desempenho aprimorado oferecido pelos heaps e tabelas do descritor, o Direct3D 12 também permite que os recursos sejam indexados dinamicamente em sombreadores, o que fornece flexibilidade incomparável e desbloqueia novas técnicas de renderização. Por exemplo, os mecanismos de renderização adiados modernos normalmente codificam um material ou identificador de objeto de algum tipo para o g-buffer intermediário. No Direct3D 11, esses mecanismos devem ter cuidado para evitar o uso de materiais demais, pois incluir muitas em um g-buffer pode retardar significativamente a passagem de renderização final. Com recursos indexáveis dinamicamente, uma cena com milhares de materiais pode ser finalizada com a mesma rapidez que apenas uma com dez.

Para obter mais informações sobre heaps e tabelas do descritor, consulte [Associação de recursos](resource-binding.md)e [diferenças no modelo de associação do Direct3D 11](binding-model.md).

## <a name="porting-from-direct3d-11"></a>Portando do Direct3D 11

O portamento do Direct3D 11 é um processo envolvido, descrito em [portando do Direct3D 11 para o Direct3D 12](porting-from-direct3d-11-to-direct3d-12.md). Consulte também o intervalo de opções em [trabalhando com o Direct3D 11, o Direct3D 10 e o Direct2D](direct3d-12-interop.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Entendendo o Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 