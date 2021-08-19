---
title: Elementos gráficos
description: Elementos gráficos mostram relações, hierarquia e ênfase visualmente. Eles incluem plano de fundo, faixas, vidro, agregadores, separadores, sombras e alças.
ms.assetid: f9e741e9-a72e-4bdb-bd95-8916c7cf344f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: cc4b5ce620660e655eeee81cab869909c14b4f8290b5852da7f480da85951a5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936097"
---
# <a name="graphic-elements"></a>Elementos gráficos

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

*Elementos gráficos* mostram relações, hierarquia e ênfase visualmente. Eles incluem plano de fundo, faixas, vidro, agregadores, separadores, sombras e alças.

![captura de tela do Windows Explorer com sombra etc. ](images/vis-graphic-image1.png)

Um exemplo com vários tipos de elementos gráficos.

Elementos gráficos geralmente não são interativos. No entanto, separadores são interativos para conteúdo reizável e os manipuladores são gráficos que mostram interatividade.

**Observação:** Diretrizes relacionadas [a caixas de](ctrl-group-boxes.md)grupo, [animações,](vis-animations.md) [ícones](vis-icons.md)e identidade [visual](exper-branding.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Embora elementos gráficos sejam um meio visual forte de indicar relações, o uso em excesso deles adiciona confusão visual e reduz o espaço disponível em uma superfície. Eles devem ser usados com moderação.

Uma tendência de design no Microsoft Windows é uma aparência mais simples e mais limpa, eliminando gráficos e linhas desnecessários.

Para decidir se um elemento gráfico é necessário, considere estas perguntas:

-   **A apresentação e a comunicação do design são tão claras e eficazes sem o elemento?** Em caso afirmado, remova-o.
-   **Você pode comunicar efetivamente as relações usando o layout sozinho?** Em caso afirmado, use [o layout.](vis-layout.md) Você pode colocar controles relacionados ao lado uns dos outros e colocar espaçamento extra entre controles não relacionados. Você também pode usar o recuo para mostrar relações hierárquicas.

![captura de tela de um layout de quatro ícones ](images/vis-graphic-image2.png)

Neste exemplo, somente o layout é usado para mostrar relações de controle.

-   **A comunicação é eficaz sem texto?** Caso contrário, use uma [caixa de grupo](ctrl-group-boxes.md), um separador rotulado ou outro [rótulo](text-ui.md).

## <a name="usage-patterns"></a>Padrões de uso

Elementos gráficos têm vários padrões de uso:



| Elemento                                                                                                              |   Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ilustrações gráficas**<br/> use para comunicar uma ideia visualmente. <br/>                         | Ilustrações gráficas são semelhantes a ícones, exceto que podem ser de qualquer tamanho e geralmente não são interativas. <br/> ![captura de tela do gráfico de histórico de uso da CPU ](images/vis-graphic-image3.png)<br/> Neste exemplo, uma ilustração gráfica é usada para sugerir a natureza de um recurso.<br/>                                                                                                                                                                                                        |
| **Telas de fundo**<br/> use para enfatizar ou des enfatizar diferentes tipos de conteúdo. <br/>           | Os bastidores podem ser usados para enfatizar conteúdo importante. <br/> ![captura de tela da mensagem de vírus em tela de fundo vermelha ](images/vis-graphic-image4.png)<br/> neste exemplo, uma segundo plano é usada para enfatizar uma tarefa importante.<br/> backgrounds também podem ser usados para des enfatizar o conteúdo secundário. <br/> ![captura de tela de itens do painel de controle ](images/vis-graphic-image5.png)<br/> Neste exemplo, as tarefas secundárias são des enfatizadas localizando-as em um painel de tarefas.<br/>   |
| **Banners**<br/> usado para indicar um status importante. <br/>                                         | Ao contrário dos backgrounds, as faixas enfatizam principalmente uma única cadeia de caracteres de texto. <br/> ![captura de tela da faixa com informações de configurações ](images/vis-graphic-image6.png)<br/> Neste exemplo, uma faixa é usada para indicar que as configurações da página são controladas por Política de Grupo.<br/>                                                                                                                                                                                                       |
| **Vidro**<br/> use estrategicamente para reduzir o peso visual de uma janela. <br/>                   | O glass pode reduzir o peso de uma superfície concentrando-se no conteúdo em vez da própria janela. <br/> ![captura de tela do pássaro na galeria de fotos do Windows ](images/vis-graphic-image7.png)<br/> Neste exemplo, o glass concentra a atenção do usuário no conteúdo em vez dos controles.<br/>                                                                                                                                                                                                 |
| **Dados aninhados e complexos**<br/> use para criar uma relação visual entre controles fortemente relacionados. <br/> | ![captura de tela das setas de navegação para trás e para frente ](images/vis-graphic-image8.png)<br/> neste exemplo, um plano de fundo do agregador é usado para enfatizar a relação entre os botões voltar e avançar no Explorer.<br/> ![captura de tela dos controles da galeria de fotos do Windows ](images/vis-graphic-image7.png)<br/> Neste exemplo, um agregador de limites é usado para enfatizar a relação entre os controles e fazer com que eles se sintam como um único controle em vez de oito.<br/> |
| **Separadores**<br/> use para separar controles fracamente relacionados ou não relacionados. <br/>                   | Separadores podem ser interativos ou não interativos. separadores interativos entre conteúdo reizável são conhecidos como divistores. <br/> ![captura de tela do separador de divisor para o botão de nome ](images/vis-graphic-image9.png)<br/> neste exemplo, um separador interativo é usado para conteúdo reizável.<br/> ![captura de tela do separador para informações do navegador ](images/vis-graphic-image10.png)<br/> Neste exemplo, o separador não é interativo.<br/>                  |
| **Sombras**<br/> use para fazer com que o conteúdo se destaque visualmente em relação ao seu plano de fundo. <br/>             | ![captura de tela de quatro fotos com sombras ](images/vis-graphic-image11.png)<br/> Neste exemplo, as sombras fazem com que a arte se destaque na parte de fundo.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Alças**<br/> use para indicar que um objeto pode ser movido ou reessado. <br/>                    | Os alças são sempre interativos e seu comportamento é sugerido pelo ponteiro do mouse ao passar o mouse. <br/> ![captura de tela de um canto da janela com o ponteiro de resize ](images/vis-graphic-image12.png)<br/> ![captura de tela da caixa de seleção com o ponteiro de resize ](images/vis-graphic-image13.png)<br/> Nesses exemplos, identificador indica que um objeto pode ser reessado.<br/>                                                                                                                       |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Não transmita informações essenciais apenas por meio de elementos gráficos.** Isso apresenta problemas de acessibilidade para usuários com deficiências visuais ou deficiências.

### <a name="graphic-designs"></a>Designs gráficos

-   **Os gráficos são mais eficazes quando reforçam uma única ideia simples.** Gráficos complexos que exigem um pensamento para interpretar não funcionam bem. Hierogly cavecs são melhores deixados para desenhos de caverna.

    **Incorreto:**

    ![captura de tela de aviso usando gráfico complexo ](images/vis-graphic-image14.png)

    Neste exemplo, um gráfico complexo do Windows XP tenta explicar ineficazmente uma decisão de confiança complexa.

-   **Não use setas, divisas, quadros de botão ou outras acessível associadas a controles interativos.** Isso convida os usuários a interagir com seus gráficos.
-   **Evite problemas de vermelho puro, amarelo e verde em seus designs.** Para evitar confusão, reserve essas cores para comunicar o status. Se você precisa usar essas cores para algo diferente do status, use tons mudos em vez de cores puras.
-   **Use designs culturalmente neutros.** O que pode ter um certo significado em um país, região ou cultura pode não ter o mesmo significado em outro.
-   **Evite usar pessoas, rostos, gênero ou partes do corpo, bem como símbolos nacionais, política e política.** Essas imagens podem não ser facilmente traduzidas ou podem ser ofensivos.
-   **Quando você precisa representar pessoas ou usuários, represente-os genericamente;** evite representações realistas.

### <a name="backgrounds-and-banners"></a>Planos de fundo e faixas

-   **Para enfatizar o conteúdo, use o texto escuro em um plano de fundo claro.** O texto preto em um plano de fundo cinza claro ou amarelo funciona bem.

    ![captura de tela do texto do link azul no plano de fundo amarelo ](images/vis-graphic-image15.png)

    Neste exemplo, o link Obtém a atenção do usuário porque ele está em um plano de fundo amarelo.

-   **Para realçar o conteúdo, use texto claro em um plano de fundo escuro.** O texto branco em um plano de fundo cinza escuro ou azul funciona bem.

    ![captura de tela do link de ajuda branco sobre o plano de fundo verde ](images/vis-graphic-image16.png)

    Neste exemplo, o plano de fundo escuro enfatiza o conteúdo.

-   **Se um gradiente for usado, verifique se a cor do texto tem bons contrastes em todo o gradiente.**
-   **Sempre use um ícone de 16x16 pixels para chamar a atenção para a faixa.** As faixas são muito fáceis de serem ignoradas do contrário. Para obter mais diretrizes e exemplos, consulte [ícones padrão](vis-std-icons.md).
-   **Use planos de fundo e faixas com cuidado.** Embora a intenção do plano de fundo ou da faixa possa ser enfatizar o conteúdo, muitas vezes os resultados são o oposto de um fenômeno conhecido como "cegueira de faixa".

### <a name="glass"></a>Vidro

-   **Considere usar o vidro estrategicamente em pequenas regiões tocando no quadro da janela sem texto.** Fazer isso pode dar a um programa uma visão mais simples, mais leve e coesa, fazendo com que a região pareça ser parte do quadro.
-   **Não use o vidro em situações em que um plano de fundo de janela simples seria mais atraente ou mais fácil de usar.**

### <a name="separators"></a>Separadores

-   **Use linhas verticais e horizontais para separadores.** Certifique-se de ter espaço suficiente entre os separadores e o conteúdo sendo separado.
-   Para separadores entre conteúdo ajustável (divisores), exiba o ponteiro de redimensionamento ao focalizar.

![Captura de tela que mostra um divisor com ponteiro de redimensionamento.](images/vis-graphic-image17.png)

![captura de tela de divisor com ponteiro de redimensionamento ](images/vis-graphic-image18.png)

Nesses exemplos, os ponteiros de redimensionamento são mostrados em foco.

### <a name="shadows"></a>Sombras

-   **Use apenas para tornar o conteúdo mais significativo do programa ou os objetos sendo arrastados visualmente em relação ao seu plano de fundo.** Considere as sombras como confusão visuais em outras circunstâncias.

### <a name="high-dpi-support"></a>Suporte a DPI alto

-   **Suporta modos de vídeo 96 e 120 pontos por polegada (DPI).** Detecte o modo de DPI na inicialização e manipule eventos de alteração de DPI. Windows é otimizado para 96 e 120 dpi e usa 96 dpi por padrão.
-   **Prefira fornecer bitmaps separados renderizados especificamente para 96 e 120 dpi sobre o dimensionamento de gráficos.** Pelo menos, forneça versões 96 e 120 de dpi para os bitmaps mais importantes, visíveis e para o centro ou para dimensionar os outros. Esses aplicativos são considerados "reconhecimento de dpi alta" e fornecem uma experiência visual geral melhor do que os programas que são dimensionados automaticamente pelo Windows.
    -   Desenvolvedores: você pode declarar um programa com reconhecimento de alto DPI (e impedir o dimensionamento automático) definindo o sinalizador de reconhecimento de dpi no manifesto do programa ou chamando a API SetProcessDPIAware () durante a inicialização do programa. Você pode usar macros para simplificar a seleção dos elementos gráficos corretos. Para os bitmaps do Win32, você pode usar SS \_ CENTERIMAGE para centralizar ou SS \_ REALSIZECONTROL para dimensionar.
-   Verifique seu programa em 96 e 120 dpi para:
    -   Elementos gráficos muito pequenos ou muito grandes.
    -   Elementos gráficos sendo recortados, sobrepostos ou não se ajustam corretamente.
    -   Gráficos que são mal alongados ("pixilated").
    -   Texto recortado ou não se ajusta em planos de fundo gráficos.

## <a name="text"></a>Texto

-   **Para acessibilidade e localização, não use nenhum texto em elementos gráficos.** Faça exceções apenas para representar a [identidade visual](exper-branding.md) e o texto como um conceito abstrato.

 

