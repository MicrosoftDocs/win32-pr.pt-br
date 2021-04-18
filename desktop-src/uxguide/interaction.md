---
title: Interação
description: A interação é a variedade de maneiras como os usuários interagem com seu aplicativo, incluindo toque, teclado, mouse e assim por diante. Use essas diretrizes para criar experiências intuitivas e informativas que são otimizadas para toque, mas funcionam consistentemente entre dispositivos de entrada.
ms.assetid: 1509c885-f4dc-4cf9-86a3-cc6754d3b4a0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: fbbbed55bbee1b1b0a028bada4e9d97682d9c293
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105770548"
---
# <a name="interaction"></a>Interação

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

A interação é a variedade de maneiras como os usuários interagem com seu aplicativo, incluindo toque, teclado, mouse e assim por diante. Use essas diretrizes para criar experiências intuitivas e informativas que são otimizadas para toque, mas funcionam consistentemente entre dispositivos de entrada.

## <a name="design-for-a-touch-first-experience"></a>Design para uma experiência de toque inicial

Primeiro e mais importante, projete o seu aplicativo com a expectativa de que o toque será o método de entrada principal dos usuários. Se você usar os controles de plataforma, o suporte para Touchpad, mouse e caneta/caneta não precisará de programação adicional, pois o Windows fornece isso gratuitamente.

Tenha em mente, porém, que uma interface do usuário otimizada para toque nem sempre é superior a uma interface do usuário tradicional. Ambos fornecem vantagens e desvantagens exclusivas para a tecnologia e o aplicativo. Na mudança para uma interface do usuário do touch-First, é importante entender as principais diferenças entre o toque (incluindo Touchpad), caneta/caneta, mouse e entrada de teclado. Não considere as propriedades e os comportamentos do dispositivo de entrada conhecidos para que sejam concedidos, pois o toque no Windows 8 faz mais do que simplesmente emular essa funcionalidade.

Como você descobrirá em breve, a entrada por toque requer uma abordagem diferente para o design da interface do usuário.

**Compare os requisitos de interação por toque**

Esta tabela mostra algumas das diferenças entre os dispositivos de entrada que você deve considerar ao projetar aplicativos da Windows Store com otimização de toque.



|                                 |                                                                                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                 |                                                     |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| **Fator**<br/>           | **Interações por toque**<br/>                                                                                                                                                                                | **Interações de mouse, teclado e caneta/stylus**<br/>                                                                                                                                                                                                                                                         | **Touchpad**<br/>                             |
| **Precisão**<br/>        | A área de contato da ponta do dedo é maior do que uma coordenada x-y única, o que aumenta a probabilidade de ativações de comando acidentais.<br/>                                                               | O mouse e a caneta/stylus fornecem uma coordenada x-y precisa.<br/>                                                                                                                                                                                                                                            | Igual ao mouse.<br/>                           |
|                                 | O formato da área de contato altera ao longo do movimento. <br/>                                                                                                                                       | Os movimentos do mouse e traços da caneta/stylus fornecem uma coordenada x-y precisa. O foco do teclado é explícito.<br/>                                                                                                                                                                                                   | Igual ao mouse.<br/>                           |
|                                 | Não há cursor do mouse para ajudar no direcionamento.<br/>                                                                                                                                                    | O cursor do mouse, o cursor da caneta/stylus e o foco do teclado, todos ajudarão no direcionamento.<br/>                                                                                                                                                                                                                   | Igual ao mouse.<br/>                           |
| **Anatomia humana**<br/>    | Movimentos com as pontas dos dedos são imprecisos porque dificultam um movimento em linha reta usando um ou mais dedos. Isso se deve à curvatura das articulações das mãos e ao número de articulações envolvidas no movimento.<br/> | É fácil realizar um movimento em linha reta com o mouse ou caneta/stylus porque a mão que os controla percorre uma distância física menor do que o cursor na tela.<br/>                                                                                                                    | Igual ao mouse.<br/>                           |
|                                 | Algumas áreas na superfície de toque de um dispositivo de vídeo podem ser inacessíveis devido à postura do dedo e à posição do punho do usuário sobre o dispositivo.<br/>                                                                | O mouse e a caneta podem atingir qualquer parte da tela, embora qualquer controle deva ser acessado pelo teclado por meio da ordem de tabulação. <br/>                                                                                                                                                                 | A postura do dedo e a alça podem ser um problema.<br/> |
|                                 | Os objetos podem ser obscurecidos por uma ou mais pontas de dedos ou pela mão do usuário. Isso é conhecido como oclusão.<br/>                                                                                                   | Os dispositivos de entrada indireta não causam oclusão.<br/>                                                                                                                                                                                                                                                       | Igual ao mouse.<br/>                           |
| **Estado de objeto**<br/>     | O toque usa um modelo de dois Estados: a superfície de toque de um dispositivo de vídeo é alterada (ativado) ou não (desativado). Não há estado de foco que possa disparar feedback visual adicional.<br/>                         | Um mouse, caneta/stylus e teclado, todos expõem um modelo de três estados: acima (off), abaixo (on) (ativado), e focalizar (foco).<br/> A focalização permite que os usuários explorem e aprendam usando as dicas de ferramentas associadas aos elementos da interface do usuário. Os efeitos de focalização e de foco podem retransmitir os objetos que são interativos e também ajudar no direcionamento. <br/> | Igual ao mouse.<br/>                           |
| **Interação sofisticada**<br/> | Suporta multitoque, pontos de entrada múltiplos (pontas dos dedos) em uma superfície de toque.<br/>                                                                                                                          | Suporta um ponto de entrada único.<br/>                                                                                                                                                                                                                                                                       | Igual ao toque.<br/>                           |
|                                 | Suporta a manipulação direta de objetos através de gestos como tocar, arrastar, deslizar, apertar e girar.<br/>                                                                                  | Sem suporte para manipulação direta quando o mouse, caneta e teclado são dispositivos de entrada indiretos.<br/>                                                                                                                                                                                                    | Igual ao mouse.<br/>                           |



 

**Observação**

A entrada indireta conta com os benefícios de mais de 25 anos de refinamento. Recursos como dicas de ferramentas disparadas por focalização foram projetadas para solucionar a exploração da interface do usuário especificamente para entradas por touchpad, mouse, caneta e teclado. Elementos da interface do usuário como esses foram reprojetados para uma experiência avançada fornecida pela entrada de toque, sem comprometer a experiência do usuário para outros dispositivos.

Fornecemos algumas diretrizes gerais de interação do usuário aqui e abordaremos as diretrizes específicas do dispositivo nesses tópicos.

-   [Tocar](/windows/desktop/uxguide/inter-touch)
-   [Mouse](/windows/desktop/uxguide/inter-mouse)
-   [Caneta](/windows/desktop/uxguide/inter-pen)
-   [Teclado](/windows/desktop/uxguide/inter-keyboard)
-   [Acessibilidade](/windows/desktop/uxguide/inter-accessibility)

## <a name="visuals-for-feedback"></a>Visuais para comentários

Os comentários visuais apropriados durante as interações com seu aplicativo ajudam os usuários a reconhecer, aprender e adaptar-se à forma como as interações são interpretadas pelo aplicativo e os comentários visuais do Windows podem indicar interações bem-sucedidas, retransmitir o status do sistema, melhorar a sensação de controle, reduzir erros, ajudar os usuários a entender o sistema e o dispositivo de entrada e incentivar a interação.

A resposta visual é importante quando o usuário recorre à entrada por toque em atividades que exigem exatidão e precisão com base no local. A exibição do feedback sempre que a entrada por toque for detectada ajudará o usuário a entender as regras de direcionamento personalizadas definidas pelo aplicativo e seus respectivos controles.

## <a name="optimize-for-accuracy"></a>Otimizar para precisão

A entrada por toque envolve toda a área de contato do dedo. Essa geometria de contato é usada para determinar o objeto de destino mais provável. Dimensione os controles para garantir uma interface do usuário confortável com objetos e controles que são fáceis e seguros de direcionar.

Tamanho, espaço e posição de seus controles para ajudar a eliminar oclusãos de dedo e mão, onde a interface do usuário é obscurecida pela própria interação de usuários.

Posicionar menus, pop-ups e dicas de ferramenta acima da área de contato sempre que possível.

## <a name="constrain-for-confidence"></a>Restringir a confiança

Evite ou minimize interações impreciso usando restrições de interface do usuário.

-   Os pontos de ajuste podem facilitar a interrupção nos locais desejados. Pontos de alinhamento especificam paradas lógicas no conteúdo do aplicativo. Cognitiva, os pontos de ajuste atuam como um mecanismo de paginação para o usuário e minimizam o fadiga de deslizamento excessivo, passar o dedo ou girar. Com eles, você pode lidar com a entrada de usuário imprecisa e garantir que um subconjunto específico de conteúdo ou informações de chave seja exibido.
-   "Trilhos" direcionais que enfatizam o eixo de movimento (vertical ou horizontal).

## <a name="avoid-timed-interactions"></a>Evitar interações temporais

As interações não devem ser diferenciadas por tempo. A mesma interação deve ter o mesmo resultado, independentemente do tempo que leva para realizá-la. Ativações baseadas em tempo geram atrasos obrigatórios para os usuários e fogem de sua natureza imersiva de manipulação direta e percepção da capacidade de resposta do sistema.

As interações em tempo limite dependem normalmente de limites invisíveis como tempo, distância ou velocidade para determinar o comando a ser realizado. As interações com tempo limite não têm nenhum comentário visual até que o sistema execute a ação e os usuários devem alcançar limites arbitrários e invisíveis para obter um resultado. A resposta visual instantânea durante as interações faz com que os usuários se sintam conectados, confiantes e no controle.

As interações que afetam diretamente os objetos e imitam as interações reais são mais intuitivas, passíveis de descoberta e memorizáveis. Elas não dependem de interações obscuras ou abstratas.

**Observação:** Uma exceção é onde você usa interações específicas de tempo para ajudar no aprendizado e na exploração (por exemplo, pressione e mantenha pressionado). O uso de descrições e indicações visuais apropriadas tem um grande efeito no uso de interações avançadas.

