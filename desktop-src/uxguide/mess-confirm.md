---
title: Confirmações
description: Uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja continuar com uma ação.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 321cab040423df3a6dc0069d568d66c85e3aa8cc
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524520"
---
# <a name="confirmations"></a>Confirmações

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja continuar com uma ação.

![Captura de tela que mostra um bloco de notas "você deseja salvar alterações?". .](images/mess-confirm-image1.png)

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

A primeira confirmação do Windows criada sem dúvida se parece com esta:

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
-   **Suponha o resultado provável, mas facilmente altere.** Se você não tiver certeza do que os usuários querem, mas houver uma opção provável, segura e segura, suponha essa opção, deixe claro o que aconteceu e facilmente altere usando um menu de contexto. Por exemplo, o Microsoft Word presume que os usuários querem ort ortá-lo corretamente. Se ele reconhecer uma palavra com ortografia incorretamente e souber a ortografia provavelmente correta, o Word fará a correção automaticamente, mas permitirá que os usuários revertem.
-   **Elimine completamente a escolha.** Se a escolha não for importante, os usuários não se importarão. Melhor simplificar [seu](/previous-versions//dn742474(v=vs.85)) programa e eliminar a escolha.

### <a name="make-confirmations-require-thought"></a>Fazer confirmações exigirem um pensamento

Para que uma confirmação tenha valor, os usuários precisam entender o motivo para não continuar. Às vezes, o motivo é óbvio, como quando os usuários estão fechando um documento com alterações que não foram salvas:

![Captura de tela que mostra uma pintura "Você deseja salvar as alterações?". .](images/mess-confirm-image3.png)

Neste exemplo, o motivo da confirmação é óbvio.

Em outras situações, o motivo pode não ser tão óbvio.

Ao escolher rótulos de botão de confirmação para caixas de diálogo, as diretrizes gerais são escolher [rótulos](win-dialog-box.md) que são respostas específicas para a instrução principal. Isso leva a uma tomada de decisão eficiente, pois os usuários precisam ler uma quantidade mínima de texto para continuar. No entanto, essa meta de eficiência pode ser contratada para confirmações. Considere este exemplo:

**Incorreto:**

![captura de tela de confirmação com o botão desinstalar ](images/mess-confirm-image4.png)

Neste exemplo, a resposta correta requer pensamento.

Se você apresentar essa confirmação imediatamente depois que o usuário tiver fornecido o comando de desinstalação, a resposta do usuário provavelmente será "é claro que desejo desinstalar!" O usuário clicará em desinstalar sem dar uma segunda ideia.

Para confirmações, não queremos que os usuários façam decisões apressars e emocional. Para encorajar os usuários a pensar sobre sua resposta, precisamos fornecer um pequeno aumento de velocidade de tomada de decisões. Quando for prático, geralmente é melhor fazer isso com a frase cuidadosa dos botões de confirmação. Por exemplo, podemos usar idioma adicional para indicar que há um motivo para não continuar.

**Melhor:**

![captura de tela do botão ' desinstalar de qualquer forma ' ](images/mess-confirm-image5.png)

Neste exemplo, "mesmo assim" é adicionado ao rótulo do botão confirmar para indicar que a confirmação fornece um motivo para não continuar.

Se essa abordagem não for prática, podemos usar botões de confirmação Sim/não.

**Também melhor:**

![captura de tela de confirmação com botões Sim/não ](images/mess-confirm-image6.png)

Neste exemplo, o uso de botões Sim/não confirmar força os usuários a, pelo menos, ler a instrução principal.

### <a name="provide-all-the-information"></a>Fornecer todas as informações

Se você for fazer uma pergunta, deverá fornecer informações suficientes para que os usuários respondam a essa pergunta de forma inteligente. Considere a caixa de diálogo Confirmar substituição de arquivo do Windows XP:

![captura de tela da caixa de diálogo ' Confirmar substituição de arquivo ' ](images/mess-confirm-image7.png)

A caixa de diálogo Confirmar substituição de arquivo do Windows XP.

Essa confirmação fornece todas as informações que os usuários podem precisar para responder à pergunta? Antes de responder, considere os cenários de usuário mais comuns:

-   Copie (ou mova) o outro arquivo, substituindo o existente.
-   Mantenha o arquivo existente, sem copiar ou mover o outro arquivo.
-   Mantenha ou copie o arquivo mais recente (cenário superior).
-   Mantenha o arquivo existente ou copie o outro arquivo, dependendo de critérios como o conteúdo e o tamanho do arquivo.
-   Mantenha o arquivo existente e copie o outro arquivo usando um nome diferente.
-   Cancele a operação se algo estiver errado ou inesperado.

Os usuários podem obter o cenário 1 clicando em Sim e cenário 2 clicando em não. Eles podem obter o cenário 3 comparando as datas dos arquivos e clicando no botão apropriado, mas observe o quanto você precisa para determinar o arquivo mais recente e, em seguida, determinar o botão apropriado, especialmente para o que é provavelmente o cenário mais comum.

Os cenários 4, 5 e 6 também são surpreendentemente difíceis. Os tamanhos de arquivo são arredondados, portanto, por exemplo, é impossível determinar se esses arquivos têm o mesmo tamanho ou mesmo se eles forem o mesmo arquivo. Os ícones são para o aplicativo usado para abrir o arquivo, para que os usuários precisem abrir os arquivos para inspecionar e comparar seu conteúdo. Ter miniaturas do conteúdo do arquivo seria muito mais útil para responder à pergunta.

A confirmação de cópia de arquivo do Windows Vista faz um trabalho muito melhor de lidar com esses cenários, fornecendo mais informações e adicionando a opção para manter ambos os arquivos:

![captura de tela da caixa de diálogo ' Copiar arquivo ' ](images/mess-confirm-image8.png)

A confirmação do arquivo de cópia do Windows Vista.

### <a name="provide-specific-useful-information"></a>Forneça informações úteis específicas

Se você for fazer uma pergunta, certifique-se de que os usuários compreendam a pergunta e as implicações das respostas alternativas. Considere esta confirmação de segurança do Windows Internet Explorer:

![captura de tela de confirmação com uma pergunta vaga ](images/mess-confirm-image9.png)

Uma confirmação de segurança vaga.

Essa confirmação faz uma pergunta de que os usuários não podem possivelmente responder de forma inteligente. O usuário solicitou que o Windows Internet Explorer exiba uma página, e essa mensagem aconselha a ele implicitamente por meio de palavras do texto e realçando não como a opção padrão.

O problema de segurança específico que a página representa não é explicado suficientemente, portanto, o risco de continuar não é claro. Quais informações na confirmação fariam com que o usuário já clicasse em não? Devido à irvagação da mensagem, a confirmação não é provavelmente desencorajar os usuários de continuar, mas fará com que eles se sintam ruins para isso.

Para que essa confirmação seja útil, ela deve fornecer mais informações específicas sobre informações que podem fazer com que o usuário decida não continuar. Em geral, para cada resposta em uma confirmação, considere os cenários que exigem e certifique-se de que há informações suficientes para que os usuários queiram escolher. Forneça opções, não dilemas.

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a>Como determinar se uma confirmação é necessária

Pensar nos cenários e a probabilidade de escolher cada resposta sugere uma maneira sistemática de determinar se uma confirmação é necessária. Se for provável que os usuários selecionem todas as respostas, a confirmação será necessária e útil. No entanto, se apenas uma resposta for provável (digamos, 98% do tempo), a confirmação será claramente desnecessária e deverá ser removida. Observe que confirmações relacionadas a problemas de segurança, legal e segurança são possíveis exceções.

![captura de tela de ' deseja alterar as configurações? ' ](images/mess-confirm-image10.png)

Essa confirmação é necessária? Os usuários nunca selecionarão nenhum? É possível, mas muito impossibilidade de ser investigado. Essa confirmação deve ser removida.

**Se você fizer apenas três coisas...**

1. Verifique se sua confirmação é realmente necessária. Deve haver um motivo legítimo e claro para não continuar e uma chance de que, às vezes, os usuários não.

2. Se o motivo da confirmação não for imediatamente óbvio, escolha os botões de confirmação que incentivam os usuários a pensar em sua resposta. Normalmente, isso é feito ao formular a confirmação como uma pergunta Sim ou não e fornecer respostas completamente autoexplicativas ou sim/não.

3. Considere todos os cenários e forneça as informações necessárias para responder à pergunta de forma inteligente.

## <a name="usage-patterns"></a>Padrões de uso

Confirmações têm vários padrões de uso:



|   Uso                                                                                                                                                                    |    Exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Confirmações rotineiras**<br/> Confirme se o usuário deseja prosseguir com uma ação de rotina e baixo risco. <br/>                                              | Essas confirmações geralmente são frases "tem certeza...?" e, com frequência, uma caixa de seleção não mostrar esta mensagem novamente para minimizar o aborrecimento. <br/> ![captura de tela de ' mover pasta para a Lixeira? ' ](images/mess-confirm-image11.png)<br/> ![captura de tela de ' não mostrar mensagem novamente ' ](images/mess-confirm-image12.png)<br/> Exemplos de confirmações rotineiras.<br/> **Observação:** Esse padrão geralmente é desnecessário e deve ser evitado.<br/>                                                                                                                                                                                                                                                                                        |
| **Confirmações de ações arriscadas**<br/> Confirme se o usuário deseja prosseguir com uma ação que tenha algum risco e não possa ser facilmente desfeito. <br/>            | Como eles têm risco, essas confirmações geralmente têm um ícone de aviso. <br/> ![Captura de tela que mostra um exemplo de confirmação de formatação de volume.](images/mess-confirm-image13.png)<br/> ![Captura de tela que mostra um exemplo de confirmação de exclusão permanente.](images/mess-confirm-image14.png)<br/> Exemplos de confirmações de ações arriscadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Confirmações de conseqüência não intencional**<br/> Confirme se o usuário deseja prosseguir com uma ação que tenha consequências inesperadas ou indesejadas. <br/> | Além de fazer uma pergunta, essas confirmações destacam as consequências indesejadas. como elas têm consequências indesejadas, essas confirmações geralmente têm um ícone de aviso. <br/> ![captura de tela de ' fechar todas as guias? ' Confirme ](images/mess-confirm-image15.png)<br/> ![captura de tela de ' cancelar instalação? ' Confirme ](images/mess-confirm-image16.png)<br/> exemplos de confirmações de conseqüência não intencional.<br/> no entanto, esse padrão requer que as consequências não sejam realmente intencionais. <br/> **incorreto**<br/> ![captura de tela de ' desativar agente de chaves? ' Confirmação ](images/mess-confirm-image17.png)<br/> As consequências são destinadas aqui, portanto, essa é uma confirmação de rotina.<br/> |
| **Esclarecimentos**<br/> esclarecer como o usuário deseja prosseguir com uma ação que tem consequências potencialmente ambíguas ou inesperadas. <br/>             | Operações do tipo "arrastar e soltar" poderão resultar em esclarecimentos se o efeito da operação puder ser interpretado ininterruptamente. <br/> ![captura de tela de 'alterar apenas esta ocorrência?'](images/mess-confirm-image18.png)<br/> ![captura de tela de 'sempre salvar na saída?' Confirmação ](images/mess-confirm-image19.png)<br/> Exemplos de esclarecimentos.<br/> **Observação:** Esse padrão deve ser evitado porque é melhor projetar ações sem consequências ambíguas e assumir o resultado desejado mais provável. <br/>                                                                                                                                                                                                                                     |
| **Confirmações de segurança**<br/> confirme se o usuário deseja prosseguir com uma ação com consequências de segurança. <br/>                                   | ![captura de tela de 'você deseja executar este software?' ](images/mess-confirm-image20.png)<br/> ![captura de tela de 'lembrar senha?' confirmação ](images/mess-confirm-image21.png)<br/> Exemplos de confirmações de segurança.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Confirmações de motivo ulterior**<br/> forneça informações sobre uma ação, mas apresente-a como uma confirmação. <br/>                                       | Embora essas caixas de diálogo sejam apresentadas como confirmações, sua meta real é a educação do usuário ou anúncio de recursos. <br/> ![captura de tela de deseja esta barra de ferramentas na barra de tarefas? ](images/mess-confirm-image22.png)<br/> Um exemplo de confirmação de motivo ulterior.<br/> **Observação:** Esse padrão não é recomendado porque geralmente há uma alternativa melhor e mais direta. Por exemplo, [animações](vis-animations.md) são uma maneira melhor de mostrar a relação entre a causa e o efeito. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Use as confirmações "Salvar alterações" somente quando houver alterações significativas.** Não confirme as alterações que não foram feitas diretamente pelo usuário, como a reformatação automática de documentos.

**Incorreto:**

![Captura de tela que mostra Microsoft Office outlook "você deseja salvar alterações?". .](images/mess-confirm-image23.png)

Este exemplo está incorreto quando usado para um email vazio ou documento que não foi alterado pelo usuário.

### <a name="icons"></a>Ícones

-   As confirmações não usam ícones de barra de título.
-   **O ícone de área de conteúdo para uma confirmação baseia-se em seu padrão de design:**



    | Padrão                                                | ícone                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | Confirmações de rotina <br/>                | Nenhum ícone. <br/>                                                                                                                         |
    | Confirmações de ação arriscada <br/>           | Ícone de aviso. <br/>                                                                                                                    |
    | Confirmações de consequência não intencionais <br/> | Use um ícone de aviso se houver risco, o ícone de recurso, se disponível; caso contrário, nenhum ícone. <br/>                                          |
    | Esclarecimentos <br/>                       | Se a confirmação envolver um documento, use a miniatura do documento; caso contrário, use o ícone de recurso, se disponível, ou nenhum ícone. <br/> |
    | Confirmações de segurança <br/>               | Ícone de aviso. <br/>                                                                                                                    |
    | Confirmações de motivo ulterior <br/>        | Nenhum ícone. <br/>                                                                                                                         |



 

-   **Não use ícones de aviso para perguntas de rotina.** Isso é um contador para o tom [incentivador do Windows e](text-style-tone.md) faz com que o uso do programa se sinta como uma atividade perigosa. Suponha que os usuários compreendam as consequências de cancelar uma tarefa antes de ela ser concluída.

**Incorreto:**

![captura de tela de 'você deseja encerrar o tutorial?' ](images/mess-confirm-image24.png)

Neste exemplo, um ícone de aviso é usado para fazer uma pergunta de rotina.

### <a name="commit-buttons"></a>Botões de commit

-   **Use respostas específicas para a instrução principal se o motivo da confirmação for óbvio ou se puder ser autoexplicativo.**

![captura de tela de 'você deseja salvar as alterações?' ](images/mess-confirm-image25.png)

Neste exemplo, o motivo da confirmação é óbvio, portanto, Salvar e Não salvar trabalho bem.

-   **Caso contrário, use os botões Sim e Não para respostas de confirmação.** Isso faz com que os usuários deem à confirmação alguma ideia antes de responder. Nunca use OK e Cancelar para confirmações.

**Correto:**

![captura de tela de 'deseja desinstalar arquivos de suporte?' ](images/mess-confirm-image26.png)

Neste exemplo, usar botões de confirmação Sim/Não força os usuários a lerem pelo menos a instrução principal.

**Incorreto:**

![captura de tela de 'cancelar sua reserva?' ](images/mess-confirm-image27.png)

Neste exemplo, usar OK/Cancelar é confuso.

-   **Para fechar um programa ou reiniciar o Windows, use respostas específicas para a instrução principal.** Para evitar qualquer confusão, não use Fechar ou Sim/Não para essa finalidade.

**Correto:**

![captura de tela do botão reiniciar janelas agora](images/mess-confirm-image28.png)

**Incorreto:**

![captura de tela do botão sim](images/mess-confirm-image29.png)

No exemplo incorreto, Sim é usado para reiniciar o Windows.

### <a name="command-links"></a>Links de comando

-   **Para o padrão de esclarecimentos, considere usar links de comando para deixar as alternativas claras.**

**Aceitável:**

![captura de tela de 'alterar uma ou todas as ocorrências?' ](images/mess-confirm-image30.png)

**Melhor:**

![captura de tela da mesma pergunta usando links de comando ](images/mess-confirm-image31.png)

No melhor exemplo, os links de comando limpam as alternativas.

-   **Apresente os links de comando mais usados primeiro.** A ordem resultante deve seguir aproximadamente a probabilidade de uso, mas também ter um fluxo lógico.
-   Se um link de comando exigir mais explicações, **forneça uma explicação complementar.** Explicações complementares descrevem por que os usuários podem querer escolher a opção ou o que acontece se a opção for escolhida.

Para obter mais diretrizes e exemplos, consulte [Links de comando.](ctrl-command-links.md)

### <a name="default-values"></a>Valores padrão

-   **A resposta padrão para uma confirmação é baseada em seu padrão de design:**



    | Padrão                                                 | Resposta padrão                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | Confirmações de rotina <br/>                | Prosseguir. <br/>                                                            |
    | Confirmações de ação arriscada <br/>           | Não continue (ou a escolha segura). <br/>                                 |
    | Confirmações de consequência não intencionais <br/> | Se as consequências são significativas, não prossiga; caso contrário, prossiga. <br/> |
    | Esclarecimentos <br/>                       | A resposta mais provável. <br/>                                           |
    | Confirmações de segurança <br/>               | Não continue. <br/>                                                      |
    | Confirmações do ulterior motivação <br/>        | Dar. <br/>                                                            |



 

### <a name="dont-show-this-message-again"></a>Não mostrar esta mensagem novamente

-   **Use esta opção somente para os padrões de confirmação da motivação e da rotina ulterior.** Para os outros padrões, se as informações forem necessárias, elas deverão ser sempre exibidas.
-   **Não forneça essa opção para justificar a exibição de uma confirmação desnecessária.** Em vez disso, elimine a confirmação.

**Incorreto:**

![captura de tela de ' ignorar estes lembretes? ' ](images/mess-confirm-image32.png)

**Ainda incorreto:**

![captura de tela de ' não mostrar mensagem novamente '](images/mess-confirm-image33.png)

Nestes exemplos, a adição de uma opção não mostrar esta mensagem novamente não corrige uma confirmação desnecessária.

Para obter mais diretrizes, consulte [caixas de diálogo](win-dialog-box.md).

### <a name="bulk-operations"></a>Operações em massa

-   Para confirmações que se aplicam a operações em massa, forneça uma opção para aplicar a confirmação a toda a operação.

![captura de tela de ' fazer isso para todos os itens? ' caixa de seleção ](images/mess-confirm-image34.png)

Este exemplo tem uma opção para operações em massa.

-   Eliminar ou adiar confirmações em uma operação em massa.

**Incorreto:**

![captura de tela da caixa de diálogo ' Confirmar exclusão de arquivo ' ](images/mess-confirm-image35.png)

Neste exemplo, o Windows Explorer no Windows XP confirma cada arquivo somente leitura durante uma movimentação de arquivo em massa. Melhor apenas copiar os arquivos somente leitura sem perguntar ou adiar a manipulação desses arquivos e apresentar a confirmação no final da tarefa.

### <a name="progressive-disclosure&quot;></a>Divulgação progressiva

-   **Se você precisar incluir informações avançadas em uma mensagem de confirmação, revele-as usando botões de divulgação progressiva (por exemplo, &quot;mostrar detalhes").** Fazer isso simplifica a confirmação para uso típico. Não oculte as informações necessárias porque os usuários talvez não as encontrem.
-   **Não use "mostrar detalhes", a menos que realmente haja mais detalhes.** Não apenas redeclare as informações existentes em um formato diferente.

Para obter diretrizes de rotulamento, consulte [divulgação progressiva](ctrl-progressive-disclosure-controls.md).

### <a name="user-account-control"></a>Controle de Conta de Usuário

-   **Não use a interface do usuário de elevação do controle de conta de usuários (UAC) como um substituto para uma confirmação.** Se uma ação precisar de uma confirmação, use uma caixa de diálogo separada. Durante a [interface do usuário de elevação](winenv-uac.md), os usuários precisam se concentrar em se eles começaram a tarefa e se o programa é confiável.
-   **Exiba a confirmação antes da interface do usuário de elevação.** Isso elimina elevações desnecessárias.

## <a name="text"></a>Text

### <a name="general"></a>Geral

-   **Remova o texto redundante.** Procure texto redundante em títulos, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de confirmação. Em geral, deixe texto completo em instruções e controles interativos e remova qualquer redundância dos outros locais.
-   **Não use "aviso" ou "cuidado" no texto.** Se os usuários precisarem tomar cuidado, indique isso usando um ícone de aviso.

**Incorreto:**

![captura de tela de confirmação de formatação de volume ](images/mess-confirm-image36.png)

Neste exemplo, o termo "aviso" é desnecessário.

### <a name="titles"></a>Títulos

-   **Use o título para identificar o comando ou o recurso de onde veio a confirmação. Exceção**
    -   Se uma confirmação for exibida por vários comandos diferentes, considere usar o nome do programa em vez disso.
    -   Se esse título fosse redundante ou confuso com a instrução principal, use o nome do programa em vez disso.

No entanto, se a confirmação for de uma tarefa de execução longa e pode ser exibida bem após a tarefa ser iniciada, sempre use o comando ou o recurso para identificar claramente o contexto.

-   **Não use o título para explicar o que fazer na caixa de diálogo** que é a finalidade da instrução principal.
-   Se ele adicionar clareza, inicie o título com a palavra confirmar.
-   **Para confirmações de ações arriscadas, você pode adicionar o nome do objeto envolvido para dar ênfase extra.**

![captura de tela do título da caixa de diálogo ' Formatar unidade f ' ](images/mess-confirm-image13.png)

Neste exemplo, a unidade a ser formatada está incluída no título.

-   Use [maiúsculas e minúsculas no estilo de título](glossary.md), sem pontuação final.

### <a name="main-instructions"></a>Instruções principais

-   **A instrução principal para uma confirmação é baseada em seu padrão de design:**



    | Padrão                                                 | Instrução principal                                                                                                                                                                                                                                                                                                                                                                                                          |
    |--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Confirmações de conseqüência não intencional <br/> | declare a consequência indesejada.<br/> **exceção:** se uma pergunta perguntando se o usuário deseja continuar claramente implica na consequência indesejada, faça a pergunta em vez disso. <br/> ![captura de tela de ' fechar todas as guias? ' Confirme ](images/mess-confirm-image15.png)<br/> Neste exemplo, pedir ao usuário para continuar suficientemente a transmitir as consequências da ação.<br/> |
    | Todos os outros <br/>                           | Faça uma única pergunta para determinar se o usuário deseja continuar. <br/>                                                                                                                                                                                                                                                                                                                              |



 

-   **Seja conciso Use apenas uma única frase completa.** Remova a instrução principal para as informações essenciais. Se você precisar explicar algo mais, use uma instrução complementar.
-   **Seja específico se houver objetos envolvidos, forneça seus nomes completos.**
-   **Use frases positivas.** Frases positivas são mais fáceis para os usuários entenderem.

**Correto:**

Deseja habilitar o compartilhamento de arquivos e impressoras?

**Incorreto:**

Deseja desabilitar o compartilhamento de arquivos e impressoras?

No entanto, a formulação deve corresponder ao comando associado, mesmo que o comando seja desenhado negativamente; Portanto, por exemplo, use Disable para confirmar um comando Disable.

-   Embora não haja regras estritas para frases, **essas frases de confirmação comuns têm a connotação indicada:**



    | Frase                                                            | Conotação                                                            |
    |-------------------------------------------------------------|-------------------------------------------------------------|
    | Tem certeza de que deseja \[ executar uma ação \] ? <br/> | Confirmando o resultado direto de uma solicitação de usuário. <br/> |
    | Deseja \[ executar uma ação \] ? <br/>           | Confirmando um efeito colateral de uma solicitação de usuário. <br/>     |
    | Deseja \[ selecionar um resultado \] ? <br/>          | Precisa de um esclarecimento. <br/>                           |
    | \[Executar uma ação \] ? <br/>                          | Sem connotação. <br/>                                 |



 

-   Para confirmações de ações arriscadas, use o termo permanentemente para indicar que uma ação não pode ser desfeita.

![captura de tela de confirmação de exclusão permanente ](images/mess-confirm-image37.png)

Neste exemplo, "permanentemente" indica que a ação não pode ser desfeita.

-   Use [a capitalização no estilo de frase](glossary.md).

### <a name="supplemental-instructions"></a>Instruções complementares

-   **A instrução complementar para uma confirmação é baseada em seu padrão de design:**

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>Padrão</strong><br/></td>
    <td><strong>Instrução complementar</strong><br/></td>
    </tr>
    <tr class="even">
    <td>Confirmações de conseqüência não intencional <br/></td>
    <td>Faça uma única pergunta para determinar se o usuário deseja continuar. <br/></td>
    </tr>
    <tr class="odd">
    <td>Todos os outros <br/></td>
    <td>Explique os motivos não óbvios pelos quais o usuário talvez não queira continuar. Esses motivos incluem: <br/>
    <ul>
    <li>Possível perda de um ou mais dos seguintes: <ul>
    <li>Um ativo valioso, como perda de dados ou perda financeira.</li>
    <li>Acesso ou integridade do sistema.</li>
    <li>Privacidade ou controle sobre informações confidenciais.</li>
    </ul></li>
    <li>Ações irreversíveis.</li>
    </ul></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Não repita a instrução principal com um texto ligeiramente diferente.** Em vez disso, omita a instrução complementar se não houver mais a adicionar.
-   **Para confirmações de** consequência não intencionais, considere usar o termo de qualquer forma para indicar concisamente que há um motivo para não continuar caso o usuário tenha ignorado a instrução principal. Confira Conceitos de design para obter mais informações.
-   Use frases completas, capitalização de estilo de frase e pontuação final.

## <a name="documentation"></a>Documentação

Ao fazer referência a confirmações:

-   Consulte uma confirmação por seu título se o título for específico para a confirmação (ou seja, não o nome do programa); caso contrário, consulte-o por sua instrução principal.
-   Se necessário, você pode consultar uma caixa de diálogo de confirmação como uma mensagem.
-   Use o texto exato, incluindo sua capitalização.
-   Quando possível, forja o texto usando negrito. Caso contrário, coloque o texto entre aspas somente se necessário para evitar confusão.

Exemplo: na mensagem **Copiar Arquivo,** clique no arquivo mais recente.

