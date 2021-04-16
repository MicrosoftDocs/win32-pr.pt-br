---
title: Confirmações
description: Uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja prosseguir com uma ação.
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b979987daa4cf2c40308a0cda9c23b08b73f4795
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104550336"
---
# <a name="confirmations"></a>Confirmações

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja prosseguir com uma ação.

![Captura de tela que mostra um bloco de notas ' deseja salvar as alterações? ' .](images/mess-confirm-image1.png)

Uma confirmação típica.

Confirmações têm estas características essenciais:

-   Eles são exibidos como o resultado direto de uma ação iniciada pelo usuário.
-   Eles verificam se o usuário deseja prosseguir com a ação.
-   Eles consistem em uma pergunta simples e duas ou mais respostas.

Confirmações são mais úteis quando a ação exige que o usuário faça uma escolha relevante e distinta que não possa ser feita posteriormente. Essa escolha geralmente envolve algum elemento de risco que não é óbvio para o usuário, mas o risco não é essencial para confirmações. Esses elementos são necessários para justificar a interrupção de resposta a uma caixa de diálogo modal.

Por outro lado, [mensagens de aviso](mess-warn.md) apresentam uma condição que pode causar um problema no futuro. Sua característica fundamental é que eles envolvem risco:

-   Eles envolvem perda potencial de um ou mais dos seguintes itens:
    -   Um ativo valioso, como perda de dados ou perda financeira.
    -   Integridade ou acesso do sistema.
    -   Privacidade ou controle sobre informações confidenciais.
    -   Tempo do usuário (um valor significativo, como 30 segundos ou mais).
-   Eles têm consequências inesperadas ou indesejadas.
-   Eles exigem o tratamento correto agora porque os erros não podem ser facilmente corrigidos e podem até mesmo ser irreversível.

Se uma confirmação envolver risco, ela também poderá ser considerada um aviso. Consequentemente, as diretrizes de mensagem de aviso também se aplicam.

**Observação:** As diretrizes relacionadas a [caixas de diálogo](win-dialog-box.md), mensagens de [erro](mess-error.md), [layout](vis-layout.md)e [mensagens de aviso](mess-warn.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

-   **O usuário está sendo solicitado a fazer uma pergunta para continuar com uma ação que tenha duas ou mais respostas?** Caso contrário, a mensagem não será uma confirmação.
-   **A interface do usuário está apresentando um erro ou problema que ocorreu?** Nesse caso, use uma [mensagem de erro](mess-error.md) em vez disso.
-   **Prosseguir com a ação requer que o usuário faça uma escolha que não tenha um padrão adequado?** Nesse caso, uma confirmação pode ser apropriada.
-   **Há um design alternativo que elimina a necessidade da confirmação?** Às vezes, a necessidade de uma confirmação indica uma falha de design. Geralmente, há uma alternativa de design melhor que não precisa de uma confirmação.
-   **O usuário está prestes a executar uma ação arriscada?** Nesse caso, uma confirmação será apropriada se a ação tiver consequências significativas ou não puder ser facilmente desfeita.
-   **O usuário está prestes a abandonar uma tarefa?** Nesse caso, não confirme. Suponha que os usuários compreendam as consequências de não concluir uma tarefa.
-   **A ação tem consequências de que os usuários podem não estar cientes?** Nesse caso, uma confirmação pode ser apropriada.
-   **Considerando o contexto atual, os usuários provavelmente estão executando uma ação em caso de erro?** Nesse caso, uma confirmação pode ser apropriada.
-   **Os usuários executam a ação com frequência?** Nesse caso, considere um design alternativo. Confirmações frequentes são irritantes e têm pouco valor porque os usuários aprendem a responder sem pensar.
-   **A ação tem implicações de segurança?** Nesse caso, uma confirmação pode ser necessária mesmo se os testes anteriores indicarem o contrário.

## <a name="design-concepts"></a>Conceitos de design

### <a name="unnecessary-confirmations-are-annoying"></a>Confirmações desnecessárias são irritantes

A primeira confirmação do Windows que nunca foi criada sem dúvida é parecida com esta:

![captura de tela de ' tem certeza? ' confirmação ](images/mess-confirm-image2.png)

A confirmação irritante original.

Isso foi um início muito inadequado. Se você quiser que os usuários detestem seu programa, apenas disparam confirmações assim por diante. Para entender o porquê, considere o ponto de vista do usuário. O usuário acabou de executar uma ação pela definição de uma confirmação, portanto, a menos que algo tenha sido clicado ou pressionado acidentalmente, é claro que o usuário deseja continuar.

Não apenas as confirmações desnecessárias são irritantes, mas elas não são eficazes na proteção do usuário contra erros. Os usuários detectam rapidamente quando um programa tem confirmações desnecessárias e sua resposta natural é descartá-los o mais rápido possível, geralmente sem ler. Consequentemente, essas confirmações fazem pouco mais do que adicionar uma etapa extra a essas tarefas.

Não use confirmações apenas porque há a possibilidade de que os usuários cometam um erro. **Em vez disso, as confirmações são mais eficientes quando usadas para confirmar ações que têm consequências significativas ou indesejadas.** Boas confirmações nunca declaram o óbvio; Eles devem comunicar algo que os usuários precisam estar cientes de um bom motivo para não continuar. E eles são usados apenas quando são realmente necessários para uma ação, como solicitar que os usuários salvem as alterações somente quando houver alterações que valem a pena ser salvas. Fazer isso exige a atenção do usuário apenas quando ele é realmente garantido.

Para outros tipos de confirmações, muitas vezes há uma alternativa de design melhor do que forçar os usuários a responder uma pergunta.

### <a name="consider-the-design-alternatives"></a>Considere as alternativas de design

Aqui estão algumas alternativas de design que eliminam a necessidade de confirmações rotineiras:

-   **Evitar erros.** Crie tarefas para que erros significativos sejam difíceis de fazer acidentalmente. Por exemplo, separe fisicamente os comandos destrutivos de outros comandos e exija que várias ações sejam concluídas.
-   **Fornecer desfazer.** Forneça a capacidade de reverter ações. Por exemplo, a exclusão de um arquivo no Microsoft Windows geralmente não exige uma confirmação porque os arquivos excluídos podem ser recuperados da lixeira. Observe que, se uma ação for muito fácil de executar, apenas fazer com que os usuários refaça a ação pode ser suficiente.
-   **Forneça comentários.** Torne os resultados indesejáveis óbvios. Fornecer somente desfazer não será suficiente se os usuários não perceberem quando cometerem um erro. Por exemplo, o efeito da manipulação direta (como uma operação de arrastar e soltar) sempre deve ser óbvio.
-   **Suponha o resultado provável, mas facilite a alteração.** Se você não tiver certeza do que os usuários desejam, mas houver uma opção provável, segura e segura, assuma essa opção, deixe claro o que aconteceu e facilite a alteração usando um menu de contexto. Por exemplo, o Microsoft Word pressupõe que os usuários desejam soletrar palavras corretamente. Se ele reconhecer uma palavra incorreta e souber a grafia provável correta, o Word fará a correção automaticamente, mas permitirá que os usuários revertam.
-   **Elimine a escolha completamente.** Se a escolha não for importante, os usuários simplesmente não se importarão. Melhor para [simplificar](/previous-versions//dn742474(v=vs.85)) seu programa e eliminar a escolha.

### <a name="make-confirmations-require-thought"></a>Fazer confirmações exigem pensamento

Para que uma confirmação tenha valor, os usuários precisam entender o motivo para não continuar. Às vezes, o motivo é óbvio, quando os usuários estão fechando um documento com alterações que não foram salvas:

![Captura de tela que mostra uma pintura ' deseja salvar as alterações? ' .](images/mess-confirm-image3.png)

Neste exemplo, o motivo da confirmação é óbvio.

Em outras situações, o motivo pode não ser tão óbvio.

Ao escolher os rótulos do botão confirmar para caixas de diálogo, as [diretrizes gerais](win-dialog-box.md) são escolher rótulos que são respostas específicas para a instrução principal. Isso leva a uma tomada de decisão eficiente, pois os usuários precisam ler uma quantidade mínima de texto para continuar. No entanto, essa meta de eficiência pode ser contratada para confirmações. Considere este exemplo:

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



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Confirmações rotineiras**<br/> Confirme se o usuário deseja prosseguir com uma ação de rotina e baixo risco. <br/>                                              | Essas confirmações geralmente são frases "tem certeza...?" e, com frequência, uma caixa de seleção não mostrar esta mensagem novamente para minimizar o aborrecimento. <br/> ![captura de tela de ' mover pasta para a Lixeira? ' ](images/mess-confirm-image11.png)<br/> ![captura de tela de ' não mostrar mensagem novamente ' ](images/mess-confirm-image12.png)<br/> Exemplos de confirmações rotineiras.<br/> **Observação:** Esse padrão geralmente é desnecessário e deve ser evitado.<br/>                                                                                                                                                                                                                                                                                        |
| **Confirmações de ações arriscadas**<br/> Confirme se o usuário deseja prosseguir com uma ação que tenha algum risco e não possa ser facilmente desfeito. <br/>            | Como eles têm risco, essas confirmações geralmente têm um ícone de aviso. <br/> ![Captura de tela que mostra um exemplo de confirmação de formatação de volume.](images/mess-confirm-image13.png)<br/> ![Captura de tela que mostra um exemplo de confirmação de exclusão permanente.](images/mess-confirm-image14.png)<br/> Exemplos de confirmações de ações arriscadas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Confirmações de conseqüência não intencional**<br/> Confirme se o usuário deseja prosseguir com uma ação que tenha consequências inesperadas ou indesejadas. <br/> | Além de fazer uma pergunta, essas confirmações destacam as consequências indesejadas. como elas têm consequências indesejadas, essas confirmações geralmente têm um ícone de aviso. <br/> ![captura de tela de ' fechar todas as guias? ' Confirme ](images/mess-confirm-image15.png)<br/> ![captura de tela de ' cancelar instalação? ' Confirme ](images/mess-confirm-image16.png)<br/> exemplos de confirmações de conseqüência não intencional.<br/> no entanto, esse padrão requer que as consequências não sejam realmente intencionais. <br/> **incorreto**<br/> ![captura de tela de ' desativar agente de chaves? ' Confirme ](images/mess-confirm-image17.png)<br/> As consequências são destinadas aqui, portanto, essa é uma confirmação de rotina.<br/> |
| **Esclarecimentos**<br/> esclareça como o usuário deseja prosseguir com uma ação que tenha consequências potencialmente ambíguas ou inesperadas. <br/>             | As operações de arrastar e soltar podem resultar em esclarecimentos se o efeito da operação puder ser interpretado incorretamente. <br/> ![captura de tela de ' alterar apenas esta ocorrência? '](images/mess-confirm-image18.png)<br/> ![captura de tela de ' sempre salvar ao sair? ' Confirme ](images/mess-confirm-image19.png)<br/> Exemplos de esclarecimentos.<br/> **Observação:** Esse padrão deve ser evitado porque é melhor criar ações sem consequências ambíguas e assumir o resultado desejado mais provável. <br/>                                                                                                                                                                                                                                     |
| **Confirmações de segurança**<br/> Confirme se o usuário deseja continuar com uma ação com consequências de segurança. <br/>                                   | ![captura de tela de ' deseja executar este software? ' ](images/mess-confirm-image20.png)<br/> ![captura de tela de ' lembrar senha? ' confirmação ](images/mess-confirm-image21.png)<br/> Exemplos de confirmações de segurança.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Confirmações do ulterior motivação**<br/> forneça informações sobre uma ação, mas apresente-as como uma confirmação. <br/>                                       | Embora essas caixas de diálogo sejam apresentadas como confirmações, sua verdadeira meta é a educação do usuário ou o anúncio dos recursos. <br/> ![captura de tela de deseja esta barra de ferramentas na barra de tarefas? ](images/mess-confirm-image22.png)<br/> Um exemplo de uma confirmação da motivação de ulterior.<br/> **Observação:** Esse padrão não é recomendado porque geralmente há uma alternativa melhor e mais direta. Por exemplo, as [animações](vis-animations.md) são uma maneira melhor de mostrar a relação entre causa e efeito. <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Use confirmações "salvar alterações" somente quando houver alterações significativas.** Não confirme as alterações que não foram feitas diretamente pelo usuário, como reformatação automática de documentos.

**Incorreto:**

![Captura de tela que mostra um Microsoft Office Outlook ' deseja salvar as alterações? ' .](images/mess-confirm-image23.png)

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



 

-   **Não use ícones de aviso para perguntas rotineiras.** Fazer isso é um contador para o [Tom incentivado do Windows](text-style-tone.md) e faz com que o seu programa se sinta como uma atividade perigosa. Suponha que os usuários compreendam as consequências de cancelar uma tarefa antes que ela seja concluída.

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

-   **Para fechar um programa ou reiniciar o Windows, use respostas específicas para a instrução principal.** Para evitar qualquer mal-entendido, não use fechar ou sim/não para essa finalidade.

**Correto:**

![captura de tela do botão reiniciar o Windows agora](images/mess-confirm-image28.png)

**Incorreto:**

![captura de tela do botão Sim](images/mess-confirm-image29.png)

No exemplo incorreto, sim é usado para reiniciar o Windows.

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

## <a name="text"></a>Texto

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
    <td>Explique quaisquer motivos não óbvios pelos quais o usuário talvez não queira continuar. Tais motivos incluem: <br/>
    <ul>
    <li>Possível perda de um ou mais dos seguintes itens: <ul>
    <li>Um ativo valioso, como perda de dados ou perda financeira.</li>
    <li>Integridade ou acesso do sistema.</li>
    <li>Privacidade ou controle sobre informações confidenciais.</li>
    </ul></li>
    <li>Ações que são irreversíveis.</li>
    </ul></td>
    </tr>
    </tbody>
    </table>

    

     

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

