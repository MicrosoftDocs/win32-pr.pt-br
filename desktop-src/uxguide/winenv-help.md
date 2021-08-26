---
title: Ajuda
description: Use a ajuda como um mecanismo secundário para ajudar os usuários a concluir e entender melhor as tarefas \ 8212; o mecanismo principal é a própria interface do usuário. Aplique essas diretrizes para tornar o conteúdo verdadeiramente útil e fácil de encontrar.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2a71abf4b90aeaf19f43997c5d8e98ad42f56d5daa86699ff8504ca5a3080bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935695"
---
# <a name="help"></a>Ajuda

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Use a ajuda como um mecanismo secundário para ajudar os usuários a concluir e compreender melhor as tarefas o mecanismo principal sendo a própria interface do usuário. Aplique essas diretrizes para tornar o conteúdo verdadeiramente útil e fácil de encontrar.

Um sistema de ajuda é composto por vários tipos de conteúdo projetados para ajudar os usuários quando eles não conseguem concluir uma tarefa, deseja entender um conceito em mais detalhes ou precisar de mais detalhes técnicos do que estão disponíveis na interface do usuário.

Neste artigo, vamos nos referir a ajuda como secundária à interface do usuário. A interface do usuário é primária porque é onde os usuários primeiro tentam resolver seus problemas. Eles consultarão o sistema de ajuda somente se não puderem realizar suas tarefas com a interface do usuário.

![captura de tela da página de ajuda e suporte do Windows ](images/winenv-help-image1.png)

o home page de ajuda e suporte do Windows, disponível no menu Iniciar.

**Observação:** As diretrizes relacionadas ao [estilo e ao Tom](text-style-tone.md) são apresentadas em um artigo separado.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

-   **Como os usuários de destino são motivados?** Quanto mais motivado eles forem descobrir a funcionalidade do seu programa e se tornarem usuários intermediários ou até mesmo avançados, mais disposto eles serão a pesquisa de respostas para suas dúvidas por tópicos de ajuda de consultoria.
-   **Você está usando a ajuda para corrigir uma interface do usuário inadequada?** Quanto melhor sua interface do usuário, menos usuários irão buscar ajuda adicional. Se o seu programa tiver uma interface do usuário primária muito clara e útil (como mensagens de erro sem jargão, assistentes bem escritos e caixas de diálogo não ambíguas), talvez você não precise de um sistema de ajuda secundário.
-   **Seu programa é relativamente simples?** Nesse caso, considere incorporar todo o conteúdo de assistência necessário às suas superfícies da interface do usuário primária. É mais provável que os usuários busquem ajuda adicional em programas que executam tarefas complexas.
-   **Seu aplicativo destina-se a desenvolvedores, profissionais de ti ou outros especialistas em software?** Esses usuários tendem a esperar ajuda de referência para convenções de linguagem de programação e ajuda conceitual detalhada para dominar os recursos.

## <a name="design-concepts"></a>Conceitos de design

Se você decidir incluir ajuda em seu programa, integre-a ao seu design geral. A interface da ajuda deve ser simples, eficiente e relevante; Ele deve permitir que os usuários obtenham ajuda facilmente e, em seguida, retornem à sua tarefa. Considere o sistema de ajuda em termos de tempo dos usuários: Minimize a interrupção primeiro, antecipando onde elas encontrarão problemas em seu programa, resolvendo esses problemas incorporando assistência fundamental diretamente à sua interface do usuário e criando pontos de entrada claros e consistentes em sua ajuda mais detalhada.

Windows assistência foi projetada de acordo com esses princípios. aqui estão algumas das alterações de design do Windows a experiência do usuário da ajuda:

-   Pontos de entrada mais detectáveis para ajudar da interface do usuário principal (especialmente novos links de ajuda de superfícies de interface do usuário, como caixas de diálogo, mensagens de erro e assistentes). Os links de ajuda levam você diretamente para o tópico pertinente na ajuda.
-   Um ícone de botão de ajuda está disponível no canto superior direito da maioria das páginas do Hub do painel de controle, bem como pastas do Shell.
-   os usuários podem optar por obter o conteúdo mais atualizado da ajuda de Windows ajuda online e suporte quando estiverem online.
-   Os tópicos de ajuda agora são baseados em tarefas, e não focados em recursos, para que os usuários possam realizar suas tarefas com rapidez e eficiência.
-   Os tópicos de ajuda agora são amplamente baseados em cenários de usuário principais conhecidos.
-   Os tópicos de ajuda têm um [Tom](text-style-tone.md)mais relaxado e informal, usando a linguagem do mundo real.
-   Os tópicos de ajuda são projetados para uma verificação efetiva, pois os usuários raramente lêem o conteúdo Word-for-Word.

### <a name="an-analogy-for-help"></a>Uma analogia para obter ajuda

Para pensar em mais detalhes sobre como projetar seu sistema de ajuda, considere uma analogia da vida diária. Você é perdido em uma cidade desconhecida. O que você faz? Muitos reagirão da seguinte forma:

-   Seja orientado; Procure pontos de referência, sinais de rua (nomes e ponteiros para locais).
-   Procure mapas.
-   Por fim, como último recurso, peça direções ou ligue para um amigo.

O design da "interface" da cidade afeta sua necessidade de assistência. Ruas bem rotuladas, direções explícitas (ponteiros para hospitais, aeroportos, museus e o Post Office), além de pontos de referência claros, como recursos geográficos proeminentes ou edifícios, ajudam você a encontrar seu caminho.

Você pede ajuda como um último recurso. É uma indicação de que a "interface" da cidade falhou por ter sido mal projetada e confusa. É mais provável que você peça ajuda em um local que tenha um rótulo específico que sugira utilidade. Por exemplo, é mais provável que você solicite ajuda em um local rotulado como "direções" ou "informações" do que um lugar geral, como o Hall da cidade, mesmo que praticamente qualquer pessoa na sala de cidade possa fornecer instruções.

Quando você solicita ajuda, é provável que você esteja frustrado e queira apenas chegar ao destino pretendido. Provavelmente, você não tem o humor de gastar tempo fazendo um tour pela cidade ou aprendendo sobre seu histórico. Além disso, sua motivação depende da importância da tarefa. Se você estiver tentando encontrar seu quarto de Hotel, fará tudo o que for necessário. No entanto, se seu objetivo for encontrar um local de importância menor, é mais provável que você venha a desistir depois de um pequeno esforço.

Todos esses aspectos da localização do seu caminho em espaço real correspondem a como os usuários normalmente encontram seu caminho no espaço virtual do seu programa. Procurar ajuda além da interface do usuário principal é por sua inorientação de natureza. Faça o melhor para mitigar essa experiência por interface do usuário bem projetada e "sinais de rua" inteligentes para direcionar os usuários às respostas de que precisam.

### <a name="designing-ui-so-that-help-is-unnecessary"></a>Projetando a interface do usuário para que a ajuda seja desnecessária

Tente tornar a ajuda desnecessária em primeiro lugar, por:

-   Facilitar a descoberta e a execução de tarefas comuns.
-   Fornecendo [instruções principais](text-ui.md)claras.
-   Fornecendo rótulos de controle claros e concisos que são orientados a tarefas e metas.
-   Fornecendo instruções complementares e explicações quando necessário.
-   Prever problemas de podem ser evitados usando controles restritos a escolhas válidas, fornecendo valores padrão adequados, manipulando todos os formatos de entrada e impedindo erros.
-   Gravando mensagens de erro que fornecem uma solução ou ação clara para o usuário tomar.
-   Evitar designs de interface de usuário confusos, como tarefas com fluxo ruim ou usar controles que estão desabilitados sem motivo aparente.
-   Trabalhar com gravadores e editores no início do ciclo de desenvolvimento para criar [texto de interface do usuário](text-ui.md) consistente de alta qualidade em todo o seu programa.

Os usuários não devem ter que ir em outro lugar para descobrir como usar sua interface do usuário. Adicione informações essenciais diretamente à interface do usuário principal, em vez de forçar os usuários de seu contexto imediato e para o painel da ajuda. Se houver informações importantes apenas em um tópico da ajuda, há uma boa chance de que os usuários não as vejam. Para obter informações que sejam opcionais e mais explicativas, use links de ajuda da interface do usuário principal para o tópico de ajuda relevante para obter assistência complementar.

### <a name="considering-user-motivation"></a>Considerando a motivação do usuário

Para a maioria dos usuários, a velocidade e a eficiência estão entre as mais imprescindíveis de programas bons. Os usuários desejam realizar seu trabalho. Em geral, eles não estão interessados em aprender sobre o programa e a tecnologia por si só; sua paciência se estende apenas ao insofár, pois esse programa atende aos seus próprios interesses e resolve problemas à mão.

Projete seu sistema de ajuda para corresponder à motivação de seus usuários. Por exemplo, considere um usuário que se inscreveu em um quiosque em um museu. Se ela não conseguir descobrir como executar a tarefa rapidamente, ela provavelmente vai apenas desistir e sair. Não é improvável gastar tempo usando a ajuda. Como alternativa, um usuário altamente motivado tem uma tolerância mais alta para o tempo gasto pesquisando o sistema de ajuda para obter respostas. Um usuário empresarial que deve balancear os livros, por exemplo, provavelmente está disposto a consultar o conteúdo da ajuda para obter o máximo desse novo aplicativo de contabilidade.

### <a name="writing-content-for-scanning"></a>Gravando conteúdo para verificação

Escreva tópicos de ajuda sabendo que eles serão verificados quanto a informações específicas, não leia Word-for-Word. Escreva de forma concisa, acessando o ponto rapidamente e fornecendo informações sobre as quais os usuários podem agir.

-   Escreva tópicos "como" usando etapas numeradas em um formato consistente para que os usuários reconheçam que estão obtendo assistência de procedimento.
-   Escreva tópicos de referência com a facilidade de varredura em mente, usando tabelas, por exemplo, para apresentar opções de interface do usuário ou sintaxe de linguagem.
-   Escreva tópicos conceituais que são organizados logicamente por subtítulos, para que o usuário possa ignorar seções inteiras de menos interesse.

Em todo o conteúdo da ajuda, é mais fácil digitalizar listas com marcadores do que blocos de texto de parágrafo padrão; Use listas com marcadores criteriosamente, mas não como um Crutch para material não organizado.

### <a name="creating-content-that-matters"></a>Criando conteúdo que importa

Considerando que nenhum sistema de ajuda pode prever todas as perguntas que cada usuário possa ter, concentre a maior parte do conteúdo ao responder às principais perguntas nos principais cenários de seus usuários de destino. Por exemplo, a pesquisa eficiente e como estabelecer a conectividade de rede (entre outras tarefas) pode ser de alta busca-após tópicos. Além disso, concentre-se nas tarefas em seus principais cenários de usuário, em vez de documentar exaustivamente um recurso ou uma tecnologia por si só.

**Dica:** O suporte técnico é uma boa fonte para o conteúdo da ajuda. As assistência técnica geralmente mantêm registros de perguntas frequentes sobre determinados programas ou tarefas que os usuários estão tentando (e falham) em realizar.

Não é necessário fornecer ajuda para todos os recursos na interface do usuário. **Com muita frequência, a Ajuda não ajuda resulta na tentativa de criar Ajuda para tudo.** Se a interface do usuário for bem projetada, a maioria desses tópicos de Ajuda não será muito útil; eles apenas vão restate o óbvio.

Se houver mais de uma maneira de executar uma tarefa, na maioria dos casos, você poderá apenas documentar a maneira mais comum usada por usuários ininteados. As exceções a isso incluem considerações de acessibilidade (documentação de equivalentes de teclado de ações do mouse, por exemplo) e considerações de plataforma (documentação para o fator forma de tablet, por exemplo, ou para ambientes de servidor em que a linha de comando pode substituir a interface gráfica do usuário).

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

-   **Link para tópicos de Ajuda específicos e relevantes.** Não vincule à Ajuda home page, ao conteúdo, a uma lista de resultados da pesquisa ou a uma página que apenas vincula a outras páginas. Evite vincular a páginas estruturadas como uma lista grande de perguntas frequentes, pois ela força os usuários a pesquisar aquela que corresponde ao link clicado. Não vincule a tópicos de Ajuda específicos que não são relevantes e úteis para a tarefa em questão. Nunca vincule a páginas vazias.
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

    Neste exemplo, o acessórios Windows Paint tem uma categoria de menu Ajuda.

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
-   **Forneça várias maneiras de acessar seu conteúdo.** Um tabela de conteúdo, um índice e um mecanismo [de](ctrl-search-boxes.md) pesquisa são três dos métodos mais comuns de melhorar a capacidade de descoberta.
-   **Se houver mais de uma maneira de executar uma tarefa, na maioria dos casos, você poderá apenas documentar a maneira mais comum usada por usuários ininteados.**

### <a name="icons"></a>Ícones

-   Use o ícone ajuda somente para janelas do Explorer e as páginas de hub de itens do painel de controle. Não use o ícone ajuda com links de Ajuda.

**Correto:**

![captura de tela da janela com o ícone de ponto de interrogação ](images/winenv-help-image12.png)

Neste exemplo, uma janela Windows Explorer usa um ícone de Ajuda para fornecer acesso à Ajuda.

**Incorreto:**

![captura de tela da janela com o ícone de ajuda no painel esquerdo ](images/winenv-help-image13.png)

Neste exemplo, o ícone ajuda no canto inferior esquerdo é usado incorretamente com um link de Ajuda.

## <a name="text"></a>Texto

**Links de ajuda**

-   Forneça informações específicas sobre o conteúdo do tópico ajuda, usando o texto conciso e relevante, conforme necessário. Os usuários geralmente ignoram links de Ajuda genéricos. Certifique-se de que os resultados do link sejam previsíveis, os usuários não devem se surpresar com os resultados.

    -   **Exceção:** Você pode usar "Mais informações" para complementar instruções que estão diretamente na interface do usuário, especialmente se fornecer informações específicas no link ajuda leva a repetição desnecessária ou torna o link menos atraente.

    **Incorreto:**

    Uma senha forte tem pelo menos seis letras, números e símbolos mistos. O que é uma senha forte?

    **Correto:**

    Uma senha forte tem pelo menos seis letras, números e símbolos mistos. Mais informações

    No exemplo incorreto, o link ajuda é repetitivo. Ele faz uma pergunta que realmente já foi respondida.

-   Sempre que possível, a frase Ajuda vincula texto em termos da pergunta primária respondida pelo conteúdo da Ajuda. Não use a frase "Saiba mais sobre", "Conte-me mais sobre" ou "Obter ajuda com isso".

    **Incorreto:**

    Saiba mais sobre como adicionar exceções

    **Correto:**

    Quais são os riscos de permitir exceções?

    Como fazer adicionar exceções?

    Nos exemplos corretos, o link é formulado em termos da pergunta principal respondida pelo tópico Ajuda.

-   Se as informações mais relevantes puderem ser resumidas de forma sucinta, coloque o resumo diretamente na interface do usuário em vez de usar um link da Ajuda. No entanto, você pode usar um link da Ajuda para fornecer informações complementares.

    **Incorreto:**

    ![captura de tela do link para o que é uma senha forte? ](images/winenv-help-image14.png)

    **Correto:**

    ![captura de tela de texto complementar sobre senhas ](images/winenv-help-image15.png)

    **Melhor:**

    ![captura de tela de texto com link para mais informações ](images/winenv-help-image16.png)

    O exemplo correto resume as informações da Ajuda de forma sucinta, melhorando muito a probabilidade de que os usuários as leiam. O melhor exemplo fornece um link de Ajuda para obter mais informações sobre esse assunto complexo.

-   A Ajuda de Frase é links para indicar claramente a assistência. Os links de ajuda nunca devem ser lidos como links de ação.
-   Use todo o link da Ajuda para o texto do link, não apenas as palavras-chave.

    **Correto:**

    Quais são os riscos de permitir exceções?

    **Incorreto:**

    Quais são os riscos de permitir exceções?

    No exemplo correto, toda a frase de link da Ajuda é usada para o texto do link.

    -   **Exceção:** Os links de ajuda para sites externos devem simplesmente usar o nome do site ou da página como o link. Qualquer texto que introduza o nome do site não precisa ser incluído no próprio link.

-   Os links de ajuda não têm que corresponder exatamente aos títulos do tópico da Ajuda, mas deve haver uma conexão forte e óbvia entre os dois. Criar links e títulos em pares por esse motivo.

    **Correto:**

    Como posso melhorar o desempenho desse recurso? (texto do link)

    Configurando esse recurso para um desempenho ideal (título do tópico)

    **Incorreto:**

    Como posso melhorar o desempenho desse recurso? (texto do link)

    Visão geral completa desse recurso (título do tópico)

    No exemplo incorreto, o título do tópico Ajuda difere substancialmente no escopo do texto do link da Ajuda e pode ser um erro.

-   Se o conteúdo da Ajuda estiver online, limpe isso no texto do link. Isso ajuda a tornar o resultado dos links previsível.

    **Correto:**

    Para obter mais formatos e ferramentas, acesse o site da Microsoft.

    **Incorreto:**

    Onde posso encontrar ferramentas e formatos adicionais?

-   Use frases completas.
-   Não use pontuação final, exceto para pontos de interrogação.
-   Não use re elipses para links ou comandos de Ajuda.

**Conteúdo da Ajuda**

-   Formatar elementos de interface do usuário usando negrito para torná-los fáceis de identificar. Isso é especialmente útil para tópicos de Ajuda de procedimento, permitindo que os usuários digitalizarem procedimentos e vejam rapidamente os elementos pertinentes da interface do usuário.
-   Formatar legendas usando itálico. Isso se aplica a tabelas, arte, capturas de tela e outros elementos gráficos que se beneficiam de uma breve explicação textual.
-   Consulte Ajuda simplesmente como Ajuda. Em geral, não use a frase Ajuda online, a menos que você esteja, na verdade, se referindo ao conteúdo em seu site.

 

