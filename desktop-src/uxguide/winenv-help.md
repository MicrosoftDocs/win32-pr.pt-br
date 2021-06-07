---
title: Ajuda
description: Use a Ajuda como um mecanismo secundário para ajudar os usuários a concluir e entender melhor as tarefas \ 8212; o mecanismo principal sendo a própria interface do usuário. Aplique essas diretrizes para tornar o conteúdo realmente útil e fácil de encontrar.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: f9b1260128eb253a2d501a810923ae809c5f8187
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443237"
---
# <a name="help"></a>Ajuda

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Use a Ajuda como um mecanismo secundário para ajudar os usuários a concluir e entender melhor as tarefas que o mecanismo principal é a própria interface do usuário. Aplique essas diretrizes para tornar o conteúdo realmente útil e fácil de encontrar.

Um sistema de Ajuda é composto por vários tipos de conteúdo projetados para ajudar os usuários quando eles não conseguem concluir uma tarefa, querem entender um conceito mais detalhadamente ou precisam de mais detalhes técnicos do que estão disponíveis na interface do usuário.

Neste artigo, nos referimos à Ajuda como secundária à interface do usuário. A interface do usuário é primária porque é aí que os usuários primeiro tentam resolver seus problemas. Eles consultarão o sistema de Ajuda somente se não puderem realizar sua tarefa com a interface do usuário.

![captura de tela da página de ajuda e suporte do Windows ](images/winenv-help-image1.png)

Os recursos de Ajuda e Suporte do Windows home page, disponíveis no menu Iniciar.

**Observação:** As diretrizes relacionadas [ao estilo e ao tom](text-style-tone.md) são apresentadas em um artigo separado.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir, considere estas perguntas:

-   **Qual é a motivação de seus usuários de destino?** Quanto mais motivadas eles descobrirem a funcionalidade do programa e se tornarem usuários intermediários ou até mesmo avançados dele, mais dispostos eles estarão pesquisando respostas para suas perguntas consultando os tópicos da Ajuda.
-   **Você está usando a Ajuda para corrigir uma interface do usuário ruim?** Quanto melhor sua interface do usuário, menos usuários buscarão ajuda adicional. Se o programa tiver uma interface do usuário primária muito clara e útil (como mensagens de erro sem jargões, assistentes bem escritos e caixas de diálogo não ambíguas), talvez você não precise de um sistema de Ajuda secundário.
-   **Seu programa é relativamente simples?** Nesse caso, considere incorporar todo o conteúdo de assistência necessário em suas superfícies de interface do usuário primárias. É mais provável que os usuários busquem ajuda adicional em programas que executam tarefas complexas.
-   **Seu aplicativo destina-se a desenvolvedores, profissionais de TI ou outros especialistas em software?** Esses usuários tendem a esperar ajuda de referência para convenções de linguagem de programação e ajuda conceitual detalhada para o domínio dos recursos.

## <a name="design-concepts"></a>Conceitos de design

Se você decidir incluir a Ajuda em seu programa, integre-a ao seu design geral. A interface de Ajuda deve ser simples, eficiente e relevante; ele deve permitir que os usuários recebam ajuda facilmente e, em seguida, retornem à tarefa. Pense em seu sistema de Ajuda em termos de tempo dos usuários: minimize a interrupção primeiro prevendo onde eles encontrarão problemas em seu programa e, em seguida, resolvendo esses problemas incorporando assistência fundamental diretamente à interface do usuário e criando pontos de entrada claros e consistentes em sua Ajuda mais detalhada.

A assistência do Windows foi projetada de acordo com esses princípios. Aqui estão algumas das alterações de design na experiência do usuário da Ajuda do Windows:

-   Mais pontos de entrada que podem ser descobertos para a Ajuda da interface do usuário primária (especialmente novos links de Ajuda de superfícies da interface do usuário, como caixas de diálogo, mensagens de erro e assistentes). Os links de ajuda levam você diretamente ao tópico pertinente em Ajuda.
-   Um ícone do botão Ajuda está disponível no canto superior direito da maioria das páginas Painel de Controle hub, bem como pastas de shell.
-   Os usuários podem optar por obter o conteúdo de Ajuda mais atualizado da Ajuda e Suporte do Windows Online quando eles estão online.
-   Os tópicos de ajuda agora são baseados em tarefas em vez de focados em recursos, para que os usuários possam realizar suas tarefas de maneira rápida e eficiente.
-   Os tópicos de ajuda agora são baseados em cenários de usuários principais conhecidos.
-   Os tópicos de ajuda têm um tom mais descontraído [e](text-style-tone.md)informal, usando a linguagem do mundo real.
-   Os tópicos de ajuda são projetados para uma verificação eficaz, pois os usuários raramente leem o conteúdo palavra por palavra.

### <a name="an-analogy-for-help"></a>Uma analogia para a Ajuda

Para pensar mais detalhadamente sobre como criar seu sistema de Ajuda, considere uma analogia da vida diária. Você está perdido em uma cidade desconhecida. O que você faz? Muitos reagiriam desta forma:

-   Ser orientado; procure pontos de referência, sinais de rua (nomes e ponteiros para locais).
-   Procure mapas.
-   Por fim, como último recurso, peça instruções ou chame um amigo.

O design da "interface" da cidade afeta sua necessidade de assistência. Rua bem rotulada, direções explícitas (ponteiros para hospital, aeroportos, aeroportos e correios) e pontos de referência claros, como recursos geográficos proeminentes ou edifícios, ajudam você a encontrar seu caminho.

Você pede ajuda como último recurso. É uma indicação de que a "interface" da cidade falhou ao ser mal projetada e confusa. É mais provável que você peça ajuda em um local que tenha um rótulo específico que sugere ajuda. Por exemplo, é mais provável que você peça ajuda em um local rotulado como "Directions" ou "Information" do que em um local geral como a Cidade, mesmo que qualquer pessoa na Cidade possa lhe dar instruções.

Quando você pede ajuda, é provável que você fique frustrado e queira apenas chegar ao destino pretendido. Você provavelmente não está no clima de gastar tempo fazendo um tour pela cidade ou aprendendo sobre sua história. Além disso, sua motivação depende da importância da tarefa. Se você estiver tentando encontrar seu quarto de hotel, fará o que for necessário. No entanto, se sua meta for encontrar um local de importância secundária, é provável que você simplesmente desmente após um esforço pequeno.

Todos esses aspectos de encontrar seu caminho no espaço real correspondem a como os usuários normalmente encontram seu caminho no espaço virtual do programa. Buscar ajuda além da interface do usuário primária é, por sua própria natureza, difícil; faça o possível para atenuar essa experiência por interface do usuário bem projetada e "sinais de rua" inteligentes para direcionar os usuários para as respostas de que precisam.

### <a name="designing-ui-so-that-help-is-unnecessary"></a>Projetando a interface do usuário para que a Ajuda seja desnecessária

Tente tornar a Ajuda desnecessária em primeiro lugar, por:

-   Facilitando a descoberta e a execução de tarefas comuns.
-   Fornecendo instruções [principais claras.](text-ui.md)
-   Fornecendo rótulos de controle claros e concisos que são orientados a meta e tarefas.
-   Fornecendo instruções complementares e explicações quando necessário.
-   Prevendo problemas que podem ser evitados usando controles restritos a opções válidas, fornecendo valores padrão adequados, tratando todos os formatos de entrada e impedindo erros.
-   Escrever mensagens de erro que fornecem uma solução ou ação clara para o usuário tomar.
-   Evitar designs de interface do usuário confusos, como tarefas com fluxo ruim ou uso de controles desabilitados sem motivo aparente.
-   Trabalhando com editores e autores no início do ciclo de desenvolvimento para criar texto de interface do usuário consistente e [de](text-ui.md) alta qualidade em todo o programa.

Os usuários não devem ter que ir para outro lugar para descobrir como usar sua interface do usuário. Adicione informações essenciais diretamente à interface do usuário primária, em vez de forçar os usuários a sair de seu contexto imediato e no painel Ajuda. Se informações importantes existirem apenas em um tópico de Ajuda, há uma boa chance de que os usuários não as vejam. Para obter informações opcionais e mais explicativas, use links de Ajuda da interface do usuário primária para o tópico de Ajuda relevante para assistência complementar.

### <a name="considering-user-motivation"></a>Considerando a motivação do usuário

Para a maioria dos usuários, a velocidade e a eficiência estão entre as virtudes fundamentais de bons programas. Os usuários querem fazer seu trabalho. Em geral, eles não estão interessados em aprender sobre o programa e a tecnologia por conta própria; sua saúde se estende apenas na medida em que o programa atende seus próprios interesses e resolve problemas em questão.

Projete seu sistema de Ajuda para corresponder à motivação dos usuários. Por exemplo, considere um usuário que se aprofundou em um quiosque em um rio. Se ela não conseguir descobrir como executar a tarefa rapidamente, provavelmente ela simplesmente vai se entregar e sair. É improvável que ela gaste tempo usando a Ajuda. Como alternativa, um usuário altamente motivada tem uma tolerância maior para o tempo gasto pesquisando seu sistema de Ajuda para obter respostas. Um usuário de negócios que deve equilibrar os livros, por exemplo, provavelmente está disposto a consultar o conteúdo da Ajuda para tirar o máximo do novo aplicativo de contabilidade.

### <a name="writing-content-for-scanning"></a>Escrevendo conteúdo para verificação

Escreva tópicos da Ajuda sabendo que eles serão examinados em busca de informações específicas, não de leitura word-for-word. Escreva de forma concisa, chegando ao ponto rapidamente e fornecendo informações sobre as que os usuários podem agir.

-   Escreva tópicos de "instrução" usando etapas numeradas em um formato consistente para que os usuários reconheçam que estão recebendo assistência de procedimento.
-   Escreva tópicos de referência com facilidade de verificação em mente, usando tabelas, por exemplo, para apresentar opções de interface do usuário ou sintaxe de linguagem.
-   Escreva tópicos conceituais organizados logicamente por subheadings, para que o usuário possa ignorar seções inteiras de menor interesse.

Em todo o conteúdo da Ajuda, é mais fácil verificar listas com marcador do que blocos de parágrafo padrão de texto; no entanto, use listas de marcador de forma criteriosa, não como uma trava para material não organizado.

### <a name="creating-content-that-matters"></a>Criando conteúdo importante

Considerando que nenhum sistema de Ajuda pode prever todas as perguntas que cada usuário pode ter, concentre a maior parte do conteúdo em responder às principais perguntas nos principais cenários para os usuários de destino. Por exemplo, a pesquisa eficaz e como estabelecer a conectividade de rede (entre outras tarefas) podem ser tópicos altamente procurados. Além disso, concentre-se em tarefas em seus principais cenários de usuário, em vez de documentar um recurso ou tecnologia exaustivamente para seu próprio bem.

**Dica:** O suporte técnico é uma boa fonte para o conteúdo da Ajuda. Os auxiliares geralmente mantêm registros de perguntas frequentes sobre programas ou tarefas específicas que os usuários estão tentando (e falhando) realizar.

Não é necessário fornecer ajuda para todos os recursos na interface do usuário. **Com muita frequência, a Ajuda não ajuda resulta na tentativa de criar Ajuda para tudo.** Se a interface do usuário for bem projetada, a maioria desses tópicos de Ajuda não será muito útil; eles apenas vão restate o óbvio.

Se houver mais de uma maneira de executar uma tarefa, na maioria dos casos, você poderá apenas documentar a maneira mais comum usada por usuários inodores. As exceções a isso incluem considerações de acessibilidade (documentação de equivalentes de teclado de ações do mouse, por exemplo) e considerações de plataforma (documentação para o fator forma de tablet, por exemplo, ou para ambientes de servidor em que a linha de comando pode substituir pela interface gráfica do usuário).

Lembre-se de que os usuários geralmente não pensam nos problemas que estão encontrando exatamente nos mesmos termos que você. Por exemplo, os usuários podem achar estranho pensar em si mesmos como uma "conta". Certifique-se de projetar sua funcionalidade de pesquisa e indexação, em seguida, para levar em conta as variações de terminologia e sinônimos prováveis.

Entre a interface do usuário primária e o sistema de Ajuda, no entanto, os termos devem ser muito semelhantes se não idênticos. Os usuários podem ficar confusos quando o idioma do sistema de Ajuda não se correlaciona muito com o que eles estão vendo na tela.

### <a name="writing-compelling-help-link-text"></a>Escrevendo texto de link da Ajuda atraente

Ao vincular a um tópico de Ajuda de sua interface do usuário primária, certifique-se de escrever um texto de link de Ajuda atraente. Linguagem clara e específica inspirador confiança. Os usuários tendem a acreditar que os links de Ajuda genéricos (um botão com a palavra "Ajuda" ou "Saiba mais" nele) não levarão às informações corretas sem um investimento significativo de tempo.

**Se você fizer apenas cinco coisas...**

1.  Projete sua interface do usuário para que os usuários não precisem de Ajuda.
2.  Faça com que sua Ajuda seja útil concentrando o conteúdo nas principais perguntas nos principais cenários para os usuários de destino.
3.  Apresente o conteúdo da Ajuda para que seja fácil verificar.
4.  Entenda que você não precisa fornecer ajuda para todos os recursos na interface do usuário.
5.  Tornar os pontos de entrada da Ajuda descobriveis e atraentes.

## <a name="usage-patterns"></a>Padrões de uso

Diferentes tipos de conteúdo servem para finalidades diferentes.



|    Tipo de conteúdo                                                                                                        |   Exemplo                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ajuda de procedimento**<br/> fornece as etapas para realizar uma tarefa. <br/>                       | A ajuda de procedimento deve se concentrar em informações de "como" em vez de "o que" ou "por quê". <br/> ![captura de tela da página de ajuda 'excluir arquivos temporários' ](images/winenv-help-image2.png)<br/> Neste exemplo, o tópico Ajuda descreve como usar um recurso do utilitário limpeza de disco, fornecendo etapas a serem seguidas em sequência.<br/>                                              |
| **Ajuda conceitual**<br/> fornece informações em segundo plano, visão geral de recursos ou processos. <br/> | A ajuda conceitual deve fornecer informações "o que" ou "por quê" além das necessárias para concluir uma tarefa. <br/> ![captura de tela da página de ajuda 'a área de trabalho (visão geral)' ](images/winenv-help-image3.png)<br/> Neste exemplo, o tópico Ajuda define o que é a área de trabalho e fornece detalhes adicionais sobre o que ela contém e por que os usuários interagem com ela.<br/>           |
| **Ajuda de referência**<br/> serve como um livro de referência online. <br/>                                | Você pode usar a ajuda de referência para documentar uma linguagem de programação ou interfaces de programação. <br/> ![captura de tela da página de ajuda 'convenções de notação' ](images/winenv-help-image4.png)<br/> Neste exemplo, o tópico Ajuda lista as convenções tipográficas em uso para esse idioma ou aplicativo específico, fornecendo as informações em uma tabela fácil de examinar.<br/> |



 

## <a name="guidelines"></a>Diretrizes

### <a name="entry-points"></a>Pontos de entrada

-   **Link para tópicos de Ajuda específicos e relevantes.** Não vincule à ajuda home page, ao conteúdo, a uma lista de resultados da pesquisa ou a uma página que apenas vincula a outras páginas. Evite vincular a páginas estruturadas como uma grande lista de perguntas frequentes, pois ela força os usuários a pesquisar aquela que corresponde ao link clicado. Não vincule a tópicos de Ajuda específicos que não são relevantes e úteis para a tarefa em questão. Nunca vincule a páginas vazias.
-   **Não coloque links de Ajuda em cada janela ou página por questão de consistência.** Fornecer um link de Ajuda em um só lugar não significa que você precisa foreá-los em todos os lugares.
-   **Use links de Ajuda para caixas de diálogo, mensagens de erro, assistentes e folhas de propriedades.** Se o link ajuda se aplicar a controles específicos, coloque-o sob eles, alinhado à esquerda. Se o link ajuda se aplicar a toda a janela, coloque-o no canto inferior esquerdo da área de conteúdo da janela.

    ![captura de tela da folha de propriedades com a caixa de grupo ](images/winenv-help-image5.png)

    Neste exemplo, o segundo link da Ajuda se aplica a um grupo de controles.

    ![captura de tela da folha de propriedades e do link de ajuda ](images/winenv-help-image6.png)

    Neste exemplo, o link Ajuda se aplica a toda a janela.

-   **Use links de Ajuda em vez de referências textuais genéricas à Ajuda sempre que tecnicamente possível.**

    **Correto:**

    Como posso reparar erros de disco?

    **Incorreto:**

    Para obter mais informações sobre como reparar erros de disco, consulte Ajuda e suporte.

-   **Use um botão Ajuda com o ícone Ajuda para as páginas do hub dos itens do painel de controle.** Coloque-o no canto superior direito. Esses botões não têm um rótulo, mas têm uma dica de ferramenta que lê a Ajuda.

    ![captura de tela do item do painel de controle com o botão de ajuda ](images/winenv-help-image7.png)

    Um item do painel de controle com um botão Ajuda.

-   **A Ajuda F1 é opcional.** Os usuários estão acostumados a encontrar informações de Ajuda relacionadas ao contexto imediato da interface do usuário na tela pressionando a tecla F1, que é rotulada Ajuda em teclados padrão. Você pode incluir a Ajuda F1 se, por exemplo, os estudos de usabilidade mostrarem que os usuários esperam encontrá-la ou sua interface do usuário do programa for complexa o suficiente para se beneficiar da assistência contextual.
-   **Programas com barras de menu podem ter uma categoria de menu Ajuda.** Para diretrizes de menu ajuda, consulte [Menus](cmd-menus.md).

    ![captura de tela da ajuda acessada na barra de menus ](images/winenv-help-image8.png)

    Neste exemplo, o acessórios do Windows Paint tem uma categoria de menu Ajuda.

-   **Para acessibilidade do teclado, forneça paradas de tabulação para botões e links da Ajuda.**
-   O comportamento do botão de ajuda e do link deve ser o seguinte: o painel ajuda é aberto e um tópico de Ajuda dedicado é exibido; A interface do usuário que invocou o painel Ajuda deve permanecer aberta para preservar a experiência contextual.
-   **Não use os seguintes estilos obsoletos de ponto de entrada da Ajuda: "Saiba mais" ou "Saiba mais sobre..." links, botões de Ajuda genéricos e botões de Ajuda contextidores na barra de título.** Embora eles tenham sido usados no passado, os estudos de usabilidade determinaram que os usuários tendem a ignorá-los. Em vez disso, use links para tópicos de Ajuda específicos. Para ver diretrizes sobre como escrever bons links de Ajuda, consulte [Links de ajuda.](#text)

    **Incorreto:**

    ![captura de tela da caixa de diálogo com um link 'saiba mais' ](images/winenv-help-image9.png)

    Não use "Saiba mais" ou "Saiba mais sobre..." Links.

    **Incorreto:**

    ![captura de tela do botão de ajuda ao lado dos botões de commit ](images/winenv-help-image10.png)

    Não use botões de Ajuda genéricos.

    **Incorreto:**

    ![captura de tela do ícone de ponto de interrogação na barra de título ](images/winenv-help-image11.png)

    Não use botões de Ajuda contextuis na barra de título.

### <a name="content"></a>Conteúdo

-   **Não crie conteúdo óbvio.** Os tópicos de ajuda que repetem o que está na interface do usuário primária não adicionam valor.
-   **Não crie conteúdo em que o usuário não possa agir de alguma forma.**
    -   **Exceção:** Algum conteúdo conceitual fornece informações importantes em segundo plano sem necessariamente levar à ação do usuário.
-   **Evite resoluções de problemas.** Por exemplo, "entre em contato com o administrador do sistema" ou "reinstale o aplicativo" tendem a frustrar os usuários.
    -   **Exceção:** Recomendamos entrar em contato com o administrador do sistema se essa for a única solução prática e os administradores do sistema esperam ser contatados para o problema.
-   **Evite conteúdo que aborda cenários de usuário altamente improváveis.** Desenvolva o conteúdo principal da Ajuda para o que você prevê que será o uso normal; observe exceções importantes ao uso esperado, mas trate esse conteúdo como uma prioridade mais baixa.
-   **Reúna comentários de seus usuários sobre como seus tópicos de Ajuda são úteis.** Permitir que os usuários rateiem tópicos individuais. Conduza [estudos de usabilidade](glossary.md) em sua documentação para verificar problemas que envolvem a qualidade e a capacidade de descoberta do conteúdo.
    -   **Dica:** Os comentários do usuário também são uma ótima maneira de gerar mais conteúdo baseado em tarefas, focado no que os usuários estão realmente fazendo com seu programa, em vez de conteúdo baseado em recursos, focado simplesmente em uma descrição da tecnologia.
-   **Fornecer várias maneiras de acessar seu conteúdo.** Um sumário, um índice e um mecanismo de [pesquisa](ctrl-search-boxes.md) são três dos métodos mais comuns de melhorar a descoberta.
-   **Se houver mais de uma maneira de executar uma tarefa, na maioria dos casos, você poderá apenas documentar a maneira mais comum usada pelos usuários inexperientes.**

### <a name="icons"></a>Ícones

-   Use o ícone de ajuda somente para janelas do Explorer e as páginas de Hub dos itens do painel de controle. Não use o ícone de ajuda com links de ajuda.

**Correto:**

![captura de tela da janela com ícone de ponto de interrogação ](images/winenv-help-image12.png)

Neste exemplo, uma janela do Windows Explorer usa um ícone de ajuda para fornecer acesso à ajuda.

**Incorreto:**

![captura de tela da janela com ícone de ajuda no painel esquerdo ](images/winenv-help-image13.png)

Neste exemplo, o ícone de ajuda na parte inferior esquerda é usado incorretamente com um link de ajuda.

## <a name="text"></a>Text

**Links de ajuda**

-   Forneça informações específicas sobre o conteúdo do tópico da ajuda, usando o máximo de texto relevante e conciso, conforme necessário. Os usuários geralmente ignoram links de ajuda genéricos. Verifique se os resultados do link são os usuários previsíveis não devem se surpreender com os resultados.

    -   **Exceção:** Você pode usar "mais informações" para complementar instruções que estão diretamente na interface do usuário, especialmente se fornecer informações específicas no link de ajuda leva a repetição desnecessária ou torna o link menos atraente.

    **Incorreto:**

    Uma senha forte tem pelo menos seis letras, números e símbolos misturados. O que é uma senha forte?

    **Correto:**

    Uma senha forte tem pelo menos seis letras, números e símbolos misturados. Mais informações

    No exemplo incorreto, o link de ajuda é repetitivo. Ele faz uma pergunta que realmente já foi respondida.

-   Sempre que possível, a ajuda de frase vincula o texto em termos da pergunta principal respondida pelo conteúdo da ajuda. Não use a frase "Saiba mais sobre", "mais informações sobre" ou "obter ajuda com este".

    **Incorreto:**

    Saiba mais sobre como adicionar exceções

    **Correto:**

    Quais são os riscos de permitir exceções?

    Como fazer Adicionar exceções?

    Nos exemplos corretos, o link é escrito em termos da pergunta principal respondida pelo tópico da ajuda.

-   Se as informações mais relevantes puderem ser resumidas sucintamente, coloque o resumo diretamente na interface do usuário em vez de usar um link de ajuda. No entanto, você pode usar um link de ajuda para fornecer informações complementares.

    **Incorreto:**

    ![captura de tela de link para o que é uma senha forte? ](images/winenv-help-image14.png)

    **Correto:**

    ![captura de tela de texto suplementar sobre senhas ](images/winenv-help-image15.png)

    **Melhor:**

    ![captura de tela de texto com link para mais informações ](images/winenv-help-image16.png)

    O exemplo correto resume as informações de ajuda de forma sucinta, melhorando muito a probabilidade de que os usuários a leiam. O exemplo melhor fornece um link de ajuda para obter mais informações sobre esse assunto complexo.

-   A frase ajuda links para indicar claramente a assistência. Os links de ajuda nunca devem ser lidos como links de ação.
-   Use o link de ajuda inteiro para o texto do link, não apenas as palavras-chave.

    **Correto:**

    Quais são os riscos de permitir exceções?

    **Incorreto:**

    Quais são os riscos de permitir exceções?

    No exemplo correto, a sentença de link de ajuda inteira é usada para o texto do link.

    -   **Exceção:** Os links de ajuda para sites externos devem simplesmente usar o nome do site ou da página como o link. Qualquer texto que introduza o nome do site não precisa ser incluído no próprio link.

-   Os links de ajuda não precisam corresponder exatamente aos títulos de tópicos da ajuda, mas deve haver uma conexão forte e óbvia entre os dois. Crie links e cabeçalhos em pares por esse motivo.

    **Correto:**

    Como posso melhorar o desempenho desse recurso? (texto do link)

    Configurando esse recurso para um desempenho ideal (título de tópico)

    **Incorreto:**

    Como posso melhorar o desempenho desse recurso? (texto do link)

    Visão geral completa deste recurso (título do tópico)

    No exemplo incorreto, o título do tópico da ajuda é substancialmente diferente no escopo do texto do link de ajuda e pode ser desorientado.

-   Se o conteúdo da ajuda estiver online, torne-o claro no texto do link. Isso ajuda a tornar o resultado dos links previsíveis.

    **Correto:**

    Para formatos e ferramentas adicionais, vá para o site da Microsoft.

    **Incorreto:**

    Onde posso encontrar formatos e ferramentas adicionais?

-   Use frases completas.
-   Não use pontuação final, exceto pontos de interrogação.
-   Não use reticências para comandos ou links de ajuda.

**Conteúdo da ajuda**

-   Formate os elementos da interface do usuário usando negrito para torná-los fáceis de identificar. Isso é especialmente útil para tópicos de ajuda de procedimentos, permitindo que os usuários examinem procedimentos e vejam rapidamente os elementos pertinentes da interface do usuário.
-   Formatar legendas usando itálico. Isso se aplica a tabelas, arte, capturas de tela e outros elementos gráficos que se beneficiam da breve explicação textual.
-   Consulte a ajuda simplesmente como ajuda. Em geral, não use a frase de ajuda online, a menos que você esteja de fato se referindo ao conteúdo em seu site.

 

