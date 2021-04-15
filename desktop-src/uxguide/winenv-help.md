---
title: Ajuda
description: Use a ajuda como um mecanismo secundário para ajudar os usuários a concluir e entender melhor as tarefas \ 8212; o mecanismo principal é a própria interface do usuário. Aplique essas diretrizes para tornar o conteúdo verdadeiramente útil e fácil de encontrar.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 907494e9a97ccaf51e4eba463c34e49854b14a81
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104569595"
---
# <a name="help"></a>Ajuda

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Use a ajuda como um mecanismo secundário para ajudar os usuários a concluir e compreender melhor as tarefas o mecanismo principal sendo a própria interface do usuário. Aplique essas diretrizes para tornar o conteúdo verdadeiramente útil e fácil de encontrar.

Um sistema de ajuda é composto por vários tipos de conteúdo projetados para ajudar os usuários quando eles não conseguem concluir uma tarefa, deseja entender um conceito em mais detalhes ou precisar de mais detalhes técnicos do que estão disponíveis na interface do usuário.

Neste artigo, vamos nos referir a ajuda como secundária à interface do usuário. A interface do usuário é primária porque é onde os usuários primeiro tentam resolver seus problemas. Eles consultarão o sistema de ajuda somente se não puderem realizar suas tarefas com a interface do usuário.

![captura de tela da página de ajuda e suporte do Windows ](images/winenv-help-image1.png)

O home page de ajuda e suporte do Windows, disponível no menu iniciar.

**Observação:** As diretrizes relacionadas ao [estilo e ao Tom](text-style-tone.md) são apresentadas em um artigo separado.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

-   **Como os usuários de destino são motivados?** Quanto mais motivado eles forem descobrir a funcionalidade do seu programa e se tornarem usuários intermediários ou até mesmo avançados, mais disposto eles serão a pesquisa de respostas para suas dúvidas por tópicos de ajuda de consultoria.
-   **Você está usando a ajuda para corrigir uma interface do usuário inadequada?** Quanto melhor sua interface do usuário, menos usuários irão buscar ajuda adicional. Se o seu programa tiver uma interface do usuário primária muito clara e útil (como mensagens de erro sem jargão, assistentes bem escritos e caixas de diálogo não ambíguas), talvez você não precise de um sistema de ajuda secundário.
-   **Seu programa é relativamente simples?** Nesse caso, considere incorporar todo o conteúdo de assistência necessário às suas superfícies da interface do usuário primária. É mais provável que os usuários busquem ajuda adicional em programas que executam tarefas complexas.
-   **Seu aplicativo destina-se a desenvolvedores, profissionais de ti ou outros especialistas em software?** Esses usuários tendem a esperar ajuda de referência para convenções de linguagem de programação e ajuda conceitual detalhada para dominar os recursos.

## <a name="design-concepts"></a>Conceitos de design

Se você decidir incluir ajuda em seu programa, integre-a ao seu design geral. A interface da ajuda deve ser simples, eficiente e relevante; Ele deve permitir que os usuários obtenham ajuda facilmente e, em seguida, retornem à sua tarefa. Considere o sistema de ajuda em termos de tempo dos usuários: Minimize a interrupção primeiro, antecipando onde elas encontrarão problemas em seu programa, resolvendo esses problemas incorporando assistência fundamental diretamente à sua interface do usuário e criando pontos de entrada claros e consistentes em sua ajuda mais detalhada.

A assistência do Windows foi projetada de acordo com esses princípios. Aqui estão algumas das alterações de design na experiência do usuário da ajuda do Windows:

-   Pontos de entrada mais detectáveis para ajudar da interface do usuário principal (especialmente novos links de ajuda de superfícies de interface do usuário, como caixas de diálogo, mensagens de erro e assistentes). Os links de ajuda levam você diretamente para o tópico pertinente na ajuda.
-   Um ícone de botão de ajuda está disponível no canto superior direito da maioria das páginas do Hub do painel de controle, bem como pastas do Shell.
-   Os usuários podem optar por obter o conteúdo mais atualizado da ajuda de ajuda online do Windows e suporte quando estiverem online.
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

Não é necessário fornecer ajuda para todos os recursos na interface do usuário. **Com muita frequência, os resultados da ajuda não ajudam a tentar criar ajuda para tudo.** Se a interface do usuário for bem projetada, a maioria desses tópicos da ajuda não será muito útil; Eles apenas reafirmam o óbvio.

Se houver mais de uma maneira de executar uma tarefa, na maioria dos casos, você poderá apenas documentar a maneira mais comum usada pelos usuários inexperientes. Exceções a isso incluem considerações sobre acessibilidade (documentando equivalentes de teclado de ações do mouse, por exemplo) e considerações sobre a plataforma (documentando o fator forma do Tablet, por exemplo, ou para ambientes de servidor nos quais a linha de comando pode substituir pela interface gráfica do usuário).

Lembre-se de que os usuários geralmente não consideram os problemas que estão encontrando exatamente os mesmos termos que você faz. Por exemplo, os usuários podem achar estranho se considerarem como uma "conta". Certifique-se de projetar sua funcionalidade de pesquisa e indexação e, em seguida, para considerar variações e sinônimos de terminologia prováveis.

No entanto, entre a interface do usuário principal e o sistema de ajuda, os termos devem ser muito semelhantes se não forem idênticos. Os usuários podem ser confundidos quando o idioma do sistema de ajuda não se correlacionar muito bem ao que estão vendo na tela.

### <a name="writing-compelling-help-link-text"></a>Escrevendo texto de link de ajuda atraente

Ao vincular a um tópico da ajuda de sua interface do usuário principal, certifique-se de escrever um texto de link de ajuda atraente. A clara e a linguagem específica inspire a confiança. Os usuários tendem a acreditar que os links de ajuda genéricos (um botão com a palavra "ajuda" ou "Saiba mais" sobre ele) não levarão às informações certas sem um investimento significativo de tempo.

**Se você fizer apenas cinco coisas...**

1.  Crie sua interface do usuário para que os usuários não precisem de ajuda.
2.  Torne sua ajuda útil concentrando-se no conteúdo das principais perguntas nos principais cenários de seus usuários de destino.
3.  Apresente o conteúdo da ajuda para que seja fácil de verificar.
4.  Entenda que você não precisa fornecer ajuda para cada recurso na interface do usuário.
5.  Torne os pontos de entrada da ajuda detectáveis e atraentes.

## <a name="usage-patterns"></a>Padrões de uso

Diferentes tipos de conteúdo têm finalidades diferentes.



|                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ajuda de procedimentos**<br/> fornece as etapas para executar uma tarefa. <br/>                       | A ajuda de procedimentos deve se concentrar nas informações de "como" em vez de "o que" ou "por quê". <br/> ![captura de tela da página de ajuda ' excluir arquivos temporários ' ](images/winenv-help-image2.png)<br/> Neste exemplo, o tópico da ajuda descreve como usar um recurso do utilitário limpeza de disco, fornecendo as etapas a serem seguidas em sequência.<br/>                                              |
| **Ajuda conceitual**<br/> fornece informações básicas, visões gerais de recursos ou processos. <br/> | A ajuda conceitual deve fornecer "What" ou "por que" informações além daquelas necessárias para concluir uma tarefa. <br/> ![captura de tela da página de ajuda da ' área de trabalho (visão geral) ' ](images/winenv-help-image3.png)<br/> Neste exemplo, o tópico da ajuda define o que é a área de trabalho e fornece detalhes adicionais sobre o que ele contém e por que os usuários interagem com ele.<br/>           |
| **Ajuda de referência**<br/> serve como um livro de referência online. <br/>                                | Você pode usar a ajuda de referência para documentar uma linguagem de programação ou interfaces de programação. <br/> ![captura de tela da página de ajuda de ' convenções de notação ' ](images/winenv-help-image4.png)<br/> Neste exemplo, o tópico da ajuda lista as convenções tipográficas em uso para esse idioma ou aplicativo específico, fornecendo as informações em uma tabela de fácil verificação.<br/> |



 

## <a name="guidelines"></a>Diretrizes

### <a name="entry-points"></a>Pontos de entrada

-   **Link para tópicos de ajuda específicos e relevantes.** Não vincule ao home page de ajuda, ao Sumário, a uma lista de resultados da pesquisa ou a uma página que apenas se vincula a outras páginas. Evite vincular a páginas estruturadas como uma grande lista de perguntas frequentes, pois ela força os usuários a procurar aquele que corresponda ao link em que eles clicaram. Não vincule a tópicos de ajuda específicos que não são relevantes e úteis para a tarefa em questão. Nunca vincular a páginas vazias.
-   **Não coloque links de ajuda em todas as janelas ou páginas para fins de consistência.** Fornecer um link de ajuda em um único lugar não significa que você precisa fornecê-los em todos os lugares.
-   **Use links de ajuda para caixas de diálogo, mensagens de erro, assistentes e folhas de propriedades.** Se o link da ajuda se aplicar a controles específicos, coloque-os sob eles, alinhados à esquerda. Se o link de ajuda se aplicar a toda a janela, coloque-o no canto inferior esquerdo da área de conteúdo da janela.

    ![captura de tela da folha de propriedades com a caixa de grupo ](images/winenv-help-image5.png)

    Neste exemplo, o segundo link de ajuda se aplica a um grupo de controles.

    ![captura de tela da folha de propriedades e link de ajuda ](images/winenv-help-image6.png)

    Neste exemplo, o link de ajuda se aplica a toda a janela.

-   **Use links de ajuda em vez de referências textuais genéricas para ajudar sempre que possível tecnicamente.**

    **Correto:**

    Como posso reparar erros de disco?

    **Incorreto:**

    Para obter mais informações sobre como reparar erros de disco, consulte ajuda e suporte.

-   **Use um botão ajuda com o ícone de ajuda para as páginas de Hub dos itens do painel de controle.** Coloque-o no canto superior direito. Esses botões não têm um rótulo, mas têm uma dica de ferramenta que lê a ajuda.

    ![captura de tela do item do painel de controle com o botão ajuda ](images/winenv-help-image7.png)

    Um item do painel de controle com um botão de ajuda.

-   **A ajuda F1 é opcional.** Os usuários se acostumaram a encontrar informações de ajuda relacionadas ao contexto imediato da interface do usuário na tela pressionando a tecla F1, que é rotulada como ajuda em teclados padrão. Você pode incluir a ajuda F1 se, por exemplo, estudos de usabilidade, mostrar que os usuários esperam encontrá-lo ou se a interface do usuário do programa é complexa o suficiente para se beneficiar da assistência contextual.
-   **Programas com barras de menu podem ter uma categoria de menu ajuda.** Para obter diretrizes do menu ajuda, consulte [menus](cmd-menus.md).

    ![captura de tela da ajuda acessada na barra de menus ](images/winenv-help-image8.png)

    Neste exemplo, o acessório de pintura do Windows tem uma categoria de menu ajuda.

-   **Para acessibilidade de teclado, forneça paradas de tabulação para botões de ajuda e links.**
-   O botão de ajuda e o comportamento do link devem ser os seguintes: o painel da ajuda é aberto e um tópico de ajuda dedicado é exibido; a interface do usuário que invocou o painel da ajuda deve permanecer aberta para preservar a experiência contextual.
-   **Não use os seguintes estilos de ponto de entrada de ajuda obsoletos: "Saiba mais" ou "Saiba mais sobre..." links, botões de ajuda genéricos e botões de ajuda sensíveis ao contexto na barra de título.** Embora eles tenham sido usados no passado, estudos de usabilidade determinaram que os usuários tendem a ignorá-los. Em vez disso, use links para tópicos de ajuda específicos. Para obter diretrizes sobre como escrever bons links de ajuda, consulte [links de ajuda](#text).

    **Incorreto:**

    ![captura de tela da caixa de diálogo com um link ' saiba mais ' ](images/winenv-help-image9.png)

    Não use "Saiba mais" ou "Saiba mais sobre..." Vincule.

    **Incorreto:**

    ![captura de tela do botão ajuda ao lado dos botões de confirmação ](images/winenv-help-image10.png)

    Não use botões de ajuda genéricos.

    **Incorreto:**

    ![captura de tela do ícone de ponto de interrogação na barra de título ](images/winenv-help-image11.png)

    Não use botões de ajuda sensíveis ao contexto na barra de título.

### <a name="content"></a>Conteúdo

-   **Não crie conteúdo óbvio.** Tópicos de ajuda que repetim o que está na interface do usuário principal não agregam valor.
-   **Não crie conteúdo que o usuário não possa agir de alguma maneira.**
    -   **Exceção:** Alguns conteúdos conceituais fornecem informações importantes sobre o plano de fundo sem necessariamente levar à ação do usuário.
-   **Evite resoluções vagas para problemas.** Por exemplo, "entre em contato com o administrador do sistema" ou "reinstalar o aplicativo" tendem a frustrar os usuários.
    -   **Exceção:** Recomende entrar em contato com o administrador do sistema se essa for a única solução prática e os administradores do sistema esperam ser contatados para o problema.
-   **Evite conteúdo que atenda a cenários de usuário altamente improvável.** Desenvolva seu conteúdo principal de ajuda para o que você prevê que será o uso normal; Observe exceções importantes para o uso esperado, mas trate esse conteúdo como uma prioridade mais baixa.
-   **Reúna comentários de seus usuários sobre como os tópicos de ajuda são úteis.** Permitir que os usuários classifiquem tópicos individuais. Conduza [estudos de usabilidade](glossary.md) em sua documentação para verificar problemas envolvendo a qualidade e a descoberta de conteúdo.
    -   **Dica:** Os comentários dos usuários também são uma ótima maneira de gerar mais conteúdo baseado em tarefas, com foco no que os usuários realmente estão fazendo com seu programa, em oposição ao conteúdo baseado em recursos, concentrando-se simplesmente em uma descrição da tecnologia.
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

## <a name="text"></a>Texto

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

 

