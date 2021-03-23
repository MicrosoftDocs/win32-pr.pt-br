---
title: Introdução ao DirectML
description: O Direct Machine Learning (DirectML) é uma API de nível baixo para o Machine Learning (ML).
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 2dd37bc4c27364e26e4bbd4ae2cf5d43031c3314
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105124"
---
# <a name="introduction-to-directml"></a>Introdução ao DirectML

## <a name="summary"></a>Resumo

O Direct Machine Learning (DirectML) é uma API de nível baixo para o Machine Learning (ML). Os primitivos de aprendizado de máquina acelerados por hardware (chamados operadores) são os blocos de construção de DirectML. A partir desses blocos de construção, você pode desenvolver técnicas de aprendizado de máquina como updimensioning, AntiAlias e transferência de estilo, para nomear, mas alguns. Denoising e super resolução, por exemplo, permitem que você alcance efeitos raytraced impressionantes com menos raios por pixel.

Você pode integrar cargas de trabalho com inferência a aprendizado de máquina em seu jogo, mecanismo, middleware, back-end ou outro aplicativo. O DirectML tem uma interface de programação e um fluxo de trabalho familiar (C++ nativo, nano-COM) DirectX 12-Style e tem suporte de todos os hardwares compatíveis com DirectX 12. Para aplicativos de exemplo do DirectML, incluindo um exemplo de um aplicativo de DirectML mínimo, consulte [aplicativos de exemplo DirectML](dml-min-app.md).

O DirectML é introduzido no Windows 10, versão 1903 e na versão correspondente do SDK do Windows.

## <a name="is-directml-appropriate-for-my-project"></a>O DirectML é apropriado para meu projeto?

DirectML é um componente sob a proteção de [Machine Learning do Windows](/windows/ai) . A API WinML de nível superior é essencialmente focada em modelos, com seu fluxo de trabalho Load-BIND-Evaluate. Mas domínios como jogos e mecanismos normalmente precisam de um nível mais baixo de abstração e um grau mais alto de controle de desenvolvedor, a fim de aproveitar ao máximo o silício. Se você estiver contando milissegundos e apertando os horários dos quadros, o DirectML atenderá às suas necessidades de aprendizado de máquina.

Para cenários confiáveis em tempo real, de alto desempenho, baixa latência e/ou com restrição de recursos, use DirectML (em vez de WinML). Você pode integrar o DirectML diretamente ao seu mecanismo existente ou ao pipeline de renderização. Ou, em um nível mais alto para estruturas e middleware de Machine Learning personalizados, o DirectML pode fornecer um back-end de alto desempenho no Windows.

O WinML é implementado usando DirectML como um de seus back-ends.

## <a name="what-work-does-directml-do-and-what-work-must-i-do-as-the-developer"></a>O que o trabalho faz DirectML; e *o que o trabalho deve fazer* como desenvolvedor?

O DirectML executa com eficiência as camadas individuais do seu modelo de inferência na GPU (ou em núcleos de aceleração de ia, se presente). Cada camada é um operador e o DirectML fornece uma biblioteca de operadores primitivos de aprendizado de máquina de baixo nível e aceleração de hardware. Esses operadores têm otimizações específicas de hardware e de arquitetura projetadas para eles (mais sobre isso na seção [por que a DirectML tem um bom desempenho?](#why-does-directml-perform-so-well)). Ao mesmo tempo, você, como desenvolvedor, vê uma interface única e independente de fornecedor para executar esses operadores.

A biblioteca de operadores no DirectML fornece todas as operações comuns que você esperaria poder usar em uma carga de trabalho de Machine Learning.

- Operadores de ativação, como **linear**, **ReLU**, **sigmoide**, **tanh** e muito mais.
- Operadores com elemento, como **Add**, **exp**, **log**, **Max**, **min**, **sub** e muito mais.
- Operadores de convolução, como **convolução** 2D e 3D e muito mais.
- Operadores de redução, como **argmin**, **Average**, **L2**, **sum** e muito mais.
- Operadores de pooling, como **Average**, **LP** e **Max**.
- Operadores de rede neural (NN), como **GEMM**, **Gru**, **lstm** e **RNN**.
- E muito mais.

Para o desempenho máximo, e para que você não pague pelo que não usa, o DirectML coloca o controle em suas mãos como desenvolvedor sobre como a carga de trabalho do Machine Learning é executada no hardware. Descobrir quais operadores executar, e quando, é sua responsabilidade como desenvolvedor. As tarefas que são deixadas para seu critério incluem: transcrever o modelo; simplificando e otimizando suas camadas; carregando pesos; alocação de recursos, associação, gerenciamento de memória (assim como com o Direct3D 12); e a execução do grafo.

Você mantém o conhecimento de alto nível de seus gráficos (você pode embutir seu código diretamente no seu modelo ou pode escrever seu próprio carregador de modelo). Você pode criar um modelo de up-scaling, por exemplo, usando várias camadas de cada um dos operadores **upsample**, **convolução**, **normalização** e **ativação** . Com essa familiaridade, o agendamento cuidadoso e o gerenciamento de barreira, você pode extrair o maior paralelismo e o desempenho do hardware. Se você estiver desenvolvendo um jogo, o gerenciamento de recursos cuidadoso e o controle do agendamento permitirão que você intercalar as cargas de trabalho de aprendizado de máquina e a renderização tradicional para saturar a GPU.

## <a name="whats-the-high-level-directml-workflow"></a>O que é o fluxo de trabalho DirectML de alto nível?

Aqui está a receita de alto nível de como esperamos que DirectML seja usado. Nas duas fases principais de inicialização e execução, você registra o trabalho em listas de comandos e, em seguida, executa-os em uma fila.

### <a name="initialization"></a>Inicialização

1. Crie seus recursos do Direct3D 12 &mdash; no dispositivo Direct3D 12, na fila de comandos, na lista de comandos e nos recursos como heaps de descritores.
2. Como você está fazendo o Machine Learning inferência, bem como sua carga de trabalho de renderização, crie recursos &mdash; do DirectML o dispositivo DirectML e as instâncias de operador. Se você tiver um modelo de aprendizado de máquina em que você precisa executar um tipo específico de convolução com um determinado tamanho de filtro tensor com um tipo de dados específico, esses serão todos os parâmetros no operador de **convolução** de DirectML.
3. Os registros DirectML funcionam nas listas de comandos do Direct3D 12. Assim, quando a inicialização é feita, você registra a associação e a inicialização de (por exemplo) seu operador de convolução na sua lista de comandos. Em seguida, feche e execute a lista de comandos em sua fila como de costume.

### <a name="execution"></a>Execução

1. Carregue seus tempos de importância em recursos. Um tensor no DirectML é representado usando um recurso regular do Direct3D 12. Por exemplo, se você quiser carregar seus dados de peso para a GPU, faça isso da mesma maneira que faria com qualquer outro recurso do Direct3D 12 (use um heap de carregamento ou a fila de cópia).
2. Em seguida, você precisa associar esses recursos do Direct3D 12 como seus tempos de entrada e de saída. Registre-se em seu comando para listar a associação e a execução de seus operadores.
3. Feche e execute a lista de comandos.

Assim como acontece com o Direct3D 12, o tempo de vida do recurso e a sincronização são de sua responsabilidade. Por exemplo, não libere seus objetos DirectML pelo menos até que eles concluam a execução na GPU.

## <a name="why-does-directml-perform-so-well"></a>Por que o DirectML tem um bom desempenho?

Há um bom motivo pelo qual você não deve simplesmente escrever seu próprio operador de convolução (por exemplo,) como HLSL em um [sombreador de computação](/windows/desktop/direct3d12/pipelines-and-shaders-with-directx-12#direct3d-12-compute-pipeline). A vantagem de usar o DirectML é que, &mdash; além de economizar o esforço de homebrewingr sua própria solução &mdash; , ele tem a capacidade de fornecer um desempenho muito melhor do que você poderia conseguir com um sombreador de computação de uso geral, escrito por mão, para algo como **convolução** ou **lstm**.

O DirectML consegue isso em parte devido ao recurso de metacomandos do Direct3D 12. Metacomandos expõem uma caixa preta de funcionalidade até DirectML, que permite aos fornecedores de hardware fornecer acesso DirectML a otimizações específicas de hardware e arquitetura específicas do fornecedor. Vários operadores &mdash; , por exemplo, a convolução seguida pela ativação &mdash; pode ser mesclada em um único metacomando.  Devido a esses fatores, o DirectML tem a capacidade de exceder o desempenho de até mesmo um sombreador de computação com ajuste à mão escrito para ser executado em uma amplitude de hardware.

Metacomandos fazem parte da API do Direct3D 12, embora estejam acoplados livremente a ela. Um metacomando é identificado por um [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)fixo, enquanto quase tudo o mais a respeito (de seu comportamento e semântica à sua assinatura e nome) não é estritamente parte da API do Direct3D 12. Em vez disso, um metacomando é especificado entre seu autor e o driver que o implementa. Nesse caso, o autor é DirectML. Metacomandos são primitivos do Direct3D 12 (assim como desenha e despachado), para que possam ser registrados em uma lista de comandos e agendados para execução em conjunto.

O DirectML acelera suas cargas de trabalho de aprendizado de máquina usando um conjunto inteiro de metacomandos do Machine Learning. Consequentemente, você não precisa escrever caminhos de código específicos do fornecedor para obter aceleração de hardware para seu inferência. Se você for executar em um chip com aceleração de ia, o DirectML usará esse hardware para acelerar muito as operações, como a convolução. Você pode usar o mesmo código que escreveu, sem modificá-lo, executá-lo em um chip que não seja de ia-acelerado (talvez a GPU integrada em seu laptop) e ainda obter grande aceleração de hardware de GPU. E se nenhuma GPU estiver disponível, DirectML retornará à CPU.
