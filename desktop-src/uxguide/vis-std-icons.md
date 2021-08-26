---
title: Ícones padrão
description: Os ícones padrão são os ícones de erro, aviso, informações e pontos de interrogação que fazem parte do Windows.
ms.assetid: 63b5c31d-5094-4299-b44b-35b2452ce706
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 74f5b70fb218606eb5f87cbad247c1c75a100f9c5e0f675bb6c075e559fd1a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936295"
---
# <a name="standard-icons"></a>Ícones padrão

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Os ícones padrão são os ícones de erro, aviso, informações e pontos de interrogação que fazem parte do Windows.

![captura de tela de quatro ícones padrão ](images/vis-std-icons-image1.png)

Os ícones padrão de erro, aviso, informações e pontos de interrogação.

Os ícones padrão têm estes significados:

-   **Ícone de erro.** A interface do usuário está apresentando um erro ou problema que ocorreu.
-   **Ícone de aviso.** A interface do usuário está apresentando uma condição que pode causar um problema no futuro.
-   **Ícone de informações.** A interface do usuário está apresentando informações úteis.
-   **Ícone de ponto de interrogação.** A interface do usuário indica um ponto de entrada de ajuda.

os ícones padrão são notáveis porque são criados em muitas Windows APIs (interfaces de programação de aplicativo), como caixas de [diálogo de tarefas](win-dialog-box.md), [caixa de mensagem](glossary.md), [balões](ctrl-balloons.md)e [notificações](mess-notif.md). Eles também são usados normalmente em [mensagens](glossary.md) in-loco e barras de [status](ctrl-status-bars.md).

**Observação:** As diretrizes relacionadas aos [ícones](vis-icons.md) são apresentadas em um artigo separado.

## <a name="design-concepts"></a>Conceitos de design

Há vários fatores na escolha do ícone padrão apropriado, que, em parte, explica por que eles são usados de forma incorreta. Os erros mais comuns são:

-   Usando um ícone de aviso para erros secundários. Os avisos não são erros "suavizados".
-   Usando um ícone padrão quando é melhor não usar nenhum ícone. Nem todas as mensagens precisam de um ícone.
-   Alarme de usuários ao fornecer avisos para pequenos problemas ou apresentar perguntas rotineiras como avisos. Isso faz com que os programas pareçam propensos a riscos e sejam prejudicados em problemas realmente significativos.

O restante desta seção explica como pensar sobre ícones padrão para evitar esses erros comuns.

### <a name="message-type-vs-severity"></a>Tipo de mensagem vs. severidade

Escolha ícones padrão com base no tipo de mensagem, não na severidade do problema subjacente. Os tipos de mensagem são:

-   **Ao.** Erro ou problema ocorrido.
-   **Alerta.** Uma condição que pode causar um problema no futuro.
-   **Divulgação.** Informações úteis.

Consequentemente, uma mensagem de erro pode receber um ícone de erro, mas nunca um ícone de aviso. Não use ícones de aviso como uma maneira de "suavizar" erros secundários. Portanto, apesar da sua diferença na gravidade, "tamanho de fonte incorreto" é um erro, enquanto "continuar com essa operação definirá sua casa em incêndio" é um aviso.

### <a name="determining-the-appropriate-message-type"></a>Determinando o tipo de mensagem apropriado

Alguns problemas podem ser apresentados como erro, aviso ou informações, dependendo da ênfase e da formulação. por exemplo, suponha que uma página da Web não possa carregar um controle de ActiveX não assinado com base na configuração atual do Windows Internet Explorer:

-   **Ao.** "esta página não pode carregar um controle de ActiveX não assinado". (Fraseada como um problema existente.)
-   **Alerta.** "esta página pode não se comportar conforme o esperado porque Windows o Internet Explorer não está configurado para carregar controles de ActiveX não assinados". ou "permitir que esta página instale um controle de ActiveX não assinado? Fazer isso de fontes não confiáveis pode prejudicar seu computador. " (Fraseada como condições que podem causar problemas futuros.)
-   **Divulgação.** "você configurou o Windows Internet Explorer para bloquear controles de ActiveX não assinados". (Fraseada como uma declaração de fato).

**Para determinar o tipo de mensagem apropriado, concentre-se no aspecto mais importante do problema que os usuários precisam conhecer ou agir.** Normalmente, se um problema impedir que o usuário Continue, ele será apresentado como um erro; Se o usuário puder continuar, é um aviso. Crie a [instrução principal](text-ui.md) ou outro texto correspondente com base nesse foco e, em seguida, escolha um ícone (padrão ou de outra forma) que corresponda ao texto. O texto da instrução principal e os ícones sempre devem corresponder.

### <a name="severity"></a>Severity

Embora a gravidade não seja uma consideração ao escolher entre os ícones de erro, de aviso e de informações, **a gravidade é um fator para determinar se um ícone padrão deve ser usado.**

Os ícones funcionam melhor quando usados para se comunicar visualmente. (Observe que, por motivos de acessibilidade, essa comunicação visual sempre deve ser redundante com outro formulário, como texto ou som.) Os usuários devem ser capazes de contar rapidamente a natureza das informações e as consequências de sua resposta, portanto, devemos diferenciar erros críticos e avisos de suas contrapartes comuns. Os erros e avisos críticos têm estas características:

-   Eles envolvem perda potencial de um ou mais dos seguintes itens:
    -   Um ativo valioso, como perda de dados ou perda financeira.
    -   Integridade ou acesso do sistema.
    -   Privacidade ou controle sobre informações confidenciais.
    -   Tempo do usuário (um valor significativo, como 30 segundos ou mais).
-   Eles têm consequências inesperadas ou indesejadas.
-   Eles exigem o tratamento correto agora, porque os erros não podem ser facilmente corrigidos e podem até mesmo ser irreversível.

Para distinguir erros não críticos e avisos de críticos, as mensagens não críticas geralmente são exibidas sem um ícone. fazer isso chama atenção para mensagens críticas, torna as mensagens críticas e não críticas visualmente distintas e é consistente com o [tom de Windows](text-style-tone.md).

Nem todas as mensagens precisam de um ícone. Os ícones não são uma maneira de decorar mensagens.

Veja a seguir um bom exemplo de um aviso crítico, pois ele atende às características definidas anteriormente.

![captura de tela de um aviso para fazer backup dos dados ](images/vis-std-icons-image2.png)

Neste exemplo, um aviso crítico alerta os usuários sobre possíveis perdas de dados irreversíveis.

No entanto, o exemplo a seguir não é crítico porque é provável que seja intencional e seus resultados sejam facilmente desfeitos.

**Incorreto:**

![captura de tela de um uso enganoso de um ícone de aviso ](images/vis-std-icons-image3.png)

Neste exemplo, essa [confirmação](mess-confirm.md) não é crítica porque é provável que seja intencional e facilmente desfeita.

Em uma interface de usuário típica, a maioria dos erros está relacionada a erros de entrada do usuário. A maioria dos erros de entrada do usuário não é essencial porque eles são facilmente corrigidos e os usuários devem corrigi-los antes de continuar. além disso, o desenho de muita atenção aos erros de usuários secundários é diferente do tom de Windows. Consequentemente, os erros de entrada de usuário secundários geralmente são exibidos sem um ícone de erro. Para reforçar sua natureza não crítica, nos referimos a isso como problemas de entrada do usuário.

![captura de tela informando os usuários da entrada correta ](images/vis-std-icons-image4.png)

Neste exemplo, esse problema de entrada de usuário secundário não é crítico, portanto, ele não precisa de um ícone quando apresentado em uma caixa de diálogo.

### <a name="avoid-overwarning"></a>Evitar aviso prévio

nós nos reavisamos sobre programas Windows. o programa típico de Windows tem ícones de aviso aparentemente em qualquer lugar, avisando sobre coisas que têm pouco significado. Em alguns programas, quase todas as perguntas são apresentadas como um aviso. A deadvertência faz com que o uso de um programa seja semelhante a uma atividade perigosa e se reduz de problemas realmente significativos.

O mero potencial para a perda de dados sozinha é insuficiente para chamar um ícone de aviso. Além disso, os resultados indesejáveis devem ser inesperados ou indesejados e não facilmente corrigidos. Caso contrário, praticamente qualquer pergunta respondida incorretamente poderia ser interpretada para resultar na perda de dados de algum tipo e mérito de um ícone de aviso.

Para concentrar os ícones de aviso em problemas realmente críticos:

-   Certifique-se de que o problema garante a maior atenção do usuário. [Confirmações e perguntas rotineiras](mess-confirm.md) não devem ter ícones de aviso.
-   Os usuários provavelmente se comportam de forma diferente como resultado do ícone de aviso? Os usuários provavelmente consideram a decisão com mais cuidado?

**Incorreto:**

![captura de tela do ícone de aviso usado desnecessariamente ](images/vis-std-icons-image5.png)

Neste exemplo, os usuários provavelmente responderão a essa pergunta de forma diferente devido ao ícone de aviso?

-   Há alguma ação significativa a ser tomada ou decisão de tomar? Avisos sem ações apenas fazem com que os usuários se sintam paranóicos.

**Incorreto:**

![captura de tela do ícone de aviso usado com lembrete ](images/vis-std-icons-image6.png)

Por que essa notificação é um aviso? O que os usuários devem fazer (ao contrário de se preocupar)?

### <a name="context"></a>Contexto

O contexto também é uma consideração no uso de ícones padrão porque o próprio contexto comunica informações. Especificamente:

-   Enquanto as caixas de diálogo (incluindo caixas de diálogo de tarefas e de mensagens) e as notificações não precisam de ícones para erros não críticos, os erros in-loco sempre precisam de ícones de erro. Caso contrário, esses comentários não modais seriam muito fáceis de ignorar.
-   Os avisos in-loco sempre precisam de ícones de aviso para distingui-los do texto regular.
-   Caixas de diálogo, notificações e balões não precisam de ícones de informações porque estão claramente apresentando informações. Por outro lado, as faixas precisam de informações de 16x16 pixels ou de outros ícones, pois esses comentários não modais seriam muito fáceis de se esquecer.

Como o contexto é um fator significativo no uso de ícones, as diretrizes de ícone padrão neste artigo são dadas em termos de seu contexto.

### <a name="evaluating-standard-icon-appropriateness"></a>Avaliando a adequação do ícone padrão

Ao avaliar o texto da interface do usuário, Leia todos os ícones padrão também. Leia os ícones de erro como "erro!", ícones de aviso como "aviso, cuidado aqui!" e ícones de informações como "atenção!". Em seguida, continue lendo o contexto restante, como a instrução principal, a área de conteúdo e os botões de confirmação. Verifique se o significado e o tom de cada ícone padrão correspondem ao significado e ao Tom de seu contexto. Se não estiverem, você encontrou um problema.

**Se você fizer apenas uma coisa...**

Verifique se o significado e o tom de cada ícone padrão correspondem ao significado e ao Tom de seu contexto. Se eles não corresponderem, altere ou remova o ícone.

## <a name="guidelines"></a>Diretrizes

**Observação:** Para as diretrizes a seguir, "in-loco" significa em qualquer superfície de janela normal, como na área de conteúdo de um assistente, folha de propriedades ou página de item do painel de controle.

### <a name="general"></a>Geral

-   Escolha ícones padrão com base em seu tipo de mensagem, não a severidade do problema subjacente:
    -   **Ao.** Erro ou problema ocorrido.
    -   **Alerta.** Uma condição que pode causar um problema no futuro.
    -   **Divulgação.** Informações úteis.
-   Se um problema se espalhar por diferentes tipos de mensagem, concentre-se no aspecto mais importante que os usuários precisam agir.
-   Os ícones devem sempre corresponder à instrução principal ou a outro texto correspondente.

**Correto:**

![captura de tela do ícone de erro usado com texto de erro ](images/vis-std-icons-image7.png)

**Incorreto:**

![captura de tela do ícone de aviso usado com texto de erro ](images/vis-std-icons-image8.png)

No exemplo incorreto, o ícone de aviso padrão não corresponde à instrução Main (que gera um erro).

### <a name="icon-size"></a>Tamanho do ícone

-   **Escolha o tamanho do ícone padrão com base no contexto:**
  



    | Contexto                         | Quando usar                                                                                        |
    |--------------------------|-----------------------------------------------------------------------------------------|
    | Caixas de diálogo<br/>  | Use 32x32 pixel para ícones de área de conteúdo; 16 pixels para ícones da área de nota de rodapé.<br/> |
    | No local<br/>      | Use 32x32 pixel para páginas de erro; ícones de 16x16 pixels para todos os outros.<br/>           |
    | Notificações<br/> | Use ícones de 16x16 pixels.<br/>                                                       |
    | Balões<br/>      | Use ícones de 16x16 pixels.<br/>                                                       |
    | Publicitária<br/>       | Use ícones de 16x16 pixels.<br/>                                                       |



 

### <a name="error-icons"></a>Ícones de erro

-   **Use ícones de erro somente quando ocorrer um erro ou um problema:**



    | Contexto                           | Quando usar                                                                                                                                                                                                                                             |
    |----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Caixas de diálogo<br/>    | Use somente para erros críticos. (não use ícones padrão para erros não críticos.) <br/> ![Captura de tela que mostra o ícone de erro usado com a mensagem de erro ](images/vis-std-icons-image9.png)<br/>                                              |
    | Erros in-loco<br/> | Use para todos os erros. <br/> ![captura de tela do ícone de erro usado com uma mensagem de erro.](images/vis-std-icons-image10.png)<br/>                                                                                                           |
    | Notificações<br/>   | Use somente para erros críticos. (para [falhas de ação](https://msdn.microsoft.com/library/windows/desktop/aa511497.aspx).) <br/> ![Captura de tela que mostra um ícone de erro usado com uma mensagem de erro de notificação.](images/vis-std-icons-image11.png)<br/> |
    | Balões<br/>        | Não use. Os balões não devem ser usados para erros críticos e não precisam de ícones de erro para erros não críticos.<br/>                                                                                                               |
    | Publicitária<br/>         | Não use. As faixas não devem ser usadas para erros.<br/>                                                                                                                                                                                  |



 

-   Em geral, os ícones de erro não são necessários para problemas de entrada não críticos do usuário. No entanto, os ícones são necessários para erros in-loco, pois, caso contrário, esses comentários contextuais seriam muito fáceis de se ignorar.
-   **Para caixas de diálogo de tarefas, não use ícones de nota de rodapé de erro.** Os ícones de erro devem ser apresentados somente na área de conteúdo.

### <a name="warning-icons"></a>Ícones de aviso

-   **Use ícones de aviso somente quando uma condição puder causar um problema no futuro:**



    | Contexto                             |  Quando usar                                                                                                                                                                                      |
    |------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Caixas de diálogo<br/>      | Use para todos os avisos. <br/> ![aviso de captura de tela de alteração de extensão de nome de arquivo ](images/vis-std-icons-image12.png)<br/>                                                   |
    | Avisos in-loco<br/> | Use para identificar o texto como um aviso. <br/> ![captura de tela de aviso de espaço livre insuficiente ](images/vis-std-icons-image13.png)<br/>                                    |
    | Notificações<br/>     | Use para todos os avisos. (para [eventos não críticos do sistema](glossary.md).) <br/> ![captura de tela de notificação de aviso de bateria fraca ](images/vis-std-icons-image14.png)<br/> |
    | Balões<br/>          | Use para [condições especiais](ctrl-balloons.md). <br/> ![captura de tela do aviso de balão de bloqueio de caps em ](images/vis-std-icons-image15.png)<br/>                           |
    | Banners<br/>           | Use para chamar a atenção para a faixa. <br/> ![captura de tela da faixa com aviso de tpm ausente ](images/vis-std-icons-image16.png)<br/>                                    |



 

-   **Não use ícones de aviso para "suavizar" erros não críticos.** Os erros não são avisos que aplicam as diretrizes de ícone de erro.
-   **Para caixas de diálogo de pergunta, use ícones de aviso somente para perguntas com consequências significativas.** Não use ícones de aviso para perguntas de rotina.

**Correto:**

![aviso de captura de tela para não interromper a restauração do sistema ](images/vis-std-icons-image17.png)

**Incorreto:**

![captura de tela de aviso sobre como descartar lembretes ](images/vis-std-icons-image18.png)

No exemplo incorreto, um ícone de aviso é usado incorretamente para uma pergunta de rotina.

-   **Para caixas de diálogo de tarefa, você pode usar um ícone de nota de rodapé de aviso para alertar os usuários sobre consequências arriscadas.** No entanto, use um ícone de aviso na área de conteúdo ou na área de nota de rodapé, mas não em ambos.

![aviso de captura de tela de um arquivo potencialmente não seguro ](images/vis-std-icons-image19.png)

Neste exemplo, um blindagem de segurança amarelo é usado em uma nota de rodapé.

### <a name="information-icons"></a>Ícones de informações

-   **Use ícones de informações somente quando o contexto não estiver, obviamente, apresentando informações:**



    | Contexto                         | Quando usar                                                                                                                                                  |
    |--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
    | Caixas de diálogo<br/>  | Não use.<br/>                                                                                                                             |
    | No local<br/>      | Não use. Em vez disso, use um texto estático sem-texto ou uma faixa.<br/>                                                                           |
    | Notificações<br/> | Não use.<br/>                                                                                                                             |
    | Balões<br/>      | Não use.<br/>                                                                                                                             |
    | Banners<br/>       | use para chamar a atenção para a faixa. <br/> ![captura de tela da faixa com informações de configurações ](images/vis-std-icons-image20.png)<br/> |



 

-   Ícones de informações não são necessários em caixas de diálogo, notificações e balão porque seu contexto comunica suficientemente que eles estão fornecendo informações aos usuários.
-   **Para caixas de diálogo de tarefa, não use ícones de nota de rodapé de informações.** As notas de rodapé são suficientemente visíveis e não precisam dizer que são informações.

### <a name="question-mark-icons"></a>Ícones de ponto de interrogação

-   **Use o ícone de ponto de interrogação somente para pontos de entrada da Ajuda.** Para obter mais informações, consulte as [Diretrizes de ponto de entrada da](winenv-help.md) Ajuda.
-   **Não use o ícone de ponto de interrogação para fazer perguntas.** Novamente, use o ícone de ponto de interrogação somente para pontos de entrada da Ajuda. Não é necessário fazer perguntas usando o ícone de ponto de interrogação, de qualquer forma, é suficiente apresentar uma instrução principal como uma pergunta.
-   **Não substitua rotineiramente ícones de ponto de interrogação por ícones de aviso.** Substitua um ícone de ponto de interrogação por um ícone de aviso somente se a pergunta tiver consequências significativas. Caso contrário, não use nenhum ícone.

 

