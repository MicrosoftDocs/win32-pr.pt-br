---
title: Caixas de pesquisa
description: Com uma caixa De pesquisa, os usuários podem localizar rapidamente objetos específicos ou texto dentro de um grande conjunto de dados filtrando ou realçando as correspondeções.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 71e0ce45e2fd0b84b0abda9462f2cb42c945790e93ea06e7dfc6ece0f65ffd65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842909"
---
# <a name="search-boxes"></a>Caixas de pesquisa

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com uma caixa De pesquisa, os usuários podem localizar rapidamente objetos específicos ou texto dentro de um grande conjunto de dados filtrando ou realçando as correspondeções. Não há nenhum controle de pesquisa padrão, mas você deve se esforçar para tornar os recursos de pesquisa do programa consistentes com os de Windows.

Há dois tipos de pesquisas:

-   **Pesquisa instantânea**, em que os resultados são exibidos imediatamente como os tipos de usuário. Nenhum botão precisa ser clicado, portanto, o símbolo de pesquisa de lupa é mostrado como um gráfico, não um botão.

    ![Captura de tela que mostra uma caixa de pesquisa instantânea com um texto explicando "Prompt" apontando para a caixa Pesquisa e um texto explicando "Símbolo de pesquisa" apontando para o gráfico de lupa.](images/ctrl-search-boxes-image1.png)

    Uma caixa de Pesquisa típica usando a Pesquisa instantânea. A pesquisa é executada automaticamente em cada tecla.

-   **Pesquisa regular**, em que uma pesquisa é executada quando o usuário clica no botão de pesquisa. O símbolo de pesquisa de lupa é mostrado em um botão.

    ![captura de tela de uma caixa de pesquisa regular ](images/ctrl-search-boxes-image2.png)

    Uma caixa de pesquisa típica usando a pesquisa regular. Os usuários clicam em um botão para executar a pesquisa.

    Você pode fornecer um ou ambos os tipos de opções de pesquisa para seus usuários.

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **Objetos específicos são difíceis de encontrar?** Isso pode ocorrer quando:
    -   Há muitos objetos.
    -   Os objetos não estão localizados em um único local. A pesquisa é especialmente útil para localizar objetos em árvores.
    -   Os dados de pesquisa são difíceis de encontrar (por exemplo, metadados).
-   **Os usuários precisam encontrar texto específico em documentos?**
-   **Seu recurso retorna resultados de pesquisa relevantes dentro de cinco segundos?** Caso não, você pode fornecer um recurso de pesquisa, mas usar um design alternativo que fornece comentários visíveis para acomodar pesquisas de longa execução, como uma caixa de diálogo de pesquisa.

## <a name="design-concepts"></a>Conceitos de design

A pesquisa é uma primeira etapa crucial em muitos cenários: os usuários devem encontrar objetos antes de usá-los. Os usuários estão salvando cada vez mais objetos em discos rígidos cada vez maiores, mas a navegação por objetos não é bem dimensionada. A pesquisa deve ser uma parte simples, consistente e confiável da experiência do usuário.

Caixas de pesquisa Windows:

-   Fazem parte de todas as janelas do Explorer, portanto, são fáceis de encontrar e reconhecer.
-   Ter aparência e comportamento consistentes.
-   São eficientes e rápidos, dando resultados instantâneos no modo de pesquisa instantânea.

Uma caixa De pesquisa é usada Windows nesses locais:

-   Exploradores
-   Experiências (Microsoft Windows Media Player, Windows Galeria de Fotos, Windows Internet Explorer)
-   menu Iniciar (para encontrar programas e arquivos recentes)
-   Painel de Controle home page (para encontrar itens e tarefas do painel de controle)
-   Ajuda (para encontrar tópicos relevantes da Ajuda)

### <a name="look-and-feel"></a>Aparência

A sensação de Pesquisa no Windows é significativamente aprimorada com o suporte à pesquisa instantânea. Ter resultados instantâneos faz Windows se sentir mais poderoso e direto.

No Windows Explorer e janelas do aplicativo, a Pesquisa está localizada no canto superior direito se for um ponto de entrada complementar. Nesse caso, os usuários procuram um mecanismo de pesquisa quando não encontram o que estão procurando na janela. No entanto, se a Pesquisa for o ponto de entrada primário, ela será centralizada na parte superior da janela.

O botão Pesquisar está conectado visualmente a uma caixa De pesquisa. Para minimizar o espaço, um [prompt opcional](ctrl-text-boxes.md) é usado dentro de uma caixa Pesquisar em vez de um rótulo. O prompt pode ser uma instrução (por exemplo, Tipo para pesquisar) ou indicar o escopo da pesquisa (por exemplo, Pesquisar imagens).

![captura de tela de uma caixa de pesquisa instantânea ](images/ctrl-search-boxes-image3.png)

Sem rótulos e botões separados, a pesquisa instantânea Windows tem uma aparência leve.

A execução de uma pesquisa bem-sucedida cria uma página virtual dos resultados da pesquisa e a adiciona à pilha Voltar e à barra de endereços. Os usuários têm várias maneiras de restaurar a página original e limpar uma caixa De pesquisa, incluindo clicar em Voltar, clicar na página original na barra de endereços, pressionar Esc ou desempurar a caixa Pesquisar.

Os usuários também podem simplesmente limpar a caixa Pesquisar sem restaurar uma página anterior de resultados. No modo de pesquisa instantânea, um botão limpar aparece depois que o usuário começa a digitar; um "x" substitui o símbolo de pesquisa de lupa. Ao passar o mouse, o "x" obtém uma aparência de botão e pode ser clicado.

![captura de tela de uma caixa de pesquisa com um ícone 'x' ](images/ctrl-search-boxes-image4.png)

O usuário pode limpar a caixa Pesquisar clicando em "x" na extremidade direita do controle.

No modo de pesquisa regular, o botão limpar é opcional. Os usuários podem achar útil, por exemplo, se uma pesquisa estiver demorando muito para ser concluída. Os usuários podem clicar no "x" para interromper a pesquisa em andamento. Se uma pesquisa já tiver sido concluída, os usuários poderão clicar no "x" para limpar a caixa Pesquisa.

## <a name="guidelines"></a>Diretrizes

### <a name="location"></a>Localização

-   Para janelas de aplicativos, localize Pesquisar no canto superior direito.
-   Para janelas pop-up, localize Pesquisar sempre que for mais conveniente e conveniente.
-   **Exceção:** Se a Pesquisa geralmente for a primeira coisa que os usuários fazem em uma janela (o ponto de entrada primário), centralmente-o na parte superior da janela.

### <a name="look"></a>Olhar

-   Use os gráficos do botão de pesquisa padrão. Há três versões:
    -   **Somente símbolo de pesquisa de lupa (sem botão ao passar o mouse).** Use para Pesquisa instantânea.
    -   **Símbolo de pesquisa de lupa com o botão .** Use quando o botão precisar ser clicado para iniciar a pesquisa.
    -   **Símbolo de pesquisa de lupa com botão e seta para baixo.** Adicione uma seta para baixo quando os usuários puderem alterar o escopo ou quando outras configurações estão disponíveis.
        -   Para Pesquisa instantânea, use apenas uma seta para baixo e mostre um botão ao passar o mouse.
        -   Para pesquisa regular, mostre a seta para baixo em um botão.

![figura de caixas de pesquisa instantâneas em estados diferentes ](images/ctrl-search-boxes-image5.png)

Especificações visuais para Pesquisa instantânea.

![figura de caixas de pesquisa regulares em estados diferentes ](images/ctrl-search-boxes-image6.png)

Especificações visuais para pesquisa regular.

-   Não use um rótulo; em vez disso, use um prompt opcional. Se os usuários tendem a assumir que a pesquisa é uma pesquisa de arquivo genérico, use o prompt para dar o escopo. Caso contrário, use Type para pesquisar ou uma frase concisa semelhante.

    ![captura de tela do prompt 'tipo a ser pesquisado' ](images/ctrl-search-boxes-image7.png)

    ![captura de tela do prompt 'pesquisar todos os bug'. ](images/ctrl-search-boxes-image8.png)

    Nesses exemplos, breves prompts textuais ajudam os usuários a trabalhar com a Pesquisa.

### <a name="interaction"></a>Interação

-   **No foco de entrada, selecione automaticamente qualquer texto inserido anteriormente.** Isso permite que os usuários insiram uma nova pesquisa digitando ou modifiquem a pesquisa anterior posicionando o a tecla caret usando as teclas de direção.

    ![captura de tela da caixa de pesquisa com texto realçada ](images/ctrl-search-boxes-image9.png)

    Neste exemplo, o texto inserido anteriormente é selecionado no foco de entrada.

-   **Atribua o atalho de teclado para que a caixa Pesquisa seja Ctrl+E.**

### <a name="functionality"></a>Funcionalidade

-   **Suporte à pesquisa instantânea sempre que possível.** Forneça pesquisas regulares e instantâneas se houver cenários em que a pesquisa regular vale o tempo de espera extra.
-   Pesquisas regulares devem retornar resultados relevantes em cinco segundos e a pesquisa instantânea deve retornar resultados dentro de dois segundos. Após esse ponto, a pesquisa pode continuar a preencher resultados menos relevantes ao longo do tempo, desde que o programa seja responsivo e os usuários possam executar outras tarefas. Talvez seja necessário indexar os dados de pesquisa para garantir essa capacidade de resposta.
-   Se você fornecer modos de pesquisa normais e instantâneos, os resultados da pesquisa instantânea deverão ser um subconjunto dos resultados da pesquisa regular.
-   Toda pesquisa é baseada em prefixo (sem Subcadeia ou pesquisa de sufixo). O uso de caracteres curinga à direita é opcional e não afeta os resultados. Se várias palavras forem inseridas, use ou pesquisando.
-   Uma pesquisa bem-sucedida adiciona uma página virtual com os resultados da pesquisa à pilha voltar e à barra de endereços. Várias pesquisas resultam em uma única página virtual, portanto, clicar em voltar sempre retorna a página original.
-   Se necessário para escala, classifique os resultados da pesquisa por relevância.
-   Uma pesquisa em branco retorna a página original.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![Figura de dimensionamento e espaçamento da caixa de pesquisa instantânea ](images/ctrl-search-boxes-image10.png)

Dimensionamento e espaçamento recomendados para pesquisa instantânea.

![figura do espaçamento e dimensionamento da caixa de pesquisa regular ](images/ctrl-search-boxes-image11.png)

Dimensionamento e espaçamento recomendados para pesquisa regular.

## <a name="text"></a>Texto

-   Para as palavras do prompt na caixa de pesquisa, faça dele uma instrução (por exemplo, digite para Pesquisar) ou indique o escopo da pesquisa (por exemplo, pesquise imagens).
-   O texto do prompt deve ser curto. Uma única palavra ou frase curta deve ser suficiente.
-   Use a capitalização com estilo de frase.
-   Não use pontuação final ou reticências.

## <a name="documentation"></a>Documentação

-   Consulte este controle como a caixa de pesquisa. Colocar em maiúscula a letra inicial da primeira palavra; Não coloque em maiúscula a letra inicial da caixa.
-   Consulte os dois tipos de pesquisa como pesquisa instantânea e pesquisa regular. Colocar em maiúscula a letra inicial da pesquisa instantânea; Não coloque em maiúscula a letra inicial da pesquisa regular.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Glossário](glossary.md)
</dt> </dl>

 

 