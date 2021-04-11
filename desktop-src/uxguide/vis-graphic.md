---
title: Elementos gráficos
description: Elementos gráficos mostram as relações, a hierarquia e a ênfase visualmente. Eles incluem planos de fundo, faixas, vidro, agregadores, separadores, sombras e identificadores.
ms.assetid: f9e741e9-a72e-4bdb-bd95-8916c7cf344f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a452668bc1685143273df80fd144642a18019213
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103930063"
---
# <a name="graphic-elements"></a>Elementos gráficos

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

*Elementos gráficos* mostram as relações, a hierarquia e a ênfase visualmente. Eles incluem planos de fundo, faixas, vidro, agregadores, separadores, sombras e identificadores.

![captura de tela do Windows Explorer com sombra, etc. ](images/vis-graphic-image1.png)

Um exemplo com vários tipos de elementos gráficos.

Os elementos gráficos geralmente não são interativos. No entanto, os separadores são interativos para conteúdo e identificadores redimensionáveis são gráficos que mostram interatividade.

**Observação:** As diretrizes relacionadas a [caixas de grupo](ctrl-group-boxes.md), [animações](vis-animations.md), [ícones](vis-icons.md)e [identidade visual](exper-branding.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Embora elementos gráficos sejam um forte modo visual de indicar relações, o excesso de uso adiciona resíduos visuais e reduz o espaço disponível em uma superfície. Eles devem ser usados com moderação.

Uma tendência de design no Microsoft Windows é uma aparência mais simples e limpa ao eliminar elementos gráficos e linhas desnecessários.

Para decidir se um elemento gráfico é necessário, considere estas perguntas:

-   **A apresentação e a comunicação do design são tão claras e eficazes sem o elemento?** Nesse caso, remova-o.
-   **Você pode efetivamente comunicar as relações usando apenas o layout?** Nesse caso, use o [layout](vis-layout.md) em vez disso. Você pode colocar controles relacionados ao lado um do outro e colocar o espaçamento adicional entre controles não relacionados. Você também pode usar recuo para mostrar relações hierárquicas.

![captura de tela de um layout de quatro ícones ](images/vis-graphic-image2.png)

Neste exemplo, layout sozinho é usado para mostrar relações de controle.

-   **A comunicação é eficaz sem texto?** Caso contrário, use uma [caixa de grupo](ctrl-group-boxes.md), um separador rotulado ou outro [rótulo](text-ui.md).

## <a name="usage-patterns"></a>Padrões de uso

Os elementos gráficos têm vários padrões de uso:



|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ilustrações gráficas**<br/> Use para comunicar visualmente uma ideia. <br/>                         | Ilustrações gráficas são semelhantes a ícones, exceto que podem ser qualquer tamanho e geralmente não são interativas. <br/> ![gráfico de histórico de uso da CPU de captura de tela ](images/vis-graphic-image3.png)<br/> Neste exemplo, uma ilustração gráfica é usada para sugerir a natureza de um recurso.<br/>                                                                                                                                                                                                        |
| **Telas de fundo**<br/> Use para enfatizar ou realçar diferentes tipos de conteúdo. <br/>           | Os planos de fundo podem ser usados para enfatizar conteúdo importante. <br/> ![captura de tela de mensagem de vírus no plano de fundo vermelho ](images/vis-graphic-image4.png)<br/> Neste exemplo, um plano de fundo é usado para enfatizar uma tarefa importante.<br/> os planos de fundo também podem ser usados para enfatizar o conteúdo secundário. <br/> ![captura de tela de itens do painel de controle ](images/vis-graphic-image5.png)<br/> Neste exemplo, as tarefas secundárias são realçadas, localizando-as em um painel de tarefas.<br/>   |
| **Publicitária**<br/> usado para indicar o status importante. <br/>                                         | Em contraste com os planos de fundo, as faixas enfatizam principalmente uma única cadeia de texto. <br/> ![captura de tela de faixa com informações de configurações ](images/vis-graphic-image6.png)<br/> Neste exemplo, uma faixa é usada para indicar que as configurações da página são controladas por Política de Grupo.<br/>                                                                                                                                                                                                       |
| **Vidro**<br/> Use estrategicamente para reduzir o peso visual de uma janela. <br/>                   | O vidro pode reduzir o peso de uma superfície concentrando-se no conteúdo em vez da própria janela. <br/> ![captura de tela de pássaro na Galeria de fotos do Windows ](images/vis-graphic-image7.png)<br/> Neste exemplo, o vidro concentra a atenção do usuário sobre o conteúdo em vez dos controles.<br/>                                                                                                                                                                                                 |
| **Dados aninhados e complexos**<br/> Use para criar uma relação visual entre controles fortemente relacionados. <br/> | ![captura de tela das setas de navegação voltar e avançar ](images/vis-graphic-image8.png)<br/> Neste exemplo, um plano de fundo de agregador é usado para enfatizar a relação entre os botões voltar e avançar no Explorer.<br/> ![captura de tela dos controles da Galeria de fotos do Windows ](images/vis-graphic-image7.png)<br/> Neste exemplo, um agregador de limite é usado para enfatizar a relação entre os controles e fazer com que eles se sintam como um único controle em vez de oito.<br/> |
| **Separadores**<br/> Use para separar controles fracamente relacionados ou não relacionados. <br/>                   | Os separadores podem ser interativos ou não interativos. os separadores interativos entre conteúdo redimensionável são conhecidos como divisores. <br/> ![captura de tela do separador de divisão para o botão nome ](images/vis-graphic-image9.png)<br/> Neste exemplo, um separador interativo é usado para conteúdo redimensionável.<br/> ![captura de tela de separador de informações do navegador ](images/vis-graphic-image10.png)<br/> Neste exemplo, o separador não é interativo.<br/>                  |
| **Sombras**<br/> Use para fazer com que o conteúdo fique visualmente em seu plano de fundo. <br/>             | ![captura de tela de quatro fotos com sombras ](images/vis-graphic-image11.png)<br/> Neste exemplo, as sombras fazem com que o trabalho artístico se destaque em relação ao plano de fundo.<br/>                                                                                                                                                                                                                                                                                                                                   |
| **Alças**<br/> Use para indicar que um objeto pode ser movido ou redimensionado. <br/>                    | Os identificadores são sempre interativos e seu comportamento é sugerido pelo ponteiro do mouse sobre o foco. <br/> ![captura de tela de um canto da janela com ponteiro de redimensionamento ](images/vis-graphic-image12.png)<br/> ![captura de tela da caixa de seleção com ponteiro de redimensionamento ](images/vis-graphic-image13.png)<br/> Nestes exemplos, os identificadores indicam que um objeto pode ser redimensionado.<br/>                                                                                                                       |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Não transmita informações essenciais apenas por meio de elementos gráficos.** Isso apresenta problemas de acessibilidade para usuários com deficiências visuais ou deficiências.

### <a name="graphic-designs"></a>Designs gráficos

-   **Os elementos gráficos são mais eficazes quando reforçam uma única ideia simples.** Gráficos complexos que exigem uma ideia de interpretação não funcionam bem. Hieroglyphics são mais bem deixados para desenhos de côncavos.

    **Incorreto:**

    ![captura de tela de aviso usando gráfico complexo ](images/vis-graphic-image14.png)

    Neste exemplo, um gráfico complexo do Windows XP tenta, de forma ineficaz, explicar uma decisão de confiança complexa.

-   **Não use setas, divisas, quadros de botão ou outros capacidades associados a controles interativos.** Fazer isso convida os usuários a interagir com seus elementos gráficos.
-   **Evite faixas de vermelho, amarelo e verde puros em seus designs.** Para evitar confusão, Reserve essas cores para comunicar o status. Se você precisar usar essas cores para algo diferente de status, use tons sem som em vez de cores puras.
-   **Use designs de cultura neutra.** O que pode ter um determinado significado em um país, região ou cultura pode não ter o mesmo significado em outro.
-   **Evite usar pessoas, rostos, gênero ou partes de corpo, bem como símbolos religiosas, políticos e nacionais.** Essas imagens podem não ser facilmente traduzidas ou podem ser ofensivas.
-   **Quando você deve representar pessoas ou usuários, descreva-os genericamente;** Evite as representações realísticas.

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

-   **Suporta modos de vídeo 96 e 120 pontos por polegada (DPI).** Detecte o modo de DPI na inicialização e manipule eventos de alteração de DPI. O Windows é otimizado para 96 e 120 dpi e usa o 96 DPI por padrão.
-   **Prefira fornecer bitmaps separados renderizados especificamente para 96 e 120 dpi sobre o dimensionamento de gráficos.** Pelo menos, forneça versões 96 e 120 de dpi para os bitmaps mais importantes, visíveis e para o centro ou para dimensionar os outros. Esses aplicativos são considerados "reconhecimento de dpi alta" e fornecem uma experiência visual geral melhor do que os programas que são dimensionados automaticamente pelo Windows.
    -   Desenvolvedores: você pode declarar um programa com reconhecimento de alto DPI (e impedir o dimensionamento automático) definindo o sinalizador de reconhecimento de dpi no manifesto do programa ou chamando a API SetProcessDPIAware () durante a inicialização do programa. Você pode usar macros para simplificar a seleção dos elementos gráficos corretos. Para os bitmaps do Win32, você pode usar SS \_ CENTERIMAGE para centralizar ou SS \_ REALSIZECONTROL para dimensionar.
-   Verifique seu programa em 96 e 120 dpi para:
    -   Elementos gráficos muito pequenos ou muito grandes.
    -   Elementos gráficos sendo recortados, sobrepostos ou não se ajustam corretamente.
    -   Gráficos que são mal alongados ("pixilated").
    -   Texto recortado ou não se ajusta em planos de fundo gráficos.

## <a name="text"></a>Texto

-   **Para acessibilidade e localização, não use nenhum texto em elementos gráficos.** Faça exceções apenas para representar a [identidade visual](exper-branding.md) e o texto como um conceito abstrato.

 

