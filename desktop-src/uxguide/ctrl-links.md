---
title: Links
description: Com um link, os usuários podem navegar para outra página, janela ou tópico de Ajuda; exibir uma definição; iniciar um comando; ou escolha uma opção.
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 161313008612d04b5009942f82f662888d1ffd35
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524251"
---
# <a name="links"></a>Links

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com um *link*, os usuários podem navegar para outra página, janela ou tópico de Ajuda; exibir uma definição; iniciar um comando; ou escolha uma opção. Um link é um texto ou um gráfico que indica que ele pode ser clicado, normalmente sendo exibido usando as cores do sistema de link visitados [ou não visitados.](vis-color.md) Tradicionalmente, os links também são sublinhados, mas essa abordagem geralmente é desnecessária e fica fora de favor para reduzir a desorganização visual.

Quando os usuários passarem o mouse sobre um link, o texto do link aparecerá como sublinhado (se ainda não estivesse) e a forma do ponteiro mudar para uma [mão](inter-mouse.md).

Um link de texto é o controle clicável de peso mais leve e geralmente é usado para reduzir a complexidade visual de um design.

> [!Note]  
> Diretrizes relacionadas a [links de comando](ctrl-command-links.md) e [layout](vis-layout.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **É o link usado para navegar para outra página, janela ou tópico de Ajuda; exibir uma definição; iniciar um comando; ou escolher uma opção?** Se não, use outro controle.
-   **Um botão de comando seria uma opção melhor?** Use um [botão de comando](ctrl-command-buttons.md) se:
    -   O controle inicia uma ação imediata, incluindo a exibição de uma janela, e esse comando está relacionado à finalidade principal da janela.
    -   Uma janela é exibida para coletar entradas ou fazer escolhas, mesmo se for para um comando secundário.
    -   O rótulo é curto, consistindo em quatro ou menos palavras, evitando assim a aparência complicada de botões longos.
    -   O comando não é em linha.
    -   O controle aparece dentro de um grupo de outros botões de comando relacionados.
    -   A ação é destrutiva ou irreversível. Como os usuários associam links à navegação (e a capacidade de fazer o back-out), os links não são apropriados para comandos com consequências significativas.
    -   Da mesma forma, em um [assistente](win-wizards.md) [ou fluxo de tarefas,](glossary.md)o comando representa o compromisso. Nesses janelas, os botões de comando sugerem compromisso, enquanto os links sugerem a navegação para a próxima etapa.

## <a name="design-concepts"></a>Conceitos de design

**Tornando os links reconhecíveis**

Os links [não têm acessível,](glossary.md)o que significa que suas propriedades visuais não **sugerem** como eles são usados e são compreendidos apenas por meio da experiência. Links sem um sublinhado e cores do sistema de link aparecem como texto normal; a única maneira de determinar seu comportamento é com sua apresentação, seu contexto ou posicionando o ponteiro sobre eles.

Surpreendentemente, essa falta de recursos geralmente é uma motivação para usar links porque eles parecem tão leves, reduzindo assim a complexidade visual de um design. Os links eliminam o quadro visualmente pesado usado por [botões de comando](ctrl-command-buttons.md) e borda usados por outros controles. Por exemplo, embora você possa usar botões de comando para tornar os comandos primários óbvios, você pode escolher links para comandos secundários para des enfatizar-los.

O desafio é, então, manter pistas visuais suficientes para que os usuários possam reconhecer os links. A diretriz fundamental é que os usuários devem ser capazes de reconhecer links por inspeção visual sozinhos, eles não devem ter que passar o mouse sobre um objeto ou clicar nele para determinar se ele é **um link**.

Os usuários poderão reconhecer um link somente por inspeção visual se o link usar as cores do sistema de [link](vis-color.md) e pelo menos uma das seguintes pistas visuais:

-   Texto sublinhado.
-   Um gráfico ou marcador, como com o texto [com o padrão de link de](#usage-patterns) ícone.
-   Posicionamento em uma navegação padrão, opção ou [](glossary.md) local de comando, como a área de conteúdo de uma janela ou em uma barra de navegação, barra de menus, barra de ferramentas ou rodapé da página.

Os usuários também podem reconhecer um link por inspeção visual com as seguintes pistas visuais, mas essas pistas não são suficientes por si só:

-   Texto que sugere clicar, como um comando que começa com um verbo imperativo, como Mostrar, Imprimir, Copiar ou Excluir.
-   Posicionamento dentro de um bloco de texto normal.

É claro que os usuários sempre podem determinar um link por meio da interação passando o mouse ou clicando. Se a descoberta de um link não for necessária para tarefas significativas, você poderá des enfatizar esses links.

![captura de tela de rótulos cinzas na tela de fundo preta ](images/ctrl-links-image1.png)

Neste exemplo, Entre em contato conosco, termos de uso, marcas comerciais e política de privacidade são links. Eles são intencionalmente des enfatizados porque não são necessários para nenhuma tarefa importante. As únicas pistas de que eles são links são que eles têm um ponteiro do mouse ao passar o mouse e estão posicionados em uma área de navegação padrão na parte inferior da janela.

**Tornando os links específicos, relevantes e previsíveis**

O texto do link deve indicar o resultado do clique no link.

Links específicos são mais atraentes para os usuários do que links gerais, **portanto, use rótulos** de link que dão informações descritivas específicas sobre o resultado do clique no link . No entanto, certifique-se de que o texto do link não seja tão específico que seja enganoso e desacente o uso adequado.

Links concisos têm maior probabilidade de serem lidos do que links detalhados. **Elimine texto e detalhes desnecessários.** Os rótulos de link não devem ser abrangentes.

Para avaliar o texto do link:

-   Certifique-se de que o texto do link reflita os cenários aos que o link dá suporte.
-   Certifique-se de que os resultados do link sejam previsíveis. Os usuários não devem se surpresa com os resultados.

**Se você fizer apenas duas coisas...**

1. Tornar os links descobertos somente pela inspeção visual. Os usuários não devem ter que interagir com seu programa para encontrar links.

2. Use links que dão informações descritivas específicas sobre o resultado do clique no link, usando o máximo de texto necessário. Os usuários devem ser capazes de prever com precisão o resultado de um link de seu texto de link e [infotip opcional](ctrl-tooltips-and-infotips.md).

## <a name="usage-patterns"></a>Padrões de uso

Os links têm vários padrões funcionais:



|    Uso                  |    Exemplo   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Links de navegação**<br/> Um link usado para navegar para outra página ou janela. <br/>                                                      | Clicar no link navega no local para outra página, como em uma janela ou assistente do navegador; ou exibe uma nova janela. Ao contrário dos links de tarefa, a navegação não inicia uma tarefa, mas simplesmente navega para outro local ou continua com uma tarefa já em andamento. A navegação implica em segurança porque o usuário sempre pode voltar.<br/> Notícias<br/> Neste exemplo, clicar no link navega para a página Títulos de notícias.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Links de tarefa**<br/> Um link usado para iniciar um novo comando. <br/>                                                                        | Clicar no link executa um comando imediatamente ou exibe uma caixa de diálogo ou página para coletar mais entradas. Ao contrário dos links de navegação, os links de tarefa iniciam uma nova tarefa em vez de continuar com uma tarefa existente. As tarefas não implicam em segurançausuários não podem reverter para o estado anterior com um comando Voltar. Os links de tarefa são chamados para evitar confusão com [links de comando](ctrl-command-links.md). <br/> Logon<br/> Neste exemplo, clicar no link inicia um comando de logon.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Links de ajuda**<br/> Um link de texto usado para exibir um tópico da Ajuda. <br/>                                                                     | Clicar no link exibe um artigo de Ajuda em uma janela separada.<br/> O que é uma senha forte?<br/> Neste exemplo, clicar no link exibe uma janela de Ajuda com o tópico determinado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Links de definição**<br/> um link de texto usado para exibir uma definição em uma infotip quando o usuário clica ou fica sobre o link. <br/> | esse padrão é útil para definir termos que podem não ser conhecidos para seus usuários sem adicionar confusão de tela.<br/> ![captura de tela da infotip exibida por foco do mouse ](images/ctrl-links-image2.png)<br/> Neste exemplo, a definição de infotip é exibida. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Links de menu**<br/> um conjunto de links de tarefa usado para criar um menu. <br/>                                                                    | como o contexto do menu indica um conjunto de links, o texto geralmente não é sublinhado (exceto ao passar o mouse) e pode não usar as cores do sistema de link.<br/> ![captura de tela de um conjunto de links ](images/ctrl-links-image3.png)<br/> Neste exemplo, um conjunto de links cria um menu.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Links de opção**<br/> uma opção selecionada ou seu espaço reservado, em que clicar no link invoca um comando para alterar essa opção.<br/>       | ao contrário dos links de texto regulares, o link altera seu texto para refletir a opção selecionada no momento e sempre é desenhado usando a cor do link não selecionada. <br/> ![captura de tela de uma regra no assistente de regras do Outlook ](images/ctrl-links-image4.png)<br/> O exemplo à esquerda mostra uma regra do assistente de regras do Microsoft Outlook com opções de espaço reservado. depois que os usuários clicam nos links e selecionam algumas opções, o exemplo à direita atualiza o texto do link para mostrar os resultados.<br/> usar links de opção é particularmente adequado se as opções têm um formato de variável. <br/> ![captura de tela de uma regra modificada no assistente de regras ](images/ctrl-links-image5.png)<br/> o exemplo à direita mostra que as regras do Outlook têm um formato variável. <br/> ![captura de tela de como o texto muda para a lista de listas listadas ](images/ctrl-links-image6.png)<br/> O exemplo à esquerda mostra um link de opção. Ele se torna uma lista lista listada quando selecionada, conforme mostrado à direita.<br/> |



 

Os links também têm vários padrões de apresentação:



|    Uso                                 |    Exemplo                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Links de texto sem-texto**<br/> consistem apenas em texto. <br/>                                      | essa apresentação é a mais flexível porque pode ser usada em qualquer lugar, incluindo [em linha.](glossary.md)<br/> ![captura de tela do texto do link azul ](images/ctrl-links-image7.png)<br/> Neste exemplo, a cor do texto identifica claramente um link em linha.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Texto com links de ícone**<br/> texto com um ícone anterior que indica sua função.<br/> | como o gráfico fornece uma indicação visual adicional de um link, é mais fácil reconhecer como um link do que um link de texto sem-texto que não está sublinhado. esse padrão normalmente usa um ícone de 16 x 16 pixels.<br/> ![captura de tela da lista de quatro links com ícones ](images/ctrl-links-image8.png)<br/> neste exemplo, os ícones fornecem uma indicação visual adicional de um link.<br/> ![captura de tela do comando play com triângulo pequeno ](images/ctrl-links-image9.png)<br/> Neste exemplo, o símbolo de Reprodução triangular padrão indica que este texto é um comando.<br/>                                                                                                                                     |
| **Links somente gráficos**<br/> consistem apenas em um gráfico.<br/>                               | devido à falta de um link de texto, não há nenhuma cor de link ou sublinhado para indicar o link. esses links dependem do design gráfico para sugerir um clique ou texto dentro do gráfico que sugere uma ação quando os usuários clicam. Às vezes, os links somente gráficos têm um efeito sobre o mouse para indicar o link. essa abordagem ajuda, mas não é descoberta apenas pela inspeção visual.<br/> ![captura de tela do ícone com o ponteiro do mouse link-select ](images/ctrl-links-image10.png)<br/> Neste exemplo, o link não pode ser descoberto apenas pela inspeção visual.<br/> **Devido a seus possíveis problemas de reconhecimento e localização, links somente gráficos não são recomendados como a única maneira de executar uma tarefa.** <br/> |



 

## <a name="guidelines"></a>Diretrizes

### <a name="interaction"></a>Interação

-   **Exibir um ponteiro ocupado se o resultado do clique em um link não for instantâneo.** Sem comentários, os usuários podem supor que o clique não aconteceu e clicar novamente.

### <a name="color"></a>Color

-   **Use as cores do sistema de tema ou link para links visitados e não visitados.** O significado dessas cores é consistente em todos os programas. Se, por algum motivo, os usuários não gostarem dessas cores (talvez por motivos de acessibilidade), eles mesmos poderão alterá-las.
-   **Para links de navegação, use cores diferentes para links visitados e não visitados.** Mantenha o histórico de links visitados somente durante a instância do programa. A cor visitada é importante para indicar onde os usuários já foram, impedindo que eles revisitem involutivamente as mesmas páginas repetidamente.
-   **Para outros tipos de links, não use a cor do link visitado.** Não há valor suficiente para identificar comandos "visitados", por exemplo.
-   **Não colora o texto que não é um link porque os usuários podem presumir que ele é um link.** Use negrito ou um tom de cinza em que, de outra forma, você usaria texto colorido.
-   **Exceção:** você pode usar texto colorido se todos os links estão sublinhados ou colocados em locais de navegação ou comando padrão.

    **Incorreto:**

    ![captura de tela da mensagem de plano de energia com texto azul ](images/ctrl-links-image11.png)

    Neste exemplo, o texto azul é usado incorretamente para texto que não é um link.

-   **Use cores da plano de fundo que contrastam com as cores do link.** A [cor do sistema de](vis-color.md) janelas é sempre uma boa opção.

    **Incorreto:**

    ![captura de tela do texto do link azul na tela de fundo azul ](images/ctrl-links-image12.png)

    Neste exemplo, a cor da tela de fundo fornece um contraste ruim com a cor do link.

### <a name="underlining"></a>Sublinhando

-   **Para links necessários para executar uma tarefa primária, forneça dicas visuais para que os usuários possam reconhecer links somente por inspeção visual.** Essas pistas incluem sublinhamento, gráficos ou marcadores e locais de link padrão. Os usuários não devem ter que passar o mouse sobre um objeto ou tentar clicar nele para determinar se ele é um link. Use texto sublinhado se o link não for óbvio de seu contexto.
-   **Não sublinha o texto que não é um link porque os usuários podem presumir que se trata de um link.** Use itálico em que você usaria texto sublinhado. Reserve o sublinhado somente para links.
-   **Ao imprimir, não imprima sublinhados ou cores de link.** Links impressos não têm valor e são potencialmente confusos.

### <a name="text-with-icon-links"></a>Texto com links de ícone

-   **Use o ícone de seta somente para links de comando.** Os links regulares não devem usar o ícone de seta, a menos que eles sejam usados como um substituto para [links de comando](ctrl-command-links.md) no Windows XP.
-   **Coloque o ícone à esquerda do texto.** O ícone precisa levar ao texto visualmente.

**Correto:**

![captura de tela do ícone anterior ao texto ](images/ctrl-links-image13.png)

**Incorreto:**

![captura de tela do ícone após o texto ](images/ctrl-links-image14.png)

No exemplo incorreto, o ícone não leva ao texto.

-   **Faça com que o resultado de clicar no ícone seja o mesmo que clicar no texto.** Fazer de outra forma seria inesperado e confuso.

### <a name="graphics-only-links"></a>Links somente gráficos

-   **Não use links somente gráficos.** Os usuários têm dificuldade em reconhecê-los como links e qualquer texto dentro do gráfico (usado para indicar sua ação quando clicado) cria um problema de localização.

### <a name="navigation-links"></a>Links de navegação

-   **Certifique-se de que os links de navegação não exigem compromisso.** Os usuários sempre devem ser capazes de retornar ao estado inicial, seja usando Voltar para navegação inplace ou Cancelar para fechar uma nova janela.
-   **Vincular a conteúdo específico em vez de conteúdo geral.** Por exemplo, é melhor vincular à seção relevante de um documento do que vincular ao início.
-   **Use um link somente se o material vinculado for relevante, útil e não redundante.** Use a contenção em links de navegação não os use apenas porque você pode.
-   **Se um link navegar para um site externo, coloque a URL** na infotip para que os usuários possam determinar o destino do link.
-   **Vincule apenas a primeira ocorrência do texto do link.** Links redundantes são desnecessários e podem dificultar a leitura do texto.

    **Correto:**

    A pasta Imagens facilita o compartilhamento de suas imagens. Você pode usar as tarefas em Imagens para enviar suas imagens por email ou publicá-las em um local seguro e privado na Web. Você também pode imprimir suas imagens diretamente da pasta Imagens.

    **Incorreto:**

    A pasta Imagens facilita o compartilhamento de suas imagens. Você pode usar as tarefas em imagens para enviar suas imagens por email ou publicá-las em um local seguro e privado na Web. Você também pode imprimir suas imagens diretamente da pasta imagens.

    No exemplo correto, somente a primeira ocorrência do texto relevante é vinculada.

    **Exceções:**

    -   **Se uma instrução tiver um link, coloque o link na instrução.**

        Usar senhas fortes é muito importante. Para obter mais informações, consulte Senhas seguras.

        Neste exemplo, o link está na instrução, em vez da primeira ocorrência.

    -   **Vincular a ocorrências posteriores se elas estiverem longe da primeira.** Por exemplo, você pode vincular de forma redundante em seções diferentes dentro de um tópico da ajuda.

### <a name="task-links"></a>Links de tarefas

-   **Use links de tarefas para comandos que não são destrutivos ou são facilmente reversívels.** Como os usuários associam links com navegação (e a capacidade de fazer backup), os links não são apropriados para comandos com consequências significativas. Comandos que exibem uma caixa de diálogo ou uma confirmação são uma boa opção.

    **Correto:**

    Iniciar

    Stop

    **Incorreto:**

    Excluir arquivo

    No exemplo incorreto, o comando é destrutivo.

### <a name="menu-links"></a>Links de menu

-   **Agrupe os links de tarefas e de navegação relacionados em menus.** Um menu de links relacionados colocados em uma navegação padrão ou local de comando facilita a localização e a compreensão dos links do que quando eles são colocados separadamente.
-   **Para menus dependentes de seleção, remova os links de menu que não se aplicam.** Não os desabilite. Isso elimina a desordem e os usuários não perderão links que exijam seleção.
-   **Para menus independentes de seleção, desabilite os links de menu que não se aplicam.** Não remova-os. Isso torna os menus mais estáveis e esses links são mais fáceis de localizar.

    ![captura de tela da caixa de diálogo com comando de menu esmaecido ](images/ctrl-links-image15.png)

    Neste exemplo de Windows Update, uma atualização está sendo executada, portanto, o comando verificar atualizações está desabilitado em vez de removido.

### <a name="link-infotips"></a>Infotips do link

-   Se um link exigir mais explicações, **forneça a explicação em uma explicação suplementar em um controle de texto separado ou um** [InfoTip](ctrl-tooltips-and-infotips.md), mas não ambos. Use frases completas e pontuação final. O fornecimento de ambos é desnecessário se o texto for o mesmo e confuso se o texto for diferente.

    ![captura de tela de link com texto suplementar ](images/ctrl-links-image16.png)

    Neste exemplo, uma explicação suplementar fornece mais informações sobre o link.

    ![captura de tela de link com InfoTip ](images/ctrl-links-image17.png)

    Neste exemplo, um InfoTip fornece mais informações.

-   **Não forneça uma InfoTip que seja meramente uma recondição do texto do link.**

    **Incorreto:**

    ![captura de tela de link com InfoTip redundante ](images/ctrl-links-image18.png)

    Neste exemplo, os riscos de infotip desagradáveis os usuários pela sua repetição.

## <a name="text"></a>Text

-   Não atribua uma [chave de acesso](glossary.md). Os links são acessados usando a tecla Tab.
-   **Use links que forneçam informações descritivas específicas sobre o resultado de clicar no link**, usando o máximo de texto necessário. O texto do link deve indicar o resultado de um clique no link. **Os usuários devem ser capazes de prever com precisão o resultado de um link de seu texto de link e de infotip opcional.**

    **Incorreto:**

    ![captura de tela de um link de aviso de notificação de segurança ](images/ctrl-links-image19.png)

    Neste exemplo, embora o link pareça importante, seu rótulo é muito geral. É mais provável que os usuários cliquem em um link mais específico.

-   Para links embutidos:
    -   Preserve as letras maiúsculas e a Pontuação do texto.
    -   Não inclua Pontuação final no link, a menos que o texto seja uma pergunta.
    -   Link na parte mais relevante do texto e escolha o texto do link que seja grande o suficiente para ser fácil de clicar.

        **Correto:**

        Vá para um grupo de notícias.

        **Incorreto:**

        Vá para um grupo de notícias.

        Nesses exemplos, "Go" não é a parte mais relevante do texto e não é grande o suficiente para fazer um bom clique de destino, enquanto "newsgroup" é.

    -   **Evite colocar dois links embutidos diferentes ao lado um do outro.** É provável que os usuários acreditem que são um único link.

        **Incorreto:**

        Para obter mais informações, consulte Diretrizes de UX.

        Neste exemplo, "UX" e "diretrizes" são dois links diferentes.

-   Para links independentes (não embutido):
    -   Use [a capitalização no estilo de frase](glossary.md).
    -   Não use pontuação final, a menos que o link seja uma pergunta.
    -   Use todo o texto como o link.
-   Use os links que são claramente diferenciados dos outros links na tela. Os usuários devem ser capazes de prever e diferenciar com precisão os destinos de link.

    **Incorreto:**

    Encontrar software antivírus

    Obter software antivírus

    **Correto:**

    Como saber se o software antivírus está instalado

    Instalar software antivírus

    No exemplo incorreto, a distinção entre os dois links não é clara.

-   Não adicionar clique ou clique aqui no texto do link. Não é necessário porque um link implica clicar. Além disso, clique aqui e aqui só não transmite nenhuma informação sobre o link quando lido por um leitor de tela.

    **Incorreto:**

    Clique aqui para obter a descrição.

    **Correto:**

    Descrição

    Nos exemplos incorretos, "clique aqui" vai sem dizer e não transmite nenhuma informação sobre o link.

**Links de navegação**

-   **Inicie o link com um substantivo e descreva claramente onde clicar no link vai.** Não use pontuação final. Na ocasião, talvez seja necessário iniciar links de navegação com um verbo, mas não usar verbos que reiteram a navegação já implícita pelo fato de vincular, como exibir, abrir ou ir para.
-   **Apresente um link de navegação como uma URL se ele navegar para uma página da Web e você espera que os usuários de destino relembrem a URL e a digitem em um navegador.** Se possível, crie essas URLs de forma que sejam curtas e fáceis de lembrar.
-   **Se o link incluir uma URL para um site que começa com "www", omita o nome do protocolo https://e use texto em minúsculas.**

    **Incorreto:**

    https://www.microsoft.com

    `www.microsoft.com`

    **Correto:**

    microsoft.com

    Nos exemplos incorretos, "https://" e "www" vão sem dizer.

**Links de tarefas**

-   **Inicie o link com um verbo imperativo e descreva claramente a tarefa que o link executa.** Não use pontuação final.
-   **Termine o link com reellipse se o comando precisar de informações adicionais (incluindo uma confirmação) para a conclusão bem-sucedida.** Não use reellipses quando a conclusão bem-sucedida da tarefa for exibir outra janela somente quando informações adicionais são necessárias para executar a tarefa.

    Imprimir...

    Neste exemplo, a Imprime... O link de comando exibe uma caixa de diálogo Imprimir para coletar mais informações.

    Impressão

    Por outro lado, neste exemplo, um link de comando Imprimir imprime uma única cópia de um documento na impressora padrão sem nenhuma interação do usuário.

    **O uso adequado de reellipses** é importante para indicar que os usuários podem fazer outras escolhas antes de executar a tarefa ou podem cancelar totalmente a tarefa . A indicação visual oferecida por reellipses permite que os usuários explorem seu software sem medo.

-   **Se necessário, termine um link de tarefa com "now" para diferenciá-lo de um link de navegação.**

    Baixar arquivos

    Baixar arquivos agora

    Neste exemplo, "Baixar arquivos" navega até uma página para baixar arquivos, enquanto "Baixar arquivos agora" realmente executa o comando .

**Links de ajuda**

Para ver diretrizes e exemplos, consulte [Ajuda](winenv-help.md).

**Dicas de informações de link**

-   Use frases completas e pontuação final.

Para obter mais diretrizes e exemplos, consulte [Dicas de ferramenta e Infotips](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Documentação

Ao se referir a links:

-   Use o texto exato do link, incluindo sua capitalização, mas não inclua as reellipses.
-   Para descrever a interação do usuário, use clique.
-   Quando possível, forja o texto do link usando texto em negrito. Caso contrário, coloque o texto do link entre aspas somente se necessário para evitar confusão.

Exemplo: para iniciar a verificação, clique **em Examinar um computador.**

 

