---
title: Caixas de pesquisa
description: Com uma caixa de pesquisa, os usuários podem localizar rapidamente objetos ou texto específicos em um grande conjunto de dados filtrando ou realçando correspondências.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9d1fca8fdb96b17098cee79fd5b62ecd7ab7531
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103930070"
---
# <a name="search-boxes"></a>Caixas de pesquisa

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com uma caixa de pesquisa, os usuários podem localizar rapidamente objetos ou texto específicos em um grande conjunto de dados filtrando ou realçando correspondências. Não há nenhum controle de pesquisa padrão, mas você deve se esforçar para tornar os recursos de pesquisa do programa consistentes com os do Windows.

Há dois tipos de pesquisas:

-   **Pesquisa instantânea**, onde os resultados são exibidos imediatamente conforme o usuário digita. Nenhum botão precisa ser clicado, portanto, o símbolo de pesquisa de lupa é mostrado como um gráfico, não um botão.

    ![Captura de tela que mostra uma caixa de pesquisa instantânea com um texto explicativo "prompt" apontando na caixa de pesquisa e um texto explicativo "símbolo de pesquisa" apontando para o gráfico de lupa.](images/ctrl-search-boxes-image1.png)

    Uma caixa de pesquisa típica usando A pesquisa instantânea. A pesquisa é executada automaticamente em cada pressionamento de tecla.

-   **Pesquisa regular**, em que uma pesquisa é executada quando o usuário clica no botão de pesquisa. O símbolo de pesquisa de lupa é mostrado em um botão.

    ![captura de tela de uma caixa de pesquisa normal ](images/ctrl-search-boxes-image2.png)

    Uma caixa de pesquisa típica usando A pesquisa regular. Os usuários clicam em um botão para executar a pesquisa.

    Você pode fornecer um ou ambos os tipos de opções de pesquisa para seus usuários.

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **Os objetos específicos são difíceis de encontrar?** Isso pode ocorrer quando:
    -   Há muitos objetos.
    -   Os objetos não estão localizados em um único local. A pesquisa é especialmente útil para localizar objetos em árvores.
    -   Os dados de pesquisa são difíceis de localizar (por exemplo, metadados).
-   **Os usuários precisam localizar texto específico em documentos?**
-   **Seu recurso retorna resultados de pesquisa relevantes dentro de cinco segundos?** Caso contrário, você pode fornecer um recurso de pesquisa, mas usar um design alternativo que fornece comentários visíveis para acomodar pesquisas de execução longa, como uma caixa de diálogo de pesquisa.

## <a name="design-concepts"></a>Conceitos de design

A pesquisa é uma primeira etapa crucial em muitos cenários: os usuários devem encontrar objetos antes de poderem usá-los. Os usuários estão economizando mais e mais objetos em discos rígidos cada vez maiores, mas procurar objetos não é bem dimensionável. A pesquisa deve ser uma parte simples, consistente e confiável da experiência do usuário.

Caixas de pesquisa no Windows:

-   Fazem parte de todas as janelas do Explorer, para que sejam fáceis de localizar e reconhecer.
-   Ter aparência e comportamento consistentes.
-   São eficientes e rápidos, oferecendo resultados instantâneos no modo de pesquisa instantânea.

Uma caixa de pesquisa é usada no Windows nestes locais:

-   Exploradores
-   Experiências (Microsoft Windows Media Player, Galeria de fotos do Windows, Windows Internet Explorer)
-   Menu iniciar (para localizar programas e arquivos recentes)
-   Home page do painel de controle (para localizar itens e tarefas do painel de controle)
-   Ajuda (para encontrar tópicos relevantes da ajuda)

### <a name="look-and-feel"></a>Aparência

A sensação de pesquisa no Windows é significativamente aprimorada com o suporte à pesquisa instantânea. Ter resultados instantâneos faz com que o Windows se sinta mais poderoso e direto.

No Windows Explorer e no Windows do aplicativo, a pesquisa está localizada no canto superior direito se for um ponto de entrada suplementar. Nesse caso, os usuários procuram um mecanismo de pesquisa quando não localizam o que estão procurando na janela. No entanto, se a pesquisa for o ponto de entrada primário, ela será centralizada na parte superior da janela.

O botão Pesquisar está visualmente conectado a uma caixa de pesquisa. Para minimizar o espaço, um [prompt](ctrl-text-boxes.md) opcional é usado dentro de uma caixa de pesquisa em vez de um rótulo. O prompt pode ser uma instrução (por exemplo, digite para Pesquisar) ou indicar o escopo da pesquisa (por exemplo, procurar imagens).

![captura de tela de uma caixa de pesquisa instantânea ](images/ctrl-search-boxes-image3.png)

Sem rótulos e botões separados, a pesquisa instantânea no Windows tem uma aparência leve.

Executar uma pesquisa bem-sucedida cria uma página virtual dos resultados da pesquisa e o adiciona à pilha voltar e à barra de endereços. Os usuários têm várias maneiras de restaurar a página original e desmarcar uma caixa de pesquisa, incluindo clicar em voltar, clicar na página original na barra de endereços, pressionar ESC ou limpar a caixa de pesquisa.

Os usuários também podem simplesmente desmarcar a caixa de pesquisa sem restaurar uma página anterior de resultados. No modo de pesquisa instantânea, um botão Limpar é exibido depois que o usuário começa a digitar; um "x" substitui o símbolo de pesquisa de lupa. Ao focalizar, o "x" Obtém uma aparência de botão e pode ser clicado.

![captura de tela de uma caixa de pesquisa com um ícone ' x ' ](images/ctrl-search-boxes-image4.png)

O usuário pode desmarcar a caixa de pesquisa clicando em "x" na extremidade direita do controle.

No modo de pesquisa normal, o botão Limpar é opcional. Os usuários podem achar útil, por exemplo, se uma pesquisa estiver demorando muito tempo para ser concluída. Os usuários podem clicar no "x" para interromper a pesquisa em andamento. Se uma pesquisa já tiver sido concluída, os usuários poderão clicar no "x" para desmarcar a caixa de pesquisa.

## <a name="guidelines"></a>Diretrizes

### <a name="location"></a>Local

-   Para janelas de aplicativos, localize Pesquisar no canto superior direito.
-   Para janelas pop-up, localize Pesquisar onde quer que seja mais sensato e conveniente.
-   **Exceção:** Se a pesquisa for geralmente a primeira coisa que os usuários fazem em uma janela (o ponto de entrada primário), centralize-o na parte superior da janela.

### <a name="look"></a>Consulte

-   Use os gráficos do botão de pesquisa padrão. Há três versões:
    -   **Somente símbolo de pesquisa de lupa (sem botão ao focalizar).** Use para pesquisa instantânea.
    -   **Símbolo de pesquisa de lupa com botão.** Use quando o botão precisa ser clicado para iniciar a pesquisa.
    -   **Símbolo de pesquisa de lupa com botão e seta suspensa.** Adicione uma seta suspensa quando os usuários puderem alterar o escopo ou quando outras configurações estiverem disponíveis.
        -   Para pesquisa instantânea, use uma seta suspensa somente e mostre um botão ao focalizar.
        -   Para pesquisa regular, mostre a seta suspensa em um botão.

![Figura de caixas de pesquisa instantâneas em Estados diferentes ](images/ctrl-search-boxes-image5.png)

Especificações visuais para pesquisa instantânea.

![Figura de caixas de pesquisa regulares em Estados diferentes ](images/ctrl-search-boxes-image6.png)

Especificações visuais para pesquisa regular.

-   Não usar um rótulo; em vez disso, use um prompt opcional. Se os usuários tendem a supor que a pesquisa é uma pesquisa de arquivo genérica, use o prompt para dar o escopo. Caso contrário, use o tipo para pesquisar ou uma frase concisa semelhante.

    ![captura de tela do prompt ' tipo para pesquisa ' ](images/ctrl-search-boxes-image7.png)

    ![captura de tela do prompt ' Pesquisar todos os gadgets ' ](images/ctrl-search-boxes-image8.png)

    Nestes exemplos, os prompts de texto breves ajudam os usuários a trabalhar com a pesquisa.

### <a name="interaction"></a>Interação

-   **No foco de entrada, selecione automaticamente qualquer texto inserido anteriormente.** Isso permite que os usuários insiram uma nova pesquisa digitando ou modifiquem a pesquisa anterior posicionando o cursor usando as teclas de direção.

    ![captura de tela da caixa de pesquisa com texto realçado ](images/ctrl-search-boxes-image9.png)

    Neste exemplo, o texto inserido anteriormente é selecionado no foco de entrada.

-   **Atribua o atalho de teclado para que a caixa de pesquisa seja Ctrl + E.**

### <a name="functionality"></a>Funcionalidade

-   **Dê suporte à pesquisa instantânea sempre que possível.** Forneça pesquisas regulares e instantâneas se houver cenários em que a pesquisa regular vale o tempo de espera extra.
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

 

 