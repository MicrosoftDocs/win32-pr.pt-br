---
title: Links
description: Com um link, os usuários podem navegar para outra página, janela ou tópico da ajuda; exibir uma definição; iniciar um comando; ou escolha uma opção.
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 521f96146de535210d79814b375499ea34399179
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104571580"
---
# <a name="links"></a>Links

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com um *link*, os usuários podem navegar para outra página, janela ou tópico da ajuda; exibir uma definição; iniciar um comando; ou escolha uma opção. Um link é um texto ou um elemento gráfico que indica que ele pode ser clicado, normalmente por ser exibido usando as cores do [sistema de link](vis-color.md)visitado ou não visitado. Tradicionalmente, os links são sublinhados também, mas essa abordagem geralmente é desnecessária e está se saindo de preferir para reduzir a desordem Visual.

Quando os usuários focalizam um link, o texto do link é exibido como sublinhado (se ainda não tiver sido) e a forma do ponteiro muda para uma [mão](inter-mouse.md).

Um link de texto é o controle clicável de peso mais leve e geralmente é usado para reduzir a complexidade visual de um design.

> [!Note]  
> As diretrizes relacionadas a [links de comando](ctrl-command-links.md) e [layout](vis-layout.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **É o link usado para navegar para outra página, janela ou tópico da ajuda; exibir uma definição; iniciar um comando; ou escolher uma opção?** Se não, use outro controle.
-   **Um botão de comando seria uma opção melhor?** Use um [botão de comando](ctrl-command-buttons.md) se:
    -   O controle inicia uma ação imediata, incluindo a exibição de uma janela, e esse comando se relaciona com a finalidade principal da janela.
    -   Uma janela é exibida para reunir entrada ou fazer escolhas, mesmo se for um comando secundário.
    -   O rótulo é curto, consistindo em quatro ou menos palavras, evitando assim a aparência estranha de botões longos.
    -   O comando não está embutido.
    -   O controle aparece dentro de um grupo de outros botões de comando relacionados.
    -   A ação é destrutiva ou irreversível. Como os usuários associam links com navegação (e a capacidade de fazer backup), os links não são apropriados para comandos com consequências significativas.
    -   Da mesma forma, em um [Assistente](win-wizards.md) ou [fluxo de tarefas](glossary.md), o comando representa o compromisso. Em tais janelas, os botões de comando sugerem o compromisso, enquanto os links sugerem navegar para a próxima etapa.

## <a name="design-concepts"></a>Conceitos de design

**Tornando os links reconhecíveis**

Os links não têm [preços](glossary.md), o que significa que **suas propriedades visuais não sugerem como eles são usados** e são compreendidos apenas por meio da experiência. Os links sem um sublinhado e vincular as cores do sistema aparecem como texto normal; a única maneira de verificar seu comportamento é de sua apresentação, de seu contexto ou do posicionamento do ponteiro sobre eles.

Surpreendentemente, essa falta de preços geralmente é uma motivação para o uso de links porque eles aparecem tão leves, reduzindo assim a complexidade visual de um design. Os links eliminam o quadro visualmente pesado usado pelos [botões de comando](ctrl-command-buttons.md) e pela borda usada por outros controles. Por exemplo, embora você possa usar botões de comando para tornar os comandos primários óbvios, você pode escolher links para comandos secundários para retorná-los.

O desafio é então manter dicas visuais suficientes para que os usuários possam reconhecer os links. A diretriz fundamental é **que os usuários devem ser capazes de reconhecer links pela inspeção visual sozinho, eles não devem ter que passar o mouse sobre um objeto ou clicar nele para determinar se ele é um link**.

Os usuários poderão reconhecer um link por inspeção visual apenas se o link usar as [cores do sistema de link](vis-color.md) e pelo menos uma das seguintes pistas visuais:

-   Texto sublinhado.
-   Um gráfico ou marcador, como com o padrão de [link texto com ícone](#usage-patterns) .
-   Posicionamento em um local de navegação, opção ou comando padrão, como a [área de conteúdo](glossary.md) de uma janela, ou em uma barra de navegação, barra de menus, barra de ferramentas ou rodapé de página.

Os usuários também podem reconhecer um link por inspeção visual com as pistas visuais a seguir, mas essas pistas não são suficientes por conta própria:

-   Texto que sugere um clique, como um comando que começa com um verbo imperativo como mostrar, imprimir, copiar ou excluir.
-   Posicionamento dentro de um bloco de texto normal.

É claro que os usuários sempre podem determinar um link por meio de interação, passando o mouse ou clicando. Se a descoberta de um link não for necessária para nenhuma tarefa significativa, você poderá realçar esses links.

![captura de tela de rótulos em cinza no plano de fundo preto ](images/ctrl-links-image1.png)

Neste exemplo, fale conosco, termos de uso, marcas registradas e política de privacidade são links. Eles são intencionalmente reenfatizados porque não são necessários para tarefas importantes. As únicas pistas de que eles são links são que eles têm um ponteiro do mouse sobre o foco e são posicionados em uma área de navegação padrão na parte inferior da janela.

**Tornando os links específicos, relevantes e previsíveis**

O texto do link deve indicar o resultado de um clique no link.

Links específicos são mais atraentes para usuários do que links gerais, portanto, **use rótulos de link que forneçam informações descritivas específicas sobre o resultado de clicar no link**. No entanto, verifique se o texto do link não é tão específico que é enganoso e não incentiva o uso adequado.

Os links concisos são mais prováveis de serem lidos do que os links detalhados. **Elimine o texto e os detalhes desnecessários.** Rótulos de link não precisam ser abrangentes.

Para avaliar o texto do link:

-   Verifique se o texto do link reflete os cenários aos quais o link dá suporte.
-   Verifique se os resultados do link são previsíveis. Os usuários não devem ficar surpresos com os resultados.

**Se você fizer apenas duas coisas...**

1. Torne os links detectáveis apenas pela inspeção visual. Os usuários não devem ter que interagir com seu programa para encontrar links.

2. Use links que forneçam informações descritivas específicas sobre o resultado de clicar no link, usando o máximo de texto necessário. Os usuários devem ser capazes de prever com precisão o resultado de um link de seu texto de link e de [InfoTip](ctrl-tooltips-and-infotips.md)opcional.

## <a name="usage-patterns"></a>Padrões de uso

Os links têm vários padrões funcionais:



|                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Links de navegação**<br/> Um link usado para navegar para outra página ou janela. <br/>                                                      | Clicar no link navega para outra página, como em uma janela do navegador ou assistente; ou exibe uma nova janela. Em contraste com os links de tarefas, a navegação não inicia uma tarefa, mas simplesmente navega para outro local ou prossegue com uma tarefa já em andamento. A navegação implica em segurança porque o usuário sempre pode voltar.<br/> Manchetes de notícias<br/> Neste exemplo, clicar no link navega até a página manchetes de notícias.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Links de tarefas**<br/> Um link usado para iniciar um novo comando. <br/>                                                                        | Clicar no link executa imediatamente um comando ou exibe uma caixa de diálogo ou página para coletar mais entradas. Em contraste com os links de navegação, os links de tarefas iniciam uma nova tarefa em vez de continuar com uma tarefa existente. As tarefas não sugerem que safetyusers não pode reverter para o estado anterior com um comando voltar. Os links de tarefas são chamados para evitar confusão com [links de comando](ctrl-command-links.md). <br/> Logon<br/> Neste exemplo, clicar no link inicia um comando de logon.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Links de ajuda**<br/> Um link de texto usado para exibir um tópico da ajuda. <br/>                                                                     | Clicar no link exibe um artigo de ajuda em uma janela separada.<br/> O que é uma senha forte?<br/> Neste exemplo, clicar no link exibe uma janela de ajuda com o tópico fornecido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Links de definição**<br/> um link de texto usado para exibir uma definição em um InfoTip quando o usuário clica ou passa o mouse sobre o link. <br/> | Esse padrão é útil para definir termos que podem não ser conhecidos por seus usuários sem adicionar aglomeração de tela.<br/> ![captura de tela de infotip exibida pelo mouse focalizado ](images/ctrl-links-image2.png)<br/> Neste exemplo, a definição InfoTip é exibida. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Links de menu**<br/> um conjunto de links de tarefas usado para criar um menu. <br/>                                                                    | como o contexto do menu indica um conjunto de links, o texto geralmente não é sublinhado (exceto no Hover) e pode não usar as cores do sistema de link.<br/> ![captura de tela de um conjunto de links ](images/ctrl-links-image3.png)<br/> Neste exemplo, um conjunto de links cria um menu.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Links de opção**<br/> uma opção selecionada ou seu espaço reservado, em que clicar no link invoca um comando para alterar essa opção.<br/>       | ao contrário de links de texto regulares, o link altera seu texto para refletir a opção selecionada no momento e é sempre desenhado usando a cor do link não visitado. <br/> ![captura de tela de uma regra no assistente de regras do Outlook ](images/ctrl-links-image4.png)<br/> o exemplo à esquerda mostra uma regra do assistente de regras do Microsoft Outlook com opções de espaço reservado. Depois que os usuários clicarem nos links e selecionarem algumas opções, o exemplo à direita atualizará o texto do link para mostrar os resultados.<br/> o uso de links de opção é particularmente adequado se as opções tiverem um formato de variável. <br/> ![captura de tela de uma regra modificada no assistente de regras ](images/ctrl-links-image5.png)<br/> o exemplo à direita mostra que as regras do Outlook têm um formato de variável. <br/> ![captura de tela de como o texto muda para a lista suspensa ](images/ctrl-links-image6.png)<br/> O exemplo à esquerda mostra um link de opção. Ela se torna uma lista suspensa quando selecionada, conforme mostrado à direita.<br/> |



 

Os links também têm vários padrões de apresentação:



|                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Links de texto sem formatação**<br/> consiste apenas em texto. <br/>                                      | Esta apresentação é a mais flexível porque pode ser usada em qualquer lugar, incluindo em [linha](glossary.md).<br/> ![captura de tela do texto do link azul ](images/ctrl-links-image7.png)<br/> Neste exemplo, a cor do texto identifica claramente um link embutido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Texto com links de ícone**<br/> texto com um ícone anterior que indica sua função.<br/> | como o elemento gráfico fornece uma indicação visual adicional de um link, é mais fácil reconhecer como um link do que um link de texto sem formatação que não está sublinhado. Esse padrão geralmente usa um ícone de 16x16 pixels.<br/> ![captura de tela da lista de quatro links com ícones ](images/ctrl-links-image8.png)<br/> Neste exemplo, os ícones fornecem uma indicação visual adicional de um link.<br/> ![captura de tela do comando Play com triângulo pequeno ](images/ctrl-links-image9.png)<br/> Neste exemplo, o símbolo de reprodução triangular padrão indica que esse texto é um comando.<br/>                                                                                                                                     |
| **Links somente para gráficos**<br/> consiste apenas em um elemento gráfico.<br/>                               | devido à falta de um link de texto, não há nenhuma cor de link ou sublinhado para indicar o link. Esses links dependem do design gráfico para sugerir um clique ou texto dentro do gráfico que sugere uma ação quando os usuários clicam. os links somente de elementos gráficos às vezes têm um mouse sobre o efeito para indicar o link. Essa abordagem ajuda, mas não é detectável apenas pela inspeção visual.<br/> ![captura de tela do ícone com link-Selecionar ponteiro do mouse ](images/ctrl-links-image10.png)<br/> Neste exemplo, o link não é detectável pela inspeção visual sozinha.<br/> **Devido a seus problemas potenciais de reconhecimento e localização, os links somente gráficos não são recomendados como a única maneira de executar uma tarefa.** <br/> |



 

## <a name="guidelines"></a>Diretrizes

### <a name="interaction"></a>Interação

-   **Exibir um ponteiro ocupado se o resultado de clicar em um link não for instantâneo.** Sem comentários, os usuários podem assumir que o clique não aconteceu e clicar novamente.

### <a name="color"></a>Cor

-   **Use as cores do sistema de tema ou de link para links visitados e não visitados.** O significado dessas cores é consistente em todos os programas. Se, por algum motivo, os usuários não gostarem dessas cores (talvez por motivos de acessibilidade), eles poderão alterá-las.
-   **Para links de navegação, use cores diferentes para links visitados e não visitados.** Mantenha o histórico dos links visitados somente pela duração da instância do programa. A cor visitada é importante para indicar onde os usuários já foram, impedindo-os de revisitar acidentalmente as mesmas páginas repetidamente.
-   **Para outros tipos de links, não use a cor do link visitado.** Não há valor suficiente na identificação de comandos "visitados", por exemplo.
-   **Não colorir o texto que não é um link porque os usuários podem pressupor que ele é um link.** Use negrito ou um tom de cinza onde, caso contrário, você usaria texto colorido.
-   **Exceção**: você pode usar texto colorido se todos os links forem sublinhados ou colocados em locais de navegação padrão ou de comando.

    **Incorreto:**

    ![captura de tela da mensagem do plano de energia com texto azul ](images/ctrl-links-image11.png)

    Neste exemplo, o texto azul é usado incorretamente para texto que não é um link.

-   **Use cores de plano de fundo que contrastem com as cores do link.** A [cor do sistema de janela](vis-color.md) é sempre uma boa opção.

    **Incorreto:**

    ![captura de tela do texto do link azul no plano de fundo azul ](images/ctrl-links-image12.png)

    Neste exemplo, a cor do plano de fundo fornece um contraste fraco com a cor do link.

### <a name="underlining"></a>Sublinhado

-   **Para links que são necessários para executar uma tarefa principal, forneça pistas visuais para que os usuários possam reconhecer links apenas por inspeção visual.** Essas pistas incluem sublinhado, gráficos ou marcadores e locais de link padrão. Os usuários não devem ter que passar o mouse sobre um objeto ou tentar clicar nele para determinar se ele é um link. Use texto sublinhado se o link não for óbvio em seu contexto.
-   **Não sublinhar texto que não seja um link porque os usuários podem pressupor que ele é um link.** Use itálico, em que você usaria o texto sublinhado. Reserve o sublinhado somente para links.
-   **Ao imprimir, não imprima sublinhados ou cores de link.** Os links impressos não têm valor e são potencialmente confusos.

### <a name="text-with-icon-links"></a>Texto com links de ícone

-   **Use o ícone de seta somente para links de comando.** Os links normais não devem usar o ícone de seta, a menos que estejam sendo usados como substitutos para [links de comando](ctrl-command-links.md) no Windows XP.
-   **Coloque o ícone à esquerda do texto.** O ícone precisa levar ao texto visualmente.

**Correto:**

![captura de tela do ícone de texto anterior ](images/ctrl-links-image13.png)

**Incorreto:**

![captura de tela do ícone de texto a seguir ](images/ctrl-links-image14.png)

No exemplo incorreto, o ícone não leva ao texto.

-   **Faça o resultado de clicar no ícone da mesma forma que clicar no texto.** Caso contrário, seria inesperado e confuso.

### <a name="graphics-only-links"></a>Links somente para gráficos

-   **Não use links somente gráficos.** Os usuários os reconhecem de forma difícil como links e qualquer texto dentro do gráfico (usado para indicar sua ação quando clicado) cria um problema de localização.

### <a name="navigation-links"></a>Links de navegação

-   **Certifique-se de que os links de navegação não exigem compromisso.** Os usuários sempre devem ser capazes de retornar ao estado inicial, seja usando voltar para navegação no local ou cancelar para fechar uma nova janela.
-   **Link para conteúdo específico em vez de conteúdo geral.** Por exemplo, é melhor vincular à seção relevante de um documento do que vincular ao início.
-   **Use um link somente se o material vinculado for relevante, útil e não redundante.** Use o retentor nos links de navegação não os use apenas porque você pode.
-   **Se um link navegar para um site externo, coloque a URL no InfoTip** para que os usuários possam determinar o destino do link.
-   **Vincule apenas a primeira ocorrência do texto do link.** Links redundantes são desnecessários e podem dificultar a leitura do texto.

    **Correto:**

    A pasta imagens facilita o compartilhamento de suas imagens. Você pode usar as tarefas em imagens para enviar suas imagens por email ou publicá-las em um local seguro e privado na Web. Você também pode imprimir suas imagens diretamente da pasta imagens.

    **Incorreto:**

    A pasta imagens facilita o compartilhamento de suas imagens. Você pode usar as tarefas em imagens para enviar suas imagens por email ou publicá-las em um local seguro e privado na Web. Você também pode imprimir suas imagens diretamente da pasta imagens.

    No exemplo correto, somente a primeira ocorrência do texto relevante é vinculada.

    **Exceção**

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

## <a name="text"></a>Texto

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
-   **Termine o link com uma elipse se o comando precisar de informações adicionais (incluindo uma confirmação) para a conclusão bem-sucedida.** Não use uma elipse quando a conclusão bem-sucedida da tarefa for exibir outra janela somente quando forem necessárias informações adicionais para executar a tarefa.

    Imprimir...

    Neste exemplo, a impressão... link de comando exibe uma caixa de diálogo de impressão para coletar mais informações.

    Imprimir

    Por outro lado, neste exemplo, um link de comando imprimir imprime uma única cópia de um documento para a impressora padrão sem nenhuma interação adicional do usuário.

    **O uso adequado de reticências é importante para indicar que os usuários podem fazer mais escolhas antes de executar a tarefa ou podem cancelar totalmente a tarefa**. A indicação visual oferecida por uma elipse permite que os usuários explorem seu software sem medo.

-   **Se necessário, termine um link de tarefa com "Now" para distingui-lo de um link de navegação.**

    Baixar arquivos

    Baixar arquivos agora

    Neste exemplo, "baixar arquivos" navega para uma página para baixar arquivos, enquanto "baixar arquivos agora", na verdade, executa o comando.

**Links de ajuda**

Para obter diretrizes e exemplos, consulte [a ajuda](winenv-help.md).

**Infotips do link**

-   Use frases completas e pontuação final.

Para obter mais diretrizes e exemplos, consulte [ToolTips and Infotips](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Documentação

Ao fazer referência a links:

-   Use o texto do link exato, incluindo suas maiúsculas e minúsculas, mas não inclua as reticências.
-   Para descrever a interação do usuário, use clique.
-   Quando possível, formate o texto do link usando texto em negrito. Caso contrário, coloque o texto do link entre aspas somente se necessário para evitar confusão.

Exemplo: para iniciar a verificação, clique em **verificar um computador**.

 

