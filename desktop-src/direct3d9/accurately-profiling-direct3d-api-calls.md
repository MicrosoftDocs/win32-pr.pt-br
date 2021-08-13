---
description: Quando você tem um aplicativo Microsoft Direct3D funcional e deseja melhorar seu desempenho, geralmente usa uma ferramenta de criação de perfil de prateleira ou alguma técnica de medida personalizada para medir o tempo necessário para executar uma ou mais chamadas de API (interface de programação de aplicativo). Se você tiver feito isso, mas estiver obtendo resultados de tempo que variam de uma sequência de renderização para a próxima, ou se estiver fazendo alterações que não contenham resultados reais de experimento, as informações a seguir poderão ajudá-lo a entender o porquê.
ms.assetid: f969be42-d541-4e8d-aec4-eb9508bcc7cf
title: Criação de perfil de chamadas à API do Direct3D com precisão (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6457e47da58a3614270f89eefa1cfa33fbf30cf26544c1013d010696a68e4602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097452"
---
# <a name="accurately-profiling-direct3d-api-calls-direct3d-9"></a>Criação de perfil de chamadas à API do Direct3D com precisão (Direct3D 9)

-   [A criação de perfil de Direct3D com precisão é difícil](#accurately-profiling-direct3d-is-difficult)
-   [Como criar um perfil com precisão de uma sequência de renderização do Direct3D](#how-to-accurately-profile-a-direct3d-render-sequence)
-   [Criando perfil de alterações de estado do Direct3D](#profiling-direct3d-state-changes)
-   [Resumo](#summary)
-   [Anexo](#appendix)

Quando você tem um aplicativo Microsoft Direct3D funcional e deseja melhorar seu desempenho, geralmente usa uma ferramenta de criação de perfil de prateleira ou alguma técnica de medida personalizada para medir o tempo necessário para executar uma ou mais chamadas de API (interface de programação de aplicativo). Se você tiver feito isso, mas estiver obtendo resultados de tempo que variam de uma sequência de renderização para a próxima, ou se estiver fazendo alterações que não contenham resultados reais de experimento, as informações a seguir poderão ajudá-lo a entender o porquê.

As informações fornecidas aqui se baseiam na suposição de que você tem conhecimento e experiência com o seguinte:

-   Programação C/C++
-   Programação de API do Direct3D
-   Medindo o tempo da API
-   A placa de vídeo e seu driver de software
-   Possíveis resultados não explicativos da experiência de criação de perfil anterior

## <a name="accurately-profiling-direct3d-is-difficult"></a>A criação de perfil de Direct3D com precisão é difícil

Um criador de perfil relata a quantidade de tempo gasto em cada chamada à API. Isso é feito para melhorar o desempenho, encontrando e ajustando pontos de acesso distantes. Há diferentes tipos de perfis e técnicas de criação de perfil.

-   Um criador de perfil de amostragem fica ocioso muito do tempo, despertando em intervalos específicos para exemplo (ou para registrar) as funções que estão sendo executadas. Ele retorna a porcentagem de tempo gasto em cada chamada. Geralmente, um gerador de perfil de amostragem não é muito invasivo para o aplicativo e tem um impacto mínimo sobre a sobrecarga do aplicativo.
-   Um criador de perfil de instrumentação mede o tempo real que leva para uma chamada para retornar. Ele requer a compilação de delimitadores de início e parada em um aplicativo. Um criador de perfil de instrumentação é comparativamente mais invasivo para um aplicativo do que um criador de perfil de amostragem.
-   Também é possível usar uma técnica de criação de perfil Personalizada com um timer de alto desempenho. Isso produz resultados muito parecidos com um criador de perfil de instrumentação.

O tipo de criador de perfil ou a técnica de criação de perfil usada é apenas parte do desafio de gerar medidas precisas.

A criação de perfil fornece respostas que ajudam você a orçar o desempenho. Por exemplo, suponha que você saiba que uma chamada à API calcula a média de 1000 ciclos de relógio a serem executados. Você pode declarar algumas conclusões sobre o desempenho, como o seguinte:

-   Uma CPU de 2 GHz (que passa 50% de seu tempo de renderização) é limitada a chamar essa API 1 milhão vezes por segundo.
-   Para obter 30 quadros por segundo, você não pode chamar essa API mais de 33.000 vezes por quadro.
-   Você só pode renderizar 3,3 K Objects por quadro (supondo que 10 dessas chamadas de API para a sequência de renderização de cada objeto).

Em outras palavras, se você tiver tempo suficiente por chamada à API, poderá responder a uma pergunta de orçamento, como o número de primitivos que podem ser renderizados interativamente. Mas os números brutos retornados por um criador de perfil de instrumentação não responderão com precisão às perguntas de orçamento. Isso ocorre porque o pipeline de gráficos tem problemas de design complexos, como o número de componentes que precisam de trabalho, o número de processadores que controlam como o trabalho flui entre componentes e estratégias de otimização implementados no tempo de execução e em um driver que são projetados para tornar o pipeline mais eficiente.

### <a name="each-api-call-goes-through-several-components"></a>Cada chamada à API passa por vários componentes

Cada chamada é processada por vários componentes do seu caminho a partir do aplicativo até a placa de vídeo. Por exemplo, considere a seguinte sequência de renderização que contém duas chamadas para desenhar um único triângulo:


```
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
```



O diagrama conceitual a seguir mostra os diferentes componentes por meio dos quais as chamadas devem ser aprovadas.

![diagrama de componentes gráficos que as chamadas de API passam](images/microbenchmarkinstructionflow2.png)

O aplicativo invoca o Direct3D, que controla a cena, manipula as interações do usuário e determina como a renderização é feita. Todo esse trabalho é especificado na sequência de renderização, que é enviada para o tempo de execução usando chamadas de API do Direct3D. A sequência de renderização é praticamente independente de hardware (ou seja, as chamadas à API são independentes de hardware, mas um aplicativo tem conhecimento de quais recursos uma placa de vídeo suporta).

O tempo de execução converte essas chamadas em um formato independente de dispositivo. O tempo de execução manipula toda a comunicação entre o aplicativo e o driver, para que um aplicativo seja executado em mais de uma parte de hardware compatível (dependendo dos recursos necessários). Ao medir uma chamada de função, um criador de perfil de instrumentação mede o tempo gasto em uma função, bem como o tempo de retorno da função. Uma limitação de um criador de perfil de instrumentação é que ele pode não incluir o tempo que leva um driver para enviar o trabalho resultante para a placa de vídeo nem a hora de o cartão de vídeo processar o trabalho. Em outras palavras, um criador de perfil de instrumentação fora do mercado falha ao atribuir todo o trabalho associado a cada chamada de função.

O driver de software usa conhecimento específico de hardware sobre a placa de vídeo para converter os comandos independentes de dispositivo em uma sequência de comandos de placa de vídeo. Os drivers também podem otimizar a sequência de comandos que são enviados para a placa de vídeo, de modo que a renderização na placa de vídeo seja feita com eficiência. Essas otimizações podem causar problemas de criação de perfil porque a quantidade de trabalho realizado não é o que parece ser (talvez você precise entender as otimizações para se considerar). O driver normalmente retorna o controle ao tempo de execução antes que a placa de vídeo termine de processar todos os comandos.

A placa de vídeo executa a maioria da renderização combinando dados do vértice e buffers de índice, texturas, informações de estado de renderização e comandos gráficos. Quando a placa de vídeo termina a renderização, o trabalho criado a partir da sequência de renderização é concluído.

Cada chamada à API do Direct3D deve ser processada por cada componente (tempo de execução, Driver e placa de vídeo) para renderizar qualquer coisa.

### <a name="there-is-more-than-one-processor-controlling-the-components"></a>Há mais de um processador controlando os componentes

A relação entre esses componentes é ainda mais complexa, pois o aplicativo, o tempo de execução e o driver são controlados por um processador e a placa de vídeo é controlada por um processador separado. O diagrama a seguir mostra dois tipos de processadores: uma CPU (unidade de processamento central) e uma GPU (unidade de processamento gráfico).

![diagrama de CPU e de uma GPU e seus componentes](images/microbenchmarkprocessors.png)

Os sistemas de PC têm pelo menos uma CPU e uma GPU, mas podem ter mais de um ou ambos. As CPUs estão localizadas na placa-mãe e as GPUs estão localizadas na placa-mãe ou na placa de vídeo. A velocidade da CPU é determinada por um chip de relógio na placa-mãe, e a velocidade da GPU é determinada por um chip de relógio separado. O relógio da CPU controla a velocidade do trabalho feito pelo aplicativo, o tempo de execução e o driver. O aplicativo envia o trabalho para a GPU por meio do tempo de execução e do driver.

A CPU e a GPU geralmente são executadas em diferentes velocidades, independentes umas das outras. A GPU pode responder ao trabalho assim que o trabalho estiver disponível (supondo que a GPU concluiu o processamento do trabalho anterior). O trabalho de GPU é feito em paralelo com o trabalho de CPU como realçado pela linha curva na figura acima. Um criador de perfil geralmente mede o desempenho da CPU, não da GPU. Isso torna o perfil desafiador, pois as medições feitas por um criador de perfil de instrumentação incluem o tempo de CPU, mas podem não incluir a hora da GPU.

A finalidade da GPU é o processamento off-load da CPU para um processador especificamente projetado para o trabalho de gráficos. Em placas de vídeo modernas, a GPU substitui grande parte do trabalho de transformação e iluminação no pipeline da CPU para a GPU. Isso reduz significativamente a carga de trabalho da CPU, deixando mais ciclos de CPU disponíveis para outro processamento. Para ajustar um aplicativo gráfico para o máximo de desempenho, você precisa medir o desempenho da CPU e da GPU e equilibrar o trabalho entre os dois tipos de processadores.

Este documento não aborda os tópicos relacionados à medição do desempenho da GPU ou ao balanceamento do trabalho entre a CPU e a GPU. Se você quiser entender melhor o desempenho de uma GPU (ou uma placa de vídeo específica), visite o site do fornecedor para procurar mais informações sobre o desempenho da GPU. Em vez disso, este documento se concentra no trabalho feito pelo tempo de execução e pelo driver, reduzindo o trabalho da GPU a um valor insignificante. Isso é, em parte, baseado na experiência que os aplicativos que apresentam problemas de desempenho geralmente são limitados por CPU.

### <a name="runtime-and-driver-optimizations-can-mask-api-measurements"></a>Otimizações de driver e tempo de execução podem mascarar medidas de API

O tempo de execução tem uma otimização de desempenho interna que pode sobrecarregar a medida de uma chamada individual. Aqui está um cenário de exemplo que demonstra esse problema. Considere a seguinte sequência de renderização:


```
  BeginScene();
    ...
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);
    ...
  EndScene();
  Present();
```



Exemplo 1: sequência de renderização simples

Observando os resultados das duas chamadas na sequência de renderização, um criador de perfil de instrumentação poderia retornar resultados semelhantes a estes:


```
Number of cycles for SetTexture       : 100
Number of cycles for DrawPrimitive    : 950,500
```



O criador de perfil retorna o número de ciclos de CPU necessários para processar o trabalho associado a cada chamada (Lembre-se de que a GPU não está incluída nesses números porque a GPU ainda não começou a trabalhar nesses comandos). Como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) exigiu quase um milhão de ciclos para processar, você poderia concluir que não é muito eficiente. No entanto, em breve você verá por que essa conclusão está incorreta e como você pode gerar resultados que podem ser usados para orçamento.

### <a name="measuring-state-changes-requires-careful-render-sequences"></a>A medição de alterações de Estado requer sequências de renderização cuidadosa

Todas as chamadas que não sejam [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)ou [**Clear**](/windows/desktop/api) (como [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), [**SetVertexDeclaration**](/windows/desktop/api)e [**setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) produzem uma alteração de estado. Cada alteração de estado define o estado do pipeline que controla como a renderização será feita.

Otimizações no tempo de execução e/ou o driver são projetados para acelerar o processamento reduzindo a quantidade de trabalho necessária. A seguir estão algumas otimizações de alteração de estado que podem poluir as médias do perfil:

-   Um driver (ou o tempo de execução) pode salvar uma alteração de estado como um estado local. Como o driver pode operar em um algoritmo "lento" (adiar o trabalho até ser absolutamente necessário), o trabalho associado a algumas alterações de estado pode ser atrasado.
-   O tempo de execução (ou um driver) pode remover alterações de estado otimizando. Um exemplo disso pode ser remover uma alteração de estado redundante que desabilite a iluminação porque a iluminação foi desabilitada anteriormente.

Não há uma maneira à prova de examinar uma sequência de renderização e concluir quais alterações de estado definirão um bit sujo e adiar o trabalho ou serão simplesmente removidas pela otimização. Mesmo que você possa identificar alterações de estado otimizadas no runtime ou driver de hoje, o runtime ou driver de amanhã provavelmente será atualizado. Você também não sabe prontamente qual era o estado anterior, portanto, é difícil identificar alterações de estado redundantes. A única maneira de verificar o custo de uma alteração de estado é medir a sequência de renderização que inclui as alterações de estado.

Como você pode ver, as complicações causadas por ter vários processadores, comandos sendo processados por mais de um componente e otimizações criadas nos componentes dificultam a previsão da criação de perfil. Na próxima seção, cada um desses desafios de criação de perfil será resolvido. Sequências de renderização direct3D de exemplo serão mostradas, com as técnicas de medição que acompanham. Com esse conhecimento, você poderá gerar medidas precisas e repetidas em chamadas individuais.

## <a name="how-to-accurately-profile-a-direct3d-render-sequence"></a>Como fazer o perfil com precisão de uma sequência de renderização direct3D

Agora que alguns dos desafios de criação de perfil foram realçados, esta seção mostrará técnicas que ajudarão você a gerar medidas de perfil que podem ser usadas para orçamento. Medidas de criação de perfil precisas e repetidas serão possíveis se você entender a relação entre os componentes controlados pela CPU e como evitar otimizações de desempenho implementadas pelo runtime e pelo driver.

Para começar, você precisa ser capaz de medir com precisão o tempo de execução de uma única chamada à API.

### <a name="pick-an-accurate-measurement-tool-like-queryperformancecounter"></a>Escolher uma ferramenta de medida precisa, como QueryPerformanceCounter

O microsoft Windows sistema operacional inclui um temporizador de alta resolução que pode ser usado para medir tempos decorridos de alta resolução. O valor atual de um temporizador desse tipo pode ser retornado [**usando QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter). Depois de invocar **QueryPerformanceCounter** para retornar valores start e stop, a diferença entre os dois valores pode ser convertida no tempo decorrido real (em segundos) usando **QueryPerformanceCounter**.

As vantagens de [**usar QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) são que ele está disponível no Windows e é fácil de usar. Basta cercar as chamadas com **uma chamada QueryPerformanceCounter** e salvar os valores start e stop. Portanto, este documento demonstrará como usar **QueryPerformanceCounter** para o perfil de tempos de execução, semelhante à maneira como um instrumentador de perfil o mediria. Veja um exemplo que mostra como inserir **QueryPerformanceCounter** em seu código-fonte:


```
  BeginScene();
    ...
    // Start profiling
    LARGE_INTEGER start, stop, freq;
    QueryPerformanceCounter(&start);

    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1); 

    QueryPerformanceCounter(&stop);
    stop.QuadPart -= start.QuadPart;
    QueryPerformanceFrequency(&freq);
    // Stop profiling
    ...
  EndScene();
  Present();
```



Exemplo 2: Implementação de criação de perfil personalizada com QPC

start e stop são dois inteiros grandes que conterão os valores de início e parada retornados pelo temporizador de alto desempenho. Observe que QueryPerformanceCounter(&start) é chamado logo antes de [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e QueryPerformanceCounter(&stop) ser chamado logo após [**DrawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Depois de obter o valor de parada, QueryPerformanceFrequency é chamado para retornar freq, que é a frequência do temporizador de alta resolução. Neste exemplo hipotético, suponha que você receba os seguintes resultados para iniciar, parar e freq:



| Variável Local | Número de tiques |
|----------------|-----------------|
| start          | 1792998845094   |
| parar           | 1792998845102   |
| Freq           | 3579545         |



 

Você pode converter esses valores no número de ciclos necessários para executar as chamadas à API como esta:


```
# ticks = (stop - start) = 1792998845102 - 1792998845094 = 8 ticks

# cycles = CPU speed * number of ticks / QPF
# 4568   = 2 GHz      * 8              / 3,579,545
```



Em outras palavras, são necessários cerca de 4568 ciclos de relógio para processar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) nesse computador de 2 GHz. Você pode converter esses valores no tempo real necessário para executar todas as chamadas como esta:


```
(stop - start)/ freq = elapsed time
8 ticks / 3,579,545 = 2.2E-6 seconds or between 2 and 3 microseconds.
```



O uso de QueryPerformanceCounter exige que você adicione medidas de início e parada à sequência de renderização e use QueryPerformanceFrequency para converter a diferença (número de tiques) no número de ciclos de CPU ou em tempo real. Identificar a técnica de medição é um bom começo para desenvolver uma implementação de criação de perfil personalizada. Mas antes de começar a fazer medidas, você precisa saber como lidar com a placa de vídeo.

### <a name="focus-on-cpu-measurements"></a>Foco nas medidas de CPU

Conforme indicado anteriormente, a CPU e a GPU funcionam em paralelo para processar o trabalho gerado pelas chamadas à API. Um aplicativo do mundo real requer a criação de perfil de ambos os tipos de processadores para descobrir se seu aplicativo é limitado por CPU ou GPU. Como o desempenho da GPU é específico do fornecedor, seria muito desafiador produzir resultados neste documento que abrangem a variedade de placas de vídeo disponíveis.

Em vez disso, este documento se concentrará apenas na criação de perfil do trabalho executado pela CPU usando uma técnica personalizada para medir o runtime e o trabalho do driver. O trabalho de GPU será reduzido para uma quantidade insignificante, para que os resultados da CPU sejam mais visíveis. Um benefício dessa abordagem é que essa técnica resulta no Apêndice que você deve ser capaz de correlacionar com suas medidas. Para reduzir o trabalho exigido pela placa de vídeo para um nível insignificante, basta reduzir o trabalho de renderização para o mínimo possível. Isso pode ser feito limitando chamadas de desenho para renderizar um único triângulo e pode ser ainda mais restrito para que cada triângulo contenha apenas um pixel.

A unidade de medida usada neste documento para medir o trabalho da CPU será o número de ciclos de relógio da CPU em vez da hora real. Os ciclos de relógio da CPU têm a vantagem de que ele é mais portátil (para aplicativos limitados à CPU) do que o tempo decorrido real entre máquinas com velocidades de CPU diferentes. Isso pode ser facilmente convertido em tempo real, se desejado.

Este documento não abrange tópicos relacionados ao balanceamento da carga de trabalho entre a CPU e a GPU. Lembre-se de que o objetivo deste documento não é medir o desempenho geral de um aplicativo, mas mostrar como medir com precisão o tempo necessário para o runtime e o driver processar chamadas à API. Com essas medidas precisas, você pode assumir a tarefa de orçamento da CPU para entender determinados cenários de desempenho.

### <a name="controlling-runtime-and-driver-optimizations"></a>Controlando otimizações de runtime e driver

Com uma técnica de medição identificada e uma estratégia para reduzir o trabalho de GPU, a próxima etapa é entender o runtime e as otimizações de driver que ficam no caminho quando você está criação de perfil.

O trabalho de CPU pode ser dividido em três buckets: o trabalho do aplicativo, o trabalho de runtime e o trabalho do driver. Ignore o trabalho do aplicativo, pois isso está sob controle do programador. Do ponto de vista do aplicativo, o runtime e o driver são como caixas pretas, pois o aplicativo não tem controle sobre o que é implementado neles. A chave é entender as técnicas de otimização que podem ser implementadas no runtime e no driver. Se você não entender essas otimizações, será muito fácil chegar à conclusão errada sobre a quantidade de trabalho que a CPU está fazendo com base nas medidas de perfil. Em particular, há dois tópicos relacionados a algo chamado buffer de comando e o que ele pode fazer para ofuscar a criação de perfil. Esses tópicos são:

-   Otimização de runtime com o Buffer de Comando. O buffer de comando é uma otimização de runtime que reduz o impacto de uma transição de modo. Para controlar o tempo da transição de modo, consulte [Controlando o buffer de comando](#controlling-the-command-buffer).
-   Negando os efeitos de tempo do Buffer de Comando. O tempo decorrido de uma transição de modo pode ter um grande impacto nas medidas de criação de perfil. A estratégia para isso é tornar [a sequência de renderização grande em comparação com a transição de modo](#make-the-render-sequence-large-compared-to-the-mode-transition).

### <a name="controlling-the-command-buffer"></a>Controlando o buffer de comando

Quando um aplicativo faz uma chamada à API, o runtime converte a chamada à API em um formato independente do dispositivo (que chamaremos de comando) e a armazena no buffer de comando. O buffer de comando é adicionado ao diagrama a seguir.

![diagrama de componentes de CPU, incluindo um buffer de comando](images/microbenchmarkcommandbuffer2.png)

Sempre que o aplicativo faz outra chamada à API, o runtime repete essa sequência e adiciona outro comando ao buffer de comando. Em algum momento, o runtime esvazia o buffer (enviando os comandos para o driver). No Windows XP, o vazio do buffer de comando causa uma transição de modo à medida que o sistema operacional alterna do runtime (em execução no modo de usuário) para o driver (em execução no modo kernel), conforme mostrado no diagrama a seguir.

-   modo de usuário – o modo de processador sem privilégios que executa o código do aplicativo. Os aplicativos de modo de usuário não podem obter acesso aos dados do sistema, exceto por meio de serviços do sistema.
-   modo kernel – o modo de processador privilegiado no qual Windows código executivo baseado em dados é executado. Um driver ou thread em execução no modo kernel tem acesso a toda a memória do sistema, acesso direto ao hardware e instruções de CPU para executar E/S com o hardware.

![diagrama de transições entre o modo de usuário e o modo kernel](images/microbenchmarkcommandbuffer3.png)

A transição ocorre sempre que a CPU muda de usuário para modo kernel (e vice-versa) e o número de ciclos necessários é grande em comparação com uma chamada à API individual. Se o runtime enviasse cada chamada à API para o driver quando ele foi invocado, cada chamada à API incorreria no custo de uma transição de modo.

Em vez disso, o buffer de comando é uma otimização de runtime projetada para reduzir o custo efetivo da transição de modo. O buffer de comando enfilia muitos comandos de driver em preparação para uma transição de modo único. Quando o runtime adiciona um comando ao buffer de comando, o controle é retornado ao aplicativo. Um profiler não tem como saber que os comandos do driver provavelmente ainda não foram enviados ao driver. Como resultado, os números retornados por um instrumentador de instrumentação off-the-shelf são enganosos, pois medem o trabalho de runtime, mas não o trabalho do driver associado.

### <a name="profile-results-without-a-mode-transition"></a>Resultados do perfil sem uma transição de modo

Usando a sequência de renderização do exemplo 2, aqui estão algumas medidas de tempo típicas que ilustram a magnitude de uma transição de modo. Supondo que as chamadas [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) não causem uma transição de modo, um instrumentador de instrumentação pronto para uso pode retornar resultados semelhantes a estes:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
```



Cada um desses números é a quantidade de tempo que leva para o runtime adicionar essas chamadas ao buffer de comando. Como não há nenhuma transição de modo, o driver ainda não fez nenhum trabalho. Os resultados do profiler são precisos, mas não medem todo o trabalho que a sequência de renderização eventualmente fará com que a CPU execute.

### <a name="profile-results-with-a-mode-transition"></a>Resultados do perfil com uma transição de modo

Agora, veja o que acontece para o mesmo exemplo quando ocorre uma transição de modo. Desta vez, suponha que [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) causem uma transição de modo. Mais uma vez, um profiler de instrumentação fora da plataforma pode retornar resultados semelhantes a estes:


```
Number of cycles for SetTexture           : 98 
Number of cycles for DrawPrimitive        : 946,900
```



O tempo medido para [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) é quase o mesmo, no entanto, o aumento significativo na quantidade de tempo gasto em [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) é devido à transição de modo. Veja o que está acontecendo:

1.  Suponha que o buffer de comando tenha espaço para um comando antes que nossa sequência de renderização seja iniciada.
2.  [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) é convertido em um formato independente de dispositivo e adicionado ao buffer de comando. Nesse cenário, essa chamada preenche o buffer de comando.
3.  O tempo de execução tenta adicionar [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ao buffer de comando, mas não pode, porque está cheio. Em vez disso, o tempo de execução esvazia o buffer de comando. Isso faz com que a transição do modo kernel. Suponha que a transição leve cerca de 5000 ciclos. Esse tempo contribui para o tempo gasto em **DrawPrimitive**.
4.  Em seguida, o driver processa o trabalho associado a todos os comandos que foram esvaziados do buffer de comandos. Suponha que o tempo do driver para processar os comandos que quase preenchem o buffer de comando seja de cerca de 935.000 ciclos. Suponha que o driver de trabalho associado a [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) seja de cerca de 2750 ciclos. Esse tempo contribui para o tempo gasto em [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).
5.  Quando o driver conclui seu trabalho, a transição do modo de usuário retorna o controle para o tempo de execução. O buffer de comando agora está vazio. Suponha que a transição leve cerca de 5000 ciclos.
6.  A sequência de renderização termina convertendo [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) e adicionando-o ao buffer de comando. Suponha que isso leve cerca de 900 ciclos. Esse tempo contribui para o tempo gasto em **DrawPrimitive**.

Resumindo os resultados, você verá:


```
DrawPrimitive = kernel-transition + driver work    + user-transition + runtime work
DrawPrimitive = 5000              + 935,000 + 2750 + 5000            + 900
DrawPrimitive = 947,950  
```



Assim como a medida para [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) sem a transição de modo (900 ciclos), a medida para **DrawPrimitive** com a transição de modo (947.950 ciclos) é precisa, mas inútil em termos de orçamento de trabalho de CPU. O resultado contém o trabalho de tempo de execução correto, o driver funciona para [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), o driver funciona para todos os comandos que precedem **SetTexture** e duas transições de modo. No entanto, a medida não tem o funcionamento do driver **DrawPrimitive** .

Uma transição de modo pode acontecer em resposta a qualquer chamada. Depende do que estava anteriormente no buffer de comandos. Você precisa controlar a transição de modo para entender a quantidade de trabalho de CPU (tempo de execução e driver) associada a cada chamada. Para fazer isso, você precisa de um mecanismo para controlar o buffer de comando e o tempo de transição de modo.

### <a name="the-query-mechanism"></a>O mecanismo de consulta

O mecanismo de consulta no Microsoft Direct3D 9 foi projetado para permitir que o tempo de execução consulte a GPU em busca de progresso e retorne determinados dados da GPU. Durante a criação de perfil, se o trabalho da GPU for minimizado para que ele tenha um impacto insignificante sobre o desempenho, você poderá retornar o status da GPU para ajudar a medir o trabalho do driver. Afinal, o trabalho do driver é concluído quando a GPU viu os comandos do driver. Além disso, o mecanismo de consulta pode ser coaxed no controle de duas características de buffer de comando que são importantes para a criação de perfil: quando o buffer de comando esvazia e quanto trabalho está no buffer.

Aqui está a mesma sequência de renderização usando o mecanismo de consulta:


```
// 1. Create an event query from the current device
IDirect3DQuery9* pEvent;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEvent);

// 2. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 3. Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

// 4. Start profiling
LARGE_INTEGER start, stop;
QueryPerformanceCounter(&start);

// 5. Invoke the API calls to be profiled.
SetTexture(...);
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 1);

// 6. Add an end marker to the command buffer queue.
pEvent->Issue(D3DISSUE_END);

// 7. Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
    
// 8. End profiling
QueryPerformanceCounter(&stop);
```



Exemplo 3: usando uma consulta para controlar o buffer de comando

Aqui está uma explicação mais detalhada de cada uma dessas linhas de código:

1.  Crie uma consulta de evento criando um objeto de consulta com o \_ evento D3DQUERYTYPE.
2.  Adicione um marcador de evento de consulta ao buffer de comando chamando [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)([**D3DISSUE \_ end**](d3dissue-end.md)). Esse marcador informa o driver para controlar quando a GPU conclui a execução de quaisquer comandos precedidos do marcador.
3.  A primeira chamada esvazia o buffer de comando porque chamar [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) com [**D3DGETDATA \_ flush**](d3dgetdata-flush.md) força o buffer de comando a ser esvaziado. Cada chamada subsequente está verificando a GPU para ver quando ele conclui o processamento de todo o trabalho de buffer de comando. Esse loop não retorna S \_ OK até que a GPU esteja ociosa.
4.  Exemplo de hora de início.
5.  Invocar as chamadas à API que estão sendo Profiles.
6.  Adicione um segundo marcador de evento de consulta ao buffer de comando. Esse marcador será usado para acompanhar a conclusão das chamadas.
7.  A primeira chamada esvazia o buffer de comando porque chamar [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) com [**D3DGETDATA \_ flush**](d3dgetdata-flush.md) força o buffer de comando a ser esvaziado. Quando a GPU termina de processar todo o trabalho de buffer de comando, **GetData** retorna S \_ OK e o loop é encerrado porque a GPU está ociosa.
8.  Exemplo de hora de parada.

Aqui estão os resultados medidos com QueryPerformanceCounter e QueryPerformanceFrequency:



| Variável Local | Número de tiques |
|----------------|-----------------|
| start          | 1792998845060   |
| parar           | 1792998845090   |
| freq           | 3579545         |



 

Convertendo tiques em ciclos novamente (em uma máquina de 2 GHz):


```
# ticks  = (stop - start) = 1792998845090 - 1792998845060 = 30 ticks
# cycles = CPU speed * number of ticks / QPF
# 16,450 = 2 GHz      * 30             / 3,579,545
```



Aqui está a divisão do número de ciclos por chamada:


```
Number of cycles for SetTexture           : 100
Number of cycles for DrawPrimitive        : 900
Number of cycles for Issue                : 200
Number of cycles for GetData              : 16,450
```



O mecanismo de consulta nos permitiu controlar o tempo de execução e o funcionamento do driver que está sendo medido. Para entender cada um desses números, veja o que está acontecendo em resposta a cada uma das chamadas à API, juntamente com os tempos estimados:

1.  A primeira chamada esvazia o buffer de comando chamando [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) com [**D3DGETDATA \_ flush**](d3dgetdata-flush.md). Quando a GPU termina de processar todo o trabalho de buffer de comando, **GetData** retorna S \_ OK e o loop é encerrado porque a GPU está ociosa.
2.  A sequência de renderização começa convertendo [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) em um formato independente de dispositivo e adicionando-o ao buffer de comando. Suponha que isso leve cerca de 100 ciclos.
3.  [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) é convertido e adicionado ao buffer de comando. Suponha que isso leve cerca de 900 ciclos.
4.  O [**problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) adiciona um marcador de consulta ao buffer de comando. Suponha que isso leve cerca de 200 ciclos.
5.  [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) faz com que o buffer de comando seja esvaziado, o que força a transição do modo kernel. Suponha que isso leve cerca de 5000 ciclos.
6.  Em seguida, o driver processa o trabalho associado a todas as quatro chamadas. Suponha que o tempo do driver para processar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) seja de cerca de 2964 ciclos, [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) é de aproximadamente 3600 ciclos, o [**problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) é de cerca de 200 ciclos. Portanto, o tempo total do driver para todos os quatro comandos é de cerca de 6450 ciclos.
    > [!Note]  
    > O driver também leva algum tempo para ver qual é o status da GPU. Como o trabalho de GPU é trivial, a GPU já deve ser feita. [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retornará S \_ OK com base na probabilidade de a GPU ser concluída.

     

7.  Quando o driver conclui seu trabalho, a transição do modo de usuário retorna o controle para o tempo de execução. O buffer de comando agora está vazio. Suponha que isso leve cerca de 5000 ciclos.

Os números para [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) incluem:


```
GetData = kernel-transition + driver work + user-transition
GetData = 5000              + 6450        + 5000           
GetData = 16,450  

driver work = SetTexture + DrawPrimitive + Issue = 
driver work = 2964       + 3600          + 200   = 6450 cycles 
```



O mecanismo de consulta usado em combinação com QueryPerformanceCounter mede todo o trabalho de CPU. Isso é feito com uma combinação de marcadores de consulta e comparações de status de consulta. Os marcadores de consulta de início e parada adicionados ao buffer de comando são usados para controlar a quantidade de trabalho no buffer. Aguardando até que o código de retorno correto seja retornado, a medida inicial é feita logo antes de uma sequência de renderização limpa ser iniciada e a medida de parada é feita logo após o driver ter concluído o trabalho associado ao conteúdo do buffer de comando. Isso captura efetivamente o trabalho de CPU feito pelo tempo de execução, bem como o driver.

Agora que você conhece o buffer de comando e o efeito que ele pode ter na criação de perfil, você deve saber que existem algumas outras condições que podem fazer com que o tempo de execução esvazie o buffer de comando. Você precisa observar isso em suas sequências de processamento. Algumas dessas condições estão em resposta a chamadas de API, outras estão em resposta às alterações de recurso no tempo de execução. Qualquer uma das condições a seguir causará uma transição de modo:

-   Quando um dos métodos Lock ([**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)) é chamado em um buffer de vértice, buffer de índice ou textura (sob determinadas condições com determinados sinalizadores).
-   Quando um dispositivo ou buffer de vértice, buffer de índice ou textura é criado.
-   Quando um buffer de dispositivo ou de vértice, um buffer de índice ou uma textura é destruído pela última versão.
-   Quando [**ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) é chamado.
-   Quando [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) é chamado.
-   Quando o buffer de comando é preenchido.
-   Quando [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) é chamado com D3DGETDATA \_ flush.

Tenha cuidado para observar essas condições em suas sequências de renderização. Sempre que uma transição de modo for adicionada, 10.000 ciclos de trabalho de driver serão adicionados às suas medições de criação de perfil. Além disso, o buffer de comando não é dimensionado estaticamente. O tempo de execução pode alterar o tamanho do buffer em resposta à quantidade de trabalho que está sendo gerada pelo aplicativo. Essa ainda é outra otimização que depende de uma sequência de renderização.

Portanto, tenha cuidado para controlar as transições do modo durante a criação de perfil. O mecanismo de consulta oferece um método robusto para esvaziar o buffer de comando para que você possa controlar o tempo da transição de modo, bem como a quantidade de trabalho que o buffer contém. No entanto, até mesmo essa técnica pode ser aprimorada reduzindo o tempo de transição do modo para torná-lo insignificante em relação ao resultado medido.

### <a name="make-the-render-sequence-large-compared-to-the-mode-transition"></a>Tornar a sequência de renderização grande em comparação com a transição de modo

No exemplo anterior, a opção de modo kernel e a opção de modo de usuário consomem cerca de 10.000 ciclos que não têm nada a ver com o tempo de execução e o driver funcionam. Como a transição de modo é incorporada ao sistema operacional, ela não pode ser reduzida para zero. Para tornar a transição de modo insignificante, a sequência de renderização precisa ser ajustada para que o driver e o funcionamento do tempo de execução sejam uma ordem de magnitude maior do que as opções de modo. Você pode tentar fazer uma subtração para remover as transições, mas amortizar o custo em um custo muito maior de sequência de renderização é mais confiável.

A estratégia para reduzir a transição de modo até que se torne insignificante é adicionar um loop à sequência de renderização. Por exemplo, vamos examinar os resultados da criação de perfil se um loop for adicionado, que repetirá a sequência de renderização 1500 vezes:


```
// Initialize the array with two textures, same size, same format
IDirect3DTexture* texArray[2];

CreateQuery(D3DQUERYTYPE_EVENT, pEvent);
pEvent->Issue(D3DISSUE_END);
while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

LARGE_INTEGER start, stop;
// Now start counting because the video card is ready
QueryPerformanceCounter(&start);

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  SetTexture(taxArray[i%2]);
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

pEvent->Issue(D3DISSUE_END);

while(S_FALSE == pEvent->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
QueryPerformanceCounter(&stop);
```



Exemplo 4: adicionar um loop à sequência de renderização

Aqui estão os resultados medidos com QueryPerformanceCounter e QueryPerformanceFrequency:



| Variável Local | Número de TICs |
|----------------|----------------|
| start          | 1792998845000  |
| parar           | 1792998847084  |
| freq           | 3579545        |



 

Usar QueryPerformanceCounter mede os tiques 2.840 agora. Converter tiques em ciclos é o mesmo que já mostramos:


```
# ticks  = (stop - start) = 1792998847084 - 1792998845000 = 2840 ticks
# cycles    = machine speed * number of ticks / QPF
# 6,900,000 = 2 GHz          * 2840           / 3,579,545
```



Em outras palavras, leva cerca de 6,9 milhões ciclos neste computador de 2 GHz processar as chamadas de 1500 no loop de processamento. Dos ciclos de 6,9 milhões, a quantidade de tempo nas transições de modo é de aproximadamente 10K, então agora os resultados do perfil estão quase totalmente medindo o trabalho associado ao [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e ao [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Observe que o exemplo de código requer uma matriz de duas texturas. Para evitar uma otimização de tempo de execução que removeria [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) se ele definir o mesmo ponteiro de textura sempre que for chamado, basta usar uma matriz de duas texturas. Dessa forma, cada vez que passar pelo loop, o ponteiro de textura é alterado e o trabalho completo associado a **SetTexture** é executado. Certifique-se de que ambas as texturas sejam do mesmo tamanho e formato, para que nenhum outro Estado seja alterado quando a textura tiver.

E agora você tem uma técnica para a criação de perfil do Direct3D. Ele se baseia no contador de alto desempenho (QueryPerformanceCounter) para registrar o número de tiques que leva a CPU para processar o trabalho. O trabalho é cuidadosamente controlado para ser o tempo de execução e o funcionamento do driver associados a chamadas de API usando o mecanismo de consulta. Uma consulta fornece dois meios de controle: primeiro para esvaziar o buffer de comando antes do início da sequência de renderização e depois para retornar quando o trabalho da GPU for concluído.

Até agora, este documento mostrou como criar um perfil de uma sequência de renderização. Cada sequência de renderização foi bem simples, contendo uma única chamada [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) e uma chamada [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . Isso foi feito para se concentrar no buffer de comandos e no uso do mecanismo de consulta para controlá-lo. Aqui está um breve resumo de como criar um perfil de uma sequência de renderização arbitrária:

-   Use um contador de alto desempenho como o QueryPerformanceCounter para medir o tempo necessário para processar cada chamada à API. Use QueryPerformanceFrequency e a taxa de relógio da CPU para converter isso para o número de ciclos de CPU por chamada à API.
-   Minimize a quantidade de trabalho de GPU renderizando listas de triângulo, onde cada triângulo contém um pixel.
-   Use o mecanismo de consulta para esvaziar o buffer de comando antes da sequência de renderização. Isso garante que a criação de perfil irá capturar a quantidade correta de tempo de execução e o trabalho de driver associados à sequência de renderização.
-   Controle a quantidade de trabalho adicionada ao buffer de comando com marcadores de eventos de consulta. Essa mesma consulta detecta quando a GPU conclui seu trabalho. Como o trabalho de GPU é trivial, é praticamente equivalente a medir quando o trabalho do driver é concluído.

Todas essas técnicas são usadas para perfilar alterações de estado. Supondo que você leu e entendeu como controlar o buffer de comando e tenha concluído com êxito as medidas de linha de base em [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), você está pronto para adicionar alterações de estado às sequências de renderização. Há alguns desafios de criação de perfil adicionais ao adicionar alterações de estado a uma sequência de renderização. Se você pretende adicionar alterações de estado às sequências de renderização, certifique-se de continuar na próxima seção.

## <a name="profiling-direct3d-state-changes"></a>Criando perfil de alterações de estado do Direct3D

O Direct3D usa muitos Estados de renderização para controlar quase todos os aspectos do pipeline. As APIs que causam alterações de estado incluem qualquer função ou método diferente das \* chamadas primitivas de desenho.

As alterações de estado são complicadas porque talvez você não consiga ver o custo de uma alteração de estado sem renderização. Isso é resultado do algoritmo lento que o driver e a GPU usam para adiar o trabalho até que absolutamente precise ser feito. Em geral, você deve seguir estas etapas para medir uma alteração de estado único:

1.  Perfil [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) primeiro.
2.  Adicione uma alteração de estado à sequência de renderização e o perfil da nova sequência.
3.  Subtraia a diferença entre as duas sequências para obter o custo da alteração de estado.

Naturalmente, tudo o que você aprendeu sobre o uso do mecanismo de consulta e a colocação da sequência de renderização em um loop para negar o custo da transição de modo ainda se aplica.

### <a name="profiling-a-simple-state-change"></a>Criação de perfil de uma alteração de estado simples

Começando com uma sequência de renderização que contém [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), aqui está a sequência de código para medir o custo de adição de [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture):


```
// Get the start counter value as shown in Example 4 

// Initialize a texture array as shown in Example 4
IDirect3DTexture* texArray[2];

// Render sequence loop 
for(int i = 0; i < 1500; i++)
{
  SetTexture(0, texArray[i%2];
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
}

// Get the stop counter value as shown in Example 4 
```



Exemplo 5: medindo uma chamada à API de alteração de estado

Observe que o loop contém duas chamadas, [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Os loops de sequência de renderização 1500 vezes e geram resultados semelhantes a estes:



| Variável Local | Número de TICs |
|----------------|----------------|
| start          | 1792998860000  |
| parar           | 1792998870260  |
| freq           | 3579545        |



 

A conversão de tiques em ciclos novamente resulta em:


```
# ticks  = (stop - start) = 1792998870260 - 1792998860000 = 10,260 ticks
# cycles    = machine speed * number of ticks / QPF
5,775,000   = 2 GHz          * 10,260         / 3,579,545
```



A divisão pelo número de iterações no loop produz:


```
5,775,000 cycles / 1500 iterations = 3850 cycles for one iteration
```



Cada iteração do loop contém uma alteração de estado e uma chamada de desenho. Subtrair o resultado da sequência de renderização [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) deixa:


```
3850 - 1100 = 2750 cycles for SetTexture
```



Este é o número médio de ciclos para adicionar [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) a essa sequência de renderização. Essa mesma técnica pode ser aplicada a outras alterações de estado.

Por que [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) é chamada de alteração de estado simples? Como o estado que está sendo definido é restrito para que o pipeline faça a mesma quantidade de trabalho sempre que o estado for alterado. Restringir ambas as texturas ao mesmo tamanho e formato garante a mesma quantidade de trabalho para cada chamada **SetTexture** .

### <a name="profiling-a-state-change-that-needs-to-be-toggled"></a>Criação de perfil de uma alteração de estado que precisa ser alternada

Há outras alterações de estado que fazem com que a quantidade de trabalho executada pelo pipeline de gráficos seja alterada para cada iteração do loop de renderização. Por exemplo, se o teste z estiver habilitado, cada cor de pixel atualizará um destino de renderização somente depois que o valor z do novo pixel for testado em relação ao valor z do pixel existente. Se o teste z estiver desabilitado, esse teste por pixel não será feito e a saída será gravada muito mais rapidamente. Habilitar ou desabilitar o estado de teste z altera drasticamente a quantidade de trabalho realizado (pela CPU, bem como a GPU) durante a renderização.

[**Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) requer um estado de renderização específico e um valor de estado para habilitar ou desabilitar o teste de z. O valor de estado específico é avaliado em tempo de execução para determinar a quantidade de trabalho necessária. É difícil medir essa alteração de estado em um loop de renderização e ainda precondicionar o estado do pipeline para que ele alterne. A única solução é alternar a alteração de estado durante a sequência de renderização.

Por exemplo, a técnica de criação de perfil precisa ser repetida duas vezes, da seguinte maneira:

1.  Comece pela criação de perfil da sequência de renderização [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) . Chame essa linha de base.
2.  Perfil uma segunda sequência de renderização que alterna a alteração de estado. O loop de sequência de renderização contém:
    -   Uma alteração de estado para definir o estado em uma condição "false".
    -   [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) assim como a sequência original.
    -   Uma alteração de estado para definir o estado em uma condição "true".
    -   Um segundo [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para forçar que a segunda alteração de estado seja realizada.
3.  Localize a diferença entre as duas sequências de renderização. Isso é feito por:
    -   Multiplique a sequência [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) de linha de base por 2 porque há duas chamadas **DrawPrimitive** na nova sequência.
    -   Subtraia o resultado da nova sequência da sequência original.
    -   Divida o resultado por 2 para obter o custo médio das alterações de estado "false" e "true".

Com a técnica de loop usada na sequência de renderização, o custo da alteração do estado do pipeline precisa ser medido alternando o estado de um "verdadeiro" para uma condição "false" e vice-versa, para cada iteração na sequência de renderização. O significado de "true" e "false" aqui não são literais, isso simplesmente significa que o estado precisa ser definido em condições opostas. Isso faz com que ambas as alterações de estado sejam medidas durante a criação de perfil. É claro que tudo o que você aprendeu a usar o mecanismo de consulta e colocar a sequência de renderização em um loop para negar o custo da transição de modo ainda se aplica.

Por exemplo, aqui está a sequência de código para medir o custo de ativação ou desativação do teste de z:


```
// Get the start counter value as shown in Example 4 

// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the "false" condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Set the pipeline state to the "true" condition
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}

// Get the stop counter value as shown in Example 4 
```



Exemplo 5: medindo uma alteração de estado de alternância

O loop alterna o estado executando duas chamadas [**Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) . A primeira chamada **Setrenderingstate** desabilita o teste z e o segundo **setrenderingstate** habilita o teste de z. Cada **Setrenderingstate** é seguido por [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para que o trabalho associado à alteração de estado seja processado pelo driver em vez de definir apenas um bit sujo no driver.

Esses números são razoáveis para essa sequência de renderização:



| Variável Local | Número de tiques |
|----------------|-----------------|
| start          | 1792998845000   |
| parar           | 1792998861740   |
| freq           | 3579545         |



 

A conversão de tiques em ciclos novamente resulta em:


```
# ticks  = (stop - start) = 1792998861740 - 1792998845000 = 15,120 ticks
# cycles    = machine speed * number of ticks / QPF
 9,300,000  = 2 GHz          * 16,740         / 3,579,545
```



A divisão pelo número de iterações no loop produz:


```
9,300,000 cycles / 1500 iterations = 6200 cycles for one iteration
```



Cada iteração do loop contém duas alterações de estado e duas chamadas de desenho. Subtrair as chamadas Draw (supondo 1100 ciclos) deixa:


```
6200 - 1100 - 1100 = 4000 cycles for both state changes
```



Este é o número médio de ciclos para ambas as alterações de estado, portanto, o tempo médio para cada alteração de estado é:


```
4000 / 2  = 2000 cycles for each state change
```



Portanto, o número médio de ciclos para habilitar ou desabilitar o teste de z é de 2000 ciclos. Vale a pena observar que o QueryPerformanceCounter está medindo o z-Enable time e z-Disable na metade do tempo. Na verdade, essa técnica mede a média de ambas as alterações de estado. Em outras palavras, você está medindo o tempo de alternância de um estado. Usando essa técnica, você não tem como saber se os tempos de habilitação e desabilitação são equivalentes, já que você mediu a média de ambos. No entanto, esse é um número razoável para usar ao orçar um estado de alternância, pois um aplicativo que causa essa alteração de estado só pode fazer isso alternando esse estado.

Agora, você pode aplicar essas técnicas e criar o perfil de todas as alterações de estado desejadas, certo? Não exatamente. Você ainda precisa ter cuidado com as otimizações projetadas para reduzir a quantidade de trabalho que precisa ser feito. Há dois tipos de otimizações que você deve estar atento ao projetar suas sequências de processamento.

### <a name="watch-out-for-state-change-optimizations"></a>Tome cuidado com as otimizações de alteração de estado

A seção anterior mostra como criar o perfil dos dois tipos de alterações de Estado: uma alteração de estado simples que é restrita para gerar a mesma quantidade de trabalho para cada iteração e uma alteração de estado de alternância que altera drasticamente a quantidade de trabalho realizado. O que acontece se você usar a sequência de renderização anterior e adicionar outra alteração de estado a ela? Por exemplo, ele usa a sequência de renderização z>-Enable e adiciona uma comparação z-Func a ela:


```
// Add a loop to the render sequence 
for(int i = 0; i < 1500; i++)
{
  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZFUNC, D3DCMP_NEVER);

  // Precondition the pipeline state to the opposite condition
  SetRenderState(D3DRS_ZENABLE, FALSE);
  
  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 0)*3, 1);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZFUNC, D3DCMP_ALWAYS);

  // Now set the state change you want to measure
  SetRenderState(D3DRS_ZENABLE, TRUE);

  // Force the state change to propagate to the GPU
  DrawPrimitive(D3DPT_TRIANGLELIST, (2*i + 1)*3, 1); 
}
```



O estado z-Func define o nível de comparação ao gravar no buffer z (entre o valor z de um pixel atual com o valor z de um pixel no buffer de profundidade). D3DCMP \_ nunca desativa a comparação de testes de z enquanto \_ o D3DCMP sempre define a comparação para acontecer sempre que o teste z for concluído.

A criação de perfil de uma dessas alterações de estado em uma sequência de renderização com [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) gera resultados semelhantes a estes:



| Alteração de estado único | Número médio de ciclos |
|---------------------|--------------------------|
| \_Somente D3DRS ZENABLE | 2000                     |



 

ou



| Alteração de estado único | Número médio de ciclos |
|---------------------|--------------------------|
| \_Somente D3DRS ZFUNC   | 600                      |



 

Mas, se você criar o perfil de D3DRS \_ ZENABLE e D3DRS \_ ZFUNC na mesma sequência de renderização, poderá ver resultados como estes:



| Ambas as alterações de estado            | Número médio de ciclos |
|-------------------------------|--------------------------|
| D3DRS \_ ZENABLE + D3DRS \_ ZFUNC | 2000                     |



 

Você pode esperar que o resultado seja a soma dos ciclos 2000 e 600 (ou 2600), pois o driver está fazendo todo o trabalho associado à configuração de ambos os Estados de processamento. Em vez disso, a média é de 2000 ciclos.

Esse resultado reflete uma otimização de alteração de estado implementada no tempo de execução, o driver ou a GPU. Nesse caso, o driver poderia ver o primeiro [**Setprocessstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e definir um estado sujo que adiaria o trabalho até mais tarde. Quando o driver vê o segundo **Setrenderingstate**, o mesmo estado sujo pode ser definido com redundância e o mesmo trabalho seria adiado mais uma vez. Quando [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) é chamado, o trabalho associado ao estado sujo é finalmente processado. O driver executa o trabalho uma vez, o que significa que as duas primeiras alterações de estado são efetivamente consolidadas pelo driver. Da mesma forma, as terceira e quarta alterações de estado são efetivamente consolidadas pelo driver em uma única alteração de estado quando o segundo **DrawPrimitive** é chamado. O resultado líquido é que o driver e a GPU processam uma única alteração de estado para cada chamada de desenho.

Esse é um bom exemplo de otimização de driver dependente de sequência. O driver adie o trabalho duas vezes definindo um estado sujo e, em seguida, executou o trabalho uma vez para limpar o estado sujo. Esse é um bom exemplo do tipo de aperfeiçoamento de eficiência que pode ocorrer quando o trabalho é adiado até que seja absolutamente necessário.

Como você sabe quais alterações de Estado definem um estado sujo internamente e, portanto, adiam o trabalho até mais tarde? Apenas testando sequências de renderização (ou conversando com os gravadores de driver). Os drivers são atualizados e aprimorados periodicamente para que a lista de otimizações não seja estática. Há apenas uma maneira de saber absolutamente o que os custos de alteração de estado em uma determinada sequência de renderização, em um determinado conjunto de hardwares; e isso é para medir.

### <a name="watch-out-for-drawprimitive-optimizations"></a>Tome cuidado com otimizações de DrawPrimitive

Além das otimizações de alteração de estado, o tempo de execução tentará otimizar o número de chamadas de desenho que o driver precisa processar. Por exemplo, considere isso voltar para retornar chamadas de desenho:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 3); // Draw 3 primitives, vertices 0 - 8
DrawPrimitive(D3DPT_TRIANGLELIST, 9, 4); // Draw 4 primitives, vertices 9 - 20
```



Exemplo 5a: duas chamadas de desenho

Essa sequência contém duas chamadas Draw, que o tempo de execução consolidará em uma única chamada equivalente a:


```
DrawPrimitive(D3DPT_TRIANGLELIST, 0, 7); // Draw 7 primitives, vertices 0 - 20
```



Exemplo 5b: uma única chamada de desenho concatenada

O tempo de execução concatenará essas chamadas de desenho específicas em uma única chamada, o que reduz o funcionamento do driver em 50% porque o driver agora precisará processar apenas uma chamada de desenho.

Em geral, o tempo de execução concatena duas ou mais chamadas [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) de back-to-back quando:

1.  O tipo primitivo é uma lista de triângulo (D3DPT \_ TRIângulolist).
2.  Cada chamada de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) sucessiva deve referenciar vértices consecutivos dentro do buffer de vértice.

Da mesma forma, as condições certas para concatenar duas ou mais chamadas [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) de back-to-back são:

1.  O tipo primitivo é uma lista de triângulo (D3DPT \_ TRIângulolist).
2.  Cada chamada de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) sucessiva deve fazer referência sequencial de índices consecutivos dentro do buffer de índice.
3.  Cada chamada de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) sucessiva deve usar o mesmo valor para BaseVertexIndex.

Para evitar a concatenação durante a criação de perfil, modifique a sequência de renderização para que o tipo primitivo não seja uma lista de triângulos ou modifique a sequência de renderização para que não haja chamadas de desenho de back-to-back que usem vértices consecutivos (ou índices). Mais especificamente, o tempo de execução também concatena as chamadas draw que atendem às duas condições a seguir:

-   Quando a chamada anterior for [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), se a próxima chamada de desenho:
    -   usa uma lista de triângulos e
    -   Especifica o StartVertex = Previous StartVertex + anterior PrimitiveCount \* 3
-   Ao usar [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive), se a próxima chamada de desenho:
    -   usa uma lista de triângulos e
    -   Especifica o StartIndex = antigo StartIndex + anterior PrimitiveCount \* 3 e
    -   Especifica o BaseVertexIndex = BaseVertexIndex anterior

Aqui está um exemplo mais sutil da concatenação de chamada de desenho que é fácil de ignorar quando você está criando perfis. Suponha que a sequência de renderização tenha esta aparência:


```
  for(int i = 0; i < 1500; i++)
  {
    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Exemplo 5C: uma alteração de estado e uma chamada de desenho

O loop itera até 1500 triângulos, definindo uma textura e desenhando cada triângulo. Esse loop de renderização leva aproximadamente 2750 ciclos para os ciclos [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) e 1100 para [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) , conforme mostrado nas seções anteriores. Você pode, de modo intuitivo, esperar que a movimentação de **SetTexture** fora do loop de processamento deva reduzir a quantidade de trabalho feita pelo driver em 1500 \* 2750 ciclos, que é a quantidade de trabalho associada à chamada de $ **Texture** 1500 vezes. O trecho de código ficaria assim:


```
  SetTexture(...); // Set the state outside the loop
  for(int i = 0; i < 1500; i++)
  {
//    SetTexture(...);
    DrawPrimitive(D3DPT_TRIANGLELIST, i*3, 1);
  }
```



Exemplo 5D: exemplo 5C com a alteração de estado fora do loop

Mover [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) fora do loop de processamento reduz a quantidade de trabalho associada ao **SetTexture** , pois ele é chamado uma vez em vez de 1500 vezes. Um efeito secundário menos óbvio é que o trabalho para [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) também é reduzido de chamadas de 1500 para 1 chamada, pois todas as condições para concatenar chamadas de desenho são satisfeitas. Quando a sequência de renderização é processada, o tempo de execução processará chamadas de 1500 em uma única chamada de driver. Ao mover esta linha de código, a quantidade de trabalho do driver foi reduzida drasticamente:


```
total work done = runtime + driver work

Example 5c: with SetTexture in the loop:
runtime work = 1500 SetTextures + 1500 DrawPrimitives 
driver  work = 1500 SetTextures + 1500 DrawPrimitives 

Example 5d: with SetTexture outside of the loop:
runtime work = 1 SetTexture + 1 DrawPrimitive + 1499 Concatenated DrawPrimitives 
driver  work = 1 SetTexture + 1 DrawPrimitive 
```



Esses resultados estão totalmente corretos, mas são muito enganosos no contexto da pergunta original. A otimização de chamada de desenho fez com que a quantidade de trabalho do driver fosse reduzida drasticamente. Esse é um problema comum ao fazer a criação de perfil Personalizada. Ao eliminar chamadas de uma sequência de renderização, tenha cuidado para evitar a concatenação de chamada de desenho. Na verdade, esse cenário é um poderoso exemplo da quantidade de melhoria no desempenho do driver possível por essa otimização de tempo de execução.

Agora você sabe como medir as alterações de estado. Comece pela criação de perfil de [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive). Em seguida, adicione cada alteração de estado adicional à sequência (em alguns casos, adicionando uma chamada e, em outros casos, adicionando duas chamadas) e medir a diferença entre as duas sequências. Você pode converter os resultados em tiques ou ciclos ou tempo. Assim como medir as sequências de renderização com QueryPerformanceCounter, medir as alterações de estado individuais depende do mecanismo de consulta para controlar o buffer de comando e colocar as alterações de estado em um loop para minimizar o impacto das transições de modo. Essa técnica mede o custo de alternar um estado, uma vez que o criador de perfil retorna a média de habilitar e desabilitar o estado.

Com esse recurso, você pode começar a gerar sequências de renderização arbitrárias e medir com precisão o tempo de execução e o funcionamento do driver associados. Os números podem ser usados para responder a perguntas de orçamento como "Quantos mais dessas chamadas" podem ser feitas na sequência de renderização, mantendo uma taxa de quadros razoável, supondo cenários limitados à CPU.

## <a name="summary"></a>Resumo

Este documento demonstra como controlar o buffer de comando para que as chamadas individuais possam ser com o perfil correto. Os números de criação de perfil podem ser gerados em tiques, ciclos ou tempo absoluto. Elas representam a quantidade de tempo de execução e o trabalho de driver associados a cada chamada à API.

Comece com a criação de perfil de uma \* chamada primitiva de desenho em uma sequência de renderização. Lembre-se de:

1.  Use QueryPerformanceCounter para medir o número de tiques por chamada à API. Use QueryPerformanceFrequency para converter os resultados em ciclos ou tempo, se desejar.
2.  Use o mecanismo de consulta para esvaziar o buffer de comando antes de iniciar.
3.  Inclua a sequência de renderização em um loop para minimizar o impacto da transição de modo.
4.  Use o mecanismo de consulta para medir quando a GPU concluiu seu trabalho.
5.  Tome cuidado com a concatenação de tempo de execução que terá um grande impacto na quantidade de trabalho realizado.

Isso fornece um desempenho de linha de base para [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) que podem ser usados para a criação do. Para criar o perfil de uma alteração de estado, siga estas dicas adicionais:

1.  Adicione a alteração de estado a um perfil de sequência de renderização conhecido na nova sequência. Como o teste é feito em um loop, isso requer a definição do estado duas vezes em valores opostos (como habilitar e desabilitar por exemplo).
2.  Compare a diferença em tempos de ciclo entre as duas sequências.
3.  Para alterações de estado que alteram significativamente o pipeline (como [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)), subtraia a diferença entre as duas sequências para obter o tempo de alteração de estado.
4.  Para alterações de estado que alteram significativamente o pipeline (e, portanto, exigem alternância de Estados como [**Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)), subtraia a diferença entre as sequências de renderização e a divisão por 2. Isso irá gerar o número médio de ciclos para cada alteração de estado.

Mas tenha cuidado com otimizações que causam resultados inesperados durante a criação de perfil. As otimizações de alteração de estado podem definir Estados sujos que causam o trabalho a ser adiado. Isso pode causar resultados de perfil que não são tão intuitivos quanto o esperado. As chamadas de desenho concatenadas reduzirão drasticamente o trabalho do driver, o que pode levar a conclusões enganosas. As sequências de renderização cuidadosamente planejadas são usadas para impedir a alteração de estado e a ocorrência de concatenações de chamada de desenho. O truque é evitar que as otimizações ocorram durante a criação de perfil para que os números gerados sejam números de orçamento razoáveis.

> [!Note]  
> A duplicação dessa estratégia de criação de perfil em um aplicativo sem o mecanismo de consulta é mais difícil. Antes do Direct3D 9, a única maneira previsível de esvaziar o buffer de comando é bloquear uma superfície ativa (como um destino de renderização) para aguardar até que a GPU fique ociosa. Isso ocorre porque o bloqueio de uma superfície força o tempo de execução a esvaziar o buffer de comandos, caso haja algum comando de renderização no buffer que deve atualizar a superfície antes de ser bloqueado, além de aguardar a conclusão da GPU. Essa técnica é funcional, embora seja mais invasiva que usar o mecanismo de consulta introduzido no Direct3D 9.

 

## <a name="appendix"></a>Anexo

Os números nessa tabela são um intervalo de aproximações para a quantidade de tempo de execução e o trabalho de driver associados a cada uma dessas alterações de estado. As aproximaçãos se baseiam em medidas reais feitas nos drivers usando as técnicas mostradas no documento. Esses números foram gerados usando o tempo de execução do Direct3D 9 e dependem do driver.

As técnicas neste documento foram projetadas para medir o tempo de execução e o funcionamento do driver. Em geral, é impraticável fornecer resultados que correspondam ao desempenho da CPU e da GPU em todos os aplicativos, pois isso exigiria uma matriz exaustiva de sequências de processamento. Além disso, é particularmente difícil para o desempenho de benchmark da GPU porque ela é altamente dependente da configuração de estado no pipeline antes da sequência de renderização. Por exemplo, a habilitação da combinação alfa não afeta a quantidade de trabalho de CPU necessária, mas pode ter um grande impacto na quantidade de trabalho realizado pela GPU. Portanto, as técnicas neste documento restringem o trabalho de GPU ao valor mínimo possível limitando a quantidade de dados que precisam ser renderizados. Isso significa que os números na tabela corresponderão melhor aos resultados obtidos de aplicativos que são limitados por CPU (em oposição a um aplicativo limitado pela GPU).

Você é incentivado a usar as técnicas apresentadas para abordar os cenários e as configurações mais importantes para você. Os valores na tabela podem ser usados para comparar com os números que você gerar. Como cada driver varia, a única maneira de gerar os números reais que você verá é gerar resultados de criação de perfil usando seus cenários.



| Chamada à API                             | Número médio de ciclos |
|--------------------------------------|--------------------------|
| SetVertexDeclaration                 | 6500-11250             |
| SetFVF                               | 6400-11200             |
| SetVertexShader                      | 3000-12100             |
| SetPixelShader                       | 6300-7000              |
| SPECULARENABLE                       | 1900-11200             |
| SetRenderTarget                      | 6000-6250              |
| SetPixelShaderConstant (1 constante)  | 1500-9000              |
| NORMALIZENORMALS                     | 2200-8100              |
| Clarear                          | 1300-9000              |
| Setstreaming                      | 3700-5800              |
| ILUMINA                             | 1700-7500              |
| DIFFUSEMATERIALSOURCE                | 900-8300               |
| AMBIENTMATERIALSOURCE                | 900-8200               |
| COLORVERTEX                          | 800-7800               |
| SetLight                             | 2200-5100              |
| SetTransform                         | 3200-3750              |
| SetIndices                           | 900-5600               |
| TEMPERATURA                              | 1150-4800              |
| SetTexture                           | 2500-3100              |
| SPECULARMATERIALSOURCE               | 900-4600               |
| EMISSIVEMATERIALSOURCE               | 900-4500               |
| SetMaterial                          | 1000-3700              |
| ZENABLE                              | 700-3900               |
| WRAP0                                | 1600-2700              |
| MINFILTER                            | 1700-2500              |
| MAGFILTER                            | 1700-2400              |
| SetVertexShaderConstant (1 constante) | 1000-2700              |
| COLOROP                              | 1500-2100              |
| COLORARG2                            | 1300-2000              |
| COLORARG1                            | 1300-1980              |
| De seleção                             | 500-2570               |
| RECORTE                             | 500-2550               |
| DrawIndexedPrimitive                 | 1200-1400              |
| ADDRESSV                             | 1090-1500              |
| Endereço de                             | 1070-1500              |
| DrawPrimitive                        | 1050-1150              |
| SRGBTEXTURE                          | 150-1500               |
| STENCILMASK                          | 570-700                |
| STENCILZFAIL                         | 500-800                |
| STENCILREF                           | 550-700                |
| ALPHABLENDENABLE                     | 550-700                |
| STENCILFUNC                          | 560-680                |
| STENCILWRITEMASK                     | 520-700                |
| STENCILFAIL                          | 500-750                |
| ZFUNC                                | 510-700                |
| ZWRITEENABLE                         | 520-680                |
| STENCILENABLE                        | 540-650                |
| STENCILPASS                          | 560-630                |
| SRCBLEND                             | 500-685                |
| \_Estêncil dois lados \_              | 450-590                |
| ALPHATESTENABLE                      | 470-525                |
| ALPHAREF                             | 460-530                |
| ALPHAFUNC                            | 450-540                |
| DESTBLEND                            | 475-510                |
| COLORWRITEENABLE                     | 465-515                |
| \_STENCILFAIL CCW                     | 340-560                |
| \_STENCILPASS CCW                     | 340-545                |
| \_STENCILZFAIL CCW                    | 330-495                |
| SCISSORTESTENABLE                    | 375-440                |
| \_STENCILFUNC CCW                     | 250-480                |
| SetScissorRect                       | 150-340                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> </dl>

 

 
