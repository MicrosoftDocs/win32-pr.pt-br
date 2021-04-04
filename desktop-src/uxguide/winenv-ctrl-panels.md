---
title: Painéis de controle
description: Use itens do painel de controle para ajudar os usuários a configurar recursos de nível de sistema e executar tarefas relacionadas. Os programas que têm uma interface do usuário devem ser configurados diretamente de sua interface do seu.
ms.assetid: 845325ef-9f1d-4aa7-a5b0-685fac74a9f8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dde41544f2bf8c920365f160f71dce7e88d89b81
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103930061"
---
# <a name="control-panels"></a>Painéis de controle

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Use itens do painel de controle para ajudar os usuários a configurar recursos de nível de sistema e executar tarefas relacionadas. Os programas que têm uma interface do usuário devem ser configurados diretamente de sua interface do seu.

Com o painel de controle no Microsoft Windows, os usuários podem configurar recursos de nível de sistema e executar tarefas relacionadas. Exemplos de configuração de recursos no nível do sistema incluem configuração de hardware e software e configuração, segurança, manutenção do sistema e gerenciamento de conta de usuário.

O termo painel de controle refere-se a todo o recurso do painel de controle do Windows. Os painéis de controle individuais são chamados de itens do painel de controle. Um item do painel de controle é considerado de nível superior quando ele está diretamente acessível no painel de controle home page ou em uma página de categoria.

![captura de tela da categoria de fala do painel de controle ](images/winenv-ctrl-panels-image1.png)

Um item de painel de controle típico.

O painel de controle home page é o ponto de entrada principal para todos os itens do painel de controle. Ele lista os itens por sua categoria, juntamente com as tarefas mais comuns. Ele é exibido quando os usuários clicam em painel de controle no menu iniciar.

Uma página de categoria do painel de controle lista os itens em uma única categoria, juntamente com as tarefas mais comuns. Ele é exibido quando os usuários clicam em um nome de categoria no home page.

Os itens do painel de controle são implementados usando [fluxos de tarefas](glossary.md) ou folhas de propriedades. Para o Windows Vista e posterior, os fluxos de tarefas são a interface do usuário preferida.

**Desenvolvedores:** Para saber como criar itens do painel de controle, consulte [itens do painel de controle](/previous-versions//bb776838(v=vs.85)).

**Observação:** As diretrizes relacionadas às [folhas de propriedades](win-property-win.md) são apresentadas em um artigo separado.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

-   **É a finalidade de configurar recursos de nível de sistema?** Caso contrário, use outro ponto de integração. Torne os recursos do aplicativo configuráveis diretamente da interface do usuário usando caixas de diálogo de opções, em vez de usar o painel de controle. Para utilitários que não são usados para instalação, configuração ou tarefas relacionadas (como solução de problemas), use o menu iniciar como o ponto de integração.
-   **O recurso de nível de sistema tem sua própria interface do usuário?** Nesse caso, essa interface do usuário é onde os usuários devem ir para fazer alterações. Por exemplo, um utilitário de backup do sistema deve ser configurado de suas opções de programa em vez de no painel de controle.
-   **Os usuários precisarão alterar a configuração com frequência?** Nesse caso (digamos, várias vezes por semana), considere soluções alternativas, talvez além de usar o painel de controle. Por exemplo, a configuração de volume mestre do Windows pode ser configurada diretamente de seu ícone na área de notificação. Algumas configurações podem ser definidas automaticamente. No Windows Explorer, por exemplo, a guia compatibilidade para propriedades de aplicativo permite que um aplicativo seja executado no modo de cor 256 em vez de exigir que os usuários alterem o modo de vídeo manualmente.
-   **Os usuários de destino são profissionais de ti?** Nesse caso, use um snap-in do [MMC (console de gerenciamento Microsoft)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) , que foi projetado especificamente para tarefas de gerenciamento do sistema. Em alguns casos, a melhor solução é ter um item do painel de controle para usuários gerais e um snap-in do MMC para profissionais de ti.

    ![captura de tela da janela de gerenciamento do computador ](images/winenv-ctrl-panels-image2.png)

    Neste exemplo, o snap-in do MMC usuários e grupos locais fornece gerenciamento de usuários direcionado a profissionais de ti. Outros usuários têm mais probabilidade de usar o item contas de usuário no painel de controle.

-   **O recurso é um recurso OEM usado somente durante a configuração inicial do sistema?** Nesse caso, use o centro de boas-vindas do Windows como o ponto de integração.

Os itens do painel de controle são necessários porque muitos recursos de nível de sistema não têm um ponto de integração mais óbvio ou direto. No entanto, o painel de controle não deve ser exibido como "um local" para todas as definições de configuração. **Os programas que têm uma interface do usuário devem ser configurados diretamente da interface de usuário em vez de usar itens do painel de controle.**

**Incorreto:**

![captura de tela do item de opções da Internet do painel de controle ](images/winenv-ctrl-panels-image3.png)

Neste exemplo, o Windows Internet Explorer não deve ser representado no painel de controle, porque sua própria interface do usuário é um ponto de integração melhor.

### <a name="create-a-new-control-panel-item-or-extend-an-existing-one"></a>Criar um novo item do painel de controle ou estender um existente?

Para decidir, considere estas perguntas:

-   **A funcionalidade pode ser expressa como tarefas que podem ser conectadas a um item existente do painel de controle extensível?** Os seguintes itens do painel de controle são extensíveis: dispositivos Bluetooth, vídeo, Internet, teclado, mouse, rede, energia, sistema, sem fio (infravermelho).
-   **As propriedades e tarefas substituem os recursos do item existente do painel de controle extensível?** Nesse caso, você deve estender o item existente do painel de controle porque isso resulta em uma experiência de usuário mais simples. Caso contrário, crie um novo item do painel de controle.

## <a name="design-concepts"></a>Conceitos de design

**O conceito do painel de controle é baseado em uma metáfora do mundo real.** Um painel de controle do mundo real é uma coleção de controles (botões, opções, medidores e monitores) usados para monitorar e controlar um dispositivo. Os usuários desses painéis de controle geralmente precisam de treinamento para entender como usá-los.

Ao contrário de suas contrapartes do mundo real, **os designs do painel de controle do Windows são otimizados para usuários de primeira hora.** Os usuários não executam a maioria das tarefas do painel de controle com muita frequência, de modo que normalmente não se lembram de como fazê-las e precisam reaprender cada vez mais com eficiência.

Para criar um item do painel de controle que seja útil e fácil de usar:

-   Verifique se as propriedades são necessárias.
-   Apresente as propriedades em termos de metas de usuário em vez de tecnologia.
-   Apresente as propriedades no nível certo.
-   Páginas de design para tarefas específicas.
-   Páginas de design para usuários padrão e administradores protegidos.

Ao criar e avaliar itens a serem incluídos no painel de controle, determine as tarefas comuns que os usuários executam e verifique se há um caminho claro para executar essas tarefas. Os usuários normalmente executam os seguintes tipos de tarefas com itens do painel de controle:

-   Configuração inicial
-   Alterações frequentes (para a maioria das configurações)
-   Alterações frequentes (para algumas configurações importantes)
-   Reverter configurações para um estado inicial ou anterior
-   Solução de problemas

**Se você fizer apenas uma coisa...**

Crie páginas do painel de controle para tarefas específicas e apresente-as em termos de metas do usuário em vez de tecnologia.

## <a name="usage-patterns"></a>Padrões de uso

Para itens do painel de controle, você pode usar um fluxo de tarefas ou uma folha de propriedades. Aqui estão seus padrões de uso:

### <a name="task-flow-patterns"></a>Padrões de fluxo de tarefas

Itens de fluxo de tarefas usam uma página de Hub para apresentar as opções de alto nível e as páginas do spoke para executar a configuração real.

**Páginas de Hub**

-   Páginas de Hub baseadas em tarefas. Essas páginas de Hub apresentam as tarefas usadas com mais frequência. Elas são mais bem usadas para algumas tarefas mais usadas ou importantes em que os usuários precisam de mais orientações e explicações. As páginas de Hub não têm botões de confirmação. As páginas de Hub baseadas em tarefas híbridas também têm algumas propriedades ou comandos diretamente. As páginas de Hub híbrido são altamente recomendadas quando os usuários têm mais probabilidade de usar o painel de controle para acessar essas propriedades e comandos.
-   Páginas de Hub baseadas em objeto. Essas páginas de Hub apresentam os objetos disponíveis usando um controle de exibição de lista. Eles são mais bem usados quando podem existir vários objetos. As páginas de Hub não têm botões de confirmação.

**Páginas do spoke**

-   Páginas de tarefas. Essas páginas spoke apresentam uma tarefa ou uma etapa em uma tarefa com uma instrução principal específica baseada em tarefa. Eles são mais bem usados para tarefas que se beneficiam de diretrizes e explicações adicionais.
-   Páginas de formulário. Essas páginas spoke apresentam uma coleção de propriedades e tarefas relacionadas com base em uma instrução principal geral. Eles são mais bem usados para recursos que têm muitas propriedades e se beneficiam de uma apresentação direta de página única, como propriedades avançadas.

### <a name="property-sheet-patterns"></a>Padrões de folha de propriedades

-   As folhas de propriedades são mais bem usadas em itens herdados com muitas configurações direcionadas a usuários avançados. Novos itens podem obter o mesmo efeito com um fluxo de tarefas usando o padrão de página de formulário.

## <a name="guidelines"></a>Diretrizes

### <a name="property-sheet-control-panel-items"></a>Itens do painel de controle da folha de propriedades

-   **Não use folhas de propriedades para novos itens do painel de controle.** Em vez disso, use fluxos de tarefas para criar uma experiência simplificada e fazer uso completo da funcionalidade de categorização e pesquisa do painel de controle home page.

### <a name="task-flow-control-panel-items"></a>Itens do painel de controle fluxo de tarefas

**Geral**

-   **Mantenha o conteúdo e os controles mais importantes visíveis sem rolar.** Os usuários não rolarão para ver o conteúdo da página, a menos que eles tenham um motivo para. Você pode tornar os botões de confirmação sempre visíveis colocando-os em uma [área de comando](glossary.md) em vez da área de conteúdo. Não divida as páginas apenas para evitar a rolagem.
    -   **Você pode rolar as páginas longas verticalmente,** contanto que os controles mais importantes fiquem visíveis sem rolagem.
    -   **Não use a rolagem horizontal.** Em vez disso, Reprojete o conteúdo da página e use a rolagem vertical. As páginas podem ter barras de rolagem horizontais somente quando tornadas muito estreitas.
-   **Para navegar entre as páginas:**
    -   Use [links de tarefas](glossary.md) para iniciar uma tarefa.
    -   Use links de tarefas ou um botão Avançar para navegar até a próxima página em uma tarefa de várias etapas.
    -   Use os botões de confirmação para concluir uma tarefa.
    -   Use o botão voltar na barra de menus para retornar às páginas exibidas anteriormente. Não adicione um botão voltar à área de comando.
    -   Use a barra de endereços para retornar diretamente ao painel de controle home page.
    -   Use ver também links no painel de tarefas para navegar até páginas em outros itens do painel de controle. Caso contrário, a navegação deve permanecer dentro de um único item do painel de controle.
-   **Coloque somente o painel de controle home page na barra de endereços.** Clicar nesse link retorna ao painel de controle home page, abandonando qualquer trabalho em andamento sem [confirmação](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx).
-   **Não coloque um botão de comando fechar nas páginas do painel de controle.** Os usuários podem fechar uma janela do painel de controle usando o botão fechar na barra de título.

**Links de tarefas e botões**

-   **Quando uma página tem um pequeno conjunto de opções fixas, use links de tarefas em vez de uma combinação de botões de opção e um botão Avançar.** Isso permite que os usuários selecionem uma resposta com um único clique.
-   Você pode colocar links de tarefas e botões nos seguintes locais (em ordem de descoberta):
    -   A [área de comando](glossary.md) (para botões de comando somente em páginas spoke).
    -   A [área de conteúdo](glossary.md):
        -   Botões de comando
        -   Links de tarefas
        -   Outros links
    -   Links no [painel de tarefas](glossary.md) (somente páginas de Hub).
-   **Baseie o local dos links de tarefas e os botões de importância e necessidade de descoberta.**
    -   **Coloque somente os botões de confirmação na área de comando.**
    -   **Coloque as tarefas essenciais na área de conteúdo.** Os botões de comando tendem a desenhar a mais atenção, portanto, Reserve-los para comandos que os usuários devem ver. Os links de tarefas também desenham a atenção, mas menos do que botões de comando.
    -   **Reserve o painel de tarefas e links simples para tarefas secundárias (menos importantes).** O painel de tarefas é a área menos detectável de uma página de tarefas, e links simples não são tão visíveis como botões de comando e links de tarefas.
-   Para links de tarefas apresentados na área de conteúdo:
    -   **Se houver mais de sete links, agrupe os links em categorias.** Forneça títulos para cada um dos grupos.
    -   **Para menos de sete links, apresente os links em um único grupo sem um título.**
-   **Apresentar links de tarefas e botões em uma ordem lógica.** Listar links de tarefas verticalmente, botões de comando horizontalmente.
-   Em categorias, **divida os comandos em grupos relacionados.** Apresente os grupos de tarefas colocando o mais usado primeiro e, dentro de cada grupo, coloque as tarefas mais usadas primeiro. **A ordem resultante deve seguir aproximadamente a probabilidade de uso, mas também ter um fluxo lógico.**
    -   **Exceção:** Links de tarefas que resultam em fazer tudo devem ser colocados primeiro.
-   **Se houver muitos links de tarefas, forneça as tarefas mais importantes uma aparência mais proeminente** usando um ícone de pixel 24x24 e duas linhas de texto. Para tarefas menos importantes, use um ícone de 16x16 pixels ou nenhum ícone e uma única linha de texto de link.

    ![captura de tela de itens com ícones grandes e pequenos ](images/winenv-ctrl-panels-image4.png)

    Neste exemplo, os comandos importantes recebem uma aparência mais proeminente.

-   **Ter uma separação física clara entre comandos usados com frequência e comandos destrutivos.** Caso contrário, os usuários podem clicar em comandos destrutivos acidentalmente. Talvez seja necessário reordenar os comandos de certa forma para colocar comandos destrutivos juntos.
-   **Forneça o mecanismo para desfazer comandos diretamente na página.** Os usuários não precisam navegar em nenhum outro lugar para desfazer um erro.
-   **Para links de tarefas, use todos os ícones de link de tarefa padrão ou todos os ícones personalizados.** Não os misture. Considere o uso de ícones personalizados somente se:
    -   Eles ajudam os usuários a compreender as tarefas.
    -   Eles estão em conformidade com os [padrões de ícone do Aero](vis-icons.md).
    -   Eles têm uma aparência discreta.

**Caixas de diálogo**

Ao usar fluxos de tarefas, geralmente você deseja que uma tarefa flua de uma página para uma página dentro de uma única janela, mas as circunstâncias a seguir são exceções. Use as caixas de diálogo nas seguintes circunstâncias:

-   Para solicitar aos usuários um nome de usuário e uma senha de administrador. Sempre use a caixa de diálogo Gerenciador de credenciais para essa finalidade. (Deve ser [modal](glossary.md).)
-   Para confirmar um comando in-loco usando uma caixa de diálogo de tarefa ou de mensagem. (Deve ser modal.)
-   Para obter a entrada de comandos in-loco, como para comandos novos, adicionar, salvar como, renomear e imprimir.

    ![captura de tela da caixa de diálogo excluir locais de rede ](images/winenv-ctrl-panels-image5.png)

    Neste exemplo, o comando Delete é executado em uma caixa de diálogo em vez de uma página separada.

-   Para executar tarefas secundárias e autônomas. Usar uma janela não [restrita](glossary.md), secundária permite que essas tarefas sejam executadas de forma independente e fora do fluxo de tarefas principal.

### <a name="hub-pages"></a>Páginas de Hub

**Geral**

-   Use páginas de Hub com base em tarefas quando:
    -   **Há um pequeno número de tarefas mais usadas ou importantes.**
    -   **A configuração envolve um ou dois objetos** (exemplos: monitores, teclado, mouse, controladores de jogo).
    -   **A configuração aplica-se a todo o sistema** (exemplos: data e hora, segurança, opções de energia).
-   Use páginas de Hub baseadas em objeto quando:
    -   **A configuração pode envolver vários objetos** (exemplos: contas de usuário, conexões de rede, impressoras).
    -   **A configuração se aplica somente ao objeto selecionado**.
-   **Não use uma página de Hub se o item do painel de controle tiver uma única página** que contém todas as tarefas e propriedades envolvidas.

**Listas de objetos**

-   **Listar itens em uma ordem lógica.** Classifique objetos nomeados em ordem alfabética, números em ordem numérica e datas em ordem cronológica.
-   Para hubs baseados em objeto, **forneça comandos de exibição de objeto no painel de tarefas se a capacidade de alterar a exibição for importante para as tarefas**. A capacidade de alterar as exibições é importante se houver muitos objetos e a apresentação padrão não funcionar bem para todos os cenários. Os usuários podem alterar a exibição de lista mesmo que não haja comandos explícitos por meio do menu de contexto de exibição de lista, mas é menos detectável.

Para obter mais diretrizes sobre a apresentação de listas de objetos, consulte [exibições de lista](ctrl-list-views.md).

**Interação**

-   **Não coloque botões de confirmação em páginas de Hub.** As páginas de Hub são pontos de inicialização fundamental. Os usuários nunca as páginas de Hub "Commit" nunca são feitos com eles. E os botões de confirmação nas páginas de Hub fazem com que todas as tarefas sejam iniciadas de um hub confuso (os usuários se perguntarão se essas tarefas precisarem ser confirmadas).
    -   **Exceção:** Se a alteração de uma configuração exigir [elevação](glossary.md), forneça um botão aplicar com um [ícone de escudo de segurança](winenv-uac.md). Desabilite o botão confirmar depois que as alterações forem aplicadas.
-   **Considere colocar as propriedades mais úteis diretamente em páginas de Hub.** Essas páginas de Hub híbrido são altamente recomendadas quando os usuários têm mais probabilidade de usar o painel de controle para acessar essas propriedades.

    ![captura de tela da página de Hub de opções de energia ](images/winenv-ctrl-panels-image6.png)

    Neste exemplo, o item do painel de controle opções de energia tem as configurações mais úteis diretamente na página Hub.

-   **Use um modelo de confirmação imediata para qualquer configuração em páginas de Hub híbrido para que as alterações sejam feitas imediatamente.** Novamente, os usuários nunca confirmam uma página de Hub. Se uma configuração exigir um botão de confirmação, não a coloque em uma página de Hub.
-   **Considere colocar comandos simples "uma etapa" diretamente em páginas de Hub em vez de usar links de navegação.**
-   **Confirme os comandos in-loco cujos efeitos não podem ser facilmente desfeitos.** Use uma caixa de [diálogo de tarefa](win-dialog-box.md) ou de [mensagem](glossary.md).

    ![captura de tela da caixa de diálogo Confirmar exclusão ](images/winenv-ctrl-panels-image7.png)

    Neste exemplo, o comando Delete é confirmado com uma caixa de diálogo.

-   **Para páginas de Hub baseadas em tarefas, identifique cada tarefa com um link de tarefa e um ícone.** Você também pode fornecer uma descrição opcional para cada link. No entanto, tente tornar os links de tarefas autoexplicativos e fornecer descrições opcionais apenas para links que realmente precisam deles.

    ![captura de tela da página de Hub de desempenho do computador ](images/winenv-ctrl-panels-image8.png)

    Neste exemplo, cada tarefa tem um link de tarefa e um ícone.

-   **Para páginas de Hub baseadas em objeto, o clique único seleciona objetos e um clique duas vezes seleciona um objeto e navega para sua página padrão.** A página padrão normalmente é uma página de propriedades ou uma página de Hub baseada em tarefas.
-   **Uma página de Hub baseada em objeto pode navegar para um hub baseado em tarefas para os objetos selecionados.** No entanto, esses hubs secundários devem ser evitados porque fazem com que um item do painel de controle fique indireto.

**Painéis de tarefas**

Use os painéis de tarefas para apresentar links para comandos, modos de exibição e itens do painel de controle relacionados.

-   Para painéis de tarefas em hubs baseados em tarefas, apresente links na seguinte ordem:
    -   **Comandos secundários**. Apresente as principais tarefas somente na área de conteúdo. Use o painel de tarefas para tarefas secundárias e opcionais. Considere uma tarefa primária se os usuários precisarem descobri-la em cenários importantes; secundário se for aceitável para os usuários não descobrirem.
    -   **Consulte também**. Os links opcionais que navegam para itens relacionados do painel de controle.
-   Para painéis de tarefas em hubs baseados em objeto, apresente links na seguinte ordem:
    -   **Exibições de objeto**. Os links opcionais usados para controlar a apresentação dos objetos.
    -   **Comandos fixos**. Os comandos que são independentes dos objetos atualmente selecionados.
    -   **Comandos contextuais**. Os comandos que dependem dos objetos atualmente selecionados e, portanto, nem sempre são exibidos.
    -   **Consulte também**. Os links opcionais que navegam para itens relacionados do painel de controle.
-   **Não use painéis de tarefas em páginas do spoke.** Ao contrário das páginas de Hub, as páginas do spoke devem ser focadas na conclusão da tarefa. Você não deseja encorajar os usuários a navegar antes da conclusão.

**Consulte também links**

-   **Forneça também links no painel de tarefas para ajudar os usuários a localizar itens do painel de controle relacionados, ou o item do painel de controle correto, se eles tiverem um errado.** Link para itens os usuários provavelmente serão associados ao item do painel de controle.

    ![captura de tela dos links ' Ver também ' da central de ações ](images/winenv-ctrl-panels-image9.png)

    Neste exemplo, o item do painel de controle da central de ações vincula-se a itens do painel de controle relacionados.

-   **Link para uma página de tarefa específica se isso for o que os usuários têm mais probabilidade de reconhecer.** Caso contrário, vincule a todo o item do painel de controle. Use o nome do painel de controle sem adicionar a frase, o painel de controle.

### <a name="spoke-pages"></a>Páginas do spoke

**Geral**

-   **Use páginas de tarefas para tarefas mais usadas ou importantes em que os usuários precisam de mais orientações e explicações.**
-   **Use páginas de formulário para recursos que têm muitas configurações e se beneficiam de uma apresentação direta de página única.** As tarefas ideais para essas páginas normalmente envolvem alterações óbvias em algumas propriedades simples.
-   **Não use painéis de tarefas em páginas do spoke.**

**Interação**

-   **Tente limitar as tarefas principais a uma única página.** Se mais de uma página for necessária, você poderá:
    -   **Use páginas intermediárias do spoke para etapas adicionais ou opcionais.** As páginas do spoke intermediário são confirmadas pela página do spoke final.
    -   **Use janelas independentes para tarefas auxiliares independentes.** As janelas independentes são confirmadas por conta própria e, independentemente, da tarefa principal.

Isso mantém o significado dos botões de confirmação para a tarefa principal clara e não ambígua. Os usuários devem estar sempre confiantes para entender o que estão confirmando.

-   **Não use ver também links dentro de um fluxo de tarefas.** Esses links para itens relacionados, mas diferentes do painel de controle. Embora a navegação para um item diferente seja aceitável em páginas de Hub, ela não está em páginas spoke, pois isso interrompe a tarefa.
-   **Não use páginas spoke para entradas ou confirmações simples.** Em vez disso, use caixas de diálogo modais.

**Interação (páginas de spoke intermediárias)**

-   **Use links de tarefas ou um botão Avançar para navegar até a próxima página.** A maneira de prosseguir para a próxima etapa deve ser sempre óbvia.
-   **Você pode ter links de navegação para etapas de tarefas opcionais.** Para evitar confusão quando os usuários se confirmam na tarefa, essas páginas extras devem ser páginas intermediárias dentro do mesmo item do painel de controle. Eles não devem ter botões de confirmação, mas devem ser confirmados quando a tarefa principal for confirmada.

**Interação (páginas do spoke final)**

-   **Use os botões de confirmação para concluir uma tarefa.** Use um [modelo de confirmação atrasado](glossary.md) para páginas do spoke, de modo que as alterações não sejam feitas até explicitamente confirmadas (se os usuários navegarem para fora usando voltar, fechar ou a barra de endereços, as alterações serão abandonadas). Os botões de confirmação são uma pista visual de que o usuário está prestes a concluir uma tarefa. Não use links para essa finalidade.
-   **Não confirme os botões de confirmação (incluindo cancelar).** Fazer isso pode ser irritante. Exceções:
    -   A ação tem consequências significativas e, se incorreta, não corrigível prontamente.
    -   A ação pode resultar em uma perda significativa do tempo ou esforço do usuário.
    -   A ação está claramente inconsistente com outras ações.
-   **Não confirme se os usuários abandonam as alterações** navegando para longe usando voltar, fechar ou a barra de endereços. No entanto, você pode confirmar se uma navegação potencialmente indesejada pode resultar em uma perda significativa do tempo ou esforço do usuário.
-   **Não use links de comando ou de navegação** (inclusive consulte também links). Nas páginas do spoke final, os usuários devem concluir ou cancelar explicitamente a tarefa. Os usuários não devem ser incentivados a navegar em outro lugar, pois isso provavelmente cancelaria a tarefa implicitamente.
-   **Quando os usuários concluírem ou cancelarem uma tarefa, eles deverão ser enviados de volta para a página de Hub da qual a tarefa foi iniciada.** Se não houver essa página, feche a janela painel de controle. Não presuma que as páginas spoke são sempre iniciadas em outra página.
-   **Remova as páginas "confirmadas" obsoletas da pilha voltar do Windows Explorer** ao retornar os usuários de volta para a página da qual a tarefa foi iniciada. Os usuários nunca devem ver as páginas às quais eles já se confirmaram ao clicar no botão voltar. Os usuários sempre devem fazer alterações adicionais refazendo completamente a tarefa em vez de clicar em voltar para modificar páginas obsoletas.
    -   **Desenvolvedores:** Você pode remover essas páginas obsoletas usando as APIs ITravelLog:: FindTravelEntry () e ITravelLogEx::D eleteEntry ().

**Botões de confirmação**

**Observação:** Os botões cancelar são considerados botões de confirmação.

-   **Confirme as tarefas usando botões de confirmação que são respostas específicas para a instrução principal, em vez de rótulos genéricos, como OK.** Os rótulos em botões de confirmação devem fazer sentido por conta própria. Evite usar OK porque não é uma resposta específica para a instrução principal e, portanto, mais fácil de lamentavelmente. Além disso, normalmente é usado com caixas de diálogo modais e, incorretamente, indica o fechamento da janela do item do painel de controle.
    -   **Exceção**
        -   Use OK para páginas que não têm configurações.
        -   Use OK quando a resposta específica ainda for genérica, como salvar, selecionar ou escolher, como ao alterar uma configuração específica ou uma coleção de configurações.
        -   Use OK se a página tiver botões de opção que são respostas para a instrução principal. Para manter o modelo de confirmação atrasada, você não pode usar links de tarefas em uma página final do spoke.

            ![captura de tela de restrições da Web com o botão OK ](images/winenv-ctrl-panels-image10.png)

            Neste exemplo, os botões de opção, não os botões de confirmação, são respostas para a instrução principal.
-   **Forneça um botão Cancelar para permitir que os usuários abandonem explicitamente as alterações.** Embora os usuários possam abandonar implicitamente uma tarefa não confirmando as alterações, fornecer um botão Cancelar permite que eles façam isso com maior confiança.
    -   **Exceção:** Não forneça um botão Cancelar para tarefas em que os usuários não podem fazer alterações. O botão OK tem o mesmo efeito que cancelar nesse caso.
-   **Não use botões de confirmação de fechamento, concluído ou término.** Normalmente, esses botões são usados com caixas de diálogo modais e incorretamente, fechando a janela do item do painel de controle. Os usuários podem fechar a janela usando o botão fechar na barra de título. Além disso, a conclusão e a conclusão são enganosas porque os usuários são retornados para a página na qual a tarefa foi iniciada, para que eles não sejam realmente feitos.
-   **Não desabilite os botões de confirmação.** Caso contrário, os usuários precisam deduzir por que os botões de confirmação estão desabilitados. É melhor deixar os botões de confirmação habilitados e fornecer uma mensagem de erro útil sempre que houver um problema.
-   **Verifique se os botões de confirmação aparecem na página sem rolagem.** Se a página for longa, você poderá tornar os botões de confirmação sempre visíveis colocando-os em uma [área de comando](glossary.md), em vez de na área de conteúdo.

    ![captura de tela da caixa de diálogo reprodução automática ](images/winenv-ctrl-panels-image11.png)

    Neste exemplo, o tamanho da área de conteúdo é não associado, portanto, os botões de confirmação são colocados na área de comando.

-   Alinhar os botões de confirmação e usar esta ordem (da esquerda para a direita): botões de confirmação positivos, cancelar e aplicar.

**Botões de visualização**

-   Verifique se **o botão de visualização significa aplicar as alterações pendentes agora, mas restaure as configurações atuais se os usuários navegarem para fora da página sem confirmar as alterações.**
-   **Você pode usar os botões de visualização em qualquer página do spoke.** As páginas de Hub não precisam de botões de visualização porque usam um [modelo de confirmação imediata](glossary.md).
-   **Considere usar um botão de visualização em vez de um botão Aplicar para páginas do painel de controle.** Os botões de visualização são mais fáceis para os usuários entenderem e podem ser usados em qualquer página do spoke.
-   **Forneça um botão de visualização somente se a página tiver configurações (pelo menos uma) com efeitos que os usuários podem ver.** Os usuários devem ser capazes de visualizar uma alteração, avaliar a alteração e fazer outras alterações com base nessa avaliação.
-   **Sempre habilite o botão Visualizar.**

**Visualizações dinâmicas**

Um item do painel de controle tem visualização dinâmica quando o efeito das alterações em uma página do spoke pode ser visto imediatamente.

-   **Considere usar a visualização dinâmica para configurações de exibição quando:**
    -   O efeito é óbvio, normalmente porque se aplica ao monitor inteiro.
    -   O efeito pode ser aplicado sem atraso significativo.
    -   O efeito é seguro e pode ser desfeito facilmente.

        ![captura de tela da caixa de diálogo Alterar configurações de cores ](images/winenv-ctrl-panels-image12.png)

        Neste exemplo, o efeito das configurações de cor e aparência do Windows é visto imediatamente. Isso permite que os usuários façam alterações com o mínimo de esforço.

-   **Use salvar alterações e cancelar para os botões de confirmação.** "Salvar alterações" mantém as configurações atuais, enquanto cancelar reverte para as configurações originais. "Salvar alterações" é usado em vez de OK para deixar claro que todas as alterações visualizadas ainda não foram aplicadas.
-   **Não forneça um botão Aplicar.** A visualização dinâmica torna desnecessária a aplicação.
-   **Restaure as alterações se os usuários navegarem para longe** usando voltar, fechar ou a barra de endereços. Para preservar as alterações, os usuários devem confirmá-las explicitamente.

**Aplicar botões**

-   Certifique-se **de que o botão Aplicar significa aplicar as alterações pendentes (feitas desde que a tarefa foi iniciada ou a última aplicação), mas permanece na página atual.** Isso permite que os usuários avaliem as alterações antes de passar para outras tarefas.
-   **Use os botões aplicar somente nas páginas do spoke final.** Os botões aplicar não devem ser usados em páginas de spoke intermediárias para manter um modelo de confirmação imediata.
    -   **Exceção:** Você pode usar os botões aplicar em uma página de Hub híbrido se a alteração de uma configuração exigir [elevação](glossary.md). Para obter mais detalhes, consulte [interação de página de Hub](#hub-pages).
-   **Forneça um botão aplicar somente se a página tiver configurações (pelo menos uma) com efeitos que os usuários podem avaliar de maneira significativa.** Normalmente, os botões aplicar são usados quando as configurações fazem alterações visíveis. Os usuários devem ser capazes de aplicar uma alteração, avaliar a alteração e fazer outras alterações com base nessa avaliação.
-   **Habilitar o botão aplicar somente quando houver alterações pendentes;** caso contrário, desabilite-o.
-   **Atribua "A" como a chave de acesso.**

### <a name="control-panel-integration"></a>Integração do painel de controle

Para integrar o item do painel de controle com o Windows, você pode:

-   **Registre o item do painel de controle (incluindo seu nome, descrição e ícone)**, para que o Windows esteja ciente dele.
-   Se o item do painel de controle for de nível superior (veja abaixo):
    -   Associe-o à **página de categoria** apropriada.
    -   **Forneça links de tarefas (incluindo seu nome, descrição, palavras-chave e linha de comando)** para indicar as tarefas principais e permitir que os usuários naveguem diretamente para as tarefas.
-   **Forneça termos de pesquisa** para ajudar os usuários a localizar os links de tarefas usando o recurso de pesquisa do painel de controle.

    Observe que você pode fornecer essas informações somente para itens de painel de controle individuais que não pode adicionar ou alterar essas informações para itens existentes do painel de controle que você estende.

**Páginas de categoria**

-   **Adicione o item do painel de controle a uma página de categoria somente se:**

    -   A maioria dos usuários precisa dela. Exemplo: Central de rede e compartilhamento
    -   Ele é usado muitas vezes. Exemplo: sistema
    -   Ele fornece uma funcionalidade importante que não é exposta em outro lugar. Exemplo: impressoras

    Os itens do painel de controle que atendem a esses critérios são chamados de nível superior.

-   **Não adicione o item do painel de controle a uma página de categoria se:**

    -   Ele raramente é usado ou usado para configuração única. Exemplo: centro de boas-vindas
    -   Ele é destinado a usuários avançados ou profissionais de ti. Exemplo: gerenciamento de cores
    -   Ele não se aplica à configuração atual de hardware ou de software. Exemplo: Windows SideShow (se não houver suporte para o hardware atual).

    Remover esses itens do painel de controle das páginas de categoria torna os itens de nível superior mais fáceis de localizar. Dado seu uso, esses itens do painel de controle são descobertos suficientemente por meio de pesquisa ou pontos de entrada contextuais.

-   **Associe o item do painel de controle de nível superior à categoria sob a qual os usuários têm mais probabilidade de procurar.** Essa decisão deve ser baseada no teste do usuário.
-   **Considere associar o item do painel de controle de nível superior com a segunda categoria mais provável também.** Você deve associar um item do painel de controle com duas categorias se for provável que os usuários procurem suas principais tarefas em mais de um lugar.
-   **Não associe o item do painel de controle com mais de duas categorias.** O valor da categorização será subminado se os itens do painel de controle aparecerem em várias categorias.

**Links de tarefas**

-   **Associe o item do painel de controle às suas tarefas principais.** Você pode exibir até cinco tarefas em uma página de categoria, mas tarefas adicionais são usadas para pesquisa no painel de controle. Use a mesma frase que você faz para links de tarefas, possivelmente removendo algumas palavras para tornar os links de tarefa mais sucintos.
-   **Prefira que os links de tarefas levam a locais diferentes no item do painel de controle.** Ter vários links para o mesmo local pode ser confuso.

**Termos de pesquisa**

-   **Registre os termos de pesquisa para o item do painel de controle que os usuários têm mais probabilidade de usar para descrevê-lo.** Esses termos de pesquisa devem incluir:

    -   Os recursos ou objetos configurados.
    -   As tarefas principais.

    Esses termos de pesquisa devem ser baseados no teste do usuário.

-   **Inclua também sinônimos comuns para esses termos de pesquisa.** Por exemplo, monitor e exibição são sinônimos, portanto, ambas as palavras devem ser incluídas.
-   **Inclua grafias alternativas ou quebras de palavras.** Por exemplo, os usuários podem pesquisar o site e o site da Web. Considere também fornecer erros de grafia comuns.
-   **Considere os formulários de substantivos do singular e do plural.** O recurso de pesquisa do painel de controle não pesquisa automaticamente os dois formulários; forneça os formulários para os quais os usuários provavelmente pesquisarão.
-   **Use verbos conjugação presentes simples.** Se você registrar a conexão como um termo de pesquisa, o recurso de pesquisa não procurará conexões, conexões e conectadas automaticamente.
-   **Não se preocupe com o caso.** O recurso de pesquisa não diferencia maiúsculas de minúsculas.

### <a name="standard-users-and-protected-administrators"></a>Usuários padrão e administradores protegidos

**Muitas configurações exigem privilégios de administrador para serem alteradas.** Se um processo exigir privilégios de administrador, o Windows Vista e posterior exigirá que [os usuários padrão](glossary.md) e [os administradores protegidos](glossary.md) elevem seus privilégios explicitamente. Isso ajuda a impedir que códigos mal-intencionados sejam executados com privilégios de administrador.

Para obter mais informações e exemplos, consulte [controle de conta de usuário](winenv-uac.md).

### <a name="schemes-and-themes"></a>Esquemas e temas

Um esquema é uma coleção nomeada de configurações visuais. Um tema é uma coleção nomeada de configurações no sistema. Exemplos de esquemas e temas incluem exibição, mouse, telefone e modem, opções de energia e opções de som e áudio.

-   **Permitir que os usuários criem esquemas quando:**

    -   **É provável que os usuários alterem as configurações.**
    -   **Os usuários têm mais probabilidade de alterar as configurações como uma coleção.**

    Os esquemas são úteis quando os usuários estão em um ambiente diferente, como um local físico diferente (país/região, fuso horário); usando o computador em uma situação diferente (baterias, encaixadas/desencaixadas); ou usando seu computador para uma função diferente (apresentações, reprodução de vídeo).

-   **Forneça pelo menos um esquema padrão.** O esquema padrão deve estar bem nomeado e ser aplicado à maioria dos usuários na maioria das circunstâncias. Os usuários não devem precisar criar um esquema próprio.
-   **Forneça uma visualização** ou outro mecanismo para que os usuários possam ver as configurações no esquema.

    ![captura de tela da caixa de diálogo personalização ](images/winenv-ctrl-panels-image13.png)

    Neste exemplo, o item Painel de controle de personalização mostra uma visualização das configurações de área de trabalho e aparência.

-   **Forneça os comandos Salvar como e excluir.** Um comando de renomeação não é necessário. os usuários podem renomear esquemas salvando sob o nome desejado e excluindo o esquema original.
-   Se as configurações não puderem ser aplicadas sem um esquema, **não permita que os usuários excluam todos os esquemas.** Os usuários não devem precisar criar um esquema próprio.
-   Se os esquemas não forem completamente independentes (por exemplo, os esquemas de energia dependem do modo de operação atual do laptop), **Verifique se há uma maneira fácil de alterar as configurações que se aplicam em todos os esquemas.** Por exemplo, com os esquemas de energia, verifique se os usuários podem definir o que acontece quando a tampa de um computador portátil é fechada em um único local.

### <a name="miscellaneous"></a>Diversos

-   **Use extensões do painel de controle para recursos que substituem ou estendem a funcionalidade existente do Windows.** Os seguintes itens do painel de controle são extensíveis: dispositivos Bluetooth, vídeo, Internet, teclado, mouse, rede, energia, sistema, sem fio (infravermelho).

### <a name="default-values"></a>Valores padrão

-   **As configurações em um item do painel de controle devem refletir o estado atual do recurso.** Caso contrário, seria enganoso e, possivelmente, resultaria em resultados indesejados. Por exemplo, se as configurações refletirem as recomendações, mas não o estado atual, os usuários poderão clicar em Cancelar em vez de fazer alterações, pensando que nenhuma alteração é necessária.
-   **Escolha o mais seguro (para evitar a perda de dados ou acesso ao sistema) e o estado inicial mais seguro.** Suponha que a maioria dos usuários não alterará as configurações.
-   **Se não houver fatores de segurança e segurança, escolha o estado inicial mais provável ou conveniente.**

## <a name="text"></a>Texto

### <a name="item-names"></a>Nomes de item

-   **Escolha um nome descritivo que se comunique claramente e diferencie o que o item do painel de controle faz.** A maioria dos nomes descreve o recurso do Windows ou o objeto que está sendo configurado e são exibidos no modo de exibição clássico do painel de controle home page.
-   **Não inclua as palavras "configurações", "opções", "Propriedades" ou "configuração" no nome.** Isso é implícito e deixá-lo desativado torna mais fácil para os usuários verificar.

    **Incorreto:**

    Opções de acessibilidade

    Configurações do modem

    Opções de Energia

    Opções regionais e de idioma

    **Correto:**

    Acessibilidade

    Modem

    Energia

    Idiomas e formatos regionais

    Nos exemplos corretos, palavras desnecessárias são removidas.

-   **Se o item do painel de controle configurar recursos relacionados, liste somente os recursos necessários para identificar o item e liste os recursos mais prováveis de serem reconhecidos ou usados primeiro.**

    **Incorreto:**

    Opções de Pasta

    Opções de telefone e modem

    **Correto:**

    Arquivos e pastas

    Modem

    Nos exemplos corretos, os recursos de item do painel de controle primário recebem ênfase.

-   Use [a capitalização de estilo de título](glossary.md).

### <a name="page-titles"></a>Títulos de página

**Observação:** Assim como acontece com todas as janelas do Explorer, os títulos das páginas do painel de controle são exibidos na [barra de endereços](glossary.md), mas não na barra de título.

-   **Para páginas de Hub, use o nome do item do painel de controle.**
-   **Para páginas do spoke, use um resumo conciso da finalidade da página.** Use a instrução principal da página se ela for concisa; caso contrário, use uma recondição concisa da instrução principal.

    ![captura de tela da caixa de diálogo opções de energia ](images/winenv-ctrl-panels-image6.png)

    Neste exemplo, as opções de energia são usadas para o título da página em vez da instrução principal.

-   Use a capitalização de estilo de título.

### <a name="task-link-text"></a>Texto do link da tarefa

As diretrizes a seguir se aplicam a links para páginas de tarefas, como links de tarefas da página de categorias e consulte também links.

-   **Escolha nomes de tarefas concisos que se comunicam e diferenciam claramente a tarefa.** Os usuários não devem ter que descobrir o que a tarefa realmente significa ou como ela difere de outras tarefas.

    **Incorreto:**

    Ajustar configurações de exibição

    **Correto:**

    Resolução da tela

    No exemplo correto, as palavras transmitem mais precisão.

-   **Manter uma linguagem semelhante entre links de tarefas e as páginas para as quais apontam.** Os usuários não devem ficar surpresos com a página que é exibida por um link.
-   **Para páginas de tarefas, crie a instrução principal, os botões de confirmação e os links de tarefa como um conjunto de texto relacionado.**

    **Exemplos:**

    

    |                              |                                                       |
    |------------------------------|-------------------------------------------------------|
    | Link da tarefa:<br/>        | Conectar a uma rede sem fio<br/>              |
    | Instrução principal:<br/> | Escolha uma rede à qual se conectar<br/>             |
    | Botão de confirmação:<br/>    | Conectar<br/>                                    |
    | Link da tarefa:<br/>        | Configurar controles dos pais<br/>                   |
    | Instrução principal:<br/> | Escolher um usuário e configurar controles dos pais<br/> |
    | Botão de confirmação:<br/>    | Aplicar controle dos pais<br/>                     |
    | Link da tarefa:<br/>        | Resolver os conflitos de sincronização<br/>                |
    | Instrução principal:<br/> | Como você deseja resolver esse conflito?<br/>  |
    | Botão de confirmação:<br/>    | Resolver<br/>                                    |

    

     

    Esses exemplos mostram a relação do texto do link da tarefa, a instrução principal e o texto do botão de confirmação.

-   Embora as tarefas geralmente comecem com verbos, **considere omitir o verbo nas páginas de categoria se for um verbo genérico relacionado à configuração que não ajuda a comunicar a tarefa.**

    **Verbos úteis específicos:**

    Adicionar

    Verificação

    Conectar

    Copiar

    Criar

    Excluir

    Desconectar

    Instalar

    Remover

    Configuração

    Iniciar

    Stop

    Solucionar problemas

    **Verbos genéricos, não auxiliares:**

    Ajustar

    Alteração

    Choose

    Configurar

    Editar

    Gerenciar

    Aberto

    Escolher

    Definir

    Selecionar

    Mostrar

    Visualizar

-   **Se a tarefa configurar vários recursos relacionados, liste apenas os recursos representativos do conjunto.** Omita os detalhes que podem ser prontamente inferidos.

    **Incorreto:**

    Volume do alto-falante, mudo, ícone de volume

    Palestrantes, microfones, MIDI e esquemas de som

    **Correto:**

    Volume do palestrante

    Alto-falantes e microfones

    Nos exemplos corretos, somente os recursos representativos são fornecidos no link de tarefa.

-   **Você deve formular tarefas em termos de tecnologia apenas se os usuários de destino também o fizerem.**

    **Incorreto:**

    Connectoids

    Profundidade de pixel

    dpi

    **Correto:**

    Impressoras

    Scanners

    Mouse

    Os exemplos corretos são termos baseados em tecnologia que os usuários de destino têm probabilidade de usar, enquanto os exemplos incorretos não são.

-   Use os substantivos do plural somente se o sistema puder dar suporte a mais de um.
-   Use [a capitalização no estilo de frase](glossary.md).
-   Não use pontuação final.

### <a name="main-instructions"></a>Instruções principais

-   **Para a página Hub, use a instrução principal para explicar o objetivo do usuário com o item do painel de controle.** A instrução principal deve ajudar os usuários a determinar se eles selecionaram o item do painel de controle correto. Tenha em mente que os usuários podem ter selecionado o item do painel de controle em erro e estão, na verdade, procurando configurações que fazem parte de outro item do painel de controle.

    **Exemplos:**

    Mantenha seu computador seguro e atualizado

    Otimize seu computador para que seja mais fácil ver, ouvir e controlar

-   **Para páginas do spoke, use a instrução principal para explicar o que fazer na página.** A instrução deve ser uma instrução específica, uma direção imperativa ou uma pergunta. Boas instruções comunicam o objetivo do usuário com a página em vez de se concentrar puramente na mecânica de manipulação.

    **Incorreto:**

    Escolha uma tarefa de notificação

    **Correto:**

    Indique como lidar com informações de entrada

    A versão correta comunica-se melhor ao objetivo obtido pela página.

-   **Use verbos específicos sempre que possível.** Verbos específicos são mais significativos para usuários do que os genéricos.
-   Use [a capitalização no estilo de frase](glossary.md).
-   **Não inclua os períodos finais se a instrução for uma instrução.** Se a instrução for uma pergunta, inclua um ponto de interrogação final.

### <a name="supplemental-instructions"></a>Instruções complementares

-   **Para a página Hub, use a instrução complementar opcional para explicar ainda mais a finalidade do item do painel de controle.**
-   **Para páginas do spoke, use a instrução complementar opcional para apresentar informações adicionais úteis para entender ou usar a página.** Você pode fornecer informações mais detalhadas e definir a terminologia.
-   Use frases completas e [maiúsculas e minúsculas no estilo da sentença](glossary.md).

### <a name="page-text"></a>Texto da página

-   **Não redeclare a instrução principal na área de conteúdo.**
-   **Use a palavra "página" para se referir à própria página.**
-   **Use a segunda pessoa (você, seu) para informar aos usuários o que fazer** na principal instrução e na área de conteúdo. Geralmente, a segunda pessoa está implícita.

    **Exemplo:**

    Escolha as imagens que você deseja imprimir.

-   **Use a primeira pessoa (I, eu, My) para permitir que os usuários informem ao item do painel de controle o que fazer** na área de conteúdo que responde à instrução principal.

    **Exemplo:**

    Imprima as fotos na minha câmera.

### <a name="task-links"></a>Links de tarefas

-   **Escolha um texto de link conciso que se comunique claramente e diferencie o que o link da tarefa faz.** Ele deve ser auto-explicativo e corresponder à instrução principal. Os usuários não devem ter que descobrir o que o link significa realmente ou como ele difere de outros links.
-   **Sempre inicie links de tarefa com um verbo.**
-   Use [a capitalização no estilo de frase](glossary.md).
-   Não use pontuação final.
-   **Se o link da tarefa exigir mais explicações, forneça a explicação em um controle de texto separado** usando frases completas e pontuação final. No entanto, adicione essas explicações somente quando necessário não adicione explicações a todos os links de tarefas porque outro link de tarefa precisa de um.

Para obter mais informações e exemplos, consulte [links](ctrl-command-links.md).

### <a name="commit-buttons"></a>Botões de confirmação

-   **Use rótulos de botão de confirmação específicos que façam sentido por conta própria e que correspondam à instrução principal.** Idealmente, os usuários não precisam ler mais nada para entender o rótulo. Os usuários têm muito mais probabilidade de ler rótulos de botão de comando do que texto estático.
-   **Sempre iniciar os rótulos do botão de confirmação com um verbo.**
-   **Não use fechar, concluído ou concluir.** Esses rótulos de botão são mais adequados para outros tipos de janelas.
-   Use [a capitalização no estilo de frase](glossary.md).
-   Não use pontuação final.
-   Atribua uma [chave de acesso](glossary.md)exclusiva.
    -   **Exceção:** Não atribua chaves de acesso para cancelar botões, pois ESC é sua chave de acesso. Isso torna as outras chaves de acesso mais fáceis de atribuir.

## <a name="documentation"></a>Documentação

Ao fazer referência às páginas do painel de controle home page ou da categoria:

-   Na documentação do usuário, consulte painel de controle, usando maiúsculas e minúsculas no estilo de título e omitindo um artigo definitivo anterior.

    **Exemplo:**

    No painel de controle, abra **central de segurança**.

-   Em programação e outras documentações técnicas, consulte o painel de controle home page e a página categoria do painel de controle, sem colocar em maiúscula qualquer uma das palavras. Um artigo definitivo anterior é opcional.

Para itens do painel de controle:

-   Ao fazer referência a um item de painel de controle individual, use " \[ nome \] do item do painel de controle no painel de controle" ou, geralmente, "item do painel de controle" na documentação do usuário. Não use o miniaplicativo, o programa ou o painel de controle para fazer referência a itens individuais do painel de controle.
-   Ao fazer referência a uma página de Hub do item do painel de controle, use a \[ página "nome do item do painel de controle principal \] ".
-   Quando possível, formate o nome do painel de controle usando texto em negrito. Caso contrário, coloque o nome entre aspas somente se necessário para evitar confusão.

Exemplos:

-   No painel de controle, abra **controles dos pais**.
-   Retorne à página de **controles pai** principal.

