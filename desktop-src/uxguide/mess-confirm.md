---
title: Confirmações
description: Uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja continuar com uma ação.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 22fc59cee7ebd02ae5e97b5a4db9549848267120
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987459"
---
# <a name="confirmations"></a>Confirmações

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja continuar com uma ação.

![Captura de tela que mostra Bloco de notas "você deseja salvar as alterações?". .](images/mess-confirm-image1.png)

Uma confirmação típica.

As confirmações têm estas características essenciais:

-   Eles são exibidos como o resultado direto de uma ação iniciada pelo usuário.
-   Eles verificam se o usuário deseja continuar com a ação.
-   Eles consistem em uma pergunta simples e duas ou mais respostas.

As confirmações são mais úteis quando a ação exige que o usuário faça uma escolha relevante e distinta que não pode ser feita posteriormente. Essa opção geralmente envolve algum elemento de risco que não é óbvio para o usuário, mas o risco não é essencial para confirmações. Esses elementos são necessários para justificar a interrupção da resposta a um diálogo modal.

Por outro lado, [as mensagens de](mess-warn.md) aviso apresentam uma condição que pode causar um problema no futuro. Sua característica fundamental é que eles envolvem riscos:

-   Eles envolvem uma possível perda de um ou mais dos seguintes:
    -   Um ativo valioso, como perda de dados ou perda financeira.
    -   Acesso ou integridade do sistema.
    -   Privacidade ou controle sobre informações confidenciais.
    -   Tempo do usuário (uma quantidade significativa, como 30 segundos ou mais).
-   Eles têm consequências inesperadas ou não intencionais.
-   Agora, eles exigem o tratamento correto porque os erros não podem ser facilmente corrigidos e podem até mesmo ser irreversíveis.

Se uma confirmação envolver risco, ela também poderá ser considerada um aviso. Consequentemente, as diretrizes de mensagem de aviso também se aplicam.

**Observação:** As diretrizes relacionadas às [caixas de diálogo](win-dialog-box.md), mensagens [de](mess-error.md)erro, [layout](vis-layout.md)e mensagens [de aviso](mess-warn.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir, considere estas perguntas:

-   **O usuário está fazendo uma pergunta para prosseguir com uma ação que tem duas ou mais respostas?** Caso não seja, a mensagem não é uma confirmação.
-   **A interface do usuário está apresentando um erro ou problema que ocorreu?** Em caso afirmado, use uma [mensagem de erro.](mess-error.md)
-   **Continuar com a ação exige que o usuário faça uma escolha que não tenha um padrão adequado?** Em caso afirmaível, uma confirmação pode ser apropriada.
-   **Há um design alternativo que elimina a necessidade da confirmação?** A necessidade de uma confirmação às vezes indica uma falha de design. Geralmente, há uma alternativa de design melhor que não precisa de uma confirmação.
-   **O usuário está prestes a executar uma ação arriscada?** Em caso afirmativa, uma confirmação será apropriada se a ação tiver consequências significativas ou não puder ser facilmente desfeita.
-   **O usuário está prestes a abandonar uma tarefa?** Se sim, não confirme. Suponha que os usuários compreendam as consequências de não concluir uma tarefa.
-   **A ação tem consequências das quais os usuários podem não estar cientes?** Em caso afirmaível, uma confirmação pode ser apropriada.
-   **Considerando o contexto atual, os usuários provavelmente estão executando uma ação com erro?** Em caso afirmaível, uma confirmação pode ser apropriada.
-   **Os usuários executam a ação com frequência?** Se sim, considere um design alternativo. As confirmações frequentes são entediantes e têm pouco valor porque os usuários aprendem a responder sem pensar.
-   **A ação tem implicações de segurança?** Em caso afirmativos, uma confirmação pode ser necessária mesmo que os testes anteriores indiquem o contrário.

## <a name="design-concepts"></a>Conceitos de design

### <a name="unnecessary-confirmations-are-annoying"></a>As confirmações desnecessárias são entediantes

A primeira Windows que a primeira confirmação já foi criada sem dúvida se parece com esta:

![captura de tela de 'você tem certeza?' confirmação ](images/mess-confirm-image2.png)

A confirmação de confirmação de confirmação original.

Esse foi um início muito ruim. Se você quiser que os usuários odiam seu programa, basta confirmar confirmações como esta. Para entender o motivo, considere o ponto de vista do usuário. O usuário acabou de pedir para executar uma ação pela definição de uma confirmação para que, a menos que algo tenha sido de alguma forma clicado ou pressionado acidentalmente, é claro que o usuário deseja continuar.

Não apenas as confirmações desnecessárias são entediantes, mas não são eficazes na proteção do usuário contra erros. Os usuários descobrem rapidamente quando um programa tem confirmações desnecessárias e sua resposta natural é descartá-las o mais rápido possível, geralmente sem ler. Consequentemente, essas confirmações fazem pouco mais do que adicionar uma etapa extra a essas tarefas.

Não use confirmações apenas porque há a possibilidade de os usuários cometerem um erro. **Em vez disso, as confirmações são mais eficazes quando usadas para confirmar ações que têm consequências significativas ou não intencionais.** Boas confirmações nunca são o óbvio; eles devem comunicar algo que os usuários precisam estar cientes de um bom motivo para não continuar. E eles são usados somente quando são realmente necessários por uma ação, como pedir que os usuários salvem as alterações somente quando houver alterações que vale a pena salvar. Isso exige a atenção do usuário somente quando ele realmente é assegurado.

Para outros tipos de confirmações, geralmente há uma alternativa de design melhor do que forçar os usuários a responder a uma pergunta.

### <a name="consider-the-design-alternatives"></a>Considere as alternativas de design

Aqui estão algumas alternativas de design que eliminam a necessidade de confirmações de rotina:

-   **Evitar erros.** Projete tarefas para que erros significativos sejam difíceis de fazer acidentalmente. Por exemplo, separe comandos destrutivas fisicamente de outros comandos e exigirá a conclusão de várias ações.
-   **Forneça desfazer.** Forneça a capacidade de reverter ações. Por exemplo, a exclusão de um arquivo no Microsoft Windows geralmente não requer uma confirmação porque os arquivos excluídos podem ser recuperados do Lixeira. Observe que, se uma ação for muito fácil de executar, apenas fazer com que os usuários refeitom a ação pode ser suficiente.
-   **Forneça comentários.** Tornar resultados indesejáveis óbvios. Fornecer desfazer sozinho não será suficiente se os usuários não perceberem quando cometerem um erro. Por exemplo, o efeito da manipulação direta (como uma operação do tipo "arrastar e soltar" sempre deve ser óbvio.
-   **Suponha o resultado provável, mas facilmente altere.** Se você não tiver certeza do que os usuários querem, mas houver uma opção provável, segura e segura, suponha essa opção, deixe claro o que aconteceu e facilmente altere usando um menu de contexto. Por exemplo, Microsoft Word assume que os usuários querem ort ortá-lo corretamente. Se ele reconhecer uma palavra com ortografia incorretamente e souber a ortografia provavelmente correta, o Word fará a correção automaticamente, mas permitirá que os usuários revertem.
-   **Elimine completamente a escolha.** Se a escolha não for importante, os usuários não se importarão. Melhor simplificar [seu](/previous-versions//dn742474(v=vs.85)) programa e eliminar a escolha.

### <a name="make-confirmations-require-thought"></a>Fazer confirmações exigirem um pensamento

Para que uma confirmação tenha valor, os usuários precisam entender o motivo para não continuar. Às vezes, o motivo é óbvio, como quando os usuários estão fechando um documento com alterações que não foram salvas:

![Captura de tela que mostra Paint "Você deseja salvar as alterações?". .](images/mess-confirm-image3.png)

Neste exemplo, o motivo da confirmação é óbvio.

Em outras situações, o motivo pode não ser tão óbvio.

Ao escolher rótulos de botão de confirmação para caixas de diálogo, as diretrizes gerais são escolher [rótulos](win-dialog-box.md) que são respostas específicas para a instrução principal. Isso leva à tomada de decisão eficiente porque os usuários têm que ler uma quantidade mínima de texto para continuar. No entanto, essa meta de eficiência pode ser contraproducente para confirmações. Considere este exemplo:

**Incorreto:**

![captura de tela da confirmação com o botão de desinstalação ](images/mess-confirm-image4.png)

Neste exemplo, a resposta correta requer um pensamento.

Se você apresentar essa confirmação imediatamente após o usuário ter dado o comando Desinstalar, a resposta do usuário provavelmente será "É claro que quero desinstalar!" O usuário clicará em Desinstalar sem pensar duas vezes.

Para confirmações, não queremos que os usuários tomarem decisões emocional e hasty. Para incentivar os usuários a pensar em sua resposta, precisamos fornecer um pequeno aumento de velocidade de tomada de decisão. Quando prático, geralmente é melhor fazer isso frasendo cuidadosamente os botões de confirmação. Por exemplo, podemos usar linguagem adicional para indicar que há um motivo para não continuar.

**Melhor:**

![captura de tela do botão "desinstalar mesmo assim" ](images/mess-confirm-image5.png)

Neste exemplo, "de qualquer forma" é adicionado ao rótulo do botão de confirmação para indicar que a confirmação fornece um motivo para não continuar.

Se essa abordagem não for prática, podemos usar os botões Sim/Não de commit.

**Também é melhor:**

![captura de tela de confirmação com botões sim/não ](images/mess-confirm-image6.png)

Neste exemplo, usar botões de confirmação Sim/Não força os usuários a lerem pelo menos a instrução principal.

### <a name="provide-all-the-information"></a>Fornecer todas as informações

Se você for fazer uma pergunta, deverá fornecer informações suficientes para que os usuários respondam essa pergunta de forma inteligente. Considere a caixa de diálogo Confirmar Substituição de Arquivo Windows XP:

![captura de tela da caixa de diálogo 'confirmar substituição de arquivo' ](images/mess-confirm-image7.png)

A Windows caixa de diálogo Confirmar Substituição de Arquivo do XP.

Essa confirmação fornece todas as informações que os usuários talvez precisem para responder à pergunta? Antes de responder, considere os cenários de usuário mais comuns:

-   Copie (ou mova) o outro arquivo, substituindo o existente.
-   Mantenha o arquivo existente, sem copiar ou mover o outro arquivo.
-   Mantenha ou copie o arquivo mais novo (cenário principal).
-   Mantenha o arquivo existente ou copie o outro arquivo, dependendo de critérios como o conteúdo e o tamanho do arquivo.
-   Mantenha o arquivo existente e copie o outro arquivo usando um nome diferente.
-   Cancele a operação se algo estiver errado ou inesperado.

Os usuários podem obter o cenário 1 clicando em Sim e cenário 2 clicando em Não. Eles podem alcançar o cenário 3 comparando as datas do arquivo e clicando no botão apropriado, mas observe o quanto é necessário para determinar o arquivo mais recente e, em seguida, determinar o botão apropriado, especialmente para o que provavelmente será o cenário mais comum.

Os cenários 4, 5 e 6 também são surpreendentemente difíceis. Os tamanhos de arquivo são arredondados, portanto, por exemplo, é impossível determinar se esses arquivos têm o mesmo tamanho ou mesmo se são o mesmo arquivo. Os ícones são para o aplicativo usado para abrir o arquivo, portanto, os usuários teriam que abrir os arquivos para inspecionar e comparar seu conteúdo. Ter miniaturas do conteúdo do arquivo seria muito mais útil para responder à pergunta.

A confirmação copiar arquivo do Windows Vista faz um trabalho muito melhor de lidar com esses cenários fornecendo mais informações e adicionando a opção para manter ambos os arquivos:

![captura de tela da caixa de diálogo 'copiar arquivo' ](images/mess-confirm-image8.png)

A confirmação Windows Arquivo de Cópia do Vista.

### <a name="provide-specific-useful-information"></a>Fornecer informações específicas e úteis

Se você for fazer uma pergunta, verifique se os usuários entendem a pergunta e as implicações das respostas alternativas. Considere esta Windows Internet Explorer de segurança:

![captura de tela de confirmação com uma pergunta vaga ](images/mess-confirm-image9.png)

Uma confirmação de segurança vaga.

Essa confirmação faz uma pergunta que os usuários não podem responder de forma inteligente. O usuário solicitou que Windows Internet Explorer exibição de uma página e essa mensagem a aconselha implicitamente por meio do texto e realçando Não como a opção padrão.

O problema de segurança específico que a página apresenta não é explicado o suficiente, portanto, o risco de continuar não é claro. Quais informações na confirmação faria com que o usuário clicasse em Não? Devido à indefinição da mensagem, a confirmação provavelmente não vai desestimular os usuários a continuar, mas fará com que eles se sintam mal em fazer isso.

Para que essa confirmação seja útil, ela deve fornecer mais informações específicas que possam fazer com que o usuário decida não continuar. Em geral, para cada resposta em uma confirmação, considere os cenários que a exigem e certifique-se de que haja informações suficientes fornecidas para que os usuários quiserem escolher. Forneça opções, não contras.

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a>Como determinar se uma confirmação é necessária

Pensar nos cenários e a probabilidade de escolher cada resposta sugere uma maneira sistemática de determinar se uma confirmação é necessária. Se os usuários provavelmente selecionarem todas as respostas, a confirmação será necessária e útil. No entanto, se apenas uma resposta for provável (digamos 98% do tempo), a confirmação será claramente desnecessária e deverá ser removida. Observe que as confirmações relacionadas a problemas de segurança, legais e de segurança são possíveis exceções.

![captura de tela de 'você deseja alterar as configurações?' ](images/mess-confirm-image10.png)

Essa confirmação é necessária? Os usuários selecionarão Não? É possível, mas muito improvável. Essa confirmação deve ser removida.

**Se você fizer apenas três coisas...**

1. Certifique-se de que sua confirmação seja realmente necessária. Deve haver um motivo legítimo e claro para não continuar e uma chance de que, às vezes, os usuários não continuarão.

2. Se o motivo da confirmação não for imediatamente óbvio, escolha os botões de confirmação que incentivam os usuários a pensar em sua resposta. Normalmente, isso é feito frasendo a confirmação como uma pergunta sim ou não e fornecendo respostas completamente autoexplicativas ou Sim/Não.

3. Considere todos os cenários e forneça as informações necessárias para responder à pergunta de forma inteligente.

## <a name="usage-patterns"></a>Padrões de uso

As confirmações têm vários padrões de uso:



|   Uso                                                                                                                                                                    |    Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Confirmações de rotina**<br/> confirme se o usuário deseja continuar com uma ação rotineira e de baixo risco. <br/>                                              | Essas confirmações geralmente são formuladas como "você tem certeza...?" e geralmente têm uma caixa de seleção não mostrar essa mensagem novamente para minimizar sua desremissão. <br/> ![captura de tela de 'mover pasta para lixeira?' ](images/mess-confirm-image11.png)<br/> ![captura de tela de "não mostrar a mensagem novamente" ](images/mess-confirm-image12.png)<br/> Exemplos de confirmações de rotina.<br/> **Observação:** Esse padrão geralmente é desnecessário e deve ser evitado.<br/>                                                                                                                                                                                                                                                                                        |
| **Confirmações de ação arriscada**<br/> confirme se o usuário deseja prosseguir com uma ação que tem algum risco e não pode ser facilmente desfeita. <br/>            | Como eles têm risco, essas confirmações geralmente têm um ícone de aviso. <br/> ![Captura de tela que mostra um exemplo de confirmação de formatação de volume.](images/mess-confirm-image13.png)<br/> ![Captura de tela que mostra um exemplo de confirmação de exclusão permanente.](images/mess-confirm-image14.png)<br/> Exemplos de confirmações de ação arriscada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Confirmações de consequência não intencionais**<br/> confirme se o usuário deseja prosseguir com uma ação que tem consequências inesperadas ou não intencionais. <br/> | Além de fazer uma pergunta, essas confirmações apontam as consequências não intencionais. como elas têm consequências não intencionais, essas confirmações geralmente têm um ícone de aviso. <br/> ![captura de tela de 'fechar todas as guias?' Confirmação ](images/mess-confirm-image15.png)<br/> ![captura de tela de 'cancelar instalação?' Confirmação ](images/mess-confirm-image16.png)<br/> exemplos de confirmações de consequências não intencionais.<br/> no entanto, esse padrão requer que as consequências sejam realmente involutas. <br/> **Incorreto:**<br/> ![captura de tela de 'desligar o key logger?' Confirme ](images/mess-confirm-image17.png)<br/> As consequências são destinadas aqui, portanto, essa é uma confirmação de rotina.<br/> |
| **Esclarecimentos**<br/> esclareça como o usuário deseja prosseguir com uma ação que tenha consequências potencialmente ambíguas ou inesperadas. <br/>             | As operações de arrastar e soltar podem resultar em esclarecimentos se o efeito da operação puder ser interpretado incorretamente. <br/> ![captura de tela de ' alterar apenas esta ocorrência? '](images/mess-confirm-image18.png)<br/> ![captura de tela de ' sempre salvar ao sair? ' Confirme ](images/mess-confirm-image19.png)<br/> Exemplos de esclarecimentos.<br/> **Observação:** Esse padrão deve ser evitado porque é melhor criar ações sem consequências ambíguas e assumir o resultado desejado mais provável. <br/>                                                                                                                                                                                                                                     |
| **Confirmações de segurança**<br/> Confirme se o usuário deseja continuar com uma ação com consequências de segurança. <br/>                                   | ![captura de tela de ' deseja executar este software? ' ](images/mess-confirm-image20.png)<br/> ![captura de tela de ' lembrar senha? ' confirmação ](images/mess-confirm-image21.png)<br/> Exemplos de confirmações de segurança.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Confirmações do ulterior motivação**<br/> forneça informações sobre uma ação, mas apresente-as como uma confirmação. <br/>                                       | Embora essas caixas de diálogo sejam apresentadas como confirmações, sua verdadeira meta é a educação do usuário ou o anúncio dos recursos. <br/> ![captura de tela de deseja esta barra de ferramentas na barra de tarefas? ](images/mess-confirm-image22.png)<br/> Um exemplo de uma confirmação da motivação de ulterior.<br/> **Observação:** Esse padrão não é recomendado porque geralmente há uma alternativa melhor e mais direta. Por exemplo, as [animações](vis-animations.md) são uma maneira melhor de mostrar a relação entre causa e efeito. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Use confirmações "salvar alterações" somente quando houver alterações significativas.** Não confirme as alterações que não foram feitas diretamente pelo usuário, como reformatação automática de documentos.

**Incorreto:**

![captura de tela que mostra um Microsoft Office Outlook ' deseja salvar as alterações? ' .](images/mess-confirm-image23.png)

Este exemplo está incorreto quando usado para um email ou documento vazio que não foi alterado pelo usuário.

### <a name="icons"></a>Ícones

-   Confirmações não usam ícones da barra de título.
-   **O ícone da área de conteúdo para uma confirmação é baseado em seu padrão de design:**



    | Padrão                                                | ícone                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | Confirmações rotineiras <br/>                | Nenhum ícone. <br/>                                                                                                                         |
    | Confirmações de ações arriscadas <br/>           | Ícone de aviso. <br/>                                                                                                                    |
    | Confirmações de conseqüência não intencional <br/> | Use um ícone de aviso se houver risco, o ícone de recurso, se disponível; caso contrário, nenhum ícone. <br/>                                          |
    | Esclarecimentos <br/>                       | Se a confirmação envolver um documento, use a miniatura do documento; caso contrário, use o ícone de recurso, se disponível, ou nenhum ícone. <br/> |
    | Confirmações de segurança <br/>               | Ícone de aviso. <br/>                                                                                                                    |
    | Confirmações do ulterior motivação <br/>        | Nenhum ícone. <br/>                                                                                                                         |



 

-   **Não use ícones de aviso para perguntas rotineiras.** fazer isso é um contador para o [tom incentivado de Windows](text-style-tone.md) e faz com que o seu programa se sinta como uma atividade perigosa. Suponha que os usuários compreendam as consequências de cancelar uma tarefa antes que ela seja concluída.

**Incorreto:**

![captura de tela de ' deseja encerrar o tutorial? ' ](images/mess-confirm-image24.png)

Neste exemplo, um ícone de aviso é usado para fazer uma pergunta rotineira.

### <a name="commit-buttons"></a>Botões de confirmação

-   **Use respostas específicas para a instrução principal se o motivo da confirmação for óbvio ou se puder se tornar auto-explicativo.**

![captura de tela de ' deseja salvar as alterações? ' ](images/mess-confirm-image25.png)

Neste exemplo, o motivo da confirmação é óbvio, portanto, salve e não salve bem o trabalho.

-   **Caso contrário, use os botões Sim e não para respostas de confirmação.** Isso faz com que os usuários consigam pensar na confirmação antes de responder. Nunca use OK e cancele para confirmações.

**Correto:**

![captura de tela de ' deseja desinstalar arquivos de suporte? ' ](images/mess-confirm-image26.png)

Neste exemplo, o uso de botões Sim/não confirmar força os usuários a, pelo menos, ler a instrução principal.

**Incorreto:**

![captura de tela de ' cancelar sua reserva? ' ](images/mess-confirm-image27.png)

Neste exemplo, usar OK/cancelar é confuso.

-   **para fechar um programa ou reiniciar Windows, use respostas específicas para a instrução principal.** Para evitar qualquer mal-entendido, não use fechar ou sim/não para essa finalidade.

**Correto:**

![captura de tela do botão reiniciar o Windows agora](images/mess-confirm-image28.png)

**Incorreto:**

![captura de tela do botão Sim](images/mess-confirm-image29.png)

No exemplo incorreto, sim é usado para reiniciar Windows.

### <a name="command-links"></a>Links de comando

-   **Para o padrão de esclarecimentos, considere o uso de links de comando para tornar as alternativas claras.**

**Aceitável:**

![captura de tela de ' alterar uma ou todas as ocorrências? ' ](images/mess-confirm-image30.png)

**Melhor:**

![captura de tela da mesma pergunta usando links de comando ](images/mess-confirm-image31.png)

No exemplo melhor, os links de comando tornam as alternativas desclaradas.

-   **Apresente os links de comando mais comumente usados primeiro.** A ordem resultante deve seguir aproximadamente a probabilidade de uso, mas também ter um fluxo lógico.
-   Se um link de comando exigir mais explicações, **forneça uma explicação suplementar.** Explicações suplementares descrevem por que os usuários talvez queiram escolher a opção ou o que acontece se a opção for escolhida.

Para obter mais diretrizes e exemplos, consulte [links de comando](ctrl-command-links.md).

### <a name="default-values"></a>Valores padrão

-   **A resposta padrão para uma confirmação é baseada em seu padrão de design:**



    | Padrão                                                 | Resposta padrão                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | Confirmações rotineiras <br/>                | Dar. <br/>                                                            |
    | Confirmações de ações arriscadas <br/>           | Não prossiga (ou a opção segura). <br/>                                 |
    | Confirmações de conseqüência não intencional <br/> | Se as consequências forem significativas, não continue; caso contrário, continue. <br/> |
    | Esclarecimentos <br/>                       | A resposta mais provável. <br/>                                           |
    | Confirmações de segurança <br/>               | Não continue. <br/>                                                      |
    | Confirmações de motivo ulterior <br/>        | Prosseguir. <br/>                                                            |



 

### <a name="dont-show-this-message-again"></a>Não mostre essa mensagem novamente

-   **Use essa opção somente para os padrões de confirmação de motivação de rotina e ulterior.** Para os outros padrões, se as informações são necessárias, ela sempre deve ser exibida.
-   **Não forneça essa opção para justificar a exibição de uma confirmação desnecessária.** Em vez disso, basta se desfazer da confirmação.

**Incorreto:**

![captura de tela de 'descartar esses lembretes?' ](images/mess-confirm-image32.png)

**Ainda incorreto:**

![captura de tela de "não mostrar a mensagem novamente"](images/mess-confirm-image33.png)

Nesses exemplos, adicionar uma opção Não mostrar esta mensagem novamente não corrige uma confirmação desnecessária.

Para obter mais diretrizes, consulte Caixas [de diálogo](win-dialog-box.md).

### <a name="bulk-operations"></a>Operações em massa

-   Para confirmações que se aplicam a operações em massa, forneça uma opção para aplicar a confirmação a toda a operação.

![captura de tela de 'fazer isso para todos os itens?' caixa de seleção ](images/mess-confirm-image34.png)

Este exemplo tem uma opção para operações em massa.

-   Elimine ou adia as confirmações em uma operação em massa.

**Incorreto:**

![captura de tela da caixa de diálogo 'confirmar exclusão de arquivo' ](images/mess-confirm-image35.png)

Neste exemplo, Windows Explorer no Windows XP confirma cada arquivo somente leitura durante uma movimentação de arquivo em massa. Melhor apenas copiar os arquivos somente leitura sem perguntar ou adiar o tratamento desses arquivos e apresentar a confirmação no final da tarefa.

### <a name="progressive-disclosure&quot;></a>Divulgação progressiva

-   **Se você precisa incluir informações avançadas em uma mensagem de confirmação, mostre-as usando botões de divulgação progressiva (por exemplo, &quot;Mostrar detalhes").** Isso simplifica a confirmação de uso típico. Não o oculta as informações necessárias porque os usuários podem não encontrá-los.
-   **Não use "Mostrar detalhes", a menos que realmente haja mais detalhes.** Não apenas restate as informações existentes em um formato diferente.

Para diretrizes de rotulagem, consulte [Divulgação progressiva.](ctrl-progressive-disclosure-controls.md)

### <a name="user-account-control"></a>Controle de Conta de Usuário

-   **Não use a interface do usuário de elevação do UAC (Controle de Conta de Usuário) como um substituto para uma confirmação.** Se uma ação precisar de uma confirmação, use uma caixa de diálogo separada. Durante a [interface do usuário de](winenv-uac.md)elevação, os usuários precisam se concentrar em se iniciaram a tarefa e se o programa é confiável.
-   **Exibir a confirmação antes da interface do usuário de elevação.** Isso elimina as elevações desnecessárias.

## <a name="text"></a>Texto

### <a name="general"></a>Geral

-   **Remova texto redundante.** Procure texto redundante em títulos, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de commit. Em geral, deixe texto completo em instruções e controles interativos e remova qualquer redundância de outros locais.
-   **Não use "aviso" ou "cuidado" no texto.** Se os usuários precisam continuar com cuidado, indique isso usando um ícone de aviso.

**Incorreto:**

![captura de tela da confirmação de formatação de volume ](images/mess-confirm-image36.png)

Neste exemplo, o termo "aviso" é desnecessário.

### <a name="titles"></a>Títulos

-   **Use o título para identificar o comando ou o recurso de onde veio a confirmação. Exceções:**
    -   Se uma confirmação for exibida por muitos comandos diferentes, considere usar o nome do programa.
    -   Se esse título for redundante ou confuso com a instrução principal, use o nome do programa.

No entanto, se a confirmação for de uma tarefa de execução longa e pode ser exibida bem após o início da tarefa, sempre use o comando ou o recurso para identificar claramente o contexto.

-   **Não use o título para explicar o que fazer na caixa** de diálogo que é a finalidade da instrução principal.
-   Se ele adiciona clareza, inicie o título com a palavra Confirmar.
-   **Para confirmações de ação arriscada, você pode adicionar o nome do objeto envolvido para ênfase extra.**

![captura de tela do título da caixa de diálogo 'format f drive' ](images/mess-confirm-image13.png)

Neste exemplo, a unidade a ser formatada está incluída no título.

-   Use [a capitalização de estilo de título](glossary.md), sem terminar a pontuação.

### <a name="main-instructions"></a>Instruções principais

-   **A instrução principal para uma confirmação baseia-se em seu padrão de design:**



    | Padrão                                                 | Instrução principal                                                                                                                                                                                                                                                                                                                                                                                                          |
    |--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Confirmações de consequência não intencionais <br/> | o estado da consequência não intencional.<br/> **exceção:** se uma pergunta perguntando se o usuário deseja continuar claramente implica a consequência não intencional, faça a pergunta. <br/> ![captura de tela de 'fechar todas as guias?' Confirmação ](images/mess-confirm-image15.png)<br/> Neste exemplo, pedir que o usuário prossiga o suficiente transmite as consequências da ação.<br/> |
    | Todos os outros <br/>                           | Faça uma única pergunta para determinar se o usuário deseja continuar. <br/>                                                                                                                                                                                                                                                                                                                              |



 

-   **Seja conciso, use apenas uma única frase completa.** Desmtrua a instrução principal para as informações essenciais. Se você precisa explicar mais alguma coisa, use uma instrução complementar.
-   **Seja específico se houver objetos envolvidos, dê seus nomes completos.**
-   **Use frases positivas.** Frase positiva é mais fácil para os usuários entenderem.

**Correto:**

Você deseja habilitar o compartilhamento de arquivos e impressoras?

**Incorreto:**

Você deseja desabilitar o compartilhamento de arquivos e impressoras?

No entanto, a frase deve corresponder ao comando associado, mesmo que o comando seja frasedo negativamente; portanto, por exemplo, use disable para confirmar um comando Disable.

-   Embora não haja regras estritas para frases, essas frases de confirmação **comuns têm a conotação indicada:**



    | Frase                                                            | Conotação                                                            |
    |-------------------------------------------------------------|-------------------------------------------------------------|
    | Tem certeza de que deseja \[ executar uma \] ação? <br/> | Confirmar o resultado direto de uma solicitação de usuário. <br/> |
    | Você deseja executar \[ uma ação \] ? <br/>           | Confirmar um efeito colateral de uma solicitação de usuário. <br/>     |
    | Você gostaria de \[ selecionar um \] resultado? <br/>          | Precisa de um esclarecimento. <br/>                           |
    | \[Executar uma ação \] ? <br/>                          | Nenhuma conotação. <br/>                                 |



 

-   Para confirmações de ação arriscada, use o termo permanentemente para indicar que uma ação não pode ser desfeita.

![captura de tela da confirmação de exclusão permanente ](images/mess-confirm-image37.png)

Neste exemplo, "permanentemente" indica que a ação não pode ser desfeita.

-   Use [a capitalização de estilo de frase](glossary.md).

### <a name="supplemental-instructions"></a>Instruções complementares

-   **A instrução complementar para uma confirmação baseia-se em seu padrão de design:**

    
| Rótulo | Valor |
|--------|-------|
| <strong>Padrão</strong><br /> | <strong>Instrução complementar</strong><br /> | 
| Confirmações de conseqüência não intencional <br /> | Faça uma única pergunta para determinar se o usuário deseja continuar. <br /> | 
| Todos os outros <br /> | Explique quaisquer motivos não óbvios pelos quais o usuário talvez não queira continuar. Tais motivos incluem: <br /><ul><li>Possível perda de um ou mais dos seguintes itens:    <ul><li>Um ativo valioso, como perda de dados ou perda financeira.</li><li>Integridade ou acesso do sistema.</li><li>Privacidade ou controle sobre informações confidenciais.</li></ul></li><li>Ações que são irreversíveis.</li></ul> | 


    

     

-   **Não repita a instrução principal com uma palavra ligeiramente diferente.** Em vez disso, omita a instrução complementar se não houver mais a adicionar.
-   **Para confirmações de conseqüência não intencional, considere usar o termo de qualquer forma para indicar de forma concisa que há um motivo para não continuar** caso o usuário tenha ignorado a instrução principal. Consulte conceitos de design para obter mais informações.
-   Use frases completas, maiúsculas e minúsculas no estilo da frase e pontuação final.

## <a name="documentation"></a>Documentação

Ao fazer referência a confirmações:

-   Consulte uma confirmação por seu título se o título for específico para a confirmação (ou seja, não o nome do programa); caso contrário, consulte-o por sua instrução principal.
-   Se necessário, você pode se referir a uma caixa de diálogo de confirmação como uma mensagem.
-   Use o texto exato, incluindo sua capitalização.
-   Quando possível, formate o texto usando negrito. Caso contrário, coloque o texto entre aspas somente se necessário para evitar confusão.

Exemplo: na mensagem **Copiar arquivo** , clique no arquivo mais recente.

