---
title: Texto da interface do usuário
description: O texto da interface do usuário é exibido nas superfícies da interface de usuários.
ms.assetid: db42fe22-9baf-453a-9b89-9bbb251b0b6f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 1c1a60ba0bfef33dcf1e72c5ba19b11c4a5f38a2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104567645"
---
# <a name="user-interface-text"></a>Texto da interface do usuário

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

O texto da interface do usuário é exibido nas superfícies da interface de usuários. Esse texto inclui rótulos de controle e texto estático:

-   Os rótulos de controle identificam controles e são colocados diretamente em ou ao lado dos controles.
-   Texto estático, que é tão chamado porque não faz parte de um controle interativo, fornece aos usuários instruções detalhadas ou explicações para que eles possam tomar decisões informadas.

**Observação:** As diretrizes relacionadas a rótulos de controle de [estilo e Tom](text-style-tone.md), [fontes](vis-fonts.md)e [controles](controls.md) de as são apresentadas em artigos separados.

## <a name="usage-patterns"></a>Padrões de uso

O texto da interface do usuário tem vários padrões de uso:



|                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Texto da barra de título**<br/> Use o texto da barra de título para identificar uma janela ou a origem de uma caixa de diálogo. <br/>                                                                            | ![captura de tela da barra de título de opções de pasta](images/text-ui-image1.png)<br/> Neste exemplo, o texto da barra de título identifica uma janela.<br/>                                                                                                                                                                                                                                                                                                             |
| **Instruções principais**<br/> Use a instrução principal proeminente para explicar de forma concisa o que fazer na janela ou na página. <br/>                                                      | A instrução deve ser uma instrução específica, uma direção imperativa ou uma pergunta. boas instruções principais comunicam o objetivo do usuário em vez de se concentrar apenas na manipulação da interface do usuário. <br/> ![captura de tela de pergunta: deseja obter a ajuda mais recente? ](images/text-ui-image2.png)<br/> Neste exemplo, o texto de instrução principal envolve diretamente o usuário com uma pergunta em termos de interesse ou benefício do usuário.<br/>             |
| **Instruções complementares**<br/> quando necessário, use uma instrução complementar para apresentar informações adicionais úteis para entender ou usar a janela ou a página. <br/> | Você pode fornecer informações mais detalhadas, fornecer contexto e definir a terminologia. instruções complementares elaboradas sobre a instrução principal sem simplesmente reformular a ti. <br/> ![captura de tela de texto ao alternar para a conta do administrador ](images/text-ui-image3.png)<br/> Neste exemplo, as instruções complementares fornecem dois possíveis cursos de ação a serem adotados em resposta às informações apresentadas na instrução principal.<br/> |
| **Rótulos de controle**<br/> rótulos diretamente no ou ao lado dos controles. <br/>                                                                                                           | ![captura de tela das opções de relógio da área de trabalho ](images/text-ui-image4.png)<br/> Neste exemplo, os rótulos de controle identificam as configurações de relógio da área de trabalho que os usuários podem selecionar ou modificar.<br/>                                                                                                                                                                                                                                                                       |
| **Explicações suplementares**<br/> um elaboration dos rótulos de controle (normalmente para links de comando, botões de opção e caixas de seleção). <br/>                                    | ![Captura de tela que mostra uma caixa de diálogo Configurações de segurança.](images/text-ui-image5.png)<br/> Neste exemplo, as explicações suplementares esclarecem as opções.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="design-concepts"></a>Conceitos de design

Os desenvolvedores de software geralmente consideram o texto relegado à documentação do produto e ao suporte técnico. "Primeiro vamos escrever o código e, em seguida, contrataremos alguém para nos ajudar a explicar o que desenvolvemos." Ainda na realidade, o texto importante é escrito anteriormente no processo, pois a interface do usuário é concebida e codificada. Esse texto é, afinal, visto com mais frequência e por mais pessoas do que talvez qualquer outro tipo de escrita técnica.

**O texto abrangente é crucial para a interface do usuário efetiva.** Os autores e editores profissionais devem trabalhar com desenvolvedores de software no texto da interface do usuário como parte integrante do processo de design. Faça com que eles trabalhem no texto antecipadamente porque problemas de texto geralmente revelam problemas de design. Se sua equipe tiver problemas para explicar um design, com muita frequência ele é o design, não a explicação, que precisa de melhoria.

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

O texto redundante não só leva um espaço de tela valioso, mas enfraquece a eficácia das ideias ou ações importantes que você está tentando transmitir. Também é um desperdício do tempo do leitor, e tudo isso em um contexto em que a verificação é a norma. **O Windows se esforça para explicar o que os usuários precisam fazer uma vez bem e concisamente.**

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

-   **Remova o texto redundante.** Procure texto redundante em títulos de janela, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de confirmação. Em geral, deixe texto completo nas instruções principais e nos controles interativos e remova qualquer redundância dos outros locais.
-   **Evite grandes blocos de texto da interface do usuário.** As maneiras de fazer isso incluem:
    -   Agrupamento de texto em frases e parágrafos menores.
    -   Quando necessário, fornecendo [links de ajuda](winenv-help.md) para informações úteis, mas não essenciais.
-   **Escolha nomes de objetos e rótulos que se comunicam claramente e diferenciam o que o objeto faz.** Os usuários não devem ter que descobrir o que o objeto realmente significa ou como ele difere de outros objetos.

    Incorreto:

    ![captura de tela da lista de monitores sem nome](images/text-ui-image8.png)

    Melhor:

    ![captura de tela da lista de adaptadores de rede específicos](images/text-ui-image9.png)

    No exemplo incorreto, os nomes de objeto não são diferenciados; o exemplo melhor mostra uma diferenciação forte por nome do produto.

-   **Se você quiser garantir que os usuários leiam texto específico relacionado a uma ação, coloque-o em um controle interativo.**
    -   **Aceitável:**
    -   ![captura de tela de aviso de formatação usando o botão OK ](images/text-ui-image10.png)
    -   Neste exemplo, há a possibilidade de que os usuários não leiam o texto que explica o que eles estão confirmando.
    -   **Melhor:**
    -   ![captura de tela da formatação de aviso e botão Formatar ](images/text-ui-image11.png)
    -   Neste exemplo, você pode ter certeza de que pelo menos os usuários entendem que estão prestes a formatar um disco.
-   **Use um espaço entre as frases.** Não dois.

### <a name="text-fonts-sizes-and-colors"></a>Fontes de texto, tamanhos e cores

-   **Use texto azul somente para links e instruções principais.**
-   **Use texto verde somente para URLs nos resultados da pesquisa.**

As fontes e cores a seguir são padrões para o Windows.



| Padrão                                                                                     | Símbolo de tema                            | Fonte, cor                                                           |
|--------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![primeira coluna: texto da barra de título ](images/text-ui-image12.png)<br/>              | CaptionFont<br/>      | 9 pt. preto ( \# 000000) Segoe UI<br/>                 |
| ![primeira coluna: instruções principais ](images/text-ui-image13.png)<br/>           | MainInstruction<br/>  | 12 pt. azul ( \# 003399) Segoe UI<br/>                 |
| ![primeira coluna: instruções secundárias ](images/text-ui-image14.png)<br/>      | Instrução<br/>      | 9 pt. preto ( \# 000000) Segoe UI<br/>                 |
| ![primeira coluna: texto normal ](images/text-ui-image15.png)<br/>                 | BodyText<br/>         | 9 pt. preto ( \# 000000) Segoe UI<br/>                 |
| ![primeira coluna: texto enfatizado ](images/text-ui-image16.png)<br/>             | BodyText<br/>         | 9 pt. preto ( \# 000000) Segoe UI, negrito ou itálico<br/> |
| ![primeira coluna: texto editável ](images/text-ui-image17.png)<br/>               | BodyText<br/>         | 9 pt. preto ( \# 000000) Segoe UI, em uma caixa<br/>       |
| ![primeira coluna: texto desabilitado ](images/text-ui-image18.png)<br/>               | Desabilitado<br/>         | 9 pt. cinza-escuro ( \# 323232) Segoe UI<br/>             |
| ![primeira coluna: link ](images/text-ui-image19.png)<br/>                        | HyperLinkText<br/>    | 9 pt. Segoe UI azul ( \# 0066CC)<br/>                  |
| ![primeira coluna: links (focalizar) ](images/text-ui-image20.png)<br/>               | Frequente<br/>              | 9 pt. azul-claro ( \# 3399FF) Segoe UI<br/>            |
| ![primeira coluna: cabeçalho do grupo ](images/text-ui-image21.png)<br/>                |  <br/>                | 11 pt. azul ( \# 003399) Segoe UI<br/>                 |
| ![primeira coluna: nome do arquivo (na exibição de conteúdo) ](images/text-ui-image22.png)<br/> |  <br/>                | 11 pt. preto ( \# 000000) Segoe UI<br/>                |
| ![primeira coluna: texto do documento ](images/text-ui-image23.png)<br/>               | (nenhum)<br/>           | 9 pt. preto ( \# 000000) Calibri<br/>                  |
| ![primeira coluna: títulos de documento ](images/text-ui-image24.png)<br/>           | (nenhum)<br/>           | 17 pt. preto ( \# 000000) Calibri<br/>                 |



 

Para obter mais informações e exemplos, consulte [fontes](vis-fonts.md) e [cores](vis-color.md).

### <a name="other-text-characteristics"></a>Outras características de texto

**Negrito**

-   **Use em negrito para chamar atenção para texto que os usuários devem ler.** Por exemplo, os usuários que verificam uma lista de opções de botão de opção podem apreciar a exibição dos rótulos em negrito, para destacar o texto que adiciona informações complementares sobre cada opção. Lembre-se de que o uso de muito mais negrito diminui seu impacto.
-   **Com os dados rotulados, use negrito para enfatizar o que for mais importante para os dados como um todo.**
    -   Para os dados mais genéricos (onde os dados têm pouco significado sem seus rótulos, como com numerais ou datas), use rótulos em negrito e dados sem formatação para que os usuários possam examinar e entender os tipos de dados com mais facilidade.
    -   Para obter principalmente dados autoexplicativos, use rótulos simples e dados em negrito para que os usuários possam se concentrar nos dados em si.
    -   Como alternativa, você pode usar texto cinza escuro para desenfatizar informações menos importantes em vez de usar negrito para enfatizar as informações mais importantes.

        ![captura de tela do modo de exibição de miniatura do Windows Explorer ](images/text-ui-image25.png)

        Neste exemplo, em vez de enfatizar os dados usando negrito, os rótulos são realçados com o uso de cinza escuro.

-   **Nem todas as fontes dão suporte a negrito, portanto, nunca deve ser crucial para entender o texto.**

**Itálico**

-   Use para fazer referência ao texto literalmente. Não use aspas para essa finalidade.

    **Correto:**

    Os termos documento e arquivo são frequentemente usados de maneira intercambiável.

-   Use para [prompts](glossary.md) em [caixas de texto](ctrl-text-boxes.md) e [listas suspensas editáveis](/windows/desktop/uxguide/ctrl-drop).

    ![captura de tela da caixa de texto de pesquisa ](images/text-ui-image26.png)

    Neste exemplo, o prompt na caixa de pesquisa é formatado como texto em itálico.

-   Use com moderação para enfatizar palavras específicas para auxiliar na compreensão.
-   **Nem todas as fontes dão suporte a itálico, portanto, nunca deve ser crucial para entender o texto.**

**Negrito itálico**

-   Não use o texto da interface do usuário.

**Aplicar**

-   Não use, exceto links.
-   Não use para dar ênfase. Em vez disso, use itálico.

### <a name="punctuation&quot;></a>Pontuação

**Finais**

-   **Não coloque no final dos rótulos de controle, nas instruções principais ou nos links da ajuda.**
-   Coloque no final das instruções complementares, explicações suplementares ou qualquer outro texto estático que forma uma frase completa.

**Pontos de interrogação**

-   **Coloque ao final de todas as perguntas.** Ao contrário dos períodos, os pontos de interrogação são usados para todos os tipos de texto.

**Pontos de exclamação**

-   Em aplicativos de negócios, evite.
    -   **Exceções:** Os pontos de exclamação são usados às vezes no contexto de conclusão do download (&quot;concluído!") e para chamar a atenção para o conteúdo da Web ("novo!").

**Vírgulas**

-   Em uma lista de três ou mais itens, sempre coloque uma vírgula após o próximo item na lista.

**Dois-pontos**

-   **Use dois-pontos no final dos rótulos de controle externo.** Isso é particularmente importante para acessibilidade porque algumas tecnologias assistenciais procuram dois-pontos para identificar Rótulos de controle.
-   Use dois pontos para introduzir uma lista de itens.

**Reticências**

-   **As reticências significam inintegridade.** Use reticências no texto da interface do usuário da seguinte maneira:
    -   **Comandos:** Indique que um comando precisa de informações adicionais. Não use reticências sempre que uma ação exibir outra janela somente quando forem necessárias informações adicionais. Para obter mais informações, consulte [botões de comando](ctrl-command-buttons.md).
    -   **Dados:** Indica que o texto está truncado.
    -   **Rótulos:** Indique que uma tarefa está em andamento (por exemplo, "pesquisando...").

        **Dica:** O texto truncado em uma janela ou página com espaço não utilizado indica um layout insatisfatório ou um tamanho de janela padrão muito pequeno. Busque layouts e tamanhos de janela padrão que eliminem ou reduzem a quantidade de texto truncado. Veja [Layout](vis-layout.md) para obter mais informações.

-   **Não torne as reticências interativas.** Para mostrar texto truncado, permita que os usuários redimensionem o controle para ver mais texto ou usar um [controle de divulgação progressiva](ctrl-progressive-disclosure-controls.md) .

**Aspas e apóstrofos**

-   Para fazer referência ao texto literalmente, use formatação em itálico e não aspas.
-   Coloque os títulos de janela e os rótulos de controle entre aspas somente se necessário para evitar confusão e não é possível formatar usando negrito em vez disso.
-   Para aspas, prefira aspas duplas (""); Evite aspas simples.

    **Correto:**

    Tem certeza de que deseja excluir "pasta Cat de Sparky"?

    **Incorreto:**

    Tem certeza de que deseja excluir a ' pasta Cat ' do Sparky?

### <a name="capitalization"></a>Uso de maiúsculas

-   **Use a capitalização de estilo de título para títulos, capitalização de estilo de frase para todos os outros elementos da interface do usuário.** Fazer isso é mais apropriado para o [Tom do Windows](text-style-tone.md).

    -   **Exceção:** Para aplicativos herdados, você pode usar a capitalização de estilo de título para botões de comando, menus e títulos de coluna, se necessário, para evitar a mistura de estilos de capitalização.

        ![captura de tela da folha de propriedades genérica ](images/text-ui-image27.png)

    Este exemplo genérico mostra a capitalização e a pontuação corretas para folhas de propriedades.

    ![captura de tela da caixa de diálogo genérica ](images/text-ui-image28.png)

    Este exemplo genérico mostra a capitalização e a pontuação corretas para caixas de diálogo.

-   **Para nomes de recursos e tecnologias, seja conservador em maiúsculas.** Normalmente, somente os principais componentes devem ser capitalizados (usando a capitalização de estilo de título).

    **Correto:**

    Analysis Services, cubos, dimensões

    Analysis Services é um componente importante do SQL Server, portanto, a capitalização no estilo de título é apropriada; cubos e dimensões são elementos comuns de software de análise de banco de dados, portanto, não é necessário colocar em maiúsculas.

-   **Para nomes de recursos e tecnologias, seja consistente em maiúsculas.** Se o nome aparecer mais de uma vez em uma tela de interface do usuário, ele sempre deverá aparecer da mesma maneira. Da mesma forma, em todas as telas de interface do usuário no programa, o nome deve ser apresentado consistentemente.
-   Não coloque maiúsculas nos nomes dos elementos genéricos da interface do usuário, como barra de ferramentas, menu, barra de rolagem, botão e ícone.
    -   **Exceções:** Barra de endereços, barra de links.
-   Não use todas as letras maiúsculas para as teclas do teclado. Em vez disso, siga as letras maiúsculas usadas por teclados padrão ou em minúsculas se a chave não estiver rotulada como um painel.

    **Correto:**

    barra de espaços, guia, inserir, página acima, Ctrl + Alt + Del

    **Incorreto:**

    BARRA DE ESPAÇOS, GUIA, ENTER, PG UP, CTRL + ALT + DEL

-   **Não use todas as letras maiúsculas para dar ênfase.** Estudos mostraram que isso é difícil de ler, e os usuários tendem a se considerar como "incontestável". Para avisos, use um ícone de aviso e uma explicação com uma palavra clara da situação. Não é necessário adicionar, por exemplo, o termo aviso em todas as letras maiúsculas.

Para obter mais informações, consulte a seção "texto" ou "rótulos" nas diretrizes específicas do componente da interface do usuário.

### <a name="dates-and-times"></a>Datas e horas

-   **Não Codifique o formato de datas e horas.** Respeite a opção do usuário de opções de localidade e personalização para os formatos de data e hora. O usuário seleciona esses itens no item do painel de controle região e idioma.

    ![captura de tela do formato de data: segunda-feira, 06 de julho de 2009](images/text-ui-image29.png)![captura de tela do formato de data: 06 de julho de 2009](images/text-ui-image30.png)

    Nestes exemplos do Microsoft Outlook, os dois formatos para a data por extenso estão corretos. Eles refletem opções diferentes que os usuários fizeram no item do painel de controle região e idioma.

-   **Use o formato de data por extenso para cenários que se beneficiam de ter informações adicionais.** Use o formato de data abreviada para contextos que não têm espaço suficiente para o formato longo. Embora os usuários escolham quais informações gostaria de incluir nos formatos longo e curto, os designers escolhem qual formato exibir em seus programas com base no cenário e no contexto.

    ![captura de tela de formato com datas de início e de vencimento](images/text-ui-image31.png)

    Neste exemplo, o formato de data por extenso ajuda os usuários a organizar tarefas e prazos.

### <a name="globalization-and-localization"></a>Globalização e localização

A globalização significa criar documentos ou produtos que podem ser usados em qualquer país, região ou cultura. Localização significa adaptar documentos ou produtos para uso em uma localidade diferente do país/região de origem. Considere a globalização e a localização ao gravar o texto da interface do usuário. Seu programa pode ser traduzido em outras linguagens e usado em culturas muito diferentes do seu.

-   Para controles com conteúdo de variável (como exibições de lista e exibições de árvore), **escolha uma largura apropriada para os dados válidos mais longos.**
-   **Inclua espaço suficiente na superfície da interface do usuário por um adicional de 30%** (até 200 por cento para texto mais curto) para qualquer texto (mas não números) que será localizado. A tradução de um idioma para outro frequentemente altera o comprimento da linha de texto.
-   Não redija cadeias de caracteres de subcadeias em tempo de execução. Em vez disso, use frases completas para que não haja ambiguidade para o tradutor.
-   **Não use um controle subordinado, os valores que ele contém ou seu rótulo de unidades para criar uma frase ou frase.** Esse design não é localizável porque a estrutura da frase varia de acordo com a linguagem.

    **Incorreto:**

    ![captura de tela de caixa de texto dentro de um rótulo de caixa de seleção ](images/text-ui-image32.png)

    **Correto:**

    ![captura de tela da caixa de texto após um rótulo de caixa de seleção ](images/text-ui-image33.png)

    No exemplo incorreto, a caixa de texto é colocada dentro do rótulo da caixa de seleção.

-   Não faça um link apenas parte de uma frase, pois, quando traduzido, esse texto pode não permanecer juntos. O texto do link, portanto, deve formar uma frase completa por si só.
    -   **Exceção:** Os links de Glossário podem ser inseridos embutidos, como parte de uma frase.

Para obter mais informações, consulte o [centro de desenvolvedores do Go Global](https://msdn.microsoft.com/goglobal/).

### <a name="title-bar-text"></a>Texto da barra de título

-   Escolha o texto da barra de título com base no tipo de janela:
    -   **Janelas de programa de alto nível centradas em documentos:** Use um formato "nome do programa do nome do documento". Os nomes de documento são exibidos primeiro para dar uma sensação centrada no documento.
    -   **Janelas de programas de nível superior que não são centradas em documentos:** Exiba apenas o nome do programa.
    -   **Caixas de diálogo:** Exibe o comando, o recurso ou o programa do qual a caixa de diálogo veio. Não use o título para explicar a finalidade da caixa de diálogo que é a finalidade das principais instruções. Para obter mais diretrizes, consulte [caixas de diálogo](win-dialog-box.md).
    -   **Assistentes:** Exibir o nome do assistente. Observe que a palavra "assistente" não deve ser incluída em nomes de assistente. Para obter mais diretrizes, consulte [assistentes](win-wizards.md).
-   **Para janelas de programas de nível superior, se a legenda da barra de título e o ícone forem exibidos em destaque na parte superior da janela, você poderá ocultar a legenda da barra de título e o ícone para evitar redundância.** No entanto, você ainda precisa definir um título adequado internamente para uso pelo Windows.
-   **Para caixas de diálogo, não inclua as palavras "Dialog" ou "Progress" nos títulos.** Esses conceitos são implícitos e deixar essas palavras desativadas torna os títulos mais fáceis de serem verificados pelos usuários.

### <a name="main-instructions"></a>Instruções principais

-   **Use a instrução principal para explicar de forma concisa o que os usuários devem fazer em uma determinada janela ou página.** Boas instruções principais comunicam o objetivo do usuário em vez de se concentrar apenas na manipulação da interface do usuário.
-   **Expresse a instrução principal na forma de uma direção imperativa ou uma pergunta específica.**

    **Incorreto:**

    ![captura de tela do nome do programa como instrução principal ](images/text-ui-image34.png)

    Neste exemplo, a instrução Main simplesmente declara o nome do programa; Ele não convida explicitamente um curso de ação a ser adotado pelo usuário.

    **Exceções:** Mensagens de erro, mensagens de aviso e confirmações podem usar estruturas de frase diferentes em suas instruções principais.

-   **Use verbos específicos sempre que possível.** Os verbos específicos (exemplos: conectar, salvar, instalar) são mais significativos para os usuários do que os genéricos (exemplos: configurar, gerenciar, definir).
    -   Para páginas do painel de controle e páginas do assistente, se você não puder usar um verbo específico, poderá preferir omitir o verbo completamente.

        **Aceitável:**

        Insira sua localidade, região e idioma

        **Melhor:**

        Localidade, região e idioma

    -   Para caixas de diálogo, como mensagens de erro e avisos, não omita o verbo.

-   Não se sinta obrigado para usar o texto de instrução principal se adicioná-lo só seria redundante ou óbvio do contexto da interface do usuário.

    ![captura de tela da caixa de diálogo Salvar como ](images/text-ui-image35.png)

    Neste exemplo, o contexto da interface do usuário já está muito claro; Não é necessário adicionar o texto de instrução principal.

-   **Seja conciso Use apenas uma única frase completa.** Parênteses da instrução principal até as informações essenciais. Se você precisar explicar algo mais, considere usar uma instrução complementar.
-   Use a capitalização com estilo de frase.
-   **Não inclua os períodos finais se a instrução for uma instrução.** Se a instrução for uma pergunta, inclua um ponto de interrogação final.
-   **Para caixas de diálogo de progresso, use uma frase gerund explicando brevemente a operação em andamento,** terminando com uma elipse. Exemplo: "Imprimindo suas imagens..."
-   **Dica:** Você pode avaliar uma instrução principal ao imaginar o que você diria a um amigo ao explicar o que fazer com a janela ou a página. Se responder com a instrução principal não for natural, não ajuda ou estranha, retrabalhe com a instrução.

Para obter mais informações, consulte a seção "instrução principal" nas diretrizes específicas do componente da interface do usuário.

### <a name="supplemental-instructions"></a>Instruções complementares

-   Quando necessário, **use uma instrução complementar para apresentar informações adicionais úteis para entender ou usar a janela ou a página,** como:
    -   Fornecendo contexto para explicar por que a janela está sendo exibida se for iniciada por programa ou sistema.
    -   Qualificar informações que ajudam os usuários a decidir como agir na instrução principal.
    -   Definindo uma terminologia importante.
-   **Não use uma instrução complementar se uma não for necessária.** Prefira comunicar tudo com a instrução principal se você puder fazer isso de forma concisa.
-   **Não repita a instrução principal com uma palavra ligeiramente diferente.** Em vez disso, omita a instrução complementar se não houver nada mais a ser adicionado.
-   Use frases completas e maiúsculas e minúsculas no estilo da sentença.

### <a name="control-labels"></a>Rótulos de controle

-   **Rotular cada controle ou grupo de controles. Exceção**
    -   Caixas de texto e listas suspensas podem ser rotuladas usando prompts.
    -   Os controles de divulgação progressiva geralmente não são rotulados.
    -   **Controles subordinados usam o rótulo de seu controle associado.** Controles de rotação são sempre controles subordinados.
    -   **Omita os rótulos de controle que redefinem a instrução principal.** Nesse caso, a instrução Main usa a chave de acesso.

        **Aceitável:**

        ![captura de tela da caixa de texto com instrução e rótulo ](images/text-ui-image36.png)

        Neste exemplo, o rótulo da caixa de texto é apenas uma recondição da instrução principal.

        **Melhor:**

        ![captura de tela da caixa de texto com apenas instruções ](images/text-ui-image37.png)

        Neste exemplo, o rótulo redundante é removido, portanto, a instrução Main usa a chave de acesso.

-   Posicionamento do rótulo:
    -   Os balões, as caixas de seleção, os botões de comando, as caixas de grupo, os links, as guias e as dicas são rotulados diretamente pelo próprio controle.
    -   Listas suspensas, caixas de listagem, exibições de lista, barras de progresso, controles deslizantes, caixas de texto e modos de exibição de árvore são rotulados acima, com recuo para a esquerda ou para a esquerda.
    -   Os controles de divulgação progressiva geralmente não são rotulados. Os botões de divisa são rotulados à direita.
-   **Atribua uma chave de acesso exclusiva para cada controle interativo** , exceto links. Para obter mais informações, consulte [teclado](inter-keyboard.md).
-   **Retenha os rótulos de forma breve.** No entanto, observe que a adição de uma palavra ou duas a um rótulo pode ajudar a esclarecer e, às vezes, elimina a necessidade de explicações complementares.
-   **Prefira rótulos específicos sobre aqueles genéricos.** Idealmente, os usuários não precisam ler mais nada para entender o rótulo.

    **Incorreto:**

    ![captura de tela do botão de comando Ok ](images/text-ui-image38.png)

    **Correto:**

    ![captura de tela do botão de comando publicar ](images/text-ui-image39.png)

    No exemplo correto, um rótulo específico é usado para o botão de confirmação.

-   **Para listas de rótulos, como botões de opção, use frases paralelas** e tente manter o comprimento sobre o mesmo para todos os rótulos.
-   **Para listas de rótulos, concentre o texto do rótulo nas diferenças entre as opções.** Se todas as opções tiverem o mesmo texto introdutório, mova esse texto para o rótulo do grupo.

    **Incorreto:**

    ![captura de tela de rótulos com frases primeiro duplicadas](images/text-ui-image40.png)

    **Correto:**

    ![captura de tela da primeira frase movida para o rótulo de grupo](images/text-ui-image41.png)

    O exemplo correto move a frase introdutória idêntica para o rótulo, de modo que as duas opções sejam diferenciadas com mais clareza.

-   **Em geral, prefira frases positivas.** Por exemplo, use do em vez de não, e notifique em vez de não notificar.
    -   **Exceção:** O rótulo da caixa de seleção "não mostrar esta mensagem novamente" é amplamente usado.
-   **Omita os verbos instrutivos que se aplicam a todos os controles do tipo fornecido.** Em vez disso, focalize os rótulos sobre o que é exclusivo sobre os controles. Por exemplo, ele vai sem dizer que os usuários precisam digitar em um controle de caixa de texto ou que os usuários precisem clicar em um link.

    **Incorreto:**

    ![captura de tela do rótulo: ' Digite seu nome ' ](images/text-ui-image42.png)

    **Correto:**

    ![captura de tela do rótulo: ' seu nome ' ](images/text-ui-image43.png)

    Nos exemplos incorretos, os rótulos de controle têm verbos instrutivos que se aplicam a todos os controles de seu tipo.

-   Em alguns casos, as seguintes anotações entre parênteses para controlar rótulos podem ser úteis:
    -   **Se uma opção for opcional, considere adicionar "(opcional)" ao rótulo.**
    -   **Se uma opção for altamente recomendável, adicione "(recomendado)" ao rótulo.** Isso significa que a configuração é opcional, mas deve ser definida de qualquer forma.
    -   **Se uma opção for destinada apenas a usuários avançados, considere adicionar "(avançado)" ao rótulo.**
-   Você pode especificar unidades (segundos, conexões e assim por diante) entre parênteses após o rótulo.

    ![captura de tela do rótulo: tamanho inicial (MB) ](images/text-ui-image44.png)

    Este exemplo mostra que a unidade de medida é de megabytes (MB).

Para obter mais informações, consulte a seção "texto" ou "rótulos" nas diretrizes específicas do componente da interface do usuário.

### <a name="supplemental-explanations"></a>Explicações suplementares

-   **Use explicações suplementares quando os controles exigirem mais informações do que podem ser transmitidos por seu rótulo.** Mas não use uma explicação suplementar se uma não for necessária, prefira comunicar tudo com o rótulo de controle se você puder fazer isso de forma concisa. Normalmente, explicações suplementares são usadas com links de comando, botões de opção e caixas de seleção.
-   Quando necessário, **use negrito nos rótulos de controle para facilitar a verificação do texto** quando houver explicações suplementares.

    ![captura de tela da caixa de diálogo Configurações de segurança ](images/text-ui-image45.png)

    Neste exemplo, os rótulos do botão de opção estão em negrito para facilitar a verificação.

-   **Adicionar uma explicação suplementar a um controle em um grupo não significa que você precisa fornecer explicações para todos os outros controles no grupo.** Forneça as informações relevantes no rótulo se você puder e usar explicações somente quando necessário. Não tenha explicações suplementares que simplesmente redeclarem o rótulo para fins de consistência.

    ![captura de tela de três botões de opção ](images/text-ui-image46.png)

    Neste exemplo, dois controles no grupo incluem explicações suplementares, mas o terceiro não.

-   Se uma explicação suplementar seguir um link de comando, grave o texto suplementar na segunda pessoa.

    **Exemplo:** Link de comando: criar configurações de rede sem fio e salvar na unidade flash USB

    Explicação suplementar: isso criará configurações que você pode transferir para o roteador com uma unidade flash USB. Faça isso somente se você tiver um roteador sem fio que dê suporte à configuração da unidade flash USB.

-   Use frases completas e pontuação final.

### <a name="commit-button-labels"></a>Rótulos do botão confirmar

A tabela a seguir mostra os rótulos de botão de confirmação mais comuns e seu uso.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Rótulo do botão</strong><br/></td>
<td><strong>Significado</strong><br/></td>
<td><strong>Quando usar</strong><br/></td>
<td><strong>Chave de acesso</strong><br/></td>
</tr>
<tr class="even">
<td><strong>OK</strong><br/></td>
<td><ul>
<li>Nas caixas de diálogo: aplique as alterações ou confirme-as à tarefa e feche a janela.</li>
<li>Nas janelas de propriedades do proprietário: aplique as alterações pendentes (feitas desde que a janela foi aberta ou a última aplicação) e feche a janela.</li>
<li>Janelas de propriedade pertencentes: Mantenha as alterações, feche a janela e aplique as alterações quando as alterações da janela do proprietário forem aplicadas.</li>
</ul></td>
<td><ul>
<li>Use com o Windows que não são específicas à tarefa, como folhas de propriedades.</li>
<li>Para o Windows usado para executar uma tarefa específica, use um rótulo específico, em vez disso, que comece com um verbo (exemplo: Print).</li>
<li>Para o Windows no qual os usuários não podem fazer alterações, use fechar.</li>
</ul></td>
<td>Digite<br/></td>
</tr>
<tr class="odd">
<td><strong>Sim/não</strong><br/></td>
<td>Sim é a resposta afirmativo para uma pergunta Sim ou não, enquanto que não é a resposta negativa.<br/></td>
<td><ul>
<li>Use os botões Sim e não apenas para responder a sim ou nenhuma pergunta. Nunca use OK e cancele para Sim ou sem perguntas.</li>
<li>Prefira respostas específicas nos botões Sim e não. Embora não haja nada de errado com o uso de Sim e não, respostas específicas podem ser compreendidas mais rapidamente, resultando em uma tomada de decisão eficiente.</li>
<li>No entanto, considere o uso de Sim e nenhuma resposta se a frase de respostas específicas se tornar longa ou estranha.</li>
<li>Não use botões Sim e não se o significado da resposta não estiver claro. Nesse caso, use respostas específicas.</li>
<li>Sim e não deve sempre ser usado como um par.</li>
</ul></td>
<td>S e N<br/></td>
</tr>
<tr class="even">
<td><strong>Cancelar</strong><br/></td>
<td><ul>
<li>Nas caixas de diálogo: descartar todas as alterações ou o trabalho em andamento, reverter para o estado anterior (não deixando nenhum efeito colateral perceptível) e fechará a janela.</li>
<li>Em folhas de propriedades: descartar todas as alterações pendentes (feitas desde que a janela foi aberta ou a última aplicação) e fechar a janela.</li>
<li>Em itens do painel de controle: descartar todas as alterações ou trabalho em andamento, reverter para o estado anterior e retornar para a página de Hub da qual a tarefa foi iniciada. Se não houver essa página de Hub, feche a janela do item do painel de controle.</li>
</ul></td>
<td><ul>
<li>Use quando todas as alterações ou ações pendentes puderem ser descartadas e qualquer efeito colateral puder ser desfeito.</li>
<li>Para as alterações que não podem ser descartadas, use fechar. Para ações em andamento que podem ser interrompidas, use parar. Se as alterações iniciais ou as ações puderem ser descartadas, você poderá usar cancelar inicialmente e, em seguida, alterar para fechar ou parar quando não puder ser desfeita.</li>
</ul></td>
<td>Esc<br/></td>
</tr>
<tr class="odd">
<td><strong>Close</strong><br/></td>
<td>Feche a janela. Quaisquer alterações ou efeitos colaterais não são descartados.<br/></td>
<td><ul>
<li>Use quando as alterações ou os efeitos colaterais não puderem ser descartados. Use fechar em vez de cancelar para janelas primárias.</li>
<li>Use o para Windows no qual os usuários não podem fazer alterações.</li>
</ul></td>
<td>ALT + F4, CTRL + F4<br/></td>
</tr>
<tr class="even">
<td><strong>Parar</strong><br/></td>
<td>Pare uma tarefa em execução no momento e feche a janela. Qualquer trabalho em andamento ou efeitos colaterais não são descartados.<br/></td>
<td><ul>
<li>Use quando o trabalho em andamento e qualquer efeito colateral não puder ou não ser descartado, normalmente com barras de progresso ou animações.</li>
</ul></td>
<td>Esc<br/></td>
</tr>
<tr class="odd">
<td><strong>Aplicar</strong><br/></td>
<td>Nas folhas de propriedades do proprietário: aplique as alterações pendentes (feitas desde que a janela foi aberta ou a última aplicação), mas deixe a janela aberta. Isso permite que os usuários avaliem as alterações antes de fechar a folha de propriedades. Folhas de propriedades de propriedade: não use.<br/></td>
<td><ul>
<li>Use somente em folhas de propriedades.</li>
<li>Forneça um botão aplicar somente se a folha de propriedades tiver configurações (pelo menos uma) com efeitos que os usuários podem avaliar de maneira significativa. Normalmente, os botões aplicar são usados quando as configurações fazem alterações visíveis. Os usuários devem ser capazes de aplicar uma alteração, avaliar a alteração e fazer outras alterações com base nessa avaliação. Caso contrário, remova o botão aplicar em vez de desabilitá-lo.</li>
</ul></td>
<td>Um<br/></td>
</tr>
<tr class="even">
<td><strong>Próximo</strong><br/></td>
<td>Em assistentes e tarefas de várias etapas: avance para a próxima etapa sem confirmar a tarefa.<br/></td>
<td><ul>
<li>Use somente em assistentes e tarefas de várias etapas para avançar para a próxima etapa sem compromisso.</li>
<li>O efeito de um botão Avançar sempre pode ser desfeito clicando em voltar.</li>
</ul></td>
<td>N<br/></td>
</tr>
<tr class="odd">
<td><strong>Concluir</strong><br/></td>
<td>Em assistentes e tarefas de várias etapas: Feche a janela. Se a tarefa ainda não tiver sido executada, execute a tarefa. Se essa tarefa já tiver sido executada, quaisquer alterações ou efeitos colaterais não serão descartados.<br/></td>
<td><ul>
<li>Use somente em assistentes e tarefas de várias etapas. No entanto, o uso de Finish é desencorajado porque geralmente há um botão de confirmação melhor e mais específico:
<ul>
<li>Se você clicar no botão for confirmado na tarefa (para que a tarefa ainda não tenha sido executada), use um rótulo específico que comece com um verbo (exemplos: imprimir, conectar, iniciar) que seja uma resposta à instrução principal.</li>
<li>Se a tarefa já tiver sido executada no assistente, use fechar em vez disso.</li>
</ul></li>
<li>No entanto, você pode usar concluir quando:
<ul>
<li>O rótulo específico ainda é genérico, como salvar, selecionar, escolher ou obter.</li>
<li>A tarefa envolve alterar uma configuração ou uma coleção de configurações.</li>
</ul></li>
</ul></td>
<td>Digite<br/></td>
</tr>
<tr class="even">
<td><strong>Concluído</strong><br/></td>
<td>Não aplicável.<br/></td>
<td><ul>
<li>Não use. Concluído como um comando está gramaticalmente incorreto.</li>
</ul></td>
<td>Não aplicável.<br/></td>
</tr>
</tbody>
</table>



 

