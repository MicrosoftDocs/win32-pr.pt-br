---
title: Alterações importantes do Direct3D 11 para o Direct3D 12
description: O Direct3D 12 representa uma partida significativa do modelo de programação direct3D 11. O Direct3D 12 permite que os aplicativos se aproximam mais do hardware do que nunca.
ms.assetid: CE5066C9-7EA6-437D-9EB0-AACFB6CFAD9E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3afc5fe9a451addf1d1f7b9aeddf1f55ca40a22db99134ba71d8195c72ad2b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123829"
---
# <a name="important-changes-from-direct3d-11-to-direct3d-12"></a>Alterações importantes do Direct3D 11 para o Direct3D 12

O Direct3D 12 representa uma partida significativa do modelo de programação direct3D 11. O Direct3D 12 permite que os aplicativos se aproximam mais do hardware do que nunca. Ao estar mais próximo do hardware, o Direct3D 12 é mais rápido e eficiente. No entanto, a troca do seu aplicativo por ter aumentado a velocidade e a eficiência com o Direct3D 12 é que você é responsável por mais tarefas do que com o Direct3D 11.

-   [Sincronização explícita](#explicit-synchronization)
-   [Gerenciamento de residência de memória física](#physical-memory-residency-management)
-   [Objetos de estado do pipeline](#pipeline-state-objects)
-   [Listas de comandos e pacotes](#command-lists-and-bundles)
-   [Heaps e tabelas do descritor](#descriptor-heaps-and-tables)
-   [Portando do Direct3D 11](#porting-from-direct3d-11)
-   [Tópicos relacionados](#related-topics)

O Direct3D 12 é um retorno à programação de baixo nível; ele oferece mais controle sobre os elementos gráficos de seus jogos e aplicativos introduzindo estes novos recursos: objetos para representar o estado geral do pipeline, listas de comandos e pacotes para envio de trabalho e heaps de descritor e tabelas para acesso a recursos.

Seu aplicativo aumentou a velocidade e a eficiência com o Direct3D 12, mas você é responsável por mais tarefas do que com o Direct3D 11.

## <a name="explicit-synchronization"></a>Sincronização explícita

-   No Direct3D 12, a sincronização de CPU-GPU agora é a responsabilidade explícita do aplicativo e não é mais executada implicitamente pelo runtime, como está no Direct3D 11. Esse fato também significa que nenhuma verificação automática de riscos de pipeline é executada pelo Direct3D 12, portanto, novamente, essa é a responsabilidade dos aplicativos.
-   No Direct3D 12, os aplicativos são responsáveis por direcionar atualizações de dados. Ou seja, o padrão "Map/Lock-DISCARD" no Direct3D 11 deve ser executado manualmente no Direct3D 12. No Direct3D 11, se a GPU ainda estiver usando o buffer quando você [**chamar ID3D11DeviceContext::Map**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map) com [**D3D11 \_ MAP WRITE \_ \_ DISCARD,**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_map)o runtime retornará um ponteiro para uma nova região de memória em vez dos dados de buffer antigos. Isso permite que a GPU continue usando os dados antigos enquanto o aplicativo coloca os dados no novo buffer. Nenhum gerenciamento de memória adicional é necessário no aplicativo; o buffer antigo é reutilizado ou destruído automaticamente quando a GPU é concluída com ele.
-   No Direct3D 12, todas as atualizações dinâmicas (incluindo buffers constantes, buffers de vértice dinâmicos, texturas dinâmicas e assim por diante) são explicitamente controladas pelo aplicativo. Essas atualizações dinâmicas incluem quaisquer cercas de GPU ou buffer necessários. O aplicativo é responsável por manter a memória disponível até que ela não seja mais necessária.
-   O Direct3D 12 usa a contagem de referência no estilo COM somente para os tempos de vida das interfaces (usando o modelo de referência fraca do Direct3D vinculado ao tempo de vida do dispositivo). Todos os tempos de vida de memória de recurso e de descrição são a única responsabilidade do aplicativo a ser mantido pela duração adequada e não são contados por referência. O Direct3D 11 também usa a contagem de referência para gerenciar os tempos de vida das dependências da interface.

## <a name="physical-memory-residency-management"></a>Gerenciamento de residência de memória física

Um aplicativo Direct3D 12 deve impedir condições de corrida entre várias filas, vários adaptadores e threads de CPU. D3D12 não sincroniza mais a CPU e a GPU, nem dá suporte a mecanismos convenientes para renomeação de recursos ou vários buffers. As cercas devem ser usadas para evitar que várias unidades de processamento de memória sejam sobressumentadas antes que outra unidade de processamento termine de usá-la.

O aplicativo Direct3D 12 deve garantir que os dados residam na memória enquanto a GPU os lê. A memória usada por cada objeto se tornou residente durante a criação do objeto . Os aplicativos que chamam esses métodos devem usar cercas para garantir que a GPU não acesse objetos que foram despejados.

As barreiras de recursos são outro tipo de sincronização necessária, usado para sincronizar transições de recursos e sub-recursos em um nível muito granular.

Consulte Gerenciamento [de memória no Direct3D 12](memory-management.md).

## <a name="pipeline-state-objects"></a>Objetos de estado do pipeline

O Direct3D 11 permite a manipulação de estado do pipeline por meio de um grande conjunto de objetos independentes. Por exemplo, o estado do assembler de entrada, o estado do sombreador de pixel, o estado do rasterizador e o estado de fusão de saída podem ser modificados independentemente. Esse design fornece uma representação conveniente e relativamente de alto nível do pipeline de gráficos, mas não utiliza os recursos de hardware moderno, principalmente porque os vários estados geralmente são interdependentes. Por exemplo, muitas GPUs combinam o sombreador de pixel e o estado de fusão de saída em uma única representação de hardware. Mas como a API do Direct3D 11 permite que esses estágios de pipeline sejam definidos separadamente, o driver de exibição não pode resolver problemas de estado do pipeline até que o estado seja finalizado, o que não é até o tempo de desenho. Esse esquema atrasa a configuração do estado de hardware, o que significa sobrecarga extra e menos chamadas de desenho máximas por quadro.

O Direct3D 12 aborda esse esquema unificando grande parte do estado do pipeline em PSOs (objetos de estado de pipeline imutáveis), que são finalizados após a criação. O hardware e os drivers podem converter imediatamente o PSO em quaisquer instruções e estado nativos de hardware necessários para executar o trabalho de GPU. Você ainda pode alterar dinamicamente qual PSO está em uso, mas para fazer isso, o hardware só precisa copiar a quantidade mínima de estado pré-computado diretamente para os registros de hardware, em vez de calcular o estado de hardware em tempo real. Usando PSOs, a sobrecarga de chamada de desenho é reduzida significativamente e muitas outras chamadas de desenho podem ocorrer por quadro. Para obter mais informações sobre PSOs, consulte Gerenciando o estado do pipeline de [gráficos no Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="command-lists-and-bundles"></a>Listas de comandos e pacotes

No Direct3D 11, todo o envio de trabalho é feito por meio do contexto imediato [,](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render)que representa um único fluxo de comandos que vão para a GPU. Para alcançar o dimensionamento multithread, os jogos também [têm contextos adiados](/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render) disponíveis para eles. Os contextos adiados no Direct3D 11 não são mapeados perfeitamente para o hardware, portanto, é possível fazer relativamente pouco trabalho neles.

O Direct3D 12 introduz um novo modelo para envio de trabalho com base em listas de comandos que contêm a totalidade das informações necessárias para executar uma carga de trabalho específica na GPU. Cada nova lista de comandos contém informações como qual PSO usar, quais recursos de textura e buffer são necessários e os argumentos para todas as chamadas de desenho. Como cada lista de comandos é autossu contida e não herda nenhum estado, o driver pode pré-computar todos os comandos de GPU necessários de forma antecipada e livre. O único processo serial necessário é o envio final de listas de comandos para a GPU por meio da fila de comandos.

Além das listas de comandos, o Direct3D 12 também introduz um segundo nível de pré-computação de trabalho: *pacotes*. Ao contrário das listas de comandos, que são completamente autossu contidas e normalmente são construídas, enviadas uma vez e descartadas, os pacotes fornecem uma forma de herança de estado que permite a reutilização. Por exemplo, se um jogo quiser desenhar dois modelos de caracteres com texturas diferentes, uma abordagem será registrar uma lista de comandos com dois conjuntos de chamadas de desenho idênticas. Mas outra abordagem é "registrar" um pacote que desenha um único modelo de caractere e, em seguida, "reproduzir" o pacote duas vezes na lista de comandos usando recursos diferentes. No último caso, o driver de exibição só precisa calcular as instruções apropriadas uma vez e criar a lista de comandos basicamente equivale a duas chamadas de função de baixo custo.

Para obter mais informações sobre listas de comandos e pacotes, consulte [Envio de trabalho no Direct3D 12](command-queues-and-command-lists.md).

## <a name="descriptor-heaps-and-tables"></a>Heaps e tabelas do descritor

A associação de recursos no Direct3D 11 é altamente abstrata e conveniente, mas deixa muitos recursos de hardware modernos subutilizados. No Direct3D 11,  os jogos criam objetos de exibição de recursos e, em seguida, vinculam essas exibições a vários slots em vários *estágios* de sombreador no pipeline. Os sombreadores, por sua vez, leem dados desses slots de vinculação explícitos, que são fixos no momento do desenho. Esse modelo significa que sempre que um jogo for desenhar usando recursos diferentes, ele deverá rea vincular diferentes exibições a slots diferentes e chamar desenhar novamente. Esse caso também representa a sobrecarga que pode ser eliminada utilizando totalmente as funcionalidades de hardware modernas.

O Direct3D 12 altera o modelo de associação para corresponder ao hardware moderno e melhora significativamente o desempenho. Em vez de exigir exibições de recursos autônomos e mapeamento explícito para slots, o Direct3D 12 fornece um heap de descritor no qual os jogos criam suas várias exibições de recursos. Esse esquema fornece um mecanismo para a GPU gravar diretamente a descrição do recurso nativo de hardware (descritor) na memória de início. Para declarar quais recursos devem ser usados pelo pipeline para uma chamada de desenho específica, os jogos especificam uma ou mais tabelas de descritor que representam subconjuntos do heap de descritor completo. Como o heap do descritor já foi populado com os dados de descritor específicos de hardware apropriados, alterar tabelas de descritor é uma operação extremamente de baixo custo.

Além do desempenho aprimorado oferecido por heaps e tabelas de descritor, o Direct3D 12 também permite que os recursos sejam indexados dinamicamente em sombreadores, o que fornece flexibilidade sem precedentes e desbloqueia novas técnicas de renderização. Por exemplo, mecanismos de renderização adiados modernos normalmente codificam um material ou identificador de objeto de algum tipo para o buffer G intermediário. No Direct3D 11, esses mecanismos devem ter cuidado para evitar o uso de muitos materiais, pois incluir muitos em um buffer g pode reduzir significativamente a passagem de renderização final. Com recursos indexáveis dinamicamente, uma cena com mil materiais pode ser finalizada tão rapidamente quanto uma com apenas dez.

Para obter mais informações sobre heaps e tabelas de descritor, consulte [Associação](resource-binding.md)de recursos e Diferenças no modelo de associação [do Direct3D 11](binding-model.md).

## <a name="porting-from-direct3d-11"></a>Portando do Direct3D 11

A portagem do Direct3D 11 é um processo envolvido, descrito em Portando do [Direct3D 11 para o Direct3D 12.](porting-from-direct3d-11-to-direct3d-12.md) Consulte também o intervalo de opções em [Trabalhando com Direct3D 11, Direct3D 10 e Direct2D](direct3d-12-interop.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução ao Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 