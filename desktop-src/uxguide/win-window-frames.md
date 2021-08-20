---
title: Quadros de janela
description: A maioria dos programas deve usar quadros de janela padrão. Aplicativos imersivos podem ter um modo de tela inteira que oculta o quadro da janela. Considere usar o glass estrategicamente para uma aparência mais simples, mais leve e coesa.
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dee701f7aad12e348a89034010de1f44134e9d3e
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812259"
---
# <a name="window-frames"></a>Quadros de janela

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

A maioria dos programas deve usar quadros de janela padrão. Aplicativos imersivos podem ter um modo de tela inteira que oculta o quadro da janela. Considere usar o glass estrategicamente para uma aparência mais simples, mais leve e coesa.

Com um quadro de janela, os usuários podem manipular uma janela e exibir o título e o ícone para identificar seu conteúdo.

![captura de tela do quadro de janela em torno da janela do bloco de notas ](images/win-window-frames-image1.png)

Um quadro de janela típico.

**Observação:** As diretrizes relacionadas [ao gerenciamento de janelas](win-window-mgt.md) [e à identidade visual](exper-branding.md) são apresentadas em artigos separados.

## <a name="design-concepts"></a>Conceitos de design

### <a name="glass-window-frames"></a>Quadros de janela de vidro

Os quadros de janela de vidro são um novo aspecto notável da linguagem Windows Microsoft, a fim de serem atraentes e leves. Esses quadros translúcidos dão ao Windows uma aparência aberta e menos intrusiva, ajudando os usuários a se concentrarem no conteúdo e na funcionalidade, em vez da interface ao redor dele.

![captura de tela de quadro de vidro ao redor da calculadora ](images/win-window-frames-image2.png)

Quadros de janela de vidro.

Você pode usar o vidro estrategicamente em regiões pequenas dentro de uma janela que toque no quadro da janela. Essas regiões parecem fazer parte do quadro da janela, embora tecnicamente elas sejam parte da área de cliente da janela.

![captura de tela da janela com borda translúcida ](images/win-window-frames-image3.png)

Neste exemplo, o glass é usado na área do cliente para torná-lo parecido com parte do quadro.

### <a name="hidden-frames"></a>Quadros ocultos

Às vezes, o melhor quadro de janela não é nenhum quadro. Geralmente, esse é [](glossary.md) o caso da janela [](glossary.md) principal de aplicativos de tela inteira imersiva que não são usados em conjunto com outros programas, como players de mídia, jogos e aplicativos de quiosque.

Os visualizadores de conteúdo geralmente se beneficiam de ter a opção de mostrar o conteúdo em tela inteira. Os exemplos incluem Windows Internet Explorer , Windows Live Galeria de Fotos, Windows Movie Maker HD, Microsoft PowerPoint e Microsoft Word.

![captura de tela do player de mídia na exibição de tela inteira ](images/win-window-frames-image4.png)

Neste exemplo, o Windows Media Player pode exibir seu conteúdo em tela inteira.

### <a name="custom-frames"></a>Quadros personalizados

A maioria Windows aplicativos devem usar os quadros de janela padrão. No entanto, para aplicativos imersivos, de tela inteira e autônomos, como jogos e aplicativos de quiosque, pode ser apropriado usar quadros personalizados para janelas que não são mostradas em tela inteira. A motivação para usar quadros personalizados deve ser dar à experiência geral uma sensação exclusiva, não apenas para [identidade visual.](exper-branding.md)

![ilustração do quebra-cabeça e quadro de imagem embaralhado ](images/win-window-frames-image5.png)

Quadros personalizados são apropriados para aplicativos imersivos, de tela inteira e autônomos, como jogos.

## <a name="guidelines"></a>Diretrizes

### <a name="window-frames"></a>Quadros de janela

-   Use quadros de janela padrão.
    -   **Exceção:** Para dar à tela inteira imersiva, os aplicativos autônomos dão uma sensação exclusiva:
        -   Considere ocultar o quadro de janela da [janela primária.](glossary.md)
        -   Considere o uso de quadros personalizados [para a janela secundária](glossary.md).
        -   Se um quadro personalizado for apropriado, escolha um design leve e que não chama muita atenção para si mesmo.

            **Incorreto:**

            ![captura de tela de quadro de distração ](images/win-window-frames-image6.png)

            Neste exemplo, o quadro personalizado chama muita atenção para si mesmo.
-   Não adicione controles a um quadro de janela. Em vez disso, coloque os controles dentro da janela.

    **Incorreto:**

    ![captura de tela do controle no quadro da janela ](images/win-window-frames-image7.png)

    **Correto:**

    ![captura de tela do controle na área do cliente ](images/win-window-frames-image8.png)

    No exemplo correto, o controle está dentro da área do cliente em vez do quadro da janela.

### <a name="full-screen-mode"></a>Modo de tela inteira

-   Para programas que têm um modo opcional de tela inteira, para habilitar o modo de tela inteira:
    -   Tenha um comando de tela inteira modal na barra de menus ou na barra de ferramentas. Quando o usuário clicar no comando, mostre o comando em seu estado selecionado.

        ![captura de tela da janela com o item de menu de tela inteira ](images/win-window-frames-image9.png)

        Este exemplo mostra o comando de tela inteira junto com sua tecla de atalho padrão.

-   Use F11 para a tecla de atalho de tela inteira.
-   Se houver uma barra de ferramentas e o modo de tela inteira normalmente for usado, também tenha um botão de barra de ferramentas gráfica com uma dica de ferramenta tela inteira.

    ![captura de tela de tela inteira e botões de reversão ](images/win-window-frames-image10.png)

    Exemplos de botões de barra de ferramentas de tela inteira.

-   Para reverter do modo de tela inteira:
    -   Tenha um comando de tela inteira modal na barra de menus ou na barra de ferramentas. Quando o usuário clicar no comando, mostre o comando em seu estado des limpo.
    -   Use F11 para a tecla de atalho de tela inteira. Se ainda não estiver atribuído, o Esc também poderá ser usado para essa finalidade.

### <a name="glass"></a>Vidro

Os quadros de janela padrão usam o glass automaticamente Windows, mas você também pode usar o vidro em regiões que tocam no quadro da janela.

-   **Considere usar o vidro estrategicamente em regiões pequenas que tocam no quadro da janela sem texto.** Isso pode dar a um programa uma aparência mais simples, mais leve e coesa fazendo com que a região pareça fazer parte do quadro.
-   ![captura de tela da janela com borda translúcida ](images/win-window-frames-image3.png)
-   Neste exemplo, o glass concentra a atenção do usuário no conteúdo em vez dos controles.
-   **Não use o vidro em situações em que um plano de fundo de janela simples seria mais atraente ou mais fácil de usar.**

**Correto:**

![captura de tela da janela com quatro elementos gráficos e rótulo ](images/win-window-frames-image11.png)

Neste exemplo, o glass é usado para dar à janela Alt+Tab uma aparência leve. O Glass funciona para essa janela porque consiste em elementos gráficos e um único rótulo de texto forte.

**Incorreto:**

![captura de tela da janela com doze elementos gráficos ](images/win-window-frames-image12.png)

Neste exemplo incorreto, o uso de vidro é uma distração. Um plano de fundo de janela simples seria uma opção melhor.

 

 
