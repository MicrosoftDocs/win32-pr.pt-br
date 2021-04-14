---
title: Quadros de janela
description: A maioria dos programas deve usar quadros de janela padrão. Aplicativos de imersão podem ter um modo de tela inteira que oculta o quadro da janela. Considere o uso estratégico de vidro para uma aparência mais simples, mais leve e coesa.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104569141"
---
# <a name="window-frames"></a>Quadros de janela

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

A maioria dos programas deve usar quadros de janela padrão. Aplicativos de imersão podem ter um modo de tela inteira que oculta o quadro da janela. Considere o uso estratégico de vidro para uma aparência mais simples, mais leve e coesa.

Com um quadro de janela, os usuários podem manipular uma janela e exibir o título e o ícone para identificar seu conteúdo.

![captura de tela do quadro da janela ao contrário da janela do bloco de notas ](images/win-window-frames-image1.png)

Um quadro de janela típico.

**Observação:** As diretrizes relacionadas ao [Gerenciamento de janelas](win-window-mgt.md) e à [identidade visual](exper-branding.md) são apresentadas em artigos separados.

## <a name="design-concepts"></a>Conceitos de design

### <a name="glass-window-frames"></a>Quadros de janela de vidro

Os quadros de janela de vidro são um novo aspecto surpreendente da estética do Microsoft Windows, objetivando ser atraentes e leves. Esses quadros translúcidas fornecem ao Windows uma aparência aberta e menos invasiva, ajudando os usuários a se concentrarem no conteúdo e na funcionalidade, e não na interface em torno dela.

![captura de tela do quadro de vidro em volta da calculadora ](images/win-window-frames-image2.png)

Quadros de janela de vidro.

Você pode usar o vidro estrategicamente em pequenas regiões dentro de uma janela que toca o quadro da janela. Essas regiões parecem ser parte do quadro da janela, embora tecnicamente elas façam parte da área do cliente da janela.

![captura de tela da janela com borda translúcida ](images/win-window-frames-image3.png)

Neste exemplo, o vidro é usado na área do cliente para deixá-lo parecer com parte do quadro.

### <a name="hidden-frames"></a>Quadros ocultos

Às vezes, o melhor quadro de janela não é nenhum quadro. Esse é geralmente o caso para a [janela principal](glossary.md) de aplicativos de [tela inteira](glossary.md) de imersão que não são usados em conjunto com outros programas, como media players, jogos e aplicativos de quiosque.

Os visualizadores de conteúdo geralmente se beneficiam da opção de mostrar o conteúdo em tela inteira. Os exemplos incluem o Windows Internet Explorer, a Galeria de fotos do Windows Live, o Windows Movie Maker HD, o Microsoft PowerPoint e o Microsoft Word.

![captura de tela do player de mídia no modo de exibição de tela inteira ](images/win-window-frames-image4.png)

Neste exemplo, o Windows Media Player pode exibir seu conteúdo em tela inteira.

### <a name="custom-frames"></a>Quadros personalizados

A maioria dos aplicativos do Windows deve usar os quadros de janela padrão. No entanto, para aplicativos de imersão, tela inteira e autônoma, como jogos e aplicativos de quiosque, pode ser apropriado usar quadros personalizados para qualquer janela que não seja mostrada em tela inteira. A motivação de usar quadros personalizados deve ser oferecer a experiência geral uma sensação única, não apenas para [identidade visual](exper-branding.md).

![ilustração de quebra-cabeça e quadro de imagem embaralhada ](images/win-window-frames-image5.png)

Os quadros personalizados são apropriados para aplicativos de imersão, tela inteira e autônomos, como jogos.

## <a name="guidelines"></a>Diretrizes

### <a name="window-frames"></a>Quadros de janela

-   Use quadros de janela padrão.
    -   **Exceção:** Para dar uma aparência de tela inteira, os aplicativos autônomos são uma sensação única:
        -   Considere ocultar o quadro de janela da [janela principal](glossary.md).
        -   Considere o uso de quadros personalizados para a [janela secundária](glossary.md).
        -   Se um quadro personalizado for apropriado, escolha um design que seja leve e não atraia muita atenção para si mesmo.

            **Incorreto:**

            ![captura de tela de quadro de distração ](images/win-window-frames-image6.png)

            Neste exemplo, o quadro personalizado chama muita atenção para si mesmo.
-   Não adicione controles a um quadro de janela. Em vez disso, coloque os controles dentro da janela.

    **Incorreto:**

    ![captura de tela de controle no quadro da janela ](images/win-window-frames-image7.png)

    **Correto:**

    ![captura de tela de controle na área do cliente ](images/win-window-frames-image8.png)

    No exemplo correto, o controle está dentro da área do cliente em vez do quadro da janela.

### <a name="full-screen-mode"></a>Modo de tela inteira

-   Para programas que têm um modo de tela inteira opcional, para habilitar o modo de tela inteira:
    -   Ter um comando de tela inteira modal na barra de menus ou na barra de ferramentas. Quando o usuário clicar no comando, mostrará o comando em seu estado selecionado.

        ![captura de tela de janela com item de menu de tela inteira ](images/win-window-frames-image9.png)

        Este exemplo mostra o comando de tela inteira junto com sua tecla de atalho padrão.

-   Use F11 para a tecla de atalho de tela inteira.
-   Se houver uma barra de ferramentas e o modo de tela inteira for comumente usado, também terá um botão de barra de ferramentas gráfica com uma dica de ferramenta de tela inteira.

    ![captura de tela dos botões tela inteira e reverter ](images/win-window-frames-image10.png)

    Exemplos de botões da barra de ferramentas de tela inteira.

-   Para reverter do modo de tela inteira:
    -   Ter um comando de tela inteira modal na barra de menus ou na barra de ferramentas. Quando o usuário clicar no comando, mostrará o comando em seu estado limpo.
    -   Use F11 para a tecla de atalho de tela inteira. Se ainda não tiver sido atribuído, ESC também poderá ser usado para essa finalidade.

### <a name="glass"></a>Vidro

Quadros de janela padrão usam vidro automaticamente no Windows, mas você também pode usar vidro em regiões que tocam o quadro da janela.

-   **Considere usar o vidro estrategicamente em pequenas regiões tocando no quadro da janela sem texto.** Fazer isso pode dar a um programa uma visão mais simples, mais leve e coesa, fazendo com que a região pareça ser parte do quadro.
-   ![captura de tela da janela com borda translúcida ](images/win-window-frames-image3.png)
-   Neste exemplo, o vidro concentra a atenção do usuário sobre o conteúdo em vez dos controles.
-   **Não use o vidro em situações em que um plano de fundo de janela simples seria mais atraente ou mais fácil de usar.**

**Correto:**

![captura de tela de janela com quatro elementos gráficos e rótulo ](images/win-window-frames-image11.png)

Neste exemplo, o vidro é usado para dar à janela ALT + TAB uma aparência leve. O vidro funciona para esta janela porque ele consiste em gráficos e um único rótulo de texto forte.

**Incorreto:**

![captura de tela de janela com doze elementos gráficos ](images/win-window-frames-image12.png)

Neste exemplo incorreto, o uso de vidro está me distraindo. Um plano de fundo de janela simples seria uma opção melhor.

 

 