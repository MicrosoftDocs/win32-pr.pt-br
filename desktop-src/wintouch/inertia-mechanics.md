---
title: Mecânica inércia
description: Mecânica inércia
ms.assetid: 188b6936-b36e-4e57-9118-8b61ed134c17
keywords:
- Windows Touch, inércia
- Windows Touch, animação suave
- Toque do Windows, margem elástica
- inércia, mecânica
- inércia, conceitos básicos de cálculo
- inércia, visão geral da física
- inércia, animação suave
- inércia, margem elástica
- animação suave
- margem elástica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79b27900c6921c972710e7e922ab42b834afc1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291930"
---
# <a name="inertia-mechanics"></a>Mecânica inércia

O inércia é usado para executar cálculos para animar a movimentação de objetos e habilitar o suporte para uso genérico em aplicativos que incorporam o Windows Touch. Esta seção ilustra os recursos a seguir que são habilitados pelo inércia.

-   Uma breve visão geral da física inércia.
-   Animação suave de objetos usando as propriedades de velocidade e desaceleração.
-   Animação suave de objetos usando uma propriedade de deslocamento.
-   Saltando das bordas da tela usando limites elásticos.

## <a name="inertia-physics-overview"></a>Visão geral da física do inércia

O processador inércia usa um modelo de física simples que incorpora uma posição, um valor de desaceleração e uma velocidade inicial. O tempo é usado como a entrada dinâmica para o modelo para determinar a posição atual de um objeto que está sendo inserido. O grafo e a fórmula a seguir descrevem o modelo de física usado para calcular posições de objeto.

![ilustração mostrando o grafo e a fórmula usados para calcular posições de objeto](images/velocity.png)

Na fórmula usada para calcular a posição atual (x), a velocidade inicial (v) é multiplicada pelo tempo decorrido (t) e é reduzida pelo tempo do fator de desaceleração (d) vezes ao quadrado. Isso resulta na desaceleração de objeto suave. Na ilustração anterior na parte inicial (mais à esquerda) da curva, o objeto está se movendo rapidamente porque sua velocidade atual é a velocidade inicial. Na parte final (mais à direita) da curva, o objeto foi interrompido completamente porque sua velocidade é 0. Cálculos de velocidade de objeto para a velocidade x, velocidade y e velocidade rotacional usam esta fórmula para cálculos.

Toda a distância usada para o processador inércia é relativa. Se você quiser usar as coordenadas da tela, passe as coordenadas da tela para o processador de manipulação (ou inércia); Se você quiser usar coordenadas absolutas, passe-as para o processador que você está usando. Independentemente dos valores que você está usando, o processador de manipulação usará tiques de relógio de milissegundos para processar o tempo. Esses valores podem ser passados diretamente para o processador inércia usando o método [**processtime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) ou usando o carimbo de data/hora padrão por meio de chamadas para [**processar**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process).

## <a name="smooth-object-animation-using-the-velocity-and-deceleration-properties"></a>Animação Smooth Object usando as propriedades Velocity e de desaceleração

Você pode habilitar a animação suave interagindo diretamente com o modelo de física definindo os valores de velocidade e de desaceleração na interface do processador inércia e, em seguida, chamando o [**processo**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process). O **processo** de chamada acionará as manipulações de objeto que, por sua vez, devem causar atualizações da interface do usuário Os valores de velocidade de objeto passados para o processador inércia normalmente são obtidos do processador de manipulação após a conclusão. Seu valor de desaceleração dependerá de quanto tempo você deseja que o objeto seja animado e as unidades que você está usando para seus cálculos. Como os valores são dependentes, às vezes você deve dimensionar a velocidade de entrada do processador maniplation e usar valores arbitrários para desaceleração. Os valores a seguir são típicos para vários cenários em que você está passando valores de centipixel das propriedades x e y da estrutura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) para o processador de manipulação.



| Cenário    | Set da propriedade                                                                       | Valor de desaceleração | Dimensionamento típico de entrada de velocidade                                  | Observações                                                                                 |
|-------------|------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| Tradução | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,003 f             | Nenhum.                                                           | O uso desse valor resultará em animações de distância mais longas ao usar a entrada por toque.    |
| Tradução | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,001 f             | 1/20 velocidade inicial para entradas de toque, nenhuma para entradas do mouse | O uso desse valor será animado por um segundo, dadas as entradas típicas de velocidade.      |
| Tradução | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,5 f               | Nenhum                                                            | Usar esse valor dá uma ideia natural à animação em grandes monitores do Windows Touch.   |
| Rotação    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000015 f          | Radianos convertidos em graus.                                   | O uso desse valor resulta em animações de rotação mais longas ao usar a entrada por toque.      |
| Rotação    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.00001 f           | 1/40th rotação Delta para entradas de toque, nenhum para entradas do mouse   | Esse valor está em radianos, portanto, você deve usar valores de desaceleração e velocidade muito pequenos. |
| Rotação    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000005 f          | Nenhum                                                            | Esse valor tem uma noção natural sobre grandes exibições do Windows Touch.                        |



 

## <a name="smooth-object-animation-using-the-desired-displacement-property"></a>Animação Smooth Object usando a propriedade de substituição desejada

Em alguns casos, você não deseja usar a entrada do usuário para o deslocamento de objeto, mas ainda deseja que um objeto anime suavemente na tela. Nesse caso, você pode usar as propriedades de deslocamento no processador inércia para que o processador Calcule a velocidade inicial para mover um objeto pela tela.

## <a name="controlling-object-position-using-elastic-bounds"></a>Controlando a posição do objeto usando limites elásticos

Depois que você tiver um objeto que está sendo movido na tela, normalmente desejará que ele seja interrompido antes de sair do ponto de vista do usuário. O processador inércia habilita essa funcionalidade por meio das propriedades limite e margem elástica. A imagem a seguir ilustra as várias propriedades de limite e margem em um aplicativo típico.

![captura de tela mostrando Propriedades de limite e margem elástica](images/elastic-illustrated.png)

Você define os limites esquerdo, superior, direito e inferior e as margens elásticas para seu aplicativo, e o processador inércia manipulará a manutenção dos elementos da interface do usuário dentro dos limites. Quando um objeto atinge uma margem elástica, ele ficará lento até atingir o limite. Ela nunca deixará essa margem novamente durante inércia, mas ainda será movida até que o componente perpendicular do objeto inércia seja desacelerado como 0. Na ilustração, um círculo é inserido em direção ao limite elástico esquerdo. A seta sólida mostra a direção da manipulação; o círculo sólido é a posição inicial do objeto; a seta sólida é as alterações feitas antes que o círculo atinja a margem elástica; a seta tracejada mostra onde o processador inércia manipula o círculo depois de atingir a margem; e os círculos tracejados mostram onde o objeto é interrompido.

> [!Note]  
> Definir as propriedades da margem moverá os limites para fora. Por exemplo, se o limite superior for definido como 50 e você definir a margem elástica superior como 10, seu limite superior será efetivamente 40.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulando inércia em código não gerenciado](handling-inertia-in-unmanaged-code.md)
</dt> <dt>

[Inércia](getting-started-with-inertia.md)
</dt> <dt>

[Manipulações](getting-started-with-manipulations.md)
</dt> </dl>

 

 




