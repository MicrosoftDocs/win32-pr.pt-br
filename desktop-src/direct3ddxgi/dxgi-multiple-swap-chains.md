---
description: Para melhorar o desempenho, talvez você queira criar mais de uma cadeia de permuta por dispositivo de renderização Direct3D.
ms.assetid: 29AB9799-9E4E-4A96-B4AB-F1B754794879
title: Melhorando o desempenho com várias cadeias de permuta por dispositivo de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91445660bf9efc59e9e39c88819587dce3960325df0659487eaae67a845a7329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627477"
---
# <a name="improving-performance-with-multiple-swap-chains-per-rendering-device"></a>Melhorando o desempenho com várias cadeias de permuta por dispositivo de renderização

Para melhorar o desempenho, talvez você queira criar mais de uma cadeia de permuta por dispositivo de renderização Direct3D. Use essa abordagem para salvar a memória necessária criando dispositivos adicionais ou para reduzir a quantidade de tempo de renderização a renderizar para cadeias de permuta individuais por dispositivo separadamente ou para economizar memória e reduzir o tempo de renderização.

-   [Cenários de aplicativo com várias cadeias de permuta por dispositivo](#app-scenarios-with-multiple-swap-chains-per-device)
-   [Gerenciando várias cadeias de permuta por dispositivo](#managing-multiple-swap-chains-per-device)
    -   [Definindo a latência máxima do quadro](#setting-maximum-frame-latency)
    -   [Usando o modelo de invasão com várias cadeias de permuta por dispositivo](#using-flip-model-with-multiple-swap-chains-per-device)
-   [Tópicos relacionados](#related-topics)

## <a name="app-scenarios-with-multiple-swap-chains-per-device"></a>Cenários de aplicativo com várias cadeias de permuta por dispositivo

Considere o uso de várias cadeias quando a cena do aplicativo consistir em objetos de exibição separados que são renderizados e atualizados independentemente. Por exemplo, o aplicativo tem animação em constante alteração, como vídeo em um lado e texto rolável em outro lado. Para economizar memória que normalmente precisaria criar um dispositivo extra e facilitar o compartilhamento de conteúdo entre as duas cadeias de permuta, você pode criar ambas as cadeias de permuta vinculadas ao mesmo dispositivo de renderização Direct3D. Use uma cadeia de permuta para animação e uma cadeia de permuta para texto. Um exemplo comum desse cenário é um aplicativo Direct3D que também usa a API [DirectComposition.](../directcomp/directcomposition-portal.md)

Outro cenário é quando você deseja economizar tempo de renderização definindo vários destinos de renderização em várias cadeias de troca simultaneamente. Por exemplo, suponha que você queira renderizar uma cena complexa com muitas texturas e geometrias, como carros de corrida em uma faixa, e deseja que a janela do aplicativo mostre exibições dos espelhos laterais e traseiras em duas janelas de exibição que são renderizadas por duas cadeias de troca. Se você definir as várias cadeias de permuta como destinos de renderização, seu aplicativo não precisará repetir os tempos de renderização em cada cadeia de permuta separadamente.

## <a name="managing-multiple-swap-chains-per-device"></a>Gerenciando várias cadeias de permuta por dispositivo

Use as diretrizes nesta seção para gerenciar várias cadeias de permuta que você cria para um único dispositivo de renderização Direct3D.

### <a name="setting-maximum-frame-latency"></a>Definindo a latência máxima do quadro

Use o [**método IDXGIDevice1::SetMaximumFrameLatency**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) para definir o número máximo de operações atuais que o sistema operacional pode colocar na fila para renderização na exibição. Esse número máximo é por dispositivo de renderização Direct3D em vez de por cadeia de permuta. Portanto, para garantir que o sistema operacional exerce as operações atuais no intervalo vsync pretendido, recomendamos que você não desem conjunto máximo de latência de quadro como 1 quando você cria várias cadeias de troca de modelo de in flip ou bitblt por dispositivo e quando mais de uma dessas cadeias de permuta será renderização para cada quadro. Como regra geral, se você enviar somente duas operações atuais por quadro entre todas as cadeias de permuta do mesmo dispositivo, poderá definir a latência máxima do quadro como 2. Se você não puder enviar e contar de forma confiável [](dxgi-flip-model.md) as operações atuais por quadro, poderá usar as estatísticas presentes para acompanhar quando o sistema operacional exibir as operações presentes.

### <a name="using-flip-model-with-multiple-swap-chains-per-device"></a>Usando o modelo de invasão com várias cadeias de permuta por dispositivo

Use essas diretrizes ao usar o modelo de in flip [DXGI](dxgi-flip-model.md) com várias cadeias de permuta que você cria para um único dispositivo de renderização Direct3D.

### <a name="targeting-specific-vsync-intervals-with-each-swap-chains-present-operations"></a>Direcionando intervalos vsync específicos com as operações atuais de cada cadeia de permuta

Quando você cria duas ou mais cadeias de permuta de modelo invertida por dispositivo, preste atenção às diferenças de exibição ao gerenciar a sequência de estado do dispositivo e a sequência de chamadas para o [**método IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) de todas as cadeias de permuta. Para garantir que o sistema operacional ex exibe a operação atual de cada cadeia de permuta no intervalo vsync pretendido, recomendamos garantir que o número de operações presentes na fila seja sempre pelo menos um a menos do que o número de buffers de retorno para a cadeia de permuta com o menor número de buffers de fundo.

### <a name="flip-model-swap-chains-with-two-buffers"></a>Inverter cadeias de permuta de modelo com dois buffers

Seu aplicativo pode direcionar intervalos vsync específicos quando seu número de operações presentes na fila for menor ou igual ao número de buffers de fundo – 1. Além disso, você deve usar ou renderizar cada cadeia de permuta separadamente e, em seguida, encerrar o uso de cada cadeia de permuta com uma operação atual. Portanto, quando você envia todas as operações atuais para uma cadeia de permuta de dois buffers flip-model, você atinge o limite para o número de buffers de fundo em que você deve prestar atenção especial se quiser que seu aplicativo seja direcionado a intervalos vsync específicos.

No caso de cadeias de permuta de dois buffers, para direcionar intervalos vsync específicos, você deve garantir que o sistema operacional termine a exibição da operação atual de cada cadeia de permuta antes de renderizar para o próximo buffer. Recomendamos que você termine de definir a exibição de destino de renderização e outro estado de renderização, renderizar em seguida e, em seguida, chame [**IDXGISwapChain1::P resent1 para**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) cada um dos dois buffers de uma cadeia de permuta antes de fazer o mesmo para outra cadeia de permuta. Ao trabalhar com duas ou mais cadeias de permuta, você precisa redefinir o destino de renderização e o estado de renderização no dispositivo para cada cadeia de permuta. O benefício dessa abordagem é evitar o caso em que uma ou mais das operações atuais da cadeia de permuta perdem o intervalo vsync pretendido. Para o primeiro exemplo, aplicativo com animação e texto de alteração, conforme descrito em Cenários de aplicativo com várias cadeias de permuta por dispositivo, direcionando [intervalos](#app-scenarios-with-multiple-swap-chains-per-device)presentes específicos, você tem a garantia de que, quando a animação é atualizada em uma janela de exibição, o texto correspondente renderizado por uma cadeia de permuta separada também é exibido ao mesmo tempo em outra janela de exibição. Se seu aplicativo precisar direcionar intervalos vsync específicos, você deverá seguir essas diretrizes.

Este diagrama mostra um exemplo do fluxo de código de renderização de cadeia de permuta e apresentação em um aplicativo com duas cadeias de permuta de modelo in flip cada uma com dois buffers. Nesse caso, você precisa direcionar um intervalo presente específico para cada operação atual.

![ilustração do modelo de in flip com dois buffers](images/flip-mode-2-buffers.png)

### <a name="reducing-rendering-time-by-simultaneously-setting-multiple-swap-chains-as-render-targets"></a>Reduzindo o tempo de renderização definindo simultaneamente várias cadeias de permuta como destinos de renderização

Para o segundo exemplo, carros de corrida em uma faixa, conforme descrito em Cenários de aplicativo com várias [cadeias](#app-scenarios-with-multiple-swap-chains-per-device)de permuta por dispositivo , talvez você queira trocar o direcionamento específico de intervalos vsync específicos com a economia de tempo de renderização que você ganha definindo vários destinos de renderização em todas as cadeias de permuta simultaneamente. Nesse caso, de definir vários destinos de renderização simultaneamente, renderizar a cena em cada cadeia de permuta e, em seguida, chamar [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) em cada cadeia de permuta usada na cena. O benefício dessa abordagem é reduzir o tempo de renderização. A limitação dessa abordagem é que as operações atuais da cadeia de permuta simultânea não podem ter como destino o mesmo vsync quando você usa cadeias de permuta de dois buffers. Por exemplo, o sistema operacional não exibirá o conteúdo dos espelhos do modo de exibição lateral do carro de corrida até 1 vsync depois que o mesmo conteúdo for visto no espelho do retrovisor do carro de corrida.

Este diagrama mostra um exemplo do fluxo de código de renderização de cadeia de permuta e apresentação em um aplicativo com duas cadeias de permuta de modelo in flip cada uma com dois buffers de comprimento. Neste tipo de exemplo, você economiza tempo de renderização para trocar as cadeias 1 e 2 para os buffers A e C. Mas você não pode sincronizar os intervalos vsync nos quais as operações atuais dos buffers A e C são exibidas. Esse padrão se repete para o quadro 2.

![ilustração da configuração simultânea de várias cadeias de permuta como destinos de renderização](images/multi-swap-chains-as-render-targets.png)

Para evitar a falta do intervalo vsync pretendido devido a muitas operações presentes na fila, você pode aumentar o número de buffers de fundo em cada cadeia de permuta. Mas essa técnica usa mais memória de vídeo. Para evitar intervalos vsync de destino ausentes, recomendamos que você sempre mantenha o número de operações presentes na fila menor que o número de buffers de fundo na cadeia de permuta com o menor número de buffers back. Ao definir duas cadeias de permuta como vários destinos de renderização, como você enfilfilou duas operações presentes simultaneamente em ambas as cadeias de permuta, recomendamos que você crie cadeias de permuta com pelo menos três buffers de comprimento.

O diagrama a seguir mostra um exemplo do fluxo de código de renderização de cadeia de permuta e apresentação em um aplicativo com duas cadeias de permuta de modelo in flip cada uma com três buffers de comprimento. Aqui, como o número de presentes na fila para qualquer quadro específico é 2, que é menor que o número de buffers de fundo por cadeia de permuta, seu aplicativo pode definir vários destinos de renderização e ainda direcionar os mesmos intervalos vsync para os buffers A e D no quadro 2 e para os buffers em quadros subsequentes.

![ilustração da configuração simultânea de várias cadeias de permuta como destinos de renderização destinados ao mesmo vsync](images/multi-swap-chains-as-render-targets-same-vsync.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aprimorando a apresentação com o modelo de invasões, retângulos sujos e áreas roladas](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
