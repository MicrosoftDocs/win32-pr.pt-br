---
title: Mensagens de aviso
description: Uma mensagem de aviso é uma caixa de diálogo modal, mensagem in-place, notificação ou balão que alerta o usuário de uma condição que pode causar um problema no futuro.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d12962cb8e984ffcb9f7f91875be7c6a724cea95
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982099"
---
# <a name="warning-messages"></a>Mensagens de aviso

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Uma mensagem de aviso é uma caixa de diálogo modal, mensagem in-place, notificação ou balão que alerta o usuário de uma condição que pode causar um problema no futuro.

![captura de tela de uma mensagem de aviso típica](images/mess-warn-image1.png)

Uma mensagem de aviso modal típica.

A característica fundamental dos avisos é que eles envolvem o risco de perder um ou mais dos seguintes:

-   Um ativo valioso, como dados financeiros importantes ou outros.
-   Acesso ou integridade do sistema.
-   Privacidade ou controle sobre informações confidenciais.
-   Tempo do usuário (uma quantidade significativa, como 30 segundos ou mais).

Por outro lado, uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja continuar com uma ação. Alguns tipos de avisos são apresentados como confirmações e, em caso afirmativos, as diretrizes de confirmação também se aplicam.

**Observação:** As diretrizes relacionadas às [caixas de diálogo](win-dialog-box.md), [confirmações](mess-confirm.md) [,](mess-error.md)[ícones](vis-std-icons.md)padrão de mensagens de erro, notificações e [layout](vis-layout.md) são [apresentadas](mess-notif.md)em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir, considere estas perguntas:

-   **O usuário está sendo alertado de uma condição que pode causar um problema no futuro?** Caso não seja, a mensagem não será um aviso.
-   **A interface do usuário está apresentando um erro ou um problema que já ocorreu?** Em caso afirmado, use uma mensagem de erro.
-   **É provável que os usuários executem uma ação ou alterem seu comportamento como resultado da mensagem?** Caso não seja, a condição não justifica a interrupção do usuário, portanto, é melhor suprimir o aviso.
-   **A condição é o resultado direto de uma ação iniciada pelo usuário?** Caso não seja, considere o uso [de notificações de eventos não críticas.](mess-notif.md)
-   **A condição é uma condição especial em um controle?** Em caso afirmado, use um [balão.](ctrl-balloons.md)
-   **Para confirmações, o usuário está prestes a executar uma ação arriscada?** Em caso afirmativa, um aviso será apropriado se a ação tiver consequências significativas ou não puder ser facilmente desfeita.
-   **Para outros tipos de avisos, o usuário precisa agir agora ou no futuro imediato?** Não exibir avisos se os usuários puderem continuar trabalhando de forma produtiva sem problemas imediatos. Adia o aviso até que a condição seja mais imediata e relevante.

## <a name="design-concepts"></a>Conceitos de design

### <a name="avoid-overwarning"></a>Evitar o excesso de avisos

Estamos em excesso nos programas Windows Microsoft. O programa Windows tem avisos aparentemente em todos os lugares, avisos sobre coisas que têm pouca importância. Em alguns programas, quase todas as perguntas são apresentadas como um aviso. O excesso de avisos faz com que o uso de um programa se sinta como uma atividade perigosa e prejudica problemas realmente significativos.

**Incorreto:**

![captura de tela de uma mensagem de aviso desnecessária ](images/mess-warn-image2.png)

O excesso de avisos faz com que o programa se sinta perigoso e pareça que ele foi projetado por profissionais.

O potencial de perda de dados ou um problema futuro sozinho é insuficiente para chamar um aviso. Além disso, todos os resultados indesejáveis devem ser inesperados ou não intencionais e não facilmente corrigidos. Caso contrário, qualquer erro do usuário poderia ser interpretado para resultar em perda de dados ou em um possível problema de algum tipo e ter um aviso.

### <a name="characteristics-of-good-warnings"></a>Características de bons avisos

Bons avisos:

-   **Envolver risco.** Bons avisos alertam os usuários sobre algo significativo.

**Incorreto:**

![captura de tela de 'você deseja sair?' warning ](images/mess-warn-image3.png)

E daí? Essa confirmação pressu que os usuários geralmente saem de programas por acidente.

-   **Ter relevância imediata.** Os usuários não só precisam se preocupar, mas precisam se preocupar agora. Normalmente, os usuários não estão interessados em problemas que possam ter mais tarde, desde que possam fazer seu trabalho agora.

**Incorreto:**

![captura de tela do aviso de bateria com pouca bateria em três horas ](images/mess-warn-image4.png)

Nesse caso, é melhor apenas avisar o usuário em três horas.

-   **Levar à ação.** Há algo que os usuários devem fazer ou estar cientes como resultado do aviso. Talvez eles devem tomar uma ação agora ou em algum momento no futuro imediato. Talvez eles executem uma tarefa de forma diferente como resultado. A consequência de ignorar o aviso deve ser clara. Avisos sem ações apenas fazem os usuários se sentir mal.

**Incorreto:**

![captura de tela do aviso "o live messenger está em execução" ](images/mess-warn-image5.png)

Por que essa notificação é um aviso? O que os usuários devem fazer (além de se preocupar)?

-   **Não são óbvios.** Não exibir um aviso para mostrar a consequência óbvia de uma ação. Por exemplo, suponha que os usuários compreendam as consequências de não concluir uma tarefa.

**Incorreto:**

![captura de tela do assistente de saída? Aviso ](images/mess-warn-image6.png)

Cancelar um assistente incompleto significa que a tarefa não é realizada... quem sabia?

-   **Ocorrem raramente.** Avisos constantes tornam-se rapidamente ineficaz e entediantes. Os usuários geralmente se concentram mais em se desfazer do aviso do que resolver o problema.

**Incorreto:**

![captura de tela do aviso 'atualizar assinaturas de vírus' ](images/mess-warn-image7.png)

É mais provável que os usuários se concentrem em se desfazer do aviso do que corrigir o problema subjacente.

Uma mensagem que não tem essas características ainda pode ser uma boa mensagem, mas não um bom aviso.

### <a name="determine-the-appropriate-message-type"></a>Determinar o tipo de mensagem apropriado

Alguns problemas podem ser apresentados como um erro, aviso ou informações, dependendo da ênfase e frase. Por exemplo, suponha que uma página da Web não possa carregar um controle ActiveX com base na configuração Windows Internet Explorer atual:

-   **Erro.** "Esta página não pode carregar um controle ActiveX não assinado." (Formulado como um problema existente.)
-   **Aviso.** "Esta página pode não se comportar conforme o esperado Windows Internet Explorer não está configurado para carregar controles ActiveX não assinados." ou "Permitir que esta página instale um controle ActiveX não assinado? Fazer isso de fontes não confiáveis pode prejudicar o computador." (Ambos frases como condições que podem causar problemas futuros.)
-   **Informações.** "Você configurou o Windows Internet Explorer para bloquear controles ActiveX não assinados." (Formulado como uma instrução de fato.)

**Para determinar o tipo de mensagem apropriado, concentre-se no aspecto mais importante do problema que os usuários precisam conhecer ou agir.** Normalmente, se um problema bloquear o andamento do usuário, você deverá apresentá-lo como um erro; se o usuário puder continuar, apresente-o como um aviso. Crie a [instrução principal](text-ui.md) ou outro texto correspondente com base nesse foco e escolha um ícone[(padrão](vis-std-icons.md) ou não) que corresponda ao texto. O texto de instrução principal e os ícones devem sempre corresponder.

### <a name="be-specific"></a>Ser específico

Os avisos são mais atraentes quando as seguintes informações são específicas e claras:

-   A origem do aviso.
-   A condição específica e o possível problema.
-   O que o usuário deve fazer sobre isso.
-   O que acontece se o usuário não fizer nada.

**Incorreto:**

![captura de tela de aviso de alerta de risco significativo ](images/mess-warn-image8.png)

Neste exemplo, qual é o problema potencial? O que o usuário deve fazer, além de não usar o projetor pela rede? Sem informações mais específicas, tudo o que o usuário pode fazer é se sentir mal em continuar.

**Correto:**

![captura de tela do aviso de problema e consequências ](images/mess-warn-image9.png)

Neste exemplo, o problema e as consequências são claros.

Às vezes, há um problema potencial legítimo que não permite informar os usuários sobre isso, mas a solução e as consequências não são conhecidas com certeza. Em vez de dar um aviso vaga, seja específico, dando as informações mais prováveis ou o exemplo mais comum.

**Correto:**

![captura de tela do aviso de erro de rede e soluções ](images/mess-warn-image10.png)

Neste exemplo, o aviso é específico fornecendo a solução mais provável.

No entanto, nesses casos, use palavras que indicam que há outras possibilidades. Caso contrário, os usuários poderão ser mal-sinal.

**Incorreto:**

![captura de tela do aviso de cabo de rede desconectado ](images/mess-warn-image11.png)

**Correto:**

![captura de tela do cabo pode ser um aviso desconectado ](images/mess-warn-image12.png)

No exemplo incorreto, os usuários serão confundidos se o cabo estiver claramente conectado.

**Se você fizer apenas duas coisas...**

1. Não se sobreajuste. Limite avisos a condições que envolvem risco e são imediatamente relevantes, ativas, não óbvias e pouco frequentes. Caso contrário, remova ou refrase a mensagem.

2. Forneça informações específicas e úteis.

## <a name="usage-patterns"></a>Padrões de uso

Os avisos têm vários padrões de uso:




| Rótulo | Valor |
|--------|-------|
| <strong>Reconhecimento</strong><br /> Tornar o usuário ciente de uma condição ou possível problema, mas o usuário pode não ter que fazer nada agora. <br /> | <img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br /><img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br /><img src="images/mess-warn-image15.png" alt="Screen shot of 'caps-lock-is-on' warning " /><br /><img src="images/mess-warn-image16.png" alt="Screen shot of 'TPM-not-found' warning " /><br /> Exemplos de avisos de reconhecimento.<br /> Os avisos de reconhecimento têm a seguinte apresentação: <br /><ul><li><strong>Instrução principal:</strong> Descreva a condição ou o possível problema.</li><li><strong>Instrução complementar:</strong> Explique a implicação e por que ela é importante.</li><li><strong>Botões de commit:</strong> Perto.</li></ul> | 
| <strong>Prevenção de erros</strong><br /> Tornar o usuário ciente das informações que podem impedir um problema, especialmente ao fazer escolhas. <br /> | Os avisos de prevenção de erros são apresentados melhor usando um ícone de aviso in-locar e um texto explicativo. <br /><img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br /><img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br /> Exemplos de avisos de prevenção de erros.<br /> | 
| <strong>Problema iminente</strong><br /> O usuário precisa fazer algo agora para evitar um problema iminente. <br /> | <img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br /> Um exemplo de um aviso de problema iminente.<br /> Os avisos de problema iminente têm a seguinte apresentação: <br /><ul><li><strong>Instrução principal:</strong> Descrever o que o usuário precisa fazer agora.</li><li><strong>Instrução complementar:</strong> Explique a condição e por que ela é importante.</li><li><strong>Botões de commit:</strong> Um botão de comando ou um link de comando para cada opção ou OK se a ação ocorrer fora da caixa de diálogo.</li></ul> | 
| <strong>Confirmação de ação arriscada</strong><br /> Confirme se o usuário deseja prosseguir com uma ação que tem algum risco e não pode ser facilmente desfeita. <br /> | <img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br /> Um exemplo de confirmação de ação arriscada.<br /> As confirmações de ação arriscada têm a seguinte apresentação: <br /><ul><li><strong>Instrução principal:</strong> Faça uma pergunta para determinar se o usuário deseja continuar.</li><li><strong>Instrução complementar:</strong> Explique os motivos não óbvios pelos quais o usuário talvez não queira continuar.</li><li><strong>Botões de commit:</strong> Sim, não.</li></ul>Para ver diretrizes sobre esse padrão, consulte <a href="mess-confirm.md">Confirmações</a>. <br /> | 




 

## <a name="guidelines"></a>Diretrizes

### <a name="presentation"></a>Apresentação

-   **Escolha a interface do usuário de apresentação com base no tipo de informação:**



| Interface do usuário  | Melhor usado para |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Caixas de diálogo modais<br/> | Avisos críticos (incluindo confirmações) aos quais os usuários devem responder agora.<br/>                                                 |
| No local<br/>           | Informações que podem impedir um problema, especialmente quando os usuários estão fazendo escolhas.<br/>                                         |
| Banners<br/>            | Informações que podem impedir um problema, especialmente quando relacionadas à conclusão de uma tarefa.<br/>                                     |
| Notificações<br/>      | Eventos significativos ou status que podem ser ignorados com segurança, pelo menos temporariamente.<br/>                                              |
| Balões<br/>           | Um controle está em um estado que afeta a entrada. Esse estado provavelmente não é intencional e o usuário pode não perceber que a entrada é afetada.<br/> |



 

-   **Para caixas de diálogo modais:**
    -   **Use caixas de diálogo de tarefa sempre que apropriado para obter uma aparência e layout consistentes.** As caixas de diálogo de tarefa Windows vista ou posterior, portanto, não são adequadas para versões anteriores do Windows.
    -   **Exibe apenas uma mensagem de aviso por condição.** Por exemplo, exibe um único aviso que explica completamente uma condição em vez de descrevê-la um detalhe por vez por mensagem. Exibir uma sequência de caixas de diálogo de aviso para uma única condição é confuso e entediante.
    -   **Não exibir um aviso mais de uma vez por condição.** Avisos constantes tornam-se rapidamente ineficaz e entediantes. Os usuários geralmente se concentram mais em se desfazer do aviso do que resolver o problema. Se você tiver que avisar repetidamente para uma única condição, use [o escalonamento progressivo](mess-notif.md).
-   **Não acompanhe avisos com um efeito de som ou um aviso.** Fazer isso é jarring e desnecessário.
    -   **Exceção:** Se o usuário precisa responder imediatamente, você pode usar um efeito de som.

### <a name="icons"></a>Ícones

-   Não coloque um ícone de aviso na barra de título de uma caixa de diálogo.
-   **Use um ícone de aviso.** Exceções:
    -   Se o aviso for para um recurso que tenha um ícone, você poderá usar o ícone de recurso com uma sobreposição de aviso.

        **Correto:**

        ![captura de tela do ícone de bloqueio com sobreposição do ícone de aviso ](images/mess-warn-image21.png)

        Neste exemplo, o ícone de recurso tem uma sobreposição de aviso.

-   Para caixas de diálogo modais com uma nota de rodapé de aviso, coloque o ícone de aviso na nota de rodapé em vez da área de conteúdo.

    **Correto:**

    ![captura de tela do ícone de aviso na nota de rodapé da caixa de diálogo ](images/mess-warn-image22.png)

    Neste exemplo, a nota de rodapé tem o ícone de aviso.

Para obter mais diretrizes e exemplos, consulte [Ícones Padrão.](vis-std-icons.md)

### <a name="dont-show-this-message-again"></a>Não mostre essa mensagem novamente

-   **Se uma caixa de diálogo de aviso precisar dessa opção, refrescar o aviso e sua frequência.** Se ele tiver todas as características de um bom aviso (envolve risco e é imediatamente relevante, a ação, não óbvio e pouco frequente), não deve fazer sentido para os usuários suprimi-lo.

Para obter mais diretrizes, consulte Caixas [de diálogo](win-dialog-box.md).

### <a name="progressive-disclosure"></a>Divulgação progressiva

-   **Se você precisa incluir informações avançadas em** uma mensagem de aviso, mostre-as usando botões de divulgação progressiva (por exemplo, "Mostrar detalhes"). Isso simplifica o aviso para uso típico. Não o oculta as informações necessárias porque os usuários podem não encontrá-los.
-   **Não use "Mostrar detalhes", a menos que realmente haja mais detalhes.** Não apenas restate as informações existentes em um formato diferente.

Para diretrizes de rotulagem, consulte [Divulgação progressiva.](ctrl-progressive-disclosure-controls.md)

### <a name="default-values"></a>Valores padrão

-   **Selecione a resposta mais segura, menos destrutiva ou mais segura para ser o padrão.**

## <a name="text"></a>Texto

### <a name="general"></a>Geral

-   **Remova texto redundante.** Procure-o em títulos, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de commit. Em geral, deixe texto completo em instruções e controles interativos e remova qualquer redundância de outros locais.
-   **Não use os termos "aviso" ou "cuidado" no texto.** Quando [usado corretamente,](vis-std-icons.md)o ícone de aviso comunica suficientemente que os usuários devem continuar com cuidado.

**Incorreto:**

![captura de tela do uso desnecessário de aviso no texto ](images/mess-warn-image23.png)

Neste exemplo, o termo "aviso" é desnecessário.

### <a name="titles"></a>Títulos

-   **Use o título para identificar o comando ou o recurso de onde o aviso veio.** Exceções:
    -   Se um aviso for exibido por muitos comandos diferentes, considere usar o nome do programa.
    -   Se esse título for redundante ou confuso com a instrução principal, use o nome do programa.

**Incorreto:**

![captura de tela do título da caixa de diálogo de aviso de segurança ](images/mess-warn-image24.png)

Neste exemplo, "Aviso de Segurança" não identifica o comando ou o recurso de onde o aviso veio.

-   **Não use o título para explicar o que fazer na caixa** de diálogo que é a finalidade da instrução principal.
-   Use [a capitalização de estilo de título](glossary.md), sem terminar a pontuação.

### <a name="main-instructions"></a>Instruções principais

-   A instrução principal de um aviso baseia-se em seu padrão de design:



| Padrão                        | Instrução principal                                               |
|--------------------------------------|----------------------------------------------------------------------|
| Reconhecimento<br/>                 | Descreva a condição ou o possível problema.<br/>              |
| Problema iminente<br/>          | Descrever o que o usuário precisa fazer agora.<br/>                   |
| Confirmação de ação arriscada<br/> | Faça uma pergunta para determinar se o usuário deseja continuar.<br/> |



 

-   ![captura de tela de uma notificação de bateria fraca ](images/mess-warn-image25.png)
-   Neste exemplo, a notificação de bateria fraca é um aviso de reconhecimento, portanto, a instrução principal descreve a condição.
-   ![captura de tela do aviso de bateria de alteração imediatamente ](images/mess-warn-image1.png)
-   Neste exemplo, a caixa de diálogo bateria fraca é um problema iminente, portanto, a instrução principal descreve o que o usuário precisa fazer agora.
-   **Seja conciso, use apenas uma única frase completa.** Desmtrua a instrução principal para as informações essenciais. Se você precisa explicar mais alguma coisa, use uma instrução complementar.
-   **Use palavras como "agora" e "imediatamente" se o usuário deve agir imediatamente.** Não use essas palavras se não houver urgência.
-   **Seja específico se houver objetos envolvidos, dê seus nomes completos.**
-   Use [a capitalização de estilo de frase](glossary.md).

### <a name="supplemental-instructions"></a>Instruções complementares

-   A instrução complementar para um aviso baseia-se em seu padrão de design:



| Padrão            | Instrução complementar                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| Reconhecimento<br/>                 | Explique a implicação e por que ela é importante.<br/>                        |
| Problema iminente<br/>          | Explique a condição e por que ela é importante.<br/>                          |
| Confirmação de ação arriscada<br/> | Explique os motivos não óbvios pelos quais o usuário talvez não queira continuar.<br/> |



 

-   **Não repita a instrução principal com um texto ligeiramente diferente.** Em vez disso, omita a instrução complementar se não houver mais a adicionar.
-   Use frases completas, capitalização de estilo de frase e pontuação final.

### <a name="commit-buttons"></a>Botões de commit

-   Para caixas de diálogo de aviso, os botões de confirmação são baseados em seu padrão de design:



| Padrão               | Botões de commit        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Reconhecimento<br/>                 | Fechar. Não use OK porque sugere que os possíveis problemas estão ok.<br/>                              |
| Problema iminente<br/>          | Um botão de comando ou um link de comando para cada opção ou OK se a ação ocorrer fora da caixa de diálogo.<br/> |
| Confirmação de ação arriscada<br/> | Sim, não.<br/>                                                                                             |



 

-   **Incorreto:**
-   ![captura de tela da caixa de diálogo de aviso com o botão OK ](images/mess-warn-image26.png)
-   Os problemas não estão ok, portanto, use Fechar em vez disso.

## <a name="documentation"></a>Documentação

Ao se referir a avisos:

-   Se o aviso faz uma pergunta, consulte um aviso por sua pergunta; caso contrário, use a instrução principal. Se a pergunta ou a instrução principal for longa ou detalhada, resumi-a.
-   Se necessário, você pode se referir a uma caixa de diálogo de aviso como uma mensagem.
-   Quando possível, forja o texto usando negrito. Caso contrário, coloque o texto entre aspas somente se necessário para evitar confusão.

Exemplo: na **mensagem Você deseja exibir os itens não secretivos?** , clique em Sim.

 

