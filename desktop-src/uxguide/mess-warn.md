---
title: Mensagens de aviso
description: Uma mensagem de aviso é uma caixa de diálogo modal, uma mensagem in-loco, uma notificação ou um balão que alerta o usuário sobre uma condição que pode causar um problema no futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 944c99b546df5fd313ee5bd656db58fafe991d01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470283"
---
# <a name="warning-messages"></a>Mensagens de aviso

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Uma mensagem de aviso é uma caixa de diálogo modal, uma mensagem in-loco, uma notificação ou um balão que alerta o usuário sobre uma condição que pode causar um problema no futuro.

![captura de tela de uma mensagem de aviso típica](images/mess-warn-image1.png)

Uma mensagem de aviso modal típica.

A característica fundamental dos avisos é que eles envolvem o risco de perder um ou mais dos seguintes itens:

-   Um ativo valioso, como importante finanças ou outros dados.
-   Integridade ou acesso do sistema.
-   Privacidade ou controle sobre informações confidenciais.
-   Tempo do usuário (um valor significativo, como 30 segundos ou mais).

Por outro lado, uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja prosseguir com uma ação. Alguns tipos de avisos são apresentados como confirmações e, nesse caso, as diretrizes de confirmação também se aplicam.

**Observação:** As diretrizes relacionadas [a caixas de diálogo](win-dialog-box.md), [confirmações](mess-confirm.md),[ícones padrão](vis-std-icons.md)de [mensagens de erro](mess-error.md), [notificações](mess-notif.md)e [layout](vis-layout.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

-   **O usuário está sendo alertado sobre uma condição que pode causar um problema no futuro?** Caso contrário, a mensagem não é um aviso.
-   **A interface do usuário está apresentando um erro ou problema que já ocorreu?** Nesse caso, use uma mensagem de erro em vez disso.
-   **Os usuários provavelmente executarão uma ação ou alterarão seu comportamento como resultado da mensagem?** Caso contrário, a condição não justifica a interrupção do usuário para que seja melhor suprimir o aviso.
-   **A condição é o resultado direto de uma ação iniciada pelo usuário?** Caso contrário, considere o uso de [notificações de eventos não críticas](mess-notif.md).
-   **A condição é uma condição especial em um controle?** Nesse caso, use um [balão](ctrl-balloons.md) .
-   **Para confirmações, o usuário está prestes a executar uma ação arriscada?** Nesse caso, um aviso será apropriado se a ação tiver consequências significativas ou não puder ser facilmente desfeita.
-   **Para outros tipos de avisos, o usuário precisa agir agora ou no futuro imediato?** Não exiba avisos se os usuários puderem continuar a trabalhar de maneira produtiva sem problemas imediatos. Adie o aviso até que a condição seja mais imediata e relevante.

## <a name="design-concepts"></a>Conceitos de design

### <a name="avoid-overwarning"></a>Evitar aviso prévio

nós nos reavisamos aos programas do Microsoft Windows. o programa de Windows típico tem avisos aparentemente em qualquer lugar, avisando sobre coisas que têm pouco significado. Em alguns programas, quase todas as perguntas são apresentadas como um aviso. A deadvertência faz com que o uso de um programa seja semelhante a uma atividade perigosa e se reduz de problemas realmente significativos.

**Incorreto:**

![captura de tela de uma mensagem de aviso desnecessária ](images/mess-warn-image2.png)

O alerta faz com que seu programa sinta-se perigoso e pareça que foi projetado por advogados.

A mera possibilidade de perda de dados ou um problema futuro sozinho é insuficiente para chamar um aviso. Além disso, os resultados indesejáveis devem ser inesperados ou indesejados e não facilmente corrigidos. Caso contrário, praticamente qualquer erro de usuário poderia ser interpretado para resultar em perda de dados ou em um possível problema de algum tipo e merecer um aviso.

### <a name="characteristics-of-good-warnings"></a>Características de bons avisos

Bons avisos:

-   **Envolva riscos.** Bons avisos alertam os usuários de algo significativo.

**Incorreto:**

![captura de tela de ' deseja sair? ' warning ](images/mess-warn-image3.png)

E daí? Essa confirmação pressupõe que os usuários geralmente saem de programas por acidente.

-   **Tenha relevância imediata.** Não apenas os usuários precisam se preocupar, eles precisam se preocupar agora. Os usuários normalmente não estão interessados em problemas que possam ter mais tarde, contanto que possam fazer seu trabalho agora.

**Incorreto:**

![captura de tela de aviso de bateria-pouco em três horas ](images/mess-warn-image4.png)

Nesse caso, é melhor apenas avisar o usuário em três horas.

-   **Levar à ação.** Há algo que os usuários devem fazer ou estar cientes como resultado do aviso. Talvez eles devam executar uma ação agora ou em algum momento no futuro imediato. Talvez eles executem uma tarefa de forma diferente como resultado. A consequência de ignorar o aviso deve ser clara. Avisos sem ações apenas fazem com que os usuários se sintam paranóicos.

**Incorreto:**

![aviso de captura de tela do ' Live Messenger em execução ' ](images/mess-warn-image5.png)

Por que essa notificação é um aviso? O que os usuários devem fazer (ao contrário de se preocupar)?

-   **Não são óbvias.** Não exiba um aviso para declarar a consequência óbvia de uma ação. Por exemplo, suponha que os usuários compreendam as consequências de não concluir uma tarefa.

**Incorreto:**

![captura de tela de você deseja sair do assistente? alerta ](images/mess-warn-image6.png)

Cancelar um assistente incompleto significa que a tarefa não é concluída... Quem sabia?

-   **Ocorrem com pouca frequência.** Os avisos constantes se tornam ineficientes e irritantes rapidamente. Os usuários geralmente se concentram em se livrar do aviso do que resolver o problema.

**Incorreto:**

![captura de tela do aviso "atualizar assinaturas de vírus" ](images/mess-warn-image7.png)

Os usuários têm mais probabilidade de se concentrar em se livrar do aviso do que corrigir o problema subjacente.

Uma mensagem que não tem essas características ainda pode ser uma boa mensagem, mas não é um bom aviso.

### <a name="determine-the-appropriate-message-type"></a>Determinar o tipo de mensagem apropriado

Alguns problemas podem ser apresentados como erro, aviso ou informações, dependendo da ênfase e da formulação. por exemplo, suponha que uma página da Web não possa carregar um controle de ActiveX não assinado com base na configuração atual do Windows Internet Explorer:

-   **Ao.** "esta página não pode carregar um controle de ActiveX não assinado". (Fraseada como um problema existente.)
-   **Alerta.** "esta página pode não se comportar conforme o esperado porque Windows o Internet Explorer não está configurado para carregar controles de ActiveX não assinados". ou "permitir que esta página instale um controle de ActiveX não assinado? Fazer isso de fontes não confiáveis pode prejudicar seu computador. " (Fraseada como condições que podem causar problemas futuros.)
-   **Divulgação.** "você configurou o Windows Internet Explorer para bloquear controles de ActiveX não assinados". (Fraseada como uma declaração de fato).

**Para determinar o tipo de mensagem apropriado, concentre-se no aspecto mais importante do problema que os usuários precisam conhecer ou agir.** Normalmente, se um problema impedir que o usuário Continue, você deverá apresentá-lo como um erro; Se o usuário puder continuar, apresente-o como um aviso. Crie a [instrução principal](text-ui.md) ou outro texto correspondente com base nesse foco e, em seguida, escolha um ícone ([padrão](vis-std-icons.md) ou de outra forma) que corresponda ao texto. O texto da instrução principal e os ícones sempre devem corresponder.

### <a name="be-specific"></a>Ser específico

Os avisos são mais atraentes quando as seguintes informações são específicas e claras:

-   A origem do aviso.
-   A condição específica e o problema em potencial.
-   O que o usuário deve fazer sobre ele.
-   O que acontecerá se o usuário não fizer nada.

**Incorreto:**

![captura de tela de aviso vaga de risco significativo ](images/mess-warn-image8.png)

Neste exemplo, qual é o problema em potencial? O que o usuário deve fazer, além de não usar o projetor pela rede? Sem informações mais específicas, tudo o que o usuário pode fazer é uma boa idéia de continuar.

**Correto:**

![captura de tela de aviso de problema e consequências ](images/mess-warn-image9.png)

Neste exemplo, o problema e as consequências estão claros.

Às vezes, há um problema potencial legítimo que vale a pena informar os usuários sobre, mas a solução e as consequências não são conhecidas com certeza. Em vez de dar um aviso vaga, seja específico, fornecendo as informações mais prováveis ou o exemplo mais comum.

**Correto:**

![captura de tela de avisos e soluções de erro de rede ](images/mess-warn-image10.png)

Neste exemplo, o aviso é feito específico fornecendo a solução mais provável.

No entanto, nesses casos, use palavras que indiquem que há outras possibilidades. Caso contrário, os usuários podem ser enganam.

**Incorreto:**

![captura de tela do aviso de cabo de rede não conectado ](images/mess-warn-image11.png)

**Correto:**

![aviso de captura de tela de cabo pode ser desconectado ](images/mess-warn-image12.png)

No exemplo incorreto, os usuários ficarão confusos se o cabo estiver claramente conectado.

**Se você fizer apenas duas coisas...**

1. Não avisar. Limite os avisos a condições que envolvem risco e são imediatamente relevantes, acionáveis, não óbvios e pouco frequentes. Caso contrário, remova ou reformule a mensagem.

2. Forneça informações específicas e úteis.

## <a name="usage-patterns"></a>Padrões de uso

Os avisos têm vários padrões de uso:




| | | <strong>Reconhecimento</strong><br /> Torne o usuário ciente de uma condição ou um possível problema, mas talvez o usuário não precise fazer nada agora. <br /> | <img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br /><img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br /><img src="images/mess-warn-image15.png" alt="Screen shot of 'caps-lock-is-on' warning " /><br /><img src="images/mess-warn-image16.png" alt="Screen shot of 'TPM-not-found' warning " /><br /> Exemplos de avisos de reconhecimento.<br /> Os avisos de conscientização têm a seguinte apresentação: <br /><ul><li><strong>Instrução principal:</strong> Descreva a condição ou o problema potencial.</li><li><strong>Instrução complementar:</strong> Explique a implicação e por que ela é importante.</li><li><strong>Botões de confirmação:</strong> Inclui.</li></ul> | | <strong>Prevenção de erros</strong><br /> Torne o usuário ciente de informações que podem impedir um problema, especialmente ao fazer escolhas. <br /> | Os avisos de prevenção de erros são apresentados melhor usando um ícone de aviso in-loco e um texto explicativo. <br /><img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br /><img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br /> Exemplos de avisos de prevenção de erros.<br /> | | <strong>Problema iminente</strong><br /> O usuário precisa fazer algo agora para evitar um problema iminente. <br /> | <img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br /> Um exemplo de um aviso de problema iminente.<br /> Os avisos de problema iminentes têm a seguinte apresentação: <br /><ul><li><strong>Instrução principal:</strong> Descreva o que o usuário precisa fazer agora.</li><li><strong>Instrução complementar:</strong> Explique a condição e por que ela é importante.</li><li><strong>Botões de confirmação:</strong> Um botão de comando ou link de comando para cada opção ou OK se a ação ocorrer fora da caixa de diálogo.</li></ul> | | <strong>Confirmação de ação arriscada</strong><br /> Confirme se o usuário deseja prosseguir com uma ação que tenha algum risco e não possa ser facilmente desfeito. <br /> | <img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br /> Um exemplo de confirmação de ação arriscada.<br /> Confirmações de ações arriscadas têm a seguinte apresentação: <br /><ul><li><strong>Instrução principal:</strong> Faça uma pergunta para determinar se o usuário deseja continuar.</li><li><strong>Instrução complementar:</strong> Explique quaisquer motivos não óbvios pelos quais o usuário talvez não queira continuar.</li><li><strong>Botões de confirmação:</strong> Sim, não.</li></ul>Para obter diretrizes sobre esse padrão, consulte <a href="mess-confirm.md">confirmações</a>. <br /> | 




 

## <a name="guidelines"></a>Diretrizes

### <a name="presentation"></a>Apresentação

-   **Escolha a interface do usuário de apresentação com base no tipo de informação:**



| Interface do usuário  | Mais usado para |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Caixas de diálogo modais<br/> | Avisos críticos (incluindo confirmações) que os usuários devem responder agora.<br/>                                                 |
| No local<br/>           | Informações que podem impedir um problema, especialmente quando os usuários estão fazendo escolhas.<br/>                                         |
| Publicitária<br/>            | Informações que podem impedir um problema, especialmente quando relacionadas à conclusão de uma tarefa.<br/>                                     |
| Notificações<br/>      | Eventos significativos ou status que podem ser ignorados com segurança, pelo menos temporariamente.<br/>                                              |
| Balões<br/>           | Um controle está em um estado que afeta a entrada. Esse Estado provavelmente não é intencional e o usuário pode não perceber que a entrada é afetada.<br/> |



 

-   **Para caixas de diálogo modais:**
    -   **Use caixas de diálogo de tarefas sempre que apropriado para obter uma aparência e um layout consistentes.** as caixas de diálogo de tarefas exigem o Windows Vista ou posterior, portanto, elas não são adequadas para versões anteriores do Windows.
    -   **Exibe apenas uma mensagem de aviso por condição.** Por exemplo, exiba um único aviso que explique completamente uma condição em vez de descrever um detalhe por vez por mensagem. Exibir uma sequência de caixas de diálogo de aviso para uma única condição é confuso e irritante.
    -   **Não exibir um aviso mais de uma vez por condição.** Os avisos constantes se tornam ineficientes e irritantes rapidamente. Os usuários geralmente se concentram em se livrar do aviso do que resolver o problema. Se você precisar avisar repetidamente para uma única condição, use [escalonamento progressivo](mess-notif.md).
-   **Não acompanha avisos com um efeito sonoro ou um aviso sonoro.** Fazer isso é dissonante e desnecessário.
    -   **Exceção:** Se o usuário precisar responder imediatamente, você poderá usar um efeito de som.

### <a name="icons"></a>Ícones

-   Não coloque um ícone de aviso na barra de título de uma caixa de diálogo.
-   **Use um ícone de aviso.** Exceções:
    -   Se o aviso for para um recurso que tenha um ícone, você poderá usar o ícone de recurso com uma sobreposição de aviso.

        **Correto:**

        ![captura de tela de ícone de cadeado com sobreposição de ícone de aviso ](images/mess-warn-image21.png)

        Neste exemplo, o ícone de recurso tem uma sobreposição de aviso.

-   Para caixas de diálogo modais com uma nota de rodapé de aviso, coloque o ícone de aviso na nota de rodapé em vez da área de conteúdo.

    **Correto:**

    ![captura de tela do ícone de aviso na nota de rodapé da caixa de diálogo ](images/mess-warn-image22.png)

    Neste exemplo, a nota de rodapé tem o ícone de aviso.

Para obter mais diretrizes e exemplos, consulte [ícones padrão](vis-std-icons.md).

### <a name="dont-show-this-message-again"></a>Não mostrar esta mensagem novamente

-   **Se uma caixa de diálogo de aviso precisar dessa opção, reconsidere o aviso e sua frequência.** Se ele tem todas as características de um bom aviso (envolve risco e é imediatamente relevante, acionável, não óbvio e incomum), não deve fazer sentido para os usuários suprimirem.

Para obter mais diretrizes, consulte [caixas de diálogo](win-dialog-box.md).

### <a name="progressive-disclosure"></a>Divulgação progressiva

-   **Se você precisar incluir informações avançadas em uma mensagem de aviso, revele-as usando botões de divulgação progressiva** (por exemplo, "mostrar detalhes"). Fazer isso simplifica o aviso para uso típico. Não oculte as informações necessárias porque os usuários talvez não as encontrem.
-   **Não use "mostrar detalhes", a menos que realmente haja mais detalhes.** Não apenas redeclare as informações existentes em um formato diferente.

Para obter diretrizes de rotulamento, consulte [divulgação progressiva](ctrl-progressive-disclosure-controls.md).

### <a name="default-values"></a>Valores padrão

-   **Selecione a resposta mais segura, menos destrutiva ou mais segura para ser o padrão.**

## <a name="text"></a>Texto

### <a name="general"></a>Geral

-   **Remova o texto redundante.** Procure por ele em títulos, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de confirmação. Em geral, deixe texto completo em instruções e controles interativos e remova qualquer redundância dos outros locais.
-   **Não use os termos "aviso" ou "cuidado" no texto.** Quando [usado corretamente](vis-std-icons.md), o ícone de aviso comunica suficientemente que os usuários devem continuar com cautela.

**Incorreto:**

![captura de tela de uso desnecessário de aviso no texto ](images/mess-warn-image23.png)

Neste exemplo, o termo "aviso" é desnecessário.

### <a name="titles"></a>Títulos

-   **Use o título para identificar o comando ou recurso do qual o aviso veio.** Exceções:
    -   Se um aviso for exibido por vários comandos diferentes, considere usar o nome do programa em vez disso.
    -   Se esse título fosse redundante ou confuso com a instrução principal, use o nome do programa em vez disso.

**Incorreto:**

![captura de tela do título da caixa de diálogo de aviso de segurança ](images/mess-warn-image24.png)

Neste exemplo, "aviso de segurança" não identifica o comando ou o recurso do qual veio o aviso.

-   **Não use o título para explicar o que fazer na caixa de diálogo** que é a finalidade da instrução principal.
-   Use [maiúsculas e minúsculas no estilo de título](glossary.md), sem pontuação final.

### <a name="main-instructions"></a>Instruções principais

-   A instrução principal para um aviso se baseia em seu padrão de design:



| Padrão                        | Instrução principal                                               |
|--------------------------------------|----------------------------------------------------------------------|
| Reconhecimento<br/>                 | Descreva a condição ou o problema potencial.<br/>              |
| Problema iminente<br/>          | Descreva o que o usuário precisa fazer agora.<br/>                   |
| Confirmação de ação arriscada<br/> | Faça uma pergunta para determinar se o usuário deseja continuar.<br/> |



 

-   ![captura de tela de uma notificação de bateria fraca ](images/mess-warn-image25.png)
-   Neste exemplo, a notificação de bateria fraca é um aviso de conscientização, portanto, a instrução principal descreve a condição.
-   ![captura de tela de alterar a bateria imediatamente aviso ](images/mess-warn-image1.png)
-   Neste exemplo, a caixa de diálogo de bateria fraca é um problema iminente, portanto, a instrução principal descreve o que o usuário precisa fazer agora.
-   **Seja conciso Use apenas uma única frase completa.** Remova a instrução principal para as informações essenciais. Se você precisar explicar algo mais, use uma instrução complementar.
-   **Use palavras como "Now" e "imediatamente" se o usuário precisar agir imediatamente.** Não use essas palavras se não houver urgência.
-   **Seja específico se houver objetos envolvidos, forneça seus nomes completos.**
-   Use [a capitalização no estilo de frase](glossary.md).

### <a name="supplemental-instructions"></a>Instruções complementares

-   A instrução complementar para um aviso se baseia em seu padrão de design:



| Padrão            | Instrução complementar                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| Reconhecimento<br/>                 | Explique a implicação e por que ela é importante.<br/>                        |
| Problema iminente<br/>          | Explique a condição e por que ela é importante.<br/>                          |
| Confirmação de ação arriscada<br/> | Explique quaisquer motivos não óbvios pelos quais o usuário talvez não queira continuar.<br/> |



 

-   **Não repita a instrução principal com uma palavra ligeiramente diferente.** Em vez disso, omita a instrução complementar se não houver mais a adicionar.
-   Use frases completas, maiúsculas e minúsculas no estilo da frase e pontuação final.

### <a name="commit-buttons"></a>Botões de confirmação

-   Para caixas de diálogo de aviso, os botões de confirmação se baseiam em seu padrão de design:



| Padrão               | Botões de confirmação        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Reconhecimento<br/>                 | Fechar. Não use OK porque ele sugere que problemas potenciais estão OK.<br/>                              |
| Problema iminente<br/>          | Um botão de comando ou link de comando para cada opção ou OK se a ação ocorrer fora da caixa de diálogo.<br/> |
| Confirmação de ação arriscada<br/> | Sim, não.<br/>                                                                                             |



 

-   **Incorreto:**
-   ![captura de tela da caixa de diálogo de aviso com o botão OK ](images/mess-warn-image26.png)
-   Os problemas não estão OK, portanto, use fechar.

## <a name="documentation"></a>Documentação

Ao fazer referência a avisos:

-   Se o aviso faz uma pergunta, consulte um aviso por sua pergunta; caso contrário, use a instrução principal. Se a pergunta ou a instrução principal for longa ou detalhada, resuma-a.
-   Se necessário, você pode se referir a uma caixa de diálogo de aviso como uma mensagem.
-   Quando possível, formate o texto usando negrito. Caso contrário, coloque o texto entre aspas somente se necessário para evitar confusão.

Exemplo: na mensagem **deseja exibir os itens não seguros?** , clique em Sim.

 

