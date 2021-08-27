---
title: Texto da interface do usuário
description: Saiba mais sobre o texto da interface do usuário que aparece nas superfícies da interface do usuário.
ms.assetid: db42fe22-9baf-453a-9b89-9bbb251b0b6f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b24b6fd105c89484e1ef935141acfa91ef5b2b39
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481192"
---
# <a name="user-interface-text"></a>Texto da interface do usuário

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

O texto da interface do usuário é exibido nas superfícies da interface de usuários. Esse texto inclui rótulos de controle e texto estático:

-   Os rótulos de controle identificam controles e são colocados diretamente em ou ao lado dos controles.
-   Texto estático, que é tão chamado porque não faz parte de um controle interativo, fornece aos usuários instruções detalhadas ou explicações para que eles possam tomar decisões informadas.

**Observação:** As diretrizes relacionadas a rótulos de controle de [estilo e Tom](text-style-tone.md), [fontes](vis-fonts.md)e [controles](controls.md) de as são apresentadas em artigos separados.

## <a name="usage-patterns"></a>Padrões de uso

O texto da interface do usuário tem vários padrões de uso:



|   Uso                                                                                                                                                                                          |    Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Texto da barra de título**<br/> Use o texto da barra de título para identificar uma janela ou a origem de uma caixa de diálogo. <br/>                                                                            | ![captura de tela da barra de título de opções de pasta](images/text-ui-image1.png)<br/> Neste exemplo, o texto da barra de título identifica uma janela.<br/>                                                                                                                                                                                                                                                                                                             |
| **Instruções principais**<br/> Use a instrução principal proeminente para explicar de forma concisa o que fazer na janela ou na página. <br/>                                                      | A instrução deve ser uma instrução específica, uma direção imperativa ou uma pergunta. boas instruções principais comunicam o objetivo do usuário em vez de se concentrar apenas na manipulação da interface do usuário. <br/> ![captura de tela de pergunta: deseja obter a ajuda mais recente? ](images/text-ui-image2.png)<br/> Neste exemplo, o texto de instrução principal envolve diretamente o usuário com uma pergunta em termos de interesse ou benefício do usuário.<br/>             |
| **Instruções complementares**<br/> quando necessário, use uma instrução complementar para apresentar informações adicionais úteis para entender ou usar a janela ou a página. <br/> | Você pode fornecer informações mais detalhadas, fornecer contexto e definir a terminologia. instruções complementares elaboradas sobre a instrução principal sem simplesmente reformular a ti. <br/> ![captura de tela de texto ao alternar para a conta do administrador ](images/text-ui-image3.png)<br/> Neste exemplo, as instruções complementares fornecem dois possíveis cursos de ação a serem adotados em resposta às informações apresentadas na instrução principal.<br/> |
| **Rótulos de controle**<br/> rótulos diretamente no ou ao lado dos controles. <br/>                                                                                                           | ![captura de tela das opções de relógio da área de trabalho ](images/text-ui-image4.png)<br/> Neste exemplo, os rótulos de controle identificam as configurações de relógio da área de trabalho que os usuários podem selecionar ou modificar.<br/>                                                                                                                                                                                                                                                                       |
| **Explicações suplementares**<br/> um elaboration dos rótulos de controle (normalmente para links de comando, botões de opção e caixas de seleção). <br/>                                    | ![Captura de tela que mostra uma caixa de diálogo Configurações de segurança.](images/text-ui-image5.png)<br/> Neste exemplo, as explicações suplementares esclarecem as opções.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="design-concepts"></a>Conceitos de design

Os desenvolvedores de software geralmente consideram o texto relegado à documentação do produto e ao suporte técnico. "Primeiro vamos escrever o código e, em seguida, contrataremos alguém para nos ajudar a explicar o que desenvolvemos." Ainda na realidade, o texto importante é escrito anteriormente no processo, pois a interface do usuário é concebida e codificada. Esse texto é, afinal, visto com mais frequência e por mais pessoas do que talvez qualquer outro tipo de escrita técnica.

**O texto abrangente é crucial para a interface do usuário efetiva.** Professional gravadores e editores devem funcionar com desenvolvedores de software no texto da interface do usuário como parte integrante do processo de design. Faça com que eles trabalhem no texto antecipadamente porque problemas de texto geralmente revelam problemas de design. Se sua equipe tiver problemas para explicar um design, com muita frequência ele é o design, não a explicação, que precisa de melhoria.

### <a name="a-design-model-for-ui-text"></a>Um modelo de design para texto da interface do usuário

Como você imagina o texto da interface do usuário e seu posicionamento nas suas superfícies de interface do usuário, considere estes fatos:

-   Durante o foco, a leitura de imersão, as pessoas lidam em uma ordem da esquerda para a direita, de cima para baixo (em culturas ocidentais).
-   Ao usar o software, os usuários não estão imersos na própria interface do usuário, mas em seu trabalho. Consequentemente, os usuários não lêem o texto da interface do usuário que o examinam.
-   Ao digitalizar uma janela, os usuários podem parecer ler o texto quando, na realidade, estão filtrando. Em geral, eles não entendem verdadeiramente o texto da interface do usuário, a menos que eles se compreendam a necessidade.
-   Em uma janela, diferentes elementos da interface do usuário recebem diferentes níveis de atenção. Os usuários tendem a ler os rótulos de controle primeiro, especialmente aqueles que parecem relevantes para concluir a tarefa em questão. Por outro lado, os usuários tendem a ler texto estático apenas quando acham que precisam.

Para um modelo de design geral, não assuma que os usuários leiam atentamente o texto em uma ordem da esquerda para a direita, de cima para baixo. Em vez disso, suponha que os usuários comecem verificando rapidamente toda a janela e, em seguida, leia o texto da interface do usuário em aproximadamente a seguinte ordem:

-   Controles interativos no centro
-   Os [botões de confirmação](glossary.md)
-   Controles interativos encontrados em outro lugar
-   Instrução principal
-   Explicações suplementares
-   Título da janela
-   Outro texto estático no corpo principal
-   Notas de rodapé

Você também deve supor que, depois que os usuários decidirem o que fazer, eles imediatamente irão parar de ler e fazer isso.

### <a name="eliminate-redundancy"></a>Eliminar redundância

O texto redundante não só leva um espaço de tela valioso, mas enfraquece a eficácia das ideias ou ações importantes que você está tentando transmitir. Também é um desperdício do tempo do leitor, e tudo isso em um contexto em que a verificação é a norma. **Windows se esforça para explicar o que os usuários precisam fazer uma única vez e concisamente.**

Examine cada janela e elimine palavras e instruções duplicadas, dentro e entre os controles. Não evite que textos importantes sejam explícitos sempre que necessário, mas não sejam redundantes e não expliquem o óbvio.

### <a name="avoid-over-communication"></a>Evitar comunicação excessiva

Mesmo que o texto não seja redundante, ele pode simplesmente ser um pouco simples em um esforço para explicar cada detalhe. **O excesso de texto não incentiva a leitura do olho tende a ignorar a ti de forma Ironic, resultando em menos comunicação em vez de mais.** No texto da interface do usuário, comunique-se de forma concisa as informações essenciais. Se mais informações forem necessárias para alguns usuários ou alguns cenários, forneça um link para o conteúdo mais detalhado da [ajuda](winenv-help.md)ou talvez em uma entrada de glossário para esclarecimentos de um termo.

**Incorreto:**

![captura de tela da caixa de diálogo com 6 parágrafos](images/text-ui-image6.png)

Neste exemplo, há muito texto para examinar facilmente. Embora não seja destinado ao designer, há muito texto que provavelmente os usuários clicarão em avançar sem ler nada.

Para evitar texto que desanime a leitura, crie seu texto para fazer cada contagem de palavras. O que não adiciona subtração, portanto, use texto simples e conciso.

### <a name="use-the-inverted-pyramid"></a>Usar a pirâmide invertida

A escrita acadêmica normalmente usa um estilo estrutural "pirâmide" que apresenta uma base de fatos, trabalha com esses fatos e cria até uma conclusão formando uma estrutura semelhante a pirâmide. Por outro lado, os jornalistas usam um estilo de "pirâmide invertida" que começa com a conclusão do "argumento" fundamental que os leitores devem ter. Em seguida, ele preenche progressivamente mais detalhes que os leitores podem estar interessados em talvez apenas examinar. A vantagem desse estilo é que ele fica certo até o ponto e permite que os leitores parem de ler a qualquer momento que escolherem e ainda compreendam as informações essenciais.

Você deve aplicar a estrutura de pirâmide invertida ao texto da interface do usuário. Fique à direita até o ponto com as informações essenciais, deixe que os usuários parem de ler a qualquer momento que escolherem e use um link de ajuda para apresentar o restante da pirâmide.

![captura de tela de mensagem ao ingressar no programa do Windows ](images/text-ui-image7.png)

Neste exemplo, as informações essenciais estão na consulta do texto de instrução principal, informações úteis adicionais estão nas instruções complementares e os detalhes estão disponíveis ao clicar em um link de ajuda.

**Se você fizer apenas cinco coisas...**

1.  Trabalhe no texto antecipadamente porque problemas de texto geralmente revelam problemas de design.
2.  Projete seu texto para verificação.
3.  Elimine o texto redundante.
4.  Use texto fácil de entender; Não se comunique mais.
5.  Quando necessário, forneça links para o conteúdo da ajuda para obter informações mais detalhadas.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Remova texto redundante.** Procure texto redundante em títulos de janela, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de commit. Em geral, deixe o texto completo nas instruções principais e controles interativos e remova qualquer redundância de outros locais.
-   **Evite grandes blocos de texto da interface do usuário.** As maneiras de fazer isso incluem:
    -   Em partes de texto em frases e parágrafos mais curtos.
    -   Quando necessário, fornecer [links de Ajuda](winenv-help.md) para informações úteis, mas não essenciais.
-   **Escolha nomes de objeto e rótulos que se comunicam claramente e diferenciem o que o objeto faz.** Os usuários não devem ter que descobrir o que o objeto realmente significa ou como ele difere de outros objetos.

    Incorreto:

    ![captura de tela da lista de monitores sem nome](images/text-ui-image8.png)

    Melhor:

    ![captura de tela da lista de adaptadores de rede específicos](images/text-ui-image9.png)

    No exemplo incorreto, os nomes de objeto não são diferenciados; o exemplo melhor mostra uma diferenciação forte por nome do produto.

-   **Se você quiser garantir que os usuários leiam textos específicos relacionados a uma ação, coloque-o em um controle interativo.**
    -   **Aceitável:**
    -   ![captura de tela do aviso de formatação usando o botão OK ](images/text-ui-image10.png)
    -   Neste exemplo, há uma chance de os usuários não lerem o texto que explica o que eles estão confirmando.
    -   **Melhor:**
    -   ![captura de tela do botão de aviso e formato de formatação ](images/text-ui-image11.png)
    -   Neste exemplo, você pode ter certeza de que pelo menos os usuários entendem que estão prestes a formatar um disco.
-   **Use um espaço entre frases.** Não dois.

### <a name="text-fonts-sizes-and-colors"></a>Fontes de texto, tamanhos e cores

-   **Use texto azul somente para links e instruções principais.**
-   **Use texto verde somente para URLs nos resultados da pesquisa.**

As fontes e as cores a seguir são padrões para Windows.



| Padrão                                                                                     | Símbolo de tema                            | Fonte, Cor                                                           |
|--------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![primeira coluna: texto da barra de título ](images/text-ui-image12.png)<br/>              | CaptionFont<br/>      | 9 pt. preto ( \# 000000) Segoe UI<br/>                 |
| ![primeira coluna: instruções principais ](images/text-ui-image13.png)<br/>           | MainInstruction<br/>  | 12 pt. blue ( \# 003399) Segoe UI<br/>                 |
| ![primeira coluna: instruções secundárias ](images/text-ui-image14.png)<br/>      | Instrução<br/>      | 9 pt. preto ( \# 000000) Segoe UI<br/>                 |
| ![primeira coluna: texto normal ](images/text-ui-image15.png)<br/>                 | Bodytext<br/>         | 9 pt. preto ( \# 000000) Segoe UI<br/>                 |
| ![primeira coluna: texto enfatizado ](images/text-ui-image16.png)<br/>             | Bodytext<br/>         | 9 pt. preto ( \# 000000) Segoe UI, negrito ou itálico<br/> |
| ![primeira coluna: texto editável ](images/text-ui-image17.png)<br/>               | Bodytext<br/>         | 9 pt. preto ( \# 000000) Segoe UI, em uma caixa<br/>       |
| ![primeira coluna: texto desabilitado ](images/text-ui-image18.png)<br/>               | Desabilitado<br/>         | 9 pt. cinza-escuro \# (323232) Segoe UI<br/>             |
| ![primeira coluna: link ](images/text-ui-image19.png)<br/>                        | HyperLinkText<br/>    | 9 pt. blue ( \# 0066CC) Segoe UI<br/>                  |
| ![primeira coluna: links (foco) ](images/text-ui-image20.png)<br/>               | Frequente<br/>              | 9 pt. azul-claro ( \# 3399FF) Segoe UI<br/>            |
| ![primeira coluna: título do grupo ](images/text-ui-image21.png)<br/>                |  <br/>                | 11 pt. blue ( \# 003399) Segoe UI<br/>                 |
| ![primeira coluna: nome do arquivo (na exibição de conteúdo) ](images/text-ui-image22.png)<br/> |  <br/>                | 11 pt. preto ( \# 000000) Segoe UI<br/>                |
| ![primeira coluna: texto do documento ](images/text-ui-image23.png)<br/>               | (nenhum)<br/>           | 9 pt. black ( \# 000000) Californiabri<br/>                  |
| ![primeira coluna: títulos de documento ](images/text-ui-image24.png)<br/>           | (nenhum)<br/>           | 17 pt. black ( \# 000000) Californiabri<br/>                 |



 

Para obter mais informações e exemplos, consulte [Fontes e](vis-fonts.md) [cores.](vis-color.md)

### <a name="other-text-characteristics"></a>Outras características de texto

**Negrito**

-   **Use negrito com moderação para chamar a atenção para o texto que os usuários devem ler.** Por exemplo, os usuários que examinam uma lista de opções de botão de opção podem gostar de ver os rótulos em negrito, para se destacar do texto que adiciona informações complementares sobre cada opção. Esteja ciente de que o uso de negrito demais diminui seu impacto.
-   **Com os dados rotulados, use negrito para enfatizar o que for mais importante para os dados como um todo.**
    -   Para dados genéricos principalmente (em que os dados têm pouco significado sem seus rótulos, como com numerais ou datas), use rótulos em negrito e dados simples para que os usuários possam examinar e entender mais facilmente os tipos de dados.
    -   Para dados principalmente autoexplicativos, use rótulos simples e dados em negrito para que os usuários possam se concentrar nos dados em si.
    -   Como alternativa, você pode usar texto cinza escuro para des enfatizar informações menos importantes em vez de usar negrito para enfatizar as informações mais importantes.

        ![captura de tela da exibição em miniatura do Windows Explorer ](images/text-ui-image25.png)

        Neste exemplo, em vez de enfatizar os dados usando negrito, os rótulos são des enfatizados usando cinza-escuro.

-   **Nem todas as fontes são suportadas em negrito, portanto, nunca deve ser crucial entender o texto.**

**Itálico**

-   Use para se referir ao texto literalmente. Não use aspas para essa finalidade.

    **Correto:**

    Os termos documento e arquivo geralmente são usados de forma intercambiável.

-   Use para [prompts](glossary.md) em [caixas de texto](ctrl-text-boxes.md) e listas de listas [listadas editáveis.](/windows/desktop/uxguide/ctrl-drop)

    ![captura de tela da caixa de texto de pesquisa ](images/text-ui-image26.png)

    Neste exemplo, o prompt na caixa Pesquisa é formatado como texto itálico.

-   Use com moderação para enfatizar palavras específicas para ajudar na compreensão.
-   **Nem todas as fontes suportam itálico, portanto, nunca deve ser crucial entender o texto.**

**Itálico em negrito**

-   Não use no texto da interface do usuário.

**Underline**

-   Não use, exceto para links.
-   Não use para ênfase. Em vez disso, use itálico.

### <a name="punctuation&quot;></a>Pontuação

**Períodos**

-   **Não coloque no final dos rótulos de controle, das instruções principais ou dos links de Ajuda.**
-   Coloque no final de instruções complementares, explicações complementares ou qualquer outro texto estático que forma uma frase completa.

**Pontos de interrogação**

-   **Coloque no final de todas as perguntas.** Ao contrário dos períodos, os pontos de interrogação são usados para todos os tipos de texto.

**Pontos de exclamação**

-   Em aplicativos de negócios, evite.
    -   **Exceções:** Pontos de exclamação às vezes são usados no contexto de conclusão do download (&quot;Concluído!") e para chamar a atenção para o conteúdo da Web ("Novo!").

**Vírgulas**

-   Em uma lista de três ou mais itens, sempre coloque uma vírgula após o próximo ao último item na lista.

**Vírgula**

-   **Use dois-pontos no final dos rótulos de controle externo.** Isso é particularmente importante para acessibilidade porque algumas tecnologias adaptativas procurarão dois-pontos para identificar rótulos de controle.
-   Use dois-pontos para introduzir uma lista de itens.

**Elipses**

-   **As re elipses significam a incompleta.** Use re elipses no texto da interface do usuário da seguinte forma:
    -   **Comandos:** Indique que um comando precisa de informações adicionais. Não use reellipses sempre que uma ação exibir outra janela somente quando informações adicionais são necessárias. Para obter mais informações, consulte [Botões de comando](ctrl-command-buttons.md).
    -   **Dados:** Indique que o texto está truncado.
    -   **Rótulos:** Indique que uma tarefa está em andamento (por exemplo, "Pesquisando...").

        **Dica:** Texto truncado em uma janela ou página com espaço nãoutilado indica um layout ruim ou um tamanho de janela padrão muito pequeno. Busque layouts e tamanhos de janela padrão que eliminam ou reduzem a quantidade de texto truncado. Veja [Layout](vis-layout.md) para obter mais informações.

-   **Não tornar as reellips interativas.** Para mostrar texto truncado, deixe que os usuários reesizem o controle para ver mais texto ou usem um [controle de divulgação progressiva.](ctrl-progressive-disclosure-controls.md)

**Aspas e apóstrofos**

-   Para se referir ao texto literalmente, use a formatação itálico em vez de aspas.
-   Coloque títulos de janela e rótulos de controle entre aspas somente se necessário para evitar confusão e você não poderá formatar usando negrito.
-   Para aspas, prefira aspas duplas (" "); evite aspas simples.

    **Correto:**

    Tem certeza de que deseja excluir a "pasta de gatos do Sparky"?

    **Incorreto:**

    Tem certeza de que deseja excluir a 'pasta de gatos do Sparky'?

### <a name="capitalization"></a>Uso de maiúsculas

-   **Use a capitalização de estilo de título para títulos, capitalização de estilo de frase para todos os outros elementos da interface do usuário.** Fazer isso é mais apropriado para o [Windows tom](text-style-tone.md).

    -   **Exceção:** Para aplicativos herdado, você pode usar a capitalização de estilo de título para botões de comando, menus e títulos de coluna, se necessário, para evitar a combinação de estilos de capitalização.

        ![captura de tela da folha de propriedades genéricas ](images/text-ui-image27.png)

    Este exemplo genérico mostra a capitalização e a pontuação corretas para folhas de propriedades.

    ![captura de tela da caixa de diálogo genérica ](images/text-ui-image28.png)

    Este exemplo genérico mostra a capitalização e pontuação corretas para diálogos.

-   **Para nomes de recursos e tecnologias, seja conservadora na capitalização.** Normalmente, somente os componentes principais devem ser em maiúsculas (usando a capitalização de estilo de título).

    **Correto:**

    Analysis Services, cubos, dimensões

    Analysis Services é um componente principal do SQL Server, portanto, a capitalização de estilo de título é apropriada; cubos e dimensões são elementos comuns do software de análise de banco de dados, portanto, é desnecessário capitalizá-los.

-   **Para nomes de recursos e tecnologias, seja consistente na capitalização.** Se o nome aparecer mais de uma vez em uma tela de interface do usuário, ele sempre deverá aparecer da mesma maneira. Da mesma forma, em todas as telas da interface do usuário no programa, o nome deve ser apresentado consistentemente.
-   Não use maiúsculas os nomes dos elementos de interface do usuário genéricos, como barra de ferramentas, menu, barra de rolagem, botão e ícone.
    -   **Exceções:** Barra de endereços, barra links.
-   Não use todas as letras maiúsculas para teclas de teclado. Em vez disso, siga a capitalização usada por teclados padrão ou minúsculas se a tecla não estiver rotulada no teclado.

    **Correto:**

    barra de espaços, Guia, Inserir, Página Para Cima, Ctrl+Alt+Del

    **Incorreto:**

    BARRA DE ESPAÇOS, GUIA, ENTER, PG UP, CTRL+ALT+DEL

-   **Não use todas as letras maiúsculas para ênfase.** Os estudos mostraram que isso é difícil de ler e os usuários tendem a considerar isso como "complicado". Para avisos, use um ícone de aviso e uma explicação claramente detalhada da situação. Não é necessário adicionar, por exemplo, o termo WARNING em todas as letras maiúsculas.

Para obter mais informações, consulte a seção "Texto" ou "Rótulos" nas diretrizes de componente de interface do usuário específicas.

### <a name="dates-and-times"></a>Datas e horas

-   **Não em código o formato de datas e horas.** Respeitar a escolha do usuário das opções de localidade e personalização para os formatos de data e hora. O usuário os seleciona no item do painel de controle Região e Idioma.

    ![captura de tela do formato de data: segunda-feira, 06 de julho de 2009](images/text-ui-image29.png)![captura de tela do formato de data: 06 de julho de 2009](images/text-ui-image30.png)

    Nesses exemplos do Microsoft Outlook, os dois formatos para a data longa estão corretos. Eles refletem diferentes escolhas que os usuários fizeram no item do painel de controle Região e Idioma.

-   **Use o formato de data longa para cenários que se beneficiam de ter informações adicionais.** Use o formato de data curta para contextos que não têm espaço suficiente para o formato longo. Embora os usuários escolham quais informações eles querem incluir nos formatos longo e curto, os designers escolhem qual formato exibir em seus programas com base no cenário e no contexto.

    ![captura de tela do formato com datas de início e de vencimento](images/text-ui-image31.png)

    Neste exemplo, o formato de data longa ajuda os usuários a organizar tarefas e prazos.

### <a name="globalization-and-localization"></a>Globalização e localização

Globalização significa criar documentos ou produtos que podem ser usáveis em qualquer país, região ou cultura. A localização significa adaptar documentos ou produtos para uso em uma localidade diferente do país/região de origem. Considere globalização e localização ao escrever texto da interface do usuário. Seu programa pode ser convertido em outros idiomas e usado em culturas muito diferentes das suas.

-   Para controles com conteúdo variável (como exibições de lista e exibições de árvore), escolha **uma largura apropriada para os dados válidos mais longos.**
-   Inclua espaço suficiente na superfície da interface do usuário para um adicional de **30%** (até 200% para texto mais curto) para qualquer texto (mas não números) que será localizado. A tradução de um idioma para outro geralmente altera o comprimento da linha do texto.
-   Não componha cadeias de caracteres de substrings em tempo de executar. Em vez disso, use frases completas para que não haja ambiguidade para o tradutor.
-   **Não use um controle subordinado, os valores que ele contém ou seu rótulo de unidades para criar uma frase ou frase.** Esse design não é localizável porque a estrutura de frase varia de acordo com o idioma.

    **Incorreto:**

    ![captura de tela da caixa de texto dentro de um rótulo de caixa de seleção ](images/text-ui-image32.png)

    **Correto:**

    ![captura de tela da caixa de texto após um rótulo de caixa de seleção ](images/text-ui-image33.png)

    No exemplo incorreto, a caixa de texto é colocada dentro do rótulo da caixa de seleção.

-   Não faça apenas parte de uma frase um link, porque, quando traduzido, esse texto pode não permanecer junto. Portanto, o texto do link deve formar uma frase completa por si só.
    -   **Exceção:** Os links do glossário podem ser inseridos em linha, como parte de uma frase.

Para obter mais informações, consulte [Go Global Developer Center](https://msdn.microsoft.com/goglobal/).

### <a name="title-bar-text"></a>Texto da barra de título

-   Escolha o texto da barra de título com base no tipo de janela:
    -   **Janelas de programa centradas em documentos de nível superior:** Use um formato "nome do programa de nome do documento". Os nomes de documentos são exibidos primeiro para dar uma sensação centrada em documento.
    -   **Janelas de programa de nível superior que não são centradas em documentos:** Exibe apenas o nome do programa.
    -   **Caixas de diálogo:** Exibe o comando, o recurso ou o programa do qual a caixa de diálogo veio. Não use o título para explicar a finalidade da caixa de diálogo que é a finalidade das instruções principais. Para obter mais diretrizes, consulte Caixas [de diálogo](win-dialog-box.md).
    -   **Assistentes:** Exibir o nome do assistente. Observe que a palavra "assistente" não deve ser incluída em nomes de assistente. Para obter mais diretrizes, consulte [Assistentes](win-wizards.md).
-   **Para janelas de programa de nível superior, se a legenda e o ícone da barra de título são exibidos em destaque na parte superior da janela, você pode ocultar a legenda e o ícone da barra de título para evitar redundância.** No entanto, você ainda precisa definir um título adequado internamente para uso por Windows.
-   **Para caixas de diálogo, não inclua as palavras "dialog" ou "progress" nos títulos.** Esses conceitos são implícitos e deixar essas palavras fora torna os títulos mais fáceis para os usuários verificarem.

### <a name="main-instructions"></a>Instruções principais

-   **Use a instrução principal para explicar concisamente o que os usuários devem fazer em uma determinada janela ou página.** Boas instruções principais comunicam o objetivo do usuário em vez de se concentrar apenas na manipulação da interface do usuário.
-   **Expresse a instrução principal na forma de uma direção imperativa ou pergunta específica.**

    **Incorreto:**

    ![captura de tela do nome do programa como instrução principal ](images/text-ui-image34.png)

    Neste exemplo, a instrução principal simplesmente declara o nome do programa; ele não convida explicitamente um curso de ação para o usuário tomar.

    **Exceções:** Mensagens de erro, mensagens de aviso e confirmações podem usar estruturas de frase diferentes em suas instruções principais.

-   **Use verbos específicos sempre que possível.** Verbos específicos (exemplos: conectar, salvar, instalar) são mais significativos para os usuários do que os genéricos (exemplos: configurar, gerenciar, definir).
    -   Para páginas do painel de controle e páginas do assistente, se você não puder usar um verbo específico, poderá preferir omitir completamente o verbo.

        **Aceitável:**

        Insira sua localidade, região e idioma

        **Melhor:**

        Localidade, região e idioma

    -   Para caixas de diálogo, como mensagens de erro e avisos, não omita o verbo.

-   Não se sinta obrigado a usar o texto de instrução principal se adiá-lo seria redundante ou óbvio no contexto da interface do usuário.

    ![captura de tela da caixa de diálogo Salvar como ](images/text-ui-image35.png)

    Neste exemplo, o contexto da interface do usuário já está muito claro; não é necessário adicionar texto de instrução principal.

-   **Seja conciso, use apenas uma única frase completa.** Pare a instrução principal até as informações essenciais. Se você precisa explicar mais alguma coisa, considere usar uma instrução complementar.
-   Use a capitalização com estilo de frase.
-   **Não inclua períodos finais se a instrução for uma instrução.** Se a instrução for uma pergunta, inclua um ponto de interrogação final.
-   **Para diálogos de progresso, use uma frase gerund** explicando brevemente a operação em andamento, terminando com reellipse. Exemplo: "Imprimindo suas imagens..."
-   **Dica:** Você pode avaliar uma instrução principal ao explicar o que você poderia dizer a um amigo ao explicar o que fazer com a janela ou a página. Se responder com a instrução principal for anormal, insínteante ou inconveniente, retrabalho a instrução.

Para obter mais informações, consulte a seção "Instrução principal" nas diretrizes de componente de interface do usuário específicas.

### <a name="supplemental-instructions"></a>Instruções complementares

-   Quando necessário, **use uma instrução complementar para apresentar informações adicionais úteis** para entender ou usar a janela ou a página, como:
    -   Fornecendo contexto para explicar por que a janela está sendo exibida se ela é iniciada pelo programa ou pelo sistema.
    -   Informações de qualificação que ajudam os usuários a decidir como agir na instrução principal.
    -   Definindo terminologia importante.
-   **Não use uma instrução complementar se não for necessário.** Prefira comunicar tudo com a instrução principal se você puder fazer isso de forma concisa.
-   **Não repita a instrução principal com um texto ligeiramente diferente.** Em vez disso, omita a instrução complementar se não houver mais nada a adicionar.
-   Use frases completas e capitalização de estilo de frase.

### <a name="control-labels"></a>Rótulos de controle

-   **Rotule cada controle ou grupo de controles. Exceções:**
    -   Caixas de texto e listas listadas podem ser rotuladas usando prompts.
    -   Os controles de divulgação progressiva geralmente não têm rótulo.
    -   **Os controles subordinados usam o rótulo de seu controle associado.** Controles de rotação são sempre controles subordinados.
    -   **Omita rótulos de controle que restate a instrução principal.** Nesse caso, a instrução principal recebe a chave de acesso.

        **Aceitável:**

        ![captura de tela da caixa de texto com instrução e rótulo ](images/text-ui-image36.png)

        Neste exemplo, o rótulo da caixa de texto é apenas uma reformulação da instrução principal.

        **Melhor:**

        ![captura de tela da caixa de texto somente com instrução ](images/text-ui-image37.png)

        Neste exemplo, o rótulo redundante é removido, portanto, a instrução principal assume a chave de acesso.

-   Posicionamento de rótulo:
    -   Balão, caixas de seleção, botões de comando, caixas de grupo, links, guias e dicas são rotulados diretamente pelo próprio controle.
    -   Listas listadas, caixas de listagem, exibições de lista, barras de progresso, controles deslizantes, caixas de texto e exibições de árvore são rotuladas acima, liberar para a esquerda ou para a esquerda.
    -   Os controles de divulgação progressiva geralmente não têm rótulo. Os botões de divisa são rotulados à direita.
-   **Atribua uma chave de acesso exclusiva para cada controle interativo,** exceto para links. Para obter mais informações, consulte [Teclado](inter-keyboard.md).
-   **Mantenha os rótulos curtos.** Observe, no entanto, que adicionar uma palavra ou duas a um rótulo pode ajudar a esclarecer e, às vezes, elimina a necessidade de explicações complementares.
-   **Prefira rótulos específicos em vez de genéricos.** O ideal é que os usuários não tenham que ler mais nada para entender o rótulo.

    **Incorreto:**

    ![captura de tela do botão de comando OK ](images/text-ui-image38.png)

    **Correto:**

    ![captura de tela do botão publicar comando ](images/text-ui-image39.png)

    No exemplo correto, um rótulo específico é usado para o botão de confirmação.

-   **Para listas de rótulos,** como botões de rádio, use frase paralela e tente manter o comprimento aproximadamente o mesmo para todos os rótulos.
-   **Para listas de rótulos, concentre o texto do rótulo nas diferenças entre as opções.** Se todas as opções têm o mesmo texto introdutório, mova esse texto para o rótulo do grupo.

    **Incorreto:**

    ![captura de tela de rótulos com as primeiras frases duplicadas](images/text-ui-image40.png)

    **Correto:**

    ![captura de tela da primeira frase movida para o rótulo do grupo](images/text-ui-image41.png)

    O exemplo correto move a frase introdutório idêntica para o rótulo, de modo que as duas opções sejam diferenciadas de forma mais limpa.

-   **Em geral, prefira frases positivas.** Por exemplo, use fazer em vez de não fazer e notificar em vez de não notificar.
    -   **Exceção:** O rótulo da caixa de seleção "Não mostrar esta mensagem novamente" é amplamente usado.
-   **Omita verbos instrucionais que se aplicam a todos os controles do tipo determinado.** Em vez disso, concentre os rótulos no que é exclusivo sobre os controles. Por exemplo, não é necessário dizer que os usuários precisam digitar em um controle de caixa de texto ou que os usuários precisam clicar em um link.

    **Incorreto:**

    ![captura de tela do rótulo: 'digite seu nome' ](images/text-ui-image42.png)

    **Correto:**

    ![captura de tela do rótulo: 'seu nome' ](images/text-ui-image43.png)

    Nos exemplos incorretos, os rótulos de controle têm verbos instrucionais que se aplicam a todos os controles de seu tipo.

-   Em alguns casos, as seguintes anotações parênteses para controlar rótulos podem ser úteis:
    -   **Se uma opção for opcional, considere adicionar "(opcional)" ao rótulo.**
    -   **Se uma opção for altamente recomendada, adicione "(recomendado)" ao rótulo.** Isso significa que a configuração é opcional, mas deve ser definida de qualquer forma.
    -   **Se uma opção for destinada somente a usuários avançados, considere adicionar "(advanced)" ao rótulo.**
-   Você pode especificar unidades (segundos, conexões e assim por diante) entre parênteses após o rótulo.

    ![captura de tela do rótulo: tamanho inicial (mb) ](images/text-ui-image44.png)

    Este exemplo mostra que a unidade de medida é mb (megabytes).

Para obter mais informações, consulte a seção "Texto" ou "Rótulos" nas diretrizes de componente de interface do usuário específicas.

### <a name="supplemental-explanations"></a>Explicações complementares

-   **Use explicações complementares quando os controles exigirem mais informações do que podem ser transmitidas pelo rótulo.** Mas não use uma explicação complementar se não for necessário preferir comunicar tudo com o rótulo de controle se você puder fazer isso de forma concisa. Normalmente, explicações complementares são usadas com links de comando, botões de rádio e caixas de seleção.
-   Quando necessário, **use negrito nos rótulos de controle para** facilitar a verificação do texto quando houver explicações complementares.

    ![captura de tela da caixa de diálogo configurações de segurança ](images/text-ui-image45.png)

    Neste exemplo, os rótulos de botão de rádio estão em negrito para facilitar a verificação.

-   **Adicionar uma explicação complementar a um controle em um grupo não significa que você precisa fornecer explicações para todos os outros controles no grupo.** Forneça as informações relevantes no rótulo se você puder e usar explicações somente quando necessário. Não tem explicações complementares que simplesmente restate o rótulo para consistência.

    ![captura de tela de três botões de rádio ](images/text-ui-image46.png)

    Neste exemplo, dois controles no grupo incluem explicações complementares, mas o terceiro não.

-   Se uma explicação complementar seguir um link de comando, escreva o texto suplementar na segunda pessoa.

    **Exemplo:** Link de comando: criar configurações de rede sem fio e salvar na unidade flash USB

    Explicação complementar: isso criará configurações que você pode transferir para o roteador com uma unidade flash USB. Faça isso somente se você tiver um roteador sem fio que dá suporte à configuração de unidade flash USB.

-   Use frases completas e pontuação final.

### <a name="commit-button-labels"></a>Rótulos de botão de commit

A tabela a seguir mostra os rótulos de botão de confirmação mais comuns e seu uso.




| | | <strong>Rótulo do botão</strong><br /> | <strong>Significado</strong><br /> | <strong>Quando usar</strong><br /> | <strong>Chave de acesso</strong><br /> | | <strong>OK</strong><br /> | <ul><li>Nas caixas de diálogo: aplique as alterações ou commit à tarefa e feche a janela.</li><li>Nas janelas de propriedades do proprietário: aplique as alterações pendentes (feitas desde que a janela foi aberta ou a última Aplicar) e feche a janela.</li><li>Em janelas de propriedade própria: mantenha as alterações, feche a janela e aplique as alterações quando as alterações da janela do proprietário são aplicadas.</li></ul> | <ul><li>Use com janelas que não são específicas da tarefa, como folhas de propriedades.</li><li>Para janelas usadas para executar uma tarefa específica, use um rótulo específico que comece com um verbo (exemplo: Imprimir).</li><li>Para janelas nas quais os usuários não podem fazer alterações, use Fechar.</li></ul> | Entrar<br /> | | <strong>Sim/Não</strong><br /> | Sim é a resposta afirmativa a uma pergunta sim ou não, enquanto Não é a resposta negativa.<br /> | <ul><li>Use os botões Sim e Não apenas para responder a perguntas sim ou não. Nunca use OK e Cancelar para perguntas sim ou não.</li><li>Prefira respostas específicas em vez dos botões Sim e Não. Embora não haja nada de errado com o uso de Sim e Não, respostas específicas podem ser compreendidas mais rapidamente, resultando em uma tomada de decisão eficiente.</li><li>No entanto, considere usar respostas Sim e Não se a frase de respostas específicas for longa ou complicada.</li><li>Não use os botões Sim e Não se o significado da resposta Não estiver claro. Em caso afirmado, use respostas específicas.</li><li>Sim e Não sempre devem ser usados como um par.</li></ul> | Y e N<br /> | | <strong>Cancelar</strong><br /> | <ul><li>Nas caixas de diálogo: descarte todas as alterações ou trabalhe em andamento, reverta para o estado anterior (não deixando nenhum efeito colateral perceptível) e feche a janela.</li><li>Em folhas de propriedades: descarte todas as alterações pendentes (feitas desde que a janela foi aberta ou a última Aplicar) e feche a janela.</li><li>Nos itens do painel de controle: descarte todas as alterações ou trabalhe em andamento, reverta para o estado anterior e retorne à página do hub da qual a tarefa foi lançada. Se não houver essa página de hub, feche a janela de item do painel de controle.</li></ul> | <ul><li>Use quando todas as alterações ou ações pendentes puderem ser descartadas e os efeitos colaterais puderem ser desfeitos.</li><li>Para alterações que não podem ser descartadas, use Fechar. Para ações em andamento que podem ser interrompidas, use Parar. Se inicialmente as alterações ou ações puderem ser descartadas, você poderá usar Cancelar inicialmente e, em seguida, alterar para Fechar ou Parar quando ele não puder ser desfeito.</li></ul> | Esc<br /> | | <strong>Fechar</strong><br /> | Feche a janela. Alterações ou efeitos colaterais não são descartados.<br /> | <ul><li>Use quando alterações ou efeitos colaterais não puderem ser descartados. Use Fechar em vez de Cancelar para janelas primárias.</li><li>Use para janelas nas quais os usuários não podem fazer alterações.</li></ul> | Alt+F4, Ctrl+F4<br /> | | <strong>Parar</strong><br /> | Pare uma tarefa em execução no momento e feche a janela. Qualquer trabalho em andamento ou efeitos colaterais não são descartados.<br /> | <ul><li>Use quando estiver em andamento e quaisquer efeitos colaterais não puderem ou não serão descartados, normalmente com barras de progresso ou animações.</li></ul> | Esc<br /> | | <strong>Aplicar</strong><br /> | Em folhas de propriedades do proprietário: aplique as alterações pendentes (feitas desde que a janela foi aberta ou a última Aplicar), mas deixe a janela aberta. Isso permite que os usuários avaliem as alterações antes de fechar a folha de propriedades. Em folhas de propriedades de propriedade: não use.<br /> | <ul><li>Use somente em folhas de propriedades.</li><li>Forneça um botão Aplicar somente se a folha de propriedades tiver configurações (pelo menos uma) com efeitos que os usuários podem avaliar de maneira significativa. Normalmente, os botões Aplicar são usados quando as configurações fazem alterações visíveis. Os usuários devem ser capazes de aplicar uma alteração, avaliar a alteração e fazer outras alterações com base nessa avaliação. Caso contrário, remova o botão Aplicar em vez de desabilitá-lo.</li></ul> | Um<br /> | | <strong>Próximo</strong><br /> | Em assistentes e tarefas de várias etapas: avance para a próxima etapa sem se comprometer com a tarefa.<br /> | <ul><li>Use somente em assistentes e tarefas de várias etapas para avançar para a próxima etapa sem compromisso.</li><li>O efeito de um botão Avançar sempre pode ser desfeito clicando em voltar.</li></ul> | P<br /> | | <strong>Concluir</strong><br /> | Em assistentes e tarefas de várias etapas: Feche a janela. Se a tarefa ainda não tiver sido executada, execute a tarefa. Se essa tarefa já tiver sido executada, quaisquer alterações ou efeitos colaterais não serão descartados.<br /> | <ul><li>Use somente em assistentes e tarefas de várias etapas. No entanto, o uso de Finish é desencorajado porque geralmente há um botão de confirmação melhor e mais específico:<ul><li>se você clicar no botão for confirmado na tarefa (para que a tarefa ainda não tenha sido executada), use um rótulo específico que comece com um verbo (exemplos: Print, Conexão e Start) que seja uma resposta à instrução principal.</li><li>Se a tarefa já tiver sido executada no assistente, use fechar em vez disso.</li></ul></li><li>No entanto, você pode usar concluir quando:<ul><li>O rótulo específico ainda é genérico, como salvar, selecionar, escolher ou obter.</li><li>A tarefa envolve alterar uma configuração ou uma coleção de configurações.</li></ul></li></ul> | Digita<br /> | | <strong>Concluído</strong><br /> | Não aplicável.<br /> | <ul><li>Não use. Concluído como um comando está gramaticalmente incorreto.</li></ul> | Não aplicável.<br /> | 




 

