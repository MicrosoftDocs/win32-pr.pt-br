---
title: Notificações (noções básicas de Design)
description: Uma notificação informa os usuários de eventos que não estão relacionados à atividade do usuário atual, exibindo brevemente um balão de um ícone na área de notificação.
ms.assetid: dcac2fb7-e503-4ea3-a2c5-e3cb660c040a
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5de312b33a970245d2f6f410e55a891c286d9aa7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104562784"
---
# <a name="notifications-design-basics"></a>Notificações (noções básicas de Design)

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Uma notificação informa os usuários de eventos que não estão relacionados à atividade do usuário atual, exibindo brevemente um balão de um ícone na área de notificação. A notificação pode resultar de uma ação do usuário ou de um evento de sistema significativo ou pode oferecer informações potencialmente úteis do Microsoft Windows ou de um aplicativo.

As informações em uma notificação são **úteis e relevantes, mas nunca são críticas.** Consequentemente, as notificações não exigem ação imediata do usuário e os usuários podem ignorá-las livremente.

![captura de tela de balão com ' novas atualizações ' no título ](images/mess-notif-image1.png)

Uma notificação típica.

No Windows Vista e posterior, as notificações são exibidas por uma duração fixa de 9 segundos. As notificações não são exibidas imediatamente quando os usuários estão inativos ou as proteções de tela estão em execução. O Windows enfileira automaticamente as notificações durante esses horários e exibe as notificações na fila quando o usuário retoma a atividade regular. Consequentemente, você não precisa fazer nada para lidar com essas circunstâncias especiais.

**Desenvolvedores:** Você pode determinar quando o usuário está ativo usando a API SHQueryUserNotificationState.

**Observação:** As diretrizes relacionadas à [área de notificação](winenv-notification.md), à barra de [tarefas](winenv-taskbar.md)e aos [balões](ctrl-balloons.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

-   **As informações são o resultado imediato e direto da interação dos usuários com seu aplicativo?** Nesse caso, exiba essas informações síncronas diretamente no seu aplicativo usando uma [caixa de diálogo](win-dialog-box.md), [caixa de mensagem](glossary.md), [balão](ctrl-balloons.md)ou interface do usuário [no local](glossary.md) . As notificações são apenas para informações assíncronas.

![captura de tela do alerta de segurança do Windows ](images/mess-notif-image2.png)

Neste exemplo, a caixa de diálogo exceções do firewall do Windows é exibida como um resultado direto da interação do usuário. Uma notificação não seria apropriada aqui.

-   **As informações são relevantes somente quando os usuários estão usando ativamente seu aplicativo?** Nesse caso, exiba as informações na [barra de status](ctrl-status-bars.md) do seu aplicativo ou em outra área de status.

![captura de tela da barra de status do Outlook ](images/mess-notif-image3.png)

Neste exemplo, o Outlook exibe seu estado de conexão e sincronização em sua barra de status.

-   **As informações são alteradas rapidamente, informações contínuas e em tempo real?** Os exemplos incluem progresso de processamento, cotações de ações e pontuações esportivas. Nesse caso, não use notificações porque elas não são adequadas para informações que mudam rapidamente.
-   **As informações são úteis e relevantes? Os usuários provavelmente podem alterar seu comportamento ou evitar inconveniências como resultado do recebimento das informações?** Caso contrário, não exiba as informações ou coloque-as em uma janela de status ou arquivo de log.
-   **As informações são críticas? A ação imediata é necessária?** Nesse caso, exiba as informações usando uma interface que exige atenção e não pode ser facilmente ignorada, como uma caixa de diálogo modal ou uma caixa de mensagem. Se o programa não estiver ativo, você poderá chamar a atenção para as informações críticas [piscando no botão da barra de tarefas do programa](winenv-taskbar.md) três vezes e deixando-o realçado até que o programa esteja ativo.
-   **Os principais usuários de destino são profissionais de ti?** Nesse caso, use um mecanismo de comentários alternativo, como entradas de [arquivo de log](glossary.md) ou mensagens de email. Os profissionais de ti preferem fortemente os arquivos de log para informações não críticas. Além disso, os servidores são frequentemente gerenciados remotamente e normalmente executados sem nenhum usuário conectado, tornando as notificações ineficazes.

## <a name="design-concepts"></a>Conceitos de design

As notificações efetivas que promovem uma boa experiência do usuário são:

-   **Manipulador.** O evento não é um resultado imediato e direto da interação atual dos usuários com o Microsoft Windows ou seu aplicativo.
-   **Ajudar.** Há uma chance razoável de que os usuários executem uma tarefa ou alterem seu comportamento como resultado da notificação.
-   **Relativas.** A notificação exibe informações úteis sobre as quais os usuários se preocupam e ainda não conhecem.
-   **Não é crítico.** As notificações não são modais e não exigem interação do usuário, para que os usuários possam ignorá-las livremente.
-   **Acionáveis.** Para as notificações que sugerem a execução de uma ação, essa ação é iniciada clicando na notificação. No entanto, a ação sempre pode ser adiada.
-   **Apresentado adequadamente.** A apresentação da notificação (duração, frequência, texto, ícone e interatividade) corresponde às suas circunstâncias.
-   **Não é irritante!** Há uma linha fina entre informar com cuidado os usuários de um evento e pestering-los.

Infelizmente, há muitas notificações inconvenientes, inadequadas, inúteis e irrelevantes por aí. Considere estas notificações do Hall do Windows XP da pena:

![captura de tela da notificação "Tour do Windows XP" ](images/mess-notif-image4.png)

![captura de tela da notificação ' ícones não utilizados ' ](images/mess-notif-image5.png)

![captura de tela da notificação ' Adicionar .NET Passport ' ](images/mess-notif-image6.png)

Nestes exemplos, o Windows XP está ostensivamente tentando ajudar os usuários com suas configurações iniciais. No entanto, essas notificações aparecem com muita frequência e bem depois que são úteis, portanto, são pouco mais do que anúncios de recursos não solicitados.

## <a name="user-flow-must-be-maintained"></a>O fluxo do usuário deve ser mantido

**O ideal é que os usuários imersos em seu trabalho não vejam suas notificações. Em vez disso, eles verão suas notificações somente quando o fluxo já estiver desfeito.**

No Flow: o psicologia da experiência ideal, o Mihaly Csikszentmihalyi diz que os usuários entram em um estado de fluxo quando são totalmente absorvidos na atividade durante os quais perdem sua sensação de tempo e têm sentimentos de grande satisfação.

**As notificações efetivas ajudam os usuários a manter seu fluxo apresentando informações úteis e relevantes que podem ser facilmente ignoradas.** As notificações são apresentadas em um modo periférico e de baixa chave, e não exigem interação.

Não presuma que, se as notificações não forem [sem janela restritas](glossary.md) , elas não poderão ser uma interrupção irritante. As notificações não exigem a atenção dos usuários, mas, certamente, solicitam isso. Você pode interromper o fluxo de usuários por:

-   Exibindo notificações que os usuários não se preocupam.
-   Exibindo uma notificação com muita frequência.
-   Usando várias notificações quando uma única notificação é suficiente.
-   Usando som ao exibir uma notificação.

No Windows 7, os usuários têm o controle definitivo sobre as notificações. **Se os usuários descobrirem que as notificações de um programa são muito irritantes, eles poderão optar por suprimir todas as notificações desse programa.** Certifique-se de que os usuários não façam isso em seu programa apresentando informações úteis e relevantes e seguindo essas diretrizes.

## <a name="notifications-must-be-ignorable"></a>As notificações devem ser ignoráveis

**As notificações não exigem ação imediata do usuário e os usuários podem ignorá-las livremente.**

Os desenvolvedores e designers geralmente desejam apresentar suas notificações de uma maneira que os usuários não podem ignorar. Essa meta totalmente submina o benefício principal das notificações, pois isso interromperia o fluxo dos usuários. Se os usuários forem distraídosdos por suas notificações ou se sentirem obrigadas a lê-los, o design de notificação falhou.

**Se você estiver preocupado com a possibilidade de os usuários ignorarem suas notificações, considere o seguinte:**

-   Se você estiver usando notificações corretamente e elas não exigirem ação imediata do usuário, então os usuários optarem por ignorá-las é por design. Não altere isso.
-   Se o evento exigir ação imediata do usuário, use uma interface do usuário (IU) alternativa que os usuários não podem ignorar. Confira esta interface do usuário correta? para as alternativas.

## <a name="use-progressive-escalation-where-applicable"></a>Usar escalonamento progressivo quando aplicável

Se uma notificação for usada para um evento que os usuários possam ignorar com segurança primeiro, mas que devam ser abordadas eventualmente, uma interface do usuário alternativa deverá ser usada quando a situação se tornar crítica. Essa técnica é conhecida como escalonamento progressivo.

Por exemplo, o sistema de gerenciamento de energia do Windows inicialmente indica uma bateria baixa simplesmente alterando seu ícone de área de notificação.

![captura de tela de seis ícones mostrando o status da bateria ](images/mess-notif-image7.png)

Nestes exemplos, o gerenciamento de energia do Windows usa o ícone da área de notificação para notificar os usuários da energia de bateria de forma progressiva.

À medida que a energia da bateria se torna menor, o Windows avisa os usuários de energia fraca da bateria usando uma notificação.

![captura de tela de notificação de energia de bateria fraca](images/mess-notif-image8.png)

Neste exemplo, o gerenciamento de energia do Windows usa uma notificação para informar aos usuários que a energia da bateria está fraca.

Essa notificação é exibida enquanto os usuários ainda têm várias opções. Os usuários podem conectar-se, alterar suas opções de energia, concluir o trabalho e desligar o computador, ou ignorar a notificação e continuar trabalhando. À medida que a bateria continua a drenar, o texto e o ícone da notificação refletem a urgência adicional. No entanto, quando a energia da bateria fica tão baixa que os usuários devem agir imediatamente, o gerenciamento de energia do Windows notifica os usuários usando uma caixa de mensagem [modal](glossary.md) .

![captura de tela de aviso de energia de bateria seriamente baixa](images/mess-notif-image9.png)

Neste exemplo, o gerenciamento de energia do Windows usa uma caixa de mensagem modal para notificar os usuários sobre a energia de bateria criticamente baixa.

**Se você fizer apenas três coisas...**

1.  Use notificações somente se realmente precisar. Quando você exibe uma notificação, você está potencialmente interrompendo os usuários ou até mesmo irritantes. Certifique-se de que a interrupção seja justificada.
2.  Use notificações para eventos não críticos ou situações que não exigem ação imediata do usuário. Para eventos críticos ou situações que exigem ação imediata do usuário, use uma interface de usuário alternativa (como uma caixa de diálogo modal).
3.  Se você usar notificações, torne-a uma boa experiência do usuário. Não tente forçar os usuários a ver suas notificações. Se os usuários estiverem tão imersoss em seu trabalho de que não veem suas notificações, seu design será bom.

## <a name="usage-patterns"></a>Padrões de uso

As notificações têm vários padrões de uso:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Êxito na ação</strong><br/> Notifica os usuários quando uma ação assíncrona, iniciada pelo usuário, é concluída com êxito. <br/></td>
<td><strong>Correto:</strong><br/> <img src="images/mess-notif-image10.png" alt="Screen shot of balloon showing successful updates " /><br/> Neste exemplo, Windows Update notifica os usuários quando seu computador foi atualizado com êxito.<br/> <strong>Incorreto:</strong><br/> <img src="images/mess-notif-image11.png" alt="Screen shot of balloon showing file check complete " /><br/> Neste exemplo, o Microsoft Outlook notifica os usuários quando uma verificação de arquivo de dados é concluída. O que os usuários devem fazer agora? E por que avisar os usuários sobre a conclusão bem-sucedida?<br/> <strong>Mostrar quando:</strong> Após a conclusão de uma tarefa assíncrona. Notifique os usuários sobre ações bem-sucedidas somente se eles provavelmente estiverem aguardando a conclusão ou após falhas recentes.<br/> <strong>Mostrar como:</strong> Use a opção em tempo real para que essas notificações não sejam enfileiradas quando os usuários estiverem executando um aplicativo de tela inteira ou não estiverem usando o computador ativamente.<br/> <strong>Mostre com que frequência:</strong> Mesmo.<br/> <strong>Fator de incômodo:</strong> Baixo se o sucesso não for esperado devido a falhas recentes, o sucesso é após uma falha crítica ou altamente incomum, portanto, o usuário precisa de comentários adicionais ou o usuário está aguardando a conclusão; alto se não.<br/> <strong>Alternativas:</strong> Faça comentários &quot; sob demanda &quot; exibindo um ícone (ou alterando um ícone existente) na área de notificação enquanto a operação está sendo executada; remova o ícone (ou restaure o ícone anterior) quando a operação for concluída. <br/></td>
</tr>
<tr class="even">
<td><strong>Falha na ação</strong><br/> Notifica os usuários quando uma ação assíncrona, iniciada pelo usuário, falha. <br/></td>
<td><strong>Correto:</strong><br/> <img src="images/mess-notif-image12.png" alt="Screen shot of notification of failure to install " /><br/> Neste exemplo, a ativação do Windows notifica os usuários sobre a falha.<br/> <strong>Incorreto:</strong><br/> <img src="images/mess-notif-image13.png" alt="Screen shot of notification of failure to update " /><br/> Neste exemplo, o Microsoft Outlook costumava notificar os usuários de uma falha de que eles provavelmente não se preocupam.<br/> <strong>Mostrar quando:</strong> Após a falha de uma tarefa assíncrona.<br/> <strong>Mostre com que frequência:</strong> Mesmo.<br/> <strong>Fator de incômodo:</strong> Baixo se for útil e relevante; alto se o problema se resolver imediatamente ou se os usuários não se preocupam.<br/> <strong>Alternativas:</strong> Use uma caixa de diálogo modal se os usuários precisarem resolver a falha imediatamente. <br/></td>
</tr>
<tr class="odd">
<td><strong>Evento não crítico do sistema</strong><br/> Notifica os usuários sobre o status ou eventos significativos do sistema que podem ser ignorados com segurança, pelo menos temporariamente. <br/></td>
<td><img src="images/mess-notif-image8.png" alt="Screen shot of notification of low battery power " /><br/> Neste exemplo, o Windows avisa os usuários com pouca energia da bateria, mas ainda há bastante tempo antes de executarem uma ação.<br/> <strong>Mostrar quando:</strong> Quando um evento ocorre e o usuário está ativo, ou uma condição continua a existir. Se for resultante de um problema, remova imediatamente as notificações exibidas no momento quando o problema for resolvido. Assim como acontece com as notificações de ação, notifique os usuários sobre eventos de sistema bem-sucedidos somente se os usuários provavelmente estiverem aguardando o evento ou após falhas recentes.<br/> <strong>Mostre com que frequência:</strong> Uma vez quando o evento ocorre pela primeira vez. Se isso resultar de um problema que os usuários precisam resolver, reexiba uma vez por dia.<br/> <strong>Fator de incômodo:</strong> Baixo, contanto que a notificação não seja exibida com muita frequência.<br/> <strong>Alternativas:</strong> Se os usuários devem, eventualmente, resolver um problema, use o escalonamento progressivo exibindo, por fim, uma caixa de diálogo modal quando a resolução se tornar obrigatória. <br/></td>
</tr>
<tr class="even">
<td><strong>Tarefa opcional do usuário</strong><br/> Notifica os usuários sobre as tarefas assíncronas que eles devem executar. Seja opcional ou obrigatório, a tarefa pode ser adiada com segurança. <br/></td>
<td><img src="images/mess-notif-image14.png" alt="Screen shot of notification of available updates " /><br/> Neste exemplo, Windows Update está notificando os usuários sobre uma nova atualização de segurança.<br/> <strong>Mostrar quando:</strong> Quando a necessidade de executar uma tarefa é determinada e o usuário está ativo.<br/> <strong>Mostre com que frequência:</strong> Uma vez por dia, no máximo três vezes.<br/> <strong>Fator de incômodo:</strong> Baixo, contanto que os usuários considerem a tarefa importante e a notificação não seja exibida com muita frequência.<br/> <strong>Alternativas:</strong> Se os usuários precisarem executar a tarefa eventualmente, use o escalonamento progressivo exibindo, por fim, uma caixa de diálogo modal quando a tarefa se tornar obrigatória. <br/></td>
</tr>
<tr class="odd">
<td><strong>CONHECIMENTO</strong><br/> Notifica os usuários sobre informações potencialmente úteis e relevantes. Você pode notificar os usuários sobre a relevância marginal se for opcional e os usuários aceitarem. <br/></td>
<td><strong>Correto:</strong><br/> <img src="images/mess-notif-image15.png" alt="Screen shot of notification of new e-mail message " /><br/> Neste exemplo, os usuários são notificados quando uma nova mensagem de email é recebida.<br/> <strong>Correto:</strong><br/> <img src="images/mess-notif-image16.png" alt="Screen shot of notification of contact signed in " /><br/> Neste exemplo, os usuários são notificados quando os contatos ficam online e optam por receber essas informações opcionais.<br/> <strong>Incorreto:</strong><br/> <img src="images/mess-notif-image17.png" alt="Screen shot of notification for faster performance " /><br/> Neste exemplo, as informações serão úteis apenas se o usuário já tiver portas USB de alta velocidade instaladas. Caso contrário, o usuário provavelmente não fará nada diferente como resultado dele.<br/> <strong>Mostrar quando:</strong> Quando o evento de disparo ocorre.<br/> <strong>Mostrar como:</strong> Use a opção em tempo real para que essas notificações não sejam enfileiradas quando os usuários estiverem executando um aplicativo de tela inteira ou não estiverem usando o computador ativamente.<br/> <strong>Mostre com que frequência:</strong> Mesmo.<br/> <strong>Fator de incômodo:</strong> De médio a alto, dependendo da percepção de utilidade e relevância dos usuários. Não é recomendado se houver uma baixa probabilidade de interesse do usuário.<br/> <strong>Alternativas:</strong> Não notifique os usuários. <br/></td>
</tr>
<tr class="even">
<td><strong>Anúncio de recurso</strong><br/> Notifica os usuários sobre recursos do sistema ou do aplicativo recentemente instalados e não utilizados.<br/></td>
<td><strong>Não use notificações para anúncios de recursos!</strong> Em vez disso, use outra maneira de tornar o recurso detectável, como: <br/>
<ul>
<li>Projete o recurso para ser mais fácil de descobrir em contextos onde for necessário.</li>
<li>Não faça nada de especial e permita que os usuários descubram o recurso por conta própria.</li>
</ul>
<strong>Incorreto:</strong><br/> <img src="images/mess-notif-image4.png" alt="Screen shot of notification of new features " /><br/> Não use notificações para anúncios de recursos.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Selecione o padrão de notificação com base em seu uso.** Para obter uma descrição de cada padrão de uso, consulte a tabela anterior.
-   **Não use nenhuma notificação durante a experiência inicial do Windows.** Para melhorar sua primeira experiência, o Windows 7 suprime todas as notificações exibidas durante as primeiras horas de uso. Projete seu programa supondo que os usuários não vejam essas notificações.

### <a name="what-to-notify"></a>O que notificar

-   **Não notifique as operações bem-sucedidas, exceto nas seguintes circunstâncias:**
    -   **Segurança.** Os usuários consideram que as operações de segurança sejam de importância mais alta, portanto, notifique os usuários sobre as operações de segurança bem-sucedidas.
    -   **Falha recente.** Os usuários não precisam de operações bem-sucedidas para serem concedidas se estivessem falhando imediatamente antes, portanto, notifique os usuários de sucesso quando a operação falhar recentemente.
    -   **Evite inconveniência.** Relatar operações bem-sucedidas ao fazer isso pode evitar usuários incomodar. Consequentemente, notifique os usuários quando uma operação bem-sucedida for executada de forma inesperada, por exemplo, quando uma operação for longa ou for concluída antes ou depois do esperado.
-   **Em outras circunstâncias, não forneça nenhum comentário para o sucesso ou forneça comentários "sob demanda".** Suponha que os usuários realizem as operações bem-sucedidas para serem concedidas. Você pode fornecer comentários sob demanda exibindo um ícone (ou alterando um ícone existente) na área de notificação enquanto a operação está sendo executada e removendo o ícone (ou restaurando o ícone anterior) quando a operação for concluída.
-   Para o padrão de FYI, **não dê uma notificação se os usuários puderem continuar a funcionar normalmente ou se for improvável que você faça algo diferente como resultado da notificação.**

    **Incorreto:**

    ![captura de tela de notificação para um desempenho mais rápido ](images/mess-notif-image17.png)

    Neste exemplo, as informações serão úteis apenas se o usuário já tiver as portas instaladas. Caso contrário, o usuário provavelmente não fará nada diferente como resultado dele.

    -   Exceção: **você pode notificar os usuários de informações de relevância questionável se for opcional e os usuários aceitarem.**

        **Correto:**

        ![captura de tela de notificação de contato conectado ](images/mess-notif-image16.png)

        Neste exemplo, os usuários são notificados quando os contatos ficam online e optam por receber essas informações opcionais.

-   Para os padrões de evento de sistema não críticos e FYI, **use notificações completas para um único evento.** Não apresente várias partes parciais.

    **Incorreto:**

    ![captura de tela de notificações de "novo hardware encontrado" ](images/mess-notif-image18.png)

    Esses exemplos mostram apenas quatro das oito notificações que foram exibidas pelo Windows XP quando um usuário anexa um teclado USB específico, cada uma apresentando mais informações incrementalmente.

    **Correto:**

    ![captura de tela de notificações de status de instalação ](images/mess-notif-image19.png)

    Neste exemplo, a anexação de um teclado USB resulta em duas notificações completas.

### <a name="when-to-notify"></a>Quando notificar

-   **Exibir uma notificação com base em seu padrão de design:**



|                                      |                                                                                                                                                                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Padrão**<br/>               | **Quando notificar**<br/>                                                                                                                                                                                      |
| Êxito na ação<br/>            | Após a conclusão de uma tarefa assíncrona. Notifique os usuários sobre ações bem-sucedidas somente se eles provavelmente estiverem aguardando a conclusão ou após falhas recentes.<br/>                                             |
| Falha na ação<br/>            | Após a falha de uma tarefa assíncrona.<br/>                                                                                                                                                                   |
| Evento não crítico do sistema<br/> | Quando um evento ocorre e o usuário está ativo, ou a condição continua a existir. Se isso resultar de um problema, remova a notificação atualmente exibida imediatamente depois que o problema for resolvido.<br/> |
| Tarefa opcional do usuário<br/>        | Quando a necessidade de executar uma tarefa é determinada e o usuário está ativo.<br/>                                                                                                                                   |
| CONHECIMENTO<br/>                       | Quando o evento de disparo ocorre.<br/>                                                                                                                                                                       |



 

-   Para o padrão de falha de ação, **se o problema puder ser corrigido em segundos, adie a notificação de falha por um período de tempo apropriado.** Se o problema for corrigido, não informe nada. Notificar somente após o tempo suficiente ter passado que a falha é perceptível. Se você relatar muito cedo, os usuários provavelmente não perceberão o problema relatado, mas perceberão a notificação desnecessária.

**Incorreto:**

![captura de tela sem notificação de conexão de rede ](images/mess-notif-image20.png)

Quando seguido imediatamente por:

![captura de tela de notificação de conexão bem-sucedida ](images/mess-notif-image21.png)

Neste exemplo, no Windows Vista, a notificação de nenhuma conectividade sem fio é prematuro porque, em geral, é imediatamente seguido por uma notificação de boa conectividade.

-   Para os padrões de ação êxito e FYI, **use a opção em tempo real para que as notificações obsoletas não sejam enfileiradas** quando os usuários estiverem executando um aplicativo de tela inteira ou não estiverem usando o computador ativamente.
-   Para o padrão de evento não crítico do sistema, **não crie o potencial para profusão de notificações por meio da sobredisposição de eventos vinculados a eventos bem conhecidos, como o logon do usuário.** Em vez disso, vincule o evento a um período de tempo após o evento. Por exemplo, você pode lembrar os usuários para registrar seu produto cinco minutos após o logon do usuário.

### <a name="how-long-to-notify"></a>Por quanto tempo notificar

No Windows Vista e posterior, as notificações são exibidas por uma duração fixa de 9 segundos.

### <a name="how-often-to-notify"></a>Com que frequência notificar

-   **O número de vezes para exibir uma notificação é baseado em seu padrão de design:**



|                                      |                                                                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **Padrão**<br/>               | **Com que frequência notificar**<br/>                                                                                          |
| Êxito na ação<br/>            | Uma vez.<br/>                                                                                                            |
| Falha na ação<br/>            | Uma vez.<br/>                                                                                                            |
| Evento não crítico do sistema<br/> | Uma vez quando o evento ocorre pela primeira vez. Se isso resultar de um problema que os usuários precisam resolver, reexiba uma vez por dia.<br/> |
| Tarefa opcional do usuário<br/>        | Uma vez por dia, no máximo três vezes.<br/>                                                                         |
| CONHECIMENTO<br/>                       | Uma vez.<br/>                                                                                                            |



 

-   **Para tarefas de usuário opcionais, não tente Pester os usuários no envio exibindo notificações constantemente.** Se a tarefa for necessária, exiba uma caixa de diálogo modal imediatamente em vez de usar notificações.

### <a name="notification-escalation"></a>Escalonamento de notificação

-   **Não presuma que os usuários verão suas notificações.** Os usuários não os verão quando:
    -   Eles estão imersos em seu trabalho.
    -   Eles não estão pagando atenção.
    -   Eles estão fora do computador.
    -   Eles estão executando um aplicativo de tela inteira.
    -   O administrador desativou todas as notificações para o computador.
-   **Se os usuários precisarem eventualmente executar algum tipo de ação, use o escalonamento progressivo** para exibir uma interface do usuário alternativa que os usuários não podem ignorar.

### <a name="interaction"></a>Interação

-   **Torne as notificações clicáveis quando:**
    -   **Os usuários devem executar uma ação.** Clicar na notificação deve exibir uma janela na qual os usuários possam executar a ação. Essa abordagem é preferida para os padrões de falha de ação e de design de tarefa de usuário opcional.
    -   **Os usuários talvez queiram ver mais informações.** Clicar na notificação deve exibir uma janela na qual os usuários podem exibir informações adicionais.
-   **Sempre exibir uma janela quando os usuários clicarem para executar uma ação.** Não clique em executar uma ação diretamente.
-   **Clicar para mostrar mais informações sempre deve mostrar mais informações.** Não apenas reformule as informações que já estão na notificação.

### <a name="icons"></a>Ícones

-   **Para o padrão de falha de ação, use o ícone de erro padrão.**
-   **Para os padrões de eventos do sistema não críticos, use o ícone de aviso padrão.**
-   **Para outros padrões, use ícones que mostrem objetos relacionados a ou sugerem o assunto**, como um escudo de segurança ou uma bateria para energia.
-   **Use ícones com base no seu aplicativo ou na identidade visual da empresa se os usuários de destino os reconhecerem e se não houver uma alternativa melhor.**
-   Para escalonamento progressivo, **Considere o uso de ícones com uma aparência cada vez mais Emphatic à medida que a situação se tornar mais urgente.**
-   **Não use o ícone de informações padrão.** Essas notificações são informações sem dizer.
-   **Considere o uso de ícones grandes (32x32 pixels) quando:**
    -   Os usuários compreenderão rapidamente o ícone em vez do texto.
    -   Os ícones grandes transmitem seu significado com mais clareza e eficiência do que os ícones padrão de 16x16 pixels.
    -   O ícone usa o [estilo Aero](vis-icons.md).

![captura de tela da notificação "mensagens importantes" ](images/mess-notif-image22.png)

Neste exemplo, os usuários podem compreender rapidamente a natureza da notificação com uma visão geral do ícone grande.

### <a name="notification-queuing"></a>Enfileiramento de notificações

**Observação:** As notificações são enfileiradas sempre que não podem ser exibidas imediatamente, como quando outra notificação está sendo exibida, o usuário está executando um aplicativo de tela inteira ou o usuário não está usando o computador ativamente. As notificações em tempo real permanecem na fila por apenas 60 segundos.

-   **Para os padrões de ação êxito e FYI, use a opção em tempo real** para que a notificação não seja enfileirada por tempo. Essas notificações têm valor somente quando podem ser exibidas imediatamente.
-   **Remova as notificações em fila quando elas não forem mais relevantes.**
-   **Desenvolvedores:** Você pode fazer isso definindo o sinalizador de \_ informações de nse em uFlags e definir szInfo como uma cadeia de caracteres vazia. Não há nenhum dano em fazer isso se a notificação não estiver mais na fila.

### <a name="system-integration"></a>Integração do sistema

-   Se o seu aplicativo nem sempre tiver um ícone na [área de notificação](winenv-notification.md) quando estiver em execução, **exiba um ícone temporariamente durante a tarefa ou evento assíncrono que causou a notificação.**

## <a name="text"></a>Texto

### <a name="title-text"></a>Texto do título

-   **Use o texto do título que resume brevemente as informações mais importantes que você precisa para se comunicar com os usuários em linguagem clara, simples, concisa e específica.** Os usuários devem ser capazes de entender a finalidade das informações de notificação rapidamente e com um mínimo de esforço.
-   **Use fragmentos de texto ou frases completas sem pontuação final.**
-   **Use a capitalização com estilo de frase.**
-   **Use no máximo 48 caracteres (em inglês) para acomodar a localização.** O título tem um comprimento máximo de 63 caracteres, mas você deve permitir a expansão de 30 por cento quando o texto do idioma inglês for traduzido.

### <a name="body-text"></a>Texto do corpo

-   **Use o corpo de texto que fornece uma descrição (sem repetir as informações no título) e, opcionalmente, que fornece detalhes específicos sobre a notificação e também permite que os usuários saibam qual ação está disponível.**
-   **Use frases completas com pontuação final.**
-   **Use a capitalização com estilo de frase.**
-   **Use no máximo 200 caracteres (em inglês) para acomodar a localização.** O texto do corpo tem um comprimento máximo de 255 caracteres, mas você deve permitir a expansão de 30 por cento quando o texto do idioma inglês for traduzido.
-   **Inclua informações essenciais no corpo do texto, como nomes de objetos específicos.** (Exemplos: nomes de usuário, nomes de arquivo ou URLs.) Os usuários não devem abrir outra janela para localizar essas informações.
-   **Coloque aspas duplas ao contrário dos nomes de objetos.**
    -   **Exceção:** Não use aspas quando:
        -   O nome do objeto sempre usa a [capitalização no estilo de título](glossary.md), como com nomes de usuário.
        -   O nome do objeto é offset com dois-pontos (exemplo: nome da impressora: minha impressora).
        -   O nome do objeto pode ser facilmente determinado a partir do contexto.
-   **Se você precisar truncar nomes de objeto para um tamanho máximo fixo para acomodar a localização, use uma elipse para indicar truncamento.**

    ![captura de tela da mensagem contendo o nome abreviado ](images/mess-notif-image23.png)

    Neste exemplo, um nome de objeto é truncado usando uma elipse.

-   **Use a seguinte frase se a notificação for acionável:**
    -   Se os usuários puderem clicar na notificação para executar uma ação:

        < breve descrição das informações essenciais>

        <optional details>

        Clique em para <do something> .

        ![captura de tela da mensagem: ' clique para exibir o progresso ' ](images/mess-notif-image24.png)

        Neste exemplo, os usuários podem clicar para executar uma ação.

    -   Se os usuários puderem clicar na notificação para ver mais informações:

        < breve descrição das informações essenciais>

        <optional details>

        Clique para obter mais informações.

        ![captura de tela da mensagem: clique para obter mais informações ](images/mess-notif-image25.png)

        Neste exemplo, os usuários podem clicar para obter mais informações.

-   **Não diga que o usuário "deve" executar uma ação em uma notificação.** As notificações são para informações não críticas que os usuários podem ignorar livremente. Se os usuários realmente precisarem executar uma ação, não use notificações.
-   **Se os usuários devem executar uma ação, torne a importância clara.**
-   Para os padrões de falha de ação e de evento não crítico **do sistema, descreva problemas em linguagem sem formatação.**

    **Incorreto:**

    ![captura de tela de mensagem longa e complexa ](images/mess-notif-image26.png)

    Neste exemplo, o problema é descrito usando a linguagem excessivamente técnica, mas não específica.

    **Correto:**

    ![captura de tela de mensagem clara e concisa ](images/mess-notif-image27.png)

    Neste exemplo, o problema é descrito em linguagem sem formatação.

-   **Descreva o evento de forma relevante para os usuários de destino.** Uma notificação é relevante se houver uma chance razoável de os usuários executarem uma tarefa ou alterarem seu comportamento como resultado da notificação. Muitas vezes, você pode fazer isso descrevendo as notificações em termos de metas do usuário em vez de problemas tecnológicos.

## <a name="documentation"></a>Documentação

Ao fazer referência a notificações:

-   Use o texto do título exato, incluindo sua capitalização.
-   Consulte o componente como uma notificação, não como um balão ou um alerta.
-   Para descrever a interação do usuário, use clique.
-   Quando possível, formate o texto do título usando texto em negrito. Caso contrário, coloque o título entre aspas somente se necessário para evitar confusão.

Exemplo: quando a notificação **atualizações críticas estão prontas para serem instaladas** é exibida, clique na notificação para iniciar o processo.

Ao fazer referência à área de notificação:

-   Consulte a área de notificação como a área de notificação, não a bandeja do sistema.

 

