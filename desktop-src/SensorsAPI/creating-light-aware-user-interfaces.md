---
description: Esta seção aborda o uso de dados do sensor de luz ambiente e como os recursos da interface do usuário e o conteúdo do programa podem ser otimizados para muitas condições de iluminação.
ms.assetid: c84075b2-ae41-4915-a0f6-3a9c017ae0b8
title: Criando Light-Aware interfaces de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd97bb304c3a8718ae4b32d8b9100a1e7eb7a18240b9089c112272f588ee209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890271"
---
# <a name="creating-light-aware-user-interfaces"></a>Criando Light-Aware interfaces de usuário

Esta seção aborda o uso de dados do sensor de luz ambiente e como os recursos da interface do usuário e o conteúdo do programa podem ser otimizados para muitas condições de iluminação.

Sensores de luz ambiente expõem dados que podem ser usados para determinar vários aspectos das condições de iluminação em que o sensor está localizado. Os sensores de luz ambiente podem expor o brilho geral de um ambiente (illuminance) e outros aspectos da luz ao redor, como a luminosidade ou a temperatura de cor.

Os computadores podem ser mais úteis de várias maneiras quando o sistema está respondendo às condições de iluminação. isso inclui controlar o brilho da tela do computador (um novo recurso com suporte total no Windows 7), ajustar automaticamente o nível de iluminação de teclados acesos e até mesmo o controle de brilho para outras luzes (como iluminação de botão, luzes de atividade e assim por diante).

Os programas do usuário final também podem se beneficiar de sensores leves. Os programas podem aplicar um tema apropriado para uma condição de iluminação específica, como um tema externo específico e um tema interno. Talvez o aspecto mais importante da integração do sensor leve com os programas seja a legibilidade e as otimizações legíveis baseadas em condições de iluminação.

A API do sensor permite que você crie esses programas. Considere este cenário.

## <a name="scenario-using-your-laptop-to-navigate-to-a-restaurant"></a>Cenário: usando seu laptop para navegar até um restaurante

Suponha que você deseja usar seu computador para ajudá-lo a navegar para um novo restaurante. Você começa em sua casa, pesquisando o endereço do restaurante e planejando sua rota. A captura de tela a seguir mostra como o programa de navegação pode otimizar sua interface do usuário para mostrar informações detalhadas em condições de iluminação interna.

![interface do usuário projetada para iluminação em inglês.](images/nav-normal.png)

Quando você vai para o carro, encontra a luz solar direta, o que torna a tela do laptop difícil de ler. A captura de tela a seguir mostra como o seu programa pode alterar sua interface do usuário para maximizar a legibilidade/legibilidade na luz direta. Nessa exibição, muitos dos detalhes foram omitidos e o contraste é maximizado.

![interface do usuário projetada para condições de iluminação direta.](images/nav-contrast.png)

À medida que você se aproximar do restaurante, as abordagens da noite e ficam escuras para fora. Na captura de tela a seguir, a interface do usuário do programa de navegação foi otimizada para exibição de baixa luz. Usando cores mais escuras no geral, essa interface do usuário é fácil de resumir no carro escuro.

![interface do usuário projetada para exibição de baixa luz.](images/nav-lowlight.png)

No restante desta seção, você irá explorar algumas coisas que pode fazer para otimizar seus programas para várias condições de iluminação e como você pode usar a API do sensor para ajudar a habilitar a interface do usuário com reconhecimento claro.

## <a name="in-this-section"></a>Nesta seção

-   [Conceitos básicos de Light-Aware interfaces de usuário](fundamentals-of-light-aware-user-interfaces.md)
-   [Exemplos de interfaces de usuário do Light-Aware](examples-of-light-aware-user-interfaces.md)
-   [Otimizando a experiência do usuário](optimizing-the-user-experience.md)
-   [Compreendendo e interpretando valores de Lux](understanding-and-interpreting-lux-values.md)
-   [Usando dados de sensor claro](handling-data-from-multiple-light-sensors.md)

 

 



