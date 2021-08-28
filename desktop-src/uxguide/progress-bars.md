---
title: Barras de progresso
description: Com uma barra de progresso, os usuários podem acompanhar o progresso de uma operação demorada. Uma barra de progresso pode mostrar um percentual aproximado de conclusão (determinado) ou indicar que uma operação está em andamento (indeterminada).
ms.assetid: 067961fa-2fb1-4cd1-99a4-cbe2244c3913
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a87ddece61276e5ac651f0610f34409477e18f53
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983939"
---
# <a name="progress-bars"></a>Barras de progresso

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com uma barra de progresso, os usuários podem acompanhar o progresso de uma operação demorada. Uma barra de progresso pode mostrar um percentual aproximado de conclusão (determinado) ou indicar que uma operação está em andamento (indeterminada).

Os estudos de usabilidade mostraram que os usuários estão cientes dos tempos de resposta de mais de um segundo. Consequentemente, você deve considerar que as operações que levam dois segundos ou mais para serem concluídas sejam demoradas e precisem de algum tipo de comentários de progresso.

![captura de tela de uma barra de progresso típica ](images/progress-bars-image1.png)

Uma barra de progresso típica.

> [!Note]  
> As diretrizes relacionadas [ao layout](vis-layout.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **A operação será concluída em cerca de cinco segundos ou menos?** Nesse caso, use um [indicador de atividade,](inter-mouse.md) pois exibir uma barra de progresso por uma duração tão curta seria uma distração. Se a operação geralmente leva cinco segundos ou menos, mas às vezes leva mais, comece com um ponteiro ocupado e converta em uma barra de progresso após cinco segundos.
-   **Uma barra de progresso indeterminada é usada para aguardar o usuário concluir uma tarefa?** Se sim, não use uma barra de progresso. As barras de progresso são para o progresso do computador, não para o progresso do usuário.
-   **Uma barra de progresso indeterminada é combinada com uma animação?** Em caso afirmado, use apenas a animação. A barra de progresso indeterminada é efetivamente uma animação genérica e não adiciona nenhum valor à animação.
-   **A operação é uma tarefa em segundo plano muito longa (mais de dois minutos) para a qual os usuários estão mais interessados na conclusão do que no progresso?** Em caso afirmado, use [uma notificação.](mess-notif.md) Nesse caso, os usuários fazem outras tarefas enquanto isso e não estão monitorando o progresso. O uso de uma notificação permite que os usuários executem outras tarefas sem interrupção. Exemplos dessas operações demoradas incluem impressão, backup, verificações do sistema e conversões ou transferências de dados em massa.
-   **Quando a operação for concluída, os usuários poderão repetir os resultados?** Em caso afirmado, use um controle deslizante. Exemplos dessas operações incluem gravação e reprodução de vídeo e áudio.

    ![captura de tela do player de mídia e controle deslizante ](images/progress-bars-image2.png)

    Neste exemplo, um controle deslizante é usado para indicar o progresso durante a reprodução de som. Isso permite que os usuários reproduçãom os resultados mais tarde.

## <a name="design-concepts"></a>Conceitos de design

Durante uma operação demorada, os usuários precisam de uma ideia geral do que a operação está fazendo. Eles também precisam saber:

-   Que uma operação demorada foi iniciada.
-   Esse progresso está sendo feito e que a operação eventualmente será concluída (e, portanto, não foi bloqueada).
-   O percentual aproximado da operação que foi concluída (e, portanto, o percentual restante).
-   Se eles devem cancelar a operação se não vale a pena continuar a aguardar.
-   Se eles devem continuar a aguardar ou fazer outra coisa enquanto a operação é concluída.

**Use barras de progresso determinadas** para operações que exigem um período limitado, mesmo que essa quantidade de tempo não possa ser prevista com precisão. Barras de progresso indeterminadas mostram que o progresso está sendo feito, mas não fornecem outras informações. Não escolha uma barra de progresso indeterminada com base apenas na possível falta de precisão.

Por exemplo, suponha que uma operação exija cinco etapas e cada uma dessas etapas exija uma quantidade limitada de tempo, mas a quantidade de tempo para cada etapa pode variar muito. Nesse caso, use uma barra de progresso determinada e mostre o progresso quando cada etapa for concluída proporcional à quantidade de tempo que cada etapa geralmente leva. Use uma barra de progresso indeterminada somente se uma barra de progresso determinada fazer com que os usuários concluam incorretamente que a operação foi bloqueada.

**Se você fizer apenas uma coisa...**

Certifique-se de fornecer comentários de progresso para operações demoradas e se as informações acima estão claramente comunicadas. Use barras de progresso determinadas sempre que possível.

## <a name="usage-patterns"></a>Padrões de uso

As barras de progresso têm vários padrões de uso:

### <a name="determinate-progress-bars"></a>Determinar barras de progresso




| Rótulo | Valor |
|--------|-------|
| <strong>Barras de progresso determinadas modais</strong><br /> Indique o progresso de uma operação preenchendo da esquerda para a direita e preenchendo completamente quando a operação for concluída. <br /> | Como esse feedback é <a href="glossary.md">modal,</a>os usuários não podem executar outras tarefas na janela (ou seu pai, se exibido em uma caixa de diálogo modal) até que a operação seja concluída. <br /><img src="images/progress-bars-image3.png" alt="Screen shot of progress bar in modal window " /><br /> Neste exemplo, a barra de progresso fornece comentários durante a configuração. <br /> | 
| <strong>Barras de progresso determinadas modais com um botão Cancelar ou Parar</strong><br /> Permitir que os usuários parem a operação, talvez porque a operação esteja demorando muito ou não vale a pena esperar.<br /> | <img src="images/progress-bars-image4.png" alt="Screen shot of progress bar with Stop button " /><br /> Neste exemplo, os usuários podem clicar em Parar para interromper a operação e deixar o ambiente em seu estado atual.<br /> | 
| <strong>Barras de progresso determinadas modais com um botão Cancelar ou Parar e animação</strong><br /> Permitir que os usuários parem a operação e incluam uma animação para ajudar os usuários a visualizar o efeito de uma operação.<br /> | <img src="images/progress-bars-image5.png" alt="Screen shot of progress bar with animation " /><br /> Neste exemplo, os usuários podem clicar em Parar para interromper a operação e deixar o ambiente em seu estado atual.<br /> | 
| <strong>Barras de progresso duplas determinadas modais</strong><br /> Indique o progresso de uma operação de várias etapas mostrando o progresso da etapa atual na primeira barra de progresso e o progresso geral na segunda barra.<br /> | Como a primeira barra de progresso fornece poucas informações adicionais e pode ser bastante distração, esse padrão não é recomendado. Em vez disso, todas as etapas na operação compartilham uma parte do progresso e fazer com que uma única barra de progresso seja concluída uma vez. <br /><img src="images/progress-bars-image6.png" alt="Screen shot of current and overall progress bars " /><br /> Neste exemplo, a primeira barra de progresso mostra o progresso da etapa atual e a segunda barra de progresso mostra o progresso geral.<br /><blockquote>[!Note]<br />Esse padrão geralmente é desnecessário e deve ser evitado.</blockquote><br /><br /> | 
| <strong>Barras de progresso determinadas sem modo</strong><br /> Indique o progresso de uma operação preenchendo da esquerda para a direita e preenchendo completamente quando a operação for concluída.<br /> | Ao contrário das barras de progresso modais, os usuários podem executar outras tarefas enquanto a operação está em andamento. Essas barras de progresso podem ser exibidas no contexto ou em uma barra de status. <br /><img src="images/progress-bars-image7.png" alt="Screen shot of progress bar on status bar " /><br /> Neste exemplo, Windows Internet ExplorerWindows Internet Explorer exibe seu progresso para carregar uma página da Web na barra de status. Os usuários podem executar outras tarefas enquanto a página está sendo carregada.<br /> | 




 

### <a name="indeterminate-progress-bars"></a>Barras de progresso indeterminadas



|   Tipo de barra de progresso  | Descrição             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Barras de progresso indeterminadas modais**<br/> indique que uma operação está em andamento mostrando uma animação que faz o ciclo contínuo na barra da esquerda para a direita. <br/>   | Usado somente para operações cujo progresso geral não pode ser determinado, portanto, não há nenhuma noção de conclusão. as barras de progresso determinadas são preferíveis porque indicam o percentual aproximado da operação que foi concluída e ajudam os usuários a determinar se vale a pena continuar a aguardar a operação. eles também são menos distração visualmente. <br/> ![captura de tela da barra de progresso modal e indeterminada](images/progress-bars-image8.png)<br/> Neste exemplo, Windows Update usa uma barra de progresso modal indeterminada para indicar o progresso enquanto procura atualizações.<br/> |
| **Barras de progresso indeterminadas sem modo**<br/> indique que uma operação está em andamento mostrando uma animação que faz o ciclo contínuo na barra da esquerda para a direita.<br/> | Ao contrário das barras de progresso modais, os usuários podem executar outras tarefas enquanto o processamento está em andamento. essas barras de progresso podem ser exibidas no contexto ou em uma barra de status. <br/> ![captura de tela da barra de progresso fino na janela do Outlook ](images/progress-bars-image9.png)<br/> Neste exemplo, o Microsoft Outlook usa uma barra de progresso indeterminada sem modo ao preencher as propriedades de contato. Os usuários podem continuar a usar a janela de propriedades enquanto esse trabalho está em andamento.<br/>                                                                                                                    |



 

### <a name="meters"></a>Metros



|   Digite                                                                                       |   Descrição                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Metros**<br/> Indique uma porcentagem que não esteja relacionada ao progresso. <br/> | Esse padrão não é uma barra de progresso, mas é implementado usando o controle de barra de progresso. os medidores têm uma aparência distinta para diferenciá-los das barras de progresso reais. <br/> ![captura de tela de medidor mostrando espaço livre em disco ](images/progress-bars-image10.png)<br/> Neste exemplo, o medidor mostra a porcentagem de espaço usado na unidade de disco.<br/> |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Forneça comentários sobre o progresso ao executar uma operação demorada.** Os usuários nunca devem adivinhar se o andamento está sendo feito.
-   **Indique claramente o progresso real.** A barra de progresso deve avançar se o andamento estiver sendo feito. Se o intervalo de tempos de conclusão esperados for grande, considere usar uma escala não linear para indicar o progresso para os tempos mais longos. Você não quer que os usuários concluam que seu programa foi bloqueado quando não.
-   **Indique claramente a falta de progresso.** A barra de progresso não deve ser adiantada se nenhum progresso estiver sendo feito. Você não quer que os usuários aguardem indefinidamente uma operação que nunca será concluída.
-   **Forneça detalhes úteis do progresso.** Forneça informações de progresso adicionais, mas somente se os usuários puderem fazer algo com ele. Verifique se o texto é exibido por tempo suficiente para que os usuários possam lê-lo.

    ![captura de tela da barra de progresso mostrando a taxa de transferência ](images/progress-bars-image11.png)

    Neste exemplo, os usuários podem ver a taxa de transferência. A taxa de transferência baixa aqui sugere a necessidade de usar uma conexão de rede de alta largura de banda.

-   **Não forneça detalhes desnecessários.** Geralmente, os usuários não se preocupam com os detalhes da operação que está sendo executada. Por exemplo, os usuários de um programa de instalação não se preocupam com o arquivo específico que está sendo copiado ou que os componentes do sistema estão sendo registrados porque não têm expectativas sobre esses detalhes. Normalmente, uma barra de progresso bem rotulada apenas fornece informações suficientes, portanto, forneça informações de progresso adicionais somente se os usuários puderem fazer algo com ele. Fornecer detalhes de que os usuários não se preocupam torna a experiência do usuário excessivamente complicada e técnica. Se você precisar de informações mais detalhadas para depuração, não a exiba em builds de versão.

    **Correto:**

    ![captura de tela do progresso da instalação ](images/progress-bars-image12.png)

    Neste exemplo, a barra de progresso rotulada é tudo o que é necessário.

    **Correto:**

    ![captura de tela da barra de progresso mostrando a taxa de transferência ](images/progress-bars-image11.png)

    neste exemplo, Windows Explorer está copiando os arquivos que o usuário selecionou, de modo que a exibição dos nomes de arquivo que estão sendo copiados é significativa.

    **Incorreto:**

    ![captura de tela de progresso do registro ](images/progress-bars-image13.png)

    Neste exemplo, um programa de instalação está fornecendo detalhes que não fazem sentido para o usuário.

-   **Fornecer animações úteis.** Se isso for feito bem, as animações melhorarão a experiência do usuário ajudando os usuários a visualizar a operação. Boas animações têm mais impacto do que apenas texto. por exemplo, a barra de progresso do comando Outlook excluir exibirá a lixeira do destino se os arquivos puderem ser recuperados, mas nenhuma lixeira se os arquivos não puderem ser recuperados.

    ![captura de tela do progresso da exclusão ](images/progress-bars-image14.png)

    Neste exemplo, a falta de uma lixeira reforça a exclusão permanente dos arquivos. Essas informações adicionais não seriam comunicadas com eficiência usando apenas texto.

-   **Não use animações desnecessárias.** As animações podem ser enganosas porque normalmente são executadas em um thread separado da tarefa real e, portanto, podem sugerir o progresso mesmo que a operação tenha sido bloqueada. Além disso, se a operação for mais lenta do que o esperado, os usuários às vezes supõem que a animação faz parte do motivo. Consequentemente, use apenas animações quando houver uma justificativa clara; Não use-os para tentar fazer entretenimento aos usuários.
-   **Posicione as animações centralizadas na barra de progresso.** Coloque a animação acima dos rótulos da barra de progresso, se houver. Se houver um botão cancelar ou parar à direita da barra de progresso, inclua o botão ao determinar o centro.
-   **Tocar um efeito de som na conclusão de uma operação somente se ela for muito demorada (mais de dois minutos), não frequente e importante.** Se for provável que o usuário saia de uma operação importante durante o processamento, um efeito de som restaurará a atenção do usuário. Usar um efeito de som após a conclusão em outras circunstâncias seria um aborrecimento confuso.
-   **Não roube o foco de entrada para mostrar uma atualização ou conclusão de progresso.** Os usuários geralmente alternam para outros programas enquanto aguardam e não querem ser interrompidos. As tarefas em segundo plano devem permanecer em segundo plano.
-   **Não se preocupe com o suporte técnico.** Como os comentários fornecidos pelas barras de progresso não são necessariamente precisos e a frota, as barras de progresso não são um bom mecanismo para fornecer informações para o suporte técnico. Consequentemente, se a operação puder falhar (como com um programa de instalação), não forneça informações de progresso adicionais que só são úteis para o suporte técnico. Em vez disso, forneça um mecanismo alternativo, como um arquivo de log, para registrar informações de suporte técnico.

    **Incorreto:**

    ![captura de tela da barra de progresso mostrando o nome do servidor ](images/progress-bars-image15.png)

    Neste exemplo, a barra de progresso mostra detalhes destinados ao suporte técnico.

-   **Não coloque a porcentagem concluída ou qualquer outro texto em uma barra de progresso.** Esse texto não está acessível e não é compatível com o uso de temas.

    **Incorreto:**

    ![captura de tela da barra de progresso com texto na barra ](images/progress-bars-image16.png)

    Neste exemplo, o texto de porcentagem na barra de progresso não está acessível.

-   **Não combine uma barra de progresso com um ponteiro ocupado.** Use um ou outro, mas não ambos ao mesmo tempo.
-   **Não use barras de progresso vertical.** As barras de progresso horizontais têm um mapeamento mais natural e um fluxo melhor.

### <a name="determinate-progress-bars"></a>Barras de progresso de destérmino

-   **Use as barras de progresso de desligamento para operações que exigem uma quantidade de tempo limitada,** mesmo que essa quantidade de tempo não possa ser prevista com precisão. As barras de progresso indeterminadas mostram que o progresso está sendo feito, mas não fornecem outras informações. Não escolha uma barra de progresso indeterminada com base apenas na possível falta de exatidão.
-   **Indique claramente a fase de progresso.** A barra de progresso deve ser capaz de indicar se a operação está no início, no meio ou no fim de uma operação. Por exemplo, as barras de progresso que duram imediatamente a conclusão de 99% e, em seguida, permanecem lá por muito tempo são particularmente informativas e irritantes. Nesses casos, a barra de progresso deve ser definida inicialmente para, no máximo, 33% para indicar que a operação ainda está na fase de início.
-   **Indicar claramente a conclusão.** Não deixe que uma barra de progresso vá para 100 por cento, a menos que a operação tenha sido concluída.
-   **Forneça uma estimativa de tempo restante se você puder fazer isso com precisão.** As estimativas de tempo restantes que são precisas são úteis, mas as estimativas que estão longe de marcar ou saltar de forma significativa não são úteis. Talvez seja necessário executar algum processamento para que você possa fornecer estimativas precisas. Nesse caso, não exiba estimativas potencialmente imprecisas durante esse período inicial.
-   **Não reinicie o progresso.** Uma barra de progresso perderá seu valor se ela for reiniciada (talvez porque uma etapa na operação seja concluída) porque os usuários não têm como saber quando a operação será concluída. Em vez disso, todas as etapas na operação compartilham uma parte do progresso e a barra de progresso passa para a conclusão uma vez.

    **Incorreto:**

    ![captura de tela da barra de progresso reiniciada ](images/progress-bars-image17.png)

    Neste exemplo, a operação foi movida para a etapa de copiar arquivos e redefinir a barra de progresso para essa etapa. Agora, os usuários não têm idéia de quanto progresso foi feito ou quanto tempo resta.

-   **Não faça backup do andamento.** Assim como com uma reinicialização, uma barra de progresso perderá seu valor se ele fizer backup. Sempre aumente o progresso de forma monotônico. No entanto, você pode ter uma estimativa de tempo restante que aumenta (bem como diminui), pois a taxa de progresso pode variar.

### <a name="indeterminate-progress-bars"></a>Barras de progresso indeterminadas

-   **Use barras de progresso indeterminadas somente para operações cujo progresso geral não pode ser determinado.** Use barras de progresso indeterminadas para operações que exigem um período de tempo não associado ou que acessam um número desconhecido de objetos. Use tempos limite para dar limites a operações baseadas em tempo.
-   **Converter em uma barra de progresso de destérmino quando o progresso geral puder ser determinado.** Por exemplo, se demorar muito mais do que dois segundos para determinar o número de objetos, você poderá usar uma barra de progresso indeterminada enquanto os objetos são contados e, em seguida, converter em uma barra de progresso de desterminação.
-   **Não combine barras de progresso indeterminadas com porcentagem concluída ou estimativas de tempo restante.** Se você puder fornecer essas informações, use uma barra de progresso de destérmino em vez disso.
-   **Não combine barras de progresso indeterminadas com animações.** Uma barra de progresso indeterminada é efetivamente uma animação genérica, portanto, você deve usar uma ou outra, mas nunca ambas.

    **Correto:**

    ![captura de tela de progresso na detecção do servidor ](images/progress-bars-image18.png)

    Neste exemplo, apenas uma animação é usada para mostrar que uma operação está em andamento.

### <a name="modeless-progress-bars"></a>Barras de progresso sem janela restrita

-   **Se os usuários puderem fazer algo produtivo enquanto a operação estiver em andamento, forneça comentários sem janela.** Talvez seja necessário desabilitar um subconjunto de funcionalidades que exijam a conclusão da operação.
-   **Se a janela tiver uma barra de endereços, exiba o progresso sem janela restrita na barra de endereços.**

    ![captura de tela da barra de progresso como parte da barra de endereços ](images/progress-bars-image19.png)

    Neste exemplo, o progresso sem janela restrita é mostrado na barra de endereços.

-   Caso contrário, **se a janela tiver uma barra de status, exiba o progresso sem janela restrita na barra de status.** Coloque qualquer texto correspondente à esquerda na barra de status.

    ![captura de tela da barra de progresso como parte da barra de status ](images/progress-bars-image7.png)

    Neste exemplo, o progresso sem janela restrita é mostrado na barra de status.

### <a name="modal-progress-bars"></a>Barras de progresso modais

-   **Coloque barras de progresso modais nas páginas de progresso ou** [nas caixas de diálogo de progresso](win-dialog-box.md).
-   **Forneça um botão de comando para interromper a operação se demorar mais de alguns segundos para ser concluído ou se o potencial nunca for concluído.** Rotular o botão cancelar se cancelar retornar o ambiente para seu estado anterior (sem efeitos colaterais), caso contrário, rotulará a parada do botão para indicar que ele deixa a operação parcialmente concluída intacta. Você pode alterar o rótulo do botão de cancelar para parar no meio da operação se, em algum momento, não for possível retornar o ambiente para seu estado anterior. Centralize o botão de comando verticalmente com a barra de progresso em vez de alinhar seu tops.

    **Correto:**

    ![captura de tela do andamento da espera pela rede ](images/progress-bars-image20.png)

    Neste exemplo, a interrupção da conexão de rede não tem efeito colateral, portanto, o cancelamento é usado.

    **Correto:**

    ![captura de tela da barra de progresso mostrando o tempo de cópia restante ](images/progress-bars-image21.png)

    Neste exemplo, a interrupção da cópia deixa todos os arquivos copiados, portanto, o botão de comando é rotulado como parar.

    **Incorreto:**

    ![captura de tela da barra de progresso de pesquisa e botão parar ](images/progress-bars-image22.png)

    Neste exemplo, a interrupção da pesquisa não deixa nenhum efeito colateral, portanto, o botão de comando deve ser rotulado como cancelar.

### <a name="time-remaining"></a>Tempo restante

Para barras de progresso de destérmino:

-   **Use os formatos de hora a seguir.** Comece com o primeiro dos seguintes formatos em que a unidade de tempo maior não é zero e, em seguida, altere para o próximo formato quando a unidade de tempo maior se tornar zero.

    **Para barras de progresso:**

    **Se as informações relacionadas forem mostradas em um formato de dois-pontos:**

    Tempo restante: h horas, m minutos

    Tempo restante: m minutos, s segundos

    Tempo restante: s segundos

    **Se o espaço da tela estiver em um Premium:**

    h horas, m min restante

    m min, s segundos restantes

    s segundos restantes

    **,**

    h horas, m minutos restantes

    m minutos, s segundos restantes

    s segundos restantes

    **Para barras de título:**

    hh: mm restantes

    mm: SS restantes

    0: SS restantes

    Esse formato compacto mostra as informações mais importantes primeiro, para que não sejam truncadas na barra de tarefas.

-   **Tornar as estimativas precisas, mas não dar precisão falsa.** Se a unidade maior for horas, dê minutos (se for significativo), mas não segundos.

    **Incorreto:**

    HH horas, mm minutos, ss segundos

-   **Mantenha a estimativa atualizada.** Tempo de atualização que as estimativas restantes têm pelo menos a cada 5 segundos.
-   **Concentre-se no tempo restante** porque essas são as informações que os usuários se preocupam mais. Dê tempo total decorrido somente quando houver cenários em que o tempo decorrido é útil (por exemplo, quando a tarefa provavelmente será repetida). Se a estimativa de tempo restante estiver associada a uma barra de progresso, não terá o texto de porcentagem concluída, pois essas informações são transmitidas pela própria barra de progresso.
-   **Tenha uma gramática correta.** Use unidades singulares quando o número for um.

    **Incorreto:**

    1 minutos, 1 segundo

-   **Use a capitalização com estilo de frase.**

### <a name="progress-bar-colors"></a>Cores da barra de progresso

-   **Use barras de progresso vermelho ou amarelo somente para indicar o status do progresso, não os resultados finais de uma tarefa.** Uma barra de progresso vermelha ou amarela indica que os usuários precisam executar alguma ação para concluir a tarefa. Se a condição não for recuperável, deixe a barra de progresso verde e exiba uma mensagem de erro.
-   **Ative a barra de progresso vermelha quando houver uma condição recuperável que impeça o progresso.** Exiba uma mensagem para explicar o problema e recomendar uma solução.
-   **Gire a barra de progresso em amarelo para indicar que o usuário pausou a tarefa ou que há uma condição que está** impedindo o andamento, mas o andamento ainda está ocorrendo (como, por exemplo, com conectividade de rede ruim). Se o usuário tiver pausado, altere o rótulo do botão pausar para retomar. Se o progresso for impedido, exiba uma mensagem para explicar o problema e recomendar uma solução.

### <a name="meters"></a>Medidores

-   **Use as barras de progresso somente para o progresso.** Use medidores para indicar percentuais que não estão relacionados ao progresso.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![diagrama mostrando o dimensionamento e o espaçamento da barra de progresso ](images/progress-bars-image23.png)

Dimensionamento e espaçamento recomendados para barras de progresso.

-   Sempre use a altura recomendada da barra de progresso.
    -   **Exceção:** Você poderá usar uma altura diferente se a janela pai não oferecer suporte à altura recomendada.
-   Use a largura mínima se desejar tornar a barra de progresso discreta.
-   Não use larguras mais longas do que o máximo recomendado. A barra de progresso não precisa preencher o espaço disponível.
-   Centralizar a barra de progresso horizontalmente se a janela for muito mais larga do que a largura máxima recomendada.

## <a name="labels"></a>Rótulos

### <a name="progress-bar-labels"></a>Rótulos da barra de progresso

-   **Use um rótulo conciso com um controle de texto estático para indicar o que a operação está fazendo.** Inicie o rótulo com um verbo (por exemplo, copiando) e termine com uma elipse. Esse rótulo pode ser alterado dinamicamente se a operação tiver várias etapas ou estiver processando vários objetos.
-   Não atribua uma [chave de acesso](glossary.md) exclusiva porque o controle não é interativo.
-   Use [a capitalização no estilo de frase](glossary.md).
-   Se a operação não foi iniciada diretamente pelo usuário, você pode incluir um rótulo adicional para fornecer o contexto e desculpas pela interrupção. Inicie este rótulo extra com a frase, aguarde enquanto. Esse rótulo não deve ser alterado durante a operação.

    ![captura de tela da barra de progresso com rótulo ](images/progress-bars-image24.png)

    Neste exemplo, o usuário está sendo solicitado a aguardar porque o usuário não iniciou a operação diretamente.

-   Posicione o rótulo acima da barra de progresso e alinhe o rótulo à borda esquerda da barra de progresso.

### <a name="progress-bar-details"></a>Detalhes da barra de progresso

-   Forneça detalhes em texto estático, precedendo os dados com um rótulo que termina com dois-pontos. Especifique as unidades (segundos, quilobytes e assim por diante) após o texto detalhado.

    **Correto:**

    ![captura de tela da barra de progresso mostrando a taxa de transferência ](images/progress-bars-image11.png)

    Neste exemplo, os detalhes são rotulados corretamente.

    **Incorreto:**

    ![captura de tela da barra de progresso sem o rótulo adequado ](images/progress-bars-image25.png)

    Neste exemplo, os detalhes não são rotulados, exigindo assim que os usuários determinem seu significado.

-   Use [a capitalização no estilo de frase](glossary.md).
-   Posicione os detalhes abaixo da barra de progresso e alinhe o rótulo à borda esquerda da barra de progresso.
-   Não dê ao percentual concluído ou restante porque essas informações são transmitidas pela própria barra de progresso.

### <a name="cancel-button"></a>Botão Cancelar

-   Rotular o botão cancelar se cancelar retornar o ambiente para seu estado anterior (não deixando nenhum efeito colateral); caso contrário, rotule a parada do botão para indicar que ele deixa a operação parcialmente concluída intacta.
-   Você pode alterar o rótulo do botão de cancelar para parar no meio da operação se, em algum momento, não for possível retornar o ambiente para seu estado anterior.

### <a name="progress-dialog-box-titles"></a>Títulos da caixa de diálogo progresso

-   Se a barra de progresso for exibida em uma caixa de diálogo modal, o título da caixa de diálogo deverá ser o nome do programa ou o nome da operação. Não use o que deve ser o rótulo de barra de progresso para o título da caixa de diálogo.

    **Correto:**

    ![captura de tela do título da barra de progresso com o nome da tarefa ](images/progress-bars-image26.png)

    Neste exemplo, o nome da tarefa é usado para o título da caixa de diálogo.

    **Incorreto:**

    ![captura de tela do título da caixa de diálogo redundante ](images/progress-bars-image27.png)

    Neste exemplo, o texto do título da caixa de diálogo é uma regressão do rótulo da barra de progresso. Em vez disso, o nome do programa deve ser usado.

-   Se a barra de progresso for exibida em uma caixa de diálogo sem janela restrita, otimize o título para exibição na barra de tarefas colocando concisamente as informações de distinção primeiro. Exemplo: "66% concluído".

 

