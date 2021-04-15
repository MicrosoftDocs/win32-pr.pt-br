---
description: Para melhorar o desempenho, talvez você queira criar mais de uma cadeia de permuta por dispositivo de renderização Direct3D.
ms.assetid: 29AB9799-9E4E-4A96-B4AB-F1B754794879
title: Melhorando o desempenho com várias cadeias de troca por dispositivo de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e356434521054bc13b553c8ae3d6e43d8d98ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456684"
---
# <a name="improving-performance-with-multiple-swap-chains-per-rendering-device"></a>Melhorando o desempenho com várias cadeias de troca por dispositivo de renderização

Para melhorar o desempenho, talvez você queira criar mais de uma cadeia de permuta por dispositivo de renderização Direct3D. Use essa abordagem para economizar memória exigida pela criação de dispositivos adicionais ou para reduzir a quantidade de tempo de renderização a ser renderizada em cadeias de troca individuais por dispositivo separadamente ou para economizar memória e reduzir o tempo de renderização.

-   [Cenários de aplicativo com várias cadeias de troca por dispositivo](#app-scenarios-with-multiple-swap-chains-per-device)
-   [Gerenciando várias cadeias de troca por dispositivo](#managing-multiple-swap-chains-per-device)
    -   [Definindo a latência máxima do quadro](#setting-maximum-frame-latency)
    -   [Usando o flip Model com várias cadeias de troca por dispositivo](#using-flip-model-with-multiple-swap-chains-per-device)
-   [Tópicos relacionados](#related-topics)

## <a name="app-scenarios-with-multiple-swap-chains-per-device"></a>Cenários de aplicativo com várias cadeias de troca por dispositivo

Considere o uso de várias cadeias quando a cena do aplicativo consistir em objetos de exibição separados que são renderizados e atualizados de forma independente. Por exemplo, o aplicativo muda constantemente a animação, como vídeo em um lado e texto rolável em outro lado. Para economizar memória que normalmente você precisaria para criar um dispositivo extra e facilitar o compartilhamento de conteúdo entre as duas cadeias de permuta, você pode criar ambas as cadeias de troca ligadas ao mesmo dispositivo de renderização de Direct3D. Use uma cadeia de permuta para animação e uma cadeia de permuta para texto. Um exemplo comum desse cenário é um aplicativo do Direct3D que também usa a API [DirectComposition](../directcomp/directcomposition-portal.md) .

Outro cenário é quando você deseja economizar tempo de renderização definindo vários destinos de renderização em várias cadeias de troca simultaneamente. Por exemplo, suponha que você deseja renderizar uma cena complexa com muitas texturas e geometria, como carros de corrida em uma faixa, e você deseja que a janela do aplicativo mostre exibições dos espelhos traseiro e lateral em duas janelas de exibição que são renderizadas por duas cadeias de permuta. Se você definir as várias cadeias de troca como destinos de renderização, seu aplicativo não precisará repetir os tempos de renderização em cada cadeia de troca separadamente.

## <a name="managing-multiple-swap-chains-per-device"></a>Gerenciando várias cadeias de troca por dispositivo

Use as diretrizes nesta seção para gerenciar várias cadeias de troca que você cria para um único dispositivo de renderização Direct3D.

### <a name="setting-maximum-frame-latency"></a>Definindo a latência máxima do quadro

Use o método [**IDXGIDevice1:: SetMaximumFrameLatency**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) para definir o número máximo de operações presentes que o sistema operacional pode enfileirar para renderizar para a exibição. Esse número máximo é por dispositivo de renderização de Direct3D em vez de por cadeia de troca. Portanto, para garantir que o sistema operacional exiba as operações atuais no intervalo vsync pretendido, recomendamos que você não defina a latência máxima de quadros como 1 ao criar várias cadeias de permuta de modelo de flip ou BitBlt por dispositivo e quando mais de uma dessas cadeias de permuta for renderizada para cada quadro. Como regra geral, se você enviar com confiança apenas duas operações presentes por quadro entre todas as cadeias de troca do mesmo dispositivo, poderá definir a latência máxima do quadro como 2. Se não for possível enviar e contar com confiança as operações atuais por quadro, você poderá usar as [estatísticas atuais](dxgi-flip-model.md) para controlar quando o sistema operacional exibe operações presentes.

### <a name="using-flip-model-with-multiple-swap-chains-per-device"></a>Usando o flip Model com várias cadeias de troca por dispositivo

Use essas diretrizes quando usar o [modelo de flip dxgi](dxgi-flip-model.md) com várias cadeias de troca que você cria para um único dispositivo de renderização Direct3D.

### <a name="targeting-specific-vsync-intervals-with-each-swap-chains-present-operations"></a>Direcionando intervalos de vsync específicos com as operações presentes de cada cadeia de permuta

Quando você cria duas ou mais cadeias de permuta de modelo de flip por dispositivo, preste atenção às diferenças de exibição ao gerenciar a sequência do estado do dispositivo e a sequência de chamadas para o método [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) de todas as cadeias de permuta. Para garantir que o sistema operacional exiba a operação presente de cada cadeia de permuta no intervalo vsync pretendido, recomendamos que você garanta que o número de operações presentes na fila seja sempre pelo menos um menor que o número de buffers de fundo para a cadeia de permuta com o menor número de buffers de fundo.

### <a name="flip-model-swap-chains-with-two-buffers"></a>Inverter cadeias de troca de modelo com dois buffers

Seu aplicativo pode direcionar intervalos vsync específicos quando o número de operações presentes na fila for menor ou igual ao número de buffers de fundo – 1. Além disso, você deve usar ou renderizar para cada cadeia de permuta separadamente e, em seguida, encerrar o uso de cada cadeia de permuta com uma operação atual. Assim, quando você enviar cada operação presente para uma cadeia de permuta de modelo invertida de 2 buffers, atingirá o limite para o número de buffers de fundo em que você deve prestar atenção especial se quiser que seu aplicativo direcione intervalos vsync específicos.

No caso de duas cadeias de troca de buffer, para direcionar intervalos vsync específicos, você deve garantir que o sistema operacional conclua a exibição de cada operação presente da cadeia de permuta antes de renderizar para o próximo buffer. É recomendável que você conclua a configuração da exibição de destino de renderização e outro Estado de renderização, próximo processamento e, em seguida, chame [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para cada um dos dois buffers de uma cadeia de permuta antes de fazer o mesmo para outra cadeia de permuta. Quando você trabalha com duas ou mais cadeias de permuta, precisa redefinir o destino de renderização e o estado de renderização no dispositivo para cada cadeia de permuta. A vantagem dessa abordagem é evitar o caso em que uma ou mais das operações presentes da cadeia de permuta perdem seu intervalo de vsync pretendido. Para o primeiro exemplo, aplicativo com a alteração de animação e texto, conforme descrito em [cenários de aplicativo com várias cadeias de troca por dispositivo](#app-scenarios-with-multiple-swap-chains-per-device), direcionando intervalos presentes específicos, você tem a garantia de que quando a animação for atualizada em uma janela de exibição, o texto correspondente que é processado por uma cadeia de permuta separada também será exibido ao mesmo tempo em outra janela de exibição. Se seu aplicativo precisar direcionar intervalos vsync específicos, você deverá seguir estas diretrizes.

Este diagrama mostra um exemplo do fluxo de código da renderização e da apresentação da cadeia de permuta em um aplicativo com dois cadeias de permuta do flip-Model cada um com dois buffers. Nesse caso, você precisa direcionar um intervalo atual específico para cada operação presente.

![ilustração de flip Model com dois buffers](images/flip-mode-2-buffers.png)

### <a name="reducing-rendering-time-by-simultaneously-setting-multiple-swap-chains-as-render-targets"></a>Reduzindo o tempo de renderização Configurando simultaneamente várias cadeias de troca como destinos de renderização

Para o segundo exemplo, carros de corrida em uma faixa, conforme descrito em [cenários de aplicativos com várias cadeias de troca por dispositivo](#app-scenarios-with-multiple-swap-chains-per-device), talvez você queira compensar o direcionamento de intervalos de vsync atuais específicos com a economia de tempo de renderização Configurando vários destinos de renderização em todas as cadeias de troca simultaneamente. Nesse caso, defina vários destinos de renderização simultaneamente, processe a cena em cada cadeia de permuta e, em seguida, chame [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) em cada cadeia de permuta usada na cena. O benefício dessa abordagem é reduzir o tempo de renderização. A limitação dessa abordagem é que suas operações de cadeia de permuta simultâneas não podem ter como destino o mesmo vsync quando você usa cadeias de troca de 2 buffers. Por exemplo, o sistema operacional não exibirá o conteúdo dos espelhos da exibição lateral do carro de corrida até 1 vsync após o mesmo conteúdo ser visto do espelho da exibição traseira do carro de corrida.

Este diagrama mostra um exemplo do fluxo de código de renderização e apresentação da cadeia de permuta em um aplicativo com dois cadeias de permuta de modelo invertido cada um com dois buffers de comprimento. Neste tipo de exemplo, você economiza tempos de renderização para trocar cadeias 1 e 2 para buffers A e C. Mas não é possível sincronizar os intervalos vsync nos quais as operações presentes para os buffers A e C são exibidas. Esses padrões se repete para o quadro 2.

![ilustração de configurar simultaneamente várias cadeias de troca como destinos de renderização](images/multi-swap-chains-as-render-targets.png)

Para evitar a falta do intervalo vsync pretendido devido a muitas operações presentes na fila, você pode aumentar o número de buffers de fundo em cada cadeia de permuta. Mas essa técnica usa mais memória de vídeo. Para evitar intervalos de vsync de destino ausentes, é recomendável manter sempre o número de operações presentes em fila menor que o número de buffers de fundo na cadeia de permuta com o menor número de buffers de fundo. Quando você define duas cadeias de troca como vários destinos de renderização, como você enfileira duas operações presentes simultaneamente em ambas as cadeias de troca, recomendamos que você crie cadeias de troca com pelo menos três buffers de comprimento.

O próximo diagrama mostra um exemplo do fluxo de código da renderização e da apresentação da cadeia de permuta em um aplicativo com dois cadeias de permuta do flip-Model cada um com três buffers de comprimento. Aqui, como o número de presentes na fila para qualquer quadro específico é 2, que é menor que o número de buffers de fundo por cadeia de troca, seu aplicativo pode definir vários destinos de renderização e ainda direcionar os mesmos intervalos de vsync para buffers A e D no quadro 2 e para os buffers em quadros subsequentes.

![ilustração de configurar simultaneamente várias cadeias de troca como destinos de renderização voltados o mesmo vsync](images/multi-swap-chains-as-render-targets-same-vsync.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimorando a apresentação com o modelo de flip, retângulos sujos e áreas roladas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
