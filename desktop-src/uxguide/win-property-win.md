---
title: Propriedades Windows
description: Janela de propriedades é o nome coletivo para os seguintes tipos de UIs (interfaces do usuário) Folha de propriedades usada para exibir e alterar propriedades de um objeto ou coleção de objetos em uma caixa de diálogo. Inspetor de propriedade usado para exibir e alterar propriedades de um objeto ou coleção de objetos em um painel. Caixa de diálogo Opções usada para exibir e alterar opções para um aplicativo.
ms.assetid: 18fc04da-9f84-4a44-9f3d-a9e29b121e7c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 73260459c1dc22ee488233f3c7edebe25203a811a430870fdd4e68e1c2e153ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594285"
---
# <a name="property-windows"></a>Propriedades Windows

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Janela de propriedades é o nome coletivo para os seguintes tipos de interfaces do usuário (UIs):

-   Folha de propriedades: usada para **exibir e alterar propriedades de um objeto ou coleção de objetos em uma caixa de diálogo**.
-   Inspetor de propriedade: usado para exibir e alterar propriedades de um **objeto ou coleção de objetos em um painel**.
-   Caixa de diálogo Opções: usada para **exibir e alterar opções para um aplicativo**.

Uma propriedade para um objeto é uma das seguintes:

-   Uma configuração que os usuários podem alterar (como o nome de um arquivo e o atributo somente leitura).
-   Um atributo de um objeto que os usuários não podem alterar diretamente (como o tamanho e a data de criação de um arquivo).

Ao contrário das caixas de diálogo (além de caixas de diálogo de opções) e assistentes, as janelas de propriedades normalmente suportam várias tarefas em vez de uma única tarefa.

As janelas de propriedades geralmente são organizadas em páginas, que são acessadas por meio de guias. As janelas de propriedades geralmente são associadas a guias (e vice-versa), mas as **guias não são essenciais para janelas de propriedades**.

![captura de tela da folha de propriedades do documento ](images/win-property-win-image1.png)

Uma folha de propriedades típica.

**Observação:** As diretrizes relacionadas [ao layout](vis-layout.md) e às guias são [apresentadas](ctrl-tabs.md) em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir, considere estas perguntas:

-   **Definir as propriedades exige que os usuários executem uma sequência de etapas fixa e não trivial?** Em caso afirmado, use [um assistente](win-wizards.md) [ou um fluxo de tarefas.](glossary.md)
-   **O conteúdo é exclusivamente as opções de um aplicativo?** Em caso afirmaivo, use uma caixa de diálogo de opções.
-   **O conteúdo é exclusivamente atributos de um aplicativo?** Em caso afirmado, use uma [caixa Sobre](glossary.md).
-   **O conteúdo é principalmente as propriedades de um objeto (suas configurações ou atributos)?** Caso não, use uma caixa de [diálogo padrão ou](win-dialog-box.md) a caixa de diálogo com [guias](glossary.md).
-   Os usuários **têm probabilidade de exibir ou alterar propriedades com frequência ou durante um longo período de tempo?** Se sim, use um inspetor de propriedade; caso contrário, use uma folha de propriedades.
-   Os usuários **têm probabilidade de exibir ou alterar as propriedades de vários objetos diferentes por vez?** Se sim, use um inspetor de propriedade; caso contrário, use uma folha de propriedades.

**As folhas de propriedades e os inspetores de propriedade não são exclusivos.** Você pode exibir as propriedades acessadas com mais frequência em um inspetor de propriedade e o conjunto completo na folha de propriedades.

## <a name="design-concepts"></a>Conceitos de design

**As janelas de propriedades geralmente se tornam um despejo para uma variedade ímpar de configurações baseadas em tecnologia de baixo nível.** Muitas vezes, essas propriedades são organizadas em guias, mas além disso, não são projetadas para tarefas ou usuários específicos. Como resultado, quando os usuários enfrentam uma tarefa em uma janela de propriedades, eles geralmente não sabem o que fazer.

Para garantir que as janelas de propriedades sejam úteis e úteis, siga estas etapas:

-   Certifique-se de que as propriedades sejam necessárias.
-   Apresentar propriedades em termos de metas do usuário, não tecnologia.
-   Apresentar propriedades no nível direito.
-   Criar páginas para tarefas específicas.
-   Criar páginas para usuários específicos, especialmente usuários limitados (não administradores).
-   Organize as páginas de propriedades com eficiência.

**Se você fizer apenas uma coisa...**

Apresentar propriedades em termos de metas do usuário, não tecnologia. Imagine que você está explicando a propriedade e por que ela é útil para um amigo. Como você explica isso? Qual idioma você usaria? Esse é o idioma a ser usado em suas páginas de propriedades.

## <a name="usage-patterns"></a>Padrões de uso

As janelas de propriedades têm vários padrões de uso.

-   Folhas de propriedades. As propriedades de um único objeto são exibidas em uma caixa de diálogo sem modo.
-   Folhas de propriedades de vários objetos. As propriedades de vários objetos são exibidas em uma caixa de diálogo sem modo.
-   Folhas de propriedades de configurações efetivas. As propriedades efetivas de um único objeto são exibidas em uma caixa de diálogo sem modo.
-   Caixas de diálogo Opções. As propriedades de um aplicativo são exibidas em uma caixa de diálogo modal.
-   Inspetores de propriedade. As propriedades da seleção atual (um único objeto ou grupo de objetos) são exibidas em um painel de janela sem modo ou janela desencaixada.

Todos os padrões de janela de propriedades, exceto inspetores de propriedade, usam uma commit atrasada, o que significa que as alterações só são efetivadas quando os usuários clicam em OK ou Aplicar. Os inspetores de propriedade usam uma commit imediata (as propriedades são alteradas assim que os usuários fazem alterações), portanto, não há necessidade de botões OK, Cancelar e Aplicar.

## <a name="guidelines"></a>Diretrizes

### <a name="property-sheets"></a>Folhas de propriedade

-   **Exibir uma folha de propriedades quando os usuários:**
    -   Selecione o comando Propriedades para um objeto .
    -   De definir o foco de entrada em um objeto e pressione Alt+Enter.

**Folhas de propriedades de vários objetos**

-   **Exibe as propriedades comuns de todos os objetos selecionados.** Quando os valores de propriedade diferem, exibe os controles associados a esses valores usando um estado misto. (Consulte as respectivas diretrizes de controle para usar valores de estado misto.)
-   Se o objeto selecionado for uma coleção de vários objetos discretos (como uma pasta de arquivo), exibirá as propriedades do objeto agrupado único em vez de uma folha de propriedades de vários objetos para os **objetos discretos.**

### <a name="options-dialog-boxes"></a>Caixas de diálogo Opções

-   **Não separe as opções da personalização.** Ou seja, não têm um comando Options e um comando Personalizar. Os usuários geralmente ficam confusos com essa separação. Em vez disso, acesse a personalização por meio de opções.

### <a name="property-pages"></a>Páginas de propriedades

-   **Siga estas diretrizes para a ordem da página:**
    -   Tornar a página Geral ou seu equivalente à primeira página.
    -   Tornar a página Avançado ou seu equivalente à última página.
    -   Para as páginas restantes:
        -   Organize-os em grupos de páginas relacionadas.
        -   Ordenar os grupos pela probabilidade de seu uso.
        -   Em cada grupo, ordenar as páginas por suas relações ou pela probabilidade de seu uso.
        -   Você não deve ter tantas páginas que precise exibi-las em ordem alfabética.
-   **Tornar as páginas coerentes relacionando todas as propriedades em cada página a uma única finalidade específica e baseada em tarefas.**
-   **Se o espaço permitir, explique a finalidade da janela de propriedades na parte superior da página se não for óbvio para os usuários de destino.** Se a página for usada para executar apenas uma única tarefa, frase o texto como uma **instrução clara** sobre como executar essa tarefa . Use frases completas, terminando com um ponto final.

    ![captura de tela da folha de propriedades do firewall ](images/win-property-win-image2.png)

    Neste exemplo, a finalidade do Firewall Windows Microsoft é explicada na parte superior da página Geral.

-   **Tornar conteúdo semelhante consistente entre páginas usando nomes e locais de controle consistentes.** Por exemplo, se várias páginas têm caixas Nome, tente coloque-as no mesmo local na página e use rótulos consistentes. Conteúdo semelhante não deve ser ressalto de página em página.
-   **Coloque a mesma propriedade na mesma página em todo o aplicativo.** Por exemplo, não coloque uma propriedade Expiration na guia Geral para um tipo de objeto e na guia Avançado para outro tipo.
-   **Se for provável que os usuários comecem com a última página exibida, faça com que a guia da página persista e selecione-a por padrão.** Faça com que as configurações persistam em uma janela por propriedade, por usuário. Caso contrário, selecione a primeira página por padrão.
-   **Não faça com que as configurações em uma página dependam das configurações em outras páginas.** Coloque as configurações dependentes em uma única página. Alterar uma configuração em uma página nunca deve alterar automaticamente as configurações em outras páginas.
    -   **Exceção:** Se as configurações dependentes estão em duas janelas de propriedades diferentes, use rótulos de texto estático para explicar essa relação em ambos os locais.
-   **Não role páginas de propriedades.** As guias e as barras de rolagem são usadas para aumentar a área efetiva de uma janela, mas um mecanismo deve ser suficiente. Em vez de usar barras de rolagem, faça com que as páginas de propriedades maiores e desemitam as páginas com eficiência.

**Primeiras páginas**

-   Para propriedades de objeto, **coloque o nome do objeto na primeira página.**
-   Se você estiver associando [ícones (opcionais)](vis-icons.md) aos seus objetos, **exibirá** o ícone apropriado no canto superior esquerdo da primeira página.

**Páginas gerais**

-   **Evite páginas gerais.** Você não precisa ter uma página Geral. Use uma página Geral somente se:
    -   As propriedades se aplicam a várias tarefas e são significativas para a maioria dos usuários. Não coloque propriedades especializadas ou avançadas em uma página Geral, mas você pode torná-las acessíveis por meio de um botão de comando na página Geral.
    -   As propriedades não se ajustam a uma categoria mais específica. Se fizerem isso, use esse nome para a página.

**Páginas avançadas**

-   **Evite páginas avançadas.** Use uma página Avançado somente se:
    -   As propriedades se aplicam a tarefas incomuns e são significativas principalmente para usuários avançados.
    -   As propriedades não se ajustam a uma categoria mais específica. Se fizerem isso, use esse nome para a página.
-   **Não chame propriedades avançadas com base apenas em medidas tecnológicas.** Por exemplo, uma opção de preparação de impressora pode ser um recurso avançado de impressora, mas é significativa para todos os usuários, portanto, ela não deve estar em uma página Avançado.

### <a name="owned-property-windows"></a>Janelas de propriedade de propriedade

-   **Não exibir mais de uma janela de propriedade de uma janela de propriedade.** Exibir mais de um torna difícil entender o significado dos botões OK e Cancelar. Você pode exibir outros tipos de caixas de diálogo auxiliares (como seladores de objeto) conforme necessário.

    **Incorreto:**

    ![captura de tela de três janelas de propriedade ](images/win-property-win-image3.png)

    Neste exemplo, a caixa de diálogo opções de proprietário tem três níveis de janelas de propriedade. Como resultado, os significados de OK e Cancelar são confusos.

-   Para janelas de propriedades que usam um modelo de confirmação atrasada, certifique-se de que os usuários possam cancelar as alterações feitas em uma janela de propriedade de propriedade clicando em Cancelar **na janela do proprietário.**
-   Se uma janela de propriedade de propriedade exigir uma confirmação imediata, indique que as alterações foram confirmadas renomeando o botão Cancelar na janela **do proprietário para Fechar.** Reverta o botão de volta para Cancelar se o usuário clicar em Aplicar.

    ![captura de tela da janela de propriedades com ok e close ](images/win-property-win-image4.png)

    Neste exemplo, as alterações em dicionários personalizados e configurações de gramática não podem ser canceladas. Você pode dar aos usuários esse comentário alterando Cancelar para Fechar.

**Outras janelas de propriedade**

-   Se uma janela de propriedade for usada para executar uma tarefa auxiliar, **não renomeie o botão Cancelar.** As diretrizes anteriores se aplicam somente a janelas de propriedades de propriedade, não caixas de diálogo usadas para executar tarefas auxiliares.

    ![captura de tela da janela do proprietário e limpeza do disco ](images/win-property-win-image5.png)

    Neste exemplo, a Limpeza de Disco é uma tarefa auxiliar, portanto, as diretrizes anteriores não se aplicam. Por exemplo, o botão Cancelar na janela do proprietário não deve ser alterado para Fechar.

-   Se a janela de propriedade for usada para executar uma tarefa auxiliar, não feche a janela de propriedades do proprietário quando o botão **de comando for clicado.** Fazer isso é um problema e pressu que o único motivo pelo qual o usuário exibiu a janela de propriedades era executar esse comando.

    **Incorreto:**

    ![captura de tela da caixa de diálogo opções ](images/win-property-win-image6.png)

    Neste exemplo, clicar em **Proteger documento fecha** incorretamente a caixa de diálogo Opções.

### <a name="tabs"></a>Guias

-   **Use rótulos de guia concisos.** Use uma ou duas palavras que descrevem claramente o conteúdo da página. Rótulos mais longos resultam em um uso ineficiente do espaço na tela, especialmente quando os rótulos são localizados.
-   **Use rótulos de tabulação específicos e significativos.** Evite rótulos de guia genéricos que podem ser aplicados a qualquer guia, como Geral, Avançado ou Configurações.
-   **Use guias horizontais se:**
    -   A janela de propriedades tem sete ou menos guias (incluindo extensões de terceiros).
    -   **Todas as guias se ajustam em uma linha, mesmo quando a interface do usuário é localizada.**
    -   Você usa guias horizontais nas outras janelas de propriedades em seu aplicativo.
-   **Use guias verticais se:**

    -   A janela de propriedades tem oito ou mais guias (incluindo extensões de terceiros).
    -   **O uso de guias horizontais exigiria mais de uma linha.**
    -   Você usa guias verticais nas outras janelas de propriedades em seu aplicativo.

    ![captura de tela da janela de propriedades com guias verticais ](images/win-property-win-image7.png)

    Neste exemplo, as guias verticais são usadas para acomodar oito ou mais guias.

-   **Para inspetores de propriedade, para conservar espaço,** considere usar uma lista de listas em vez de guias , especialmente se a guia atual raramente for alterada pelo usuário.
-   **Se uma guia não se aplicar ao contexto atual e** os usuários não esperarem, remova a guia. Isso simplifica a interface do usuário e os usuários não a perderão.

    **Incorreto:**

    ![captura de tela da guia locais de arquivo esmaecida ](images/win-property-win-image8.png)

    Neste exemplo, a guia Locais de Arquivo está desabilitada incorretamente quando Microsoft Word 2003 é usado como um editor de email. A página deve ser removida porque os usuários não esperam exibir ou alterar locais de arquivo nesse contexto.

-   **Se uma guia não se aplicar ao contexto atual e os usuários esperarem:**

    -   **Exibir a guia.**
    -   **Desabilite os controles na página.**
    -   **Inclua texto explicando por que os controles estão desabilitados.**

    Não desabilite a guia porque isso não é autoexplicativo e proíbe a exploração. Além disso, os usuários que procuram uma propriedade específica seriam forçados a procurar em todas as outras guias.

    ![captura de tela de controles de exibição esmaecida ](images/win-property-win-image9.png)

    Neste exemplo do Word 2003, nenhuma das opções de Exibição se aplica ao Layout de Leitura. No entanto, os usuários podem esperar que eles se apliquem com base no rótulo da guia, portanto, a página é exibida, mas as opções estão desabilitadas.

-   **Não atribua efeitos à alteração de guias.** Alterar a guia atual nunca deve ter efeitos colaterais, aplicar configurações ou resultar em uma mensagem de erro.
-   **Não aninhar guias ou combinar guias horizontais com guias verticais.** Em vez disso, reduza o número de guias, use apenas guias verticais ou use outro controle, como uma lista lista listada.
-   **Não use guias se uma janela de propriedade tiver apenas uma única guia e não for extensível.** Use uma caixa de diálogo regular com OK, Cancelar e um botão Aplicar opcional. Janelas de propriedades extensíveis (que podem ser estendidas por terceiros) sempre precisam usar guias.
-   **Não coloque ícones em guias.** Os ícones geralmente adicionam desorganização visual desnecessária, consomem espaço na tela e geralmente não melhoram a compreensão do usuário. Adicione apenas ícones que auxiliam na compreensão, como símbolos padrão.

    **Incorreto:**

    ![captura de tela de rótulos de guia com ícones ](images/win-property-win-image10.png)

    Neste exemplo, os gráficos adicionam desorganização visual desnecessária e fazem pouco para melhorar a compreensão do usuário.

-   **Não use logotipos de produtos para gráficos de tabulação.** As guias não são para identidade visual.
-   **Não role as guias horizontais.** A rolagem horizontal não é prontamente descoberta. No entanto, você pode rolar guias verticais.

    **Incorreto:**

    ![captura de tela do rótulo de guia horizontal truncada ](images/win-property-win-image11.png)

    Neste exemplo, as guias horizontais são roladas.

### <a name="command-buttons"></a>Botões de comando

-   **Coloque os botões de comando que se aplicam a todas as páginas de propriedades na parte inferior da janela de propriedades.** Alinhe os botões com a direita e use essa ordem (da esquerda para a direita): OK, Cancelar e Aplicar.
-   **Coloque botões de comando que se aplicam somente a páginas de propriedades individuais diretamente na página de propriedades.**

### <a name="commit-buttons"></a>Botões de commit

**Botões OK**

-   **Para janelas de propriedades do proprietário, o botão OK significa aplicar as alterações pendentes (feitas desde que a janela foi aberta ou a última Aplicar) e fechar a janela.**
-   **Para janelas de propriedade própria, o botão OK significa manter as alterações, fechar a janela e aplicar as alterações quando as alterações da janela do proprietário são aplicadas.**
-   **Não renomeie o botão OK.** Ao contrário de outras caixas de diálogo, as janelas de propriedades não são usadas para executar nenhuma tarefa específica. Se fizer sentido renomear o botão OK (para Imprimir, por exemplo), a janela não será uma janela de propriedade.
-   **Não atribua uma chave de acesso.**

**Botões Cancelar**

-   **O botão Cancelar significa descartar todas as alterações pendentes (feitas desde que a janela foi aberta ou a última Aplicar) e fechar a janela.**
-   **Se todas as alterações pendentes não puderem ser abandonadas, renomeie o botão Cancelar para Fechar.** Clicar em Cancelar deve abandonar todas as alterações pendentes.
-   **Se a janela de propriedade de propriedade exigir uma confirmação imediata, renomeie o botão Cancelar na janela do proprietário para Fechar para mostrar que as alterações foram confirmados.**
-   **Não atribua uma chave de acesso.**

**Aplicar botões**

-   **Para folhas de propriedades do proprietário, o botão Aplicar significa aplicar as alterações pendentes (feitas desde que a janela foi aberta ou a última Aplicar), mas deixe a janela aberta.** Isso permite que os usuários avaliem as alterações antes de fechar a folha de propriedades.
-   **Para folhas de propriedades de propriedade, não use.** Usar um botão Aplicar em uma folha de propriedades de propriedade torna difícil entender o significado dos botões de confirmação na folha de propriedades do proprietário.
-   **Forneça um botão Aplicar somente se a folha de propriedades tiver configurações (pelo menos uma) com efeitos que os usuários podem avaliar de maneira significativa.** Normalmente, os botões Aplicar são usados quando as configurações fazem alterações visíveis. Os usuários devem ser capazes de aplicar uma alteração, avaliar a alteração e fazer outras alterações com base nessa avaliação. Caso contrário, remova o botão Aplicar em vez de desabilitá-lo.

    **Incorreto:**

    ![captura de tela das propriedades do sistema com o botão Aplicar ](images/win-property-win-image12.png)

    Neste exemplo, nenhuma das propriedades do sistema tem um efeito visual, portanto, o botão Aplicar não tem valor e deve ser removido.

-   **Coloque todas as configurações que os usuários podem querer aplicar em páginas de proprietário.** Não use os botões Aplicar em folhas de propriedades de propriedade, pois isso é confuso.
-   **Use Aplicar botões somente com folhas de propriedades, não com caixas de diálogo opções.**
-   **Habilita o botão Aplicar somente quando houver alterações pendentes;** caso contrário, desabilite-o.
-   **Atribua "A" como a chave de acesso.**

**Fechar botões**

-   **Se todas as alterações pendentes não puderem ser abandonadas, renomeie o botão Cancelar para Fechar.** Clicar em Cancelar deve abandonar todas as alterações pendentes.
-   **Não confirme se os usuários descartam as alterações.**
    -   **Exceção:** Se [a](mess-confirm.md) janela de propriedades tiver configurações que exigem esforço significativo para definir e o usuário tiver feito alterações, você poderá exibir uma confirmação se o usuário clicar no botão Fechar na barra de título. O motivo é que alguns usuários assumem por engano que o botão Fechar na barra de título tem o mesmo efeito que o botão OK.
-   **Com exceção da mensagem de confirmação, certifique-se de que o botão Fechar na barra de título tenha o mesmo efeito que Cancelar ou Fechar.**

### <a name="page-contents"></a>Conteúdo da página

-   **Certifique-se de que as propriedades sejam necessárias.** Não atrapalha suas páginas com propriedades desnecessárias apenas para evitar tomar decisões de design difíceis.
-   **Apresentar propriedades em termos de metas do usuário, não tecnologia.** Só porque uma propriedade configura uma tecnologia específica não significa que você deve apresentar a propriedade em termos dessa tecnologia.
    -   Se você precisa apresentar configurações em termos de tecnologia (talvez porque os usuários reconheçam o nome da tecnologia), inclua uma breve descrição de como o usuário se beneficia dessa configuração.
-   **Apresentar propriedades no nível direito.** Você não precisa apresentar configurações individuais de baixo nível em uma página de propriedades, portanto, apresente as propriedades em um nível que faça sentido para os usuários.
-   **Criar páginas de propriedades para tarefas específicas.** Determine as tarefas que os usuários executarão e certifique-se de que haja um caminho claro para executar essas tarefas.
-   **Organize as páginas de** propriedades com eficiência reduzindo o número de guias, decidindo o que acontece em uma página com base no grupo lógico e na coerência e simplificando a apresentação da página.

<!-- -->

-   **Se uma opção for altamente recomendada, considere adicionar "(recomendado)" ao rótulo.**
-   **Forneça um botão de comando Restaurar Padrões para uma página de propriedades ou toda a janela de propriedades quando:**

    -   É provável que os usuários considerem as configurações complexas e difíceis de entender.
    -   Ter configurações incorretas pode resultar em uma funcionalidade de quebra, mas os padrões podem restaurar a funcionalidade.
    -   É mais fácil para os usuários começar de novo quando o objeto está configurado incompatibilidade.

    ![captura de tela da guia com o botão restaurar padrões ](images/win-property-win-image13.png)

    Neste exemplo, as configurações Windows firewall são complexas e podem resultar em funcionalidades interrompidas. Se houver um problema, geralmente é mais fácil para os usuários começar de novo clicando em Restaurar Padrões.

-   Confirme o comando Restaurar Padrões se seu efeito não for óbvio ou se as configurações são complexas. Indique a confirmação usando [reellipses](ctrl-command-buttons.md).
-   **Quando apropriado, exibe uma visualização dos resultados de uma configuração.**

    ![captura de tela de exemplos de ponteiro de propriedades do mouse ](images/win-property-win-image14.png)

    Neste exemplo, a página exibe uma visualização dos esquemas de ponteiro. Embora clicar em Aplicar também mostre uma versão prévia, ter uma visualização na página é mais eficiente para os usuários.

    ![captura de tela da visualização dos resultados das configurações de fonte ](images/win-property-win-image15.png)

    Neste exemplo, a caixa Visualização mostra os resultados das configurações de fonte. Este exemplo mostra que você pode visualizar configurações que não são gráficas.

### <a name="help"></a>Ajuda

-   Ao fornecer assistência ao usuário, **considere usar as seguintes opções** (listadas em sua ordem de preferência):
    -   Dê rótulos autoexplicativos a controles interativos. Os usuários têm maior probabilidade de ler os rótulos em controles interativos do que em qualquer outro texto.
    -   Forneça explicações no contexto usando rótulos de texto estático.
    -   Forneça um [link específico](ctrl-links.md) para um tópico de Ajuda relevante.
-   **Localize os links da Ajuda na parte inferior de cada página.** Se uma página tiver vários grupos distintos de configurações que têm um tópico de Ajuda (talvez dentro das caixas de grupo), localize o link Ajuda na parte inferior do grupo.
-   **Não use links gerais ou de tópicos da Ajuda ou botões de Ajuda genéricos.** Os usuários geralmente ignoram a Ajuda genérica.

Para obter mais informações e exemplos, consulte [Ajuda](winenv-help.md).

### <a name="standard-users-and-protected-administrators"></a>Usuários padrão e administradores protegidos

**Muitas configurações exigem privilégios de administrador para alteração.** Se um processo exigir privilégios de administrador, [](glossary.md) Windows e posteriores exigirão que usuários Padrão e Administradores [protegidos](glossary.md) elevem seus privilégios explicitamente. Isso ajuda a impedir que código mal-intencionado seja executado com privilégios de administrador.

Para obter mais informações e exemplos, consulte [Controle de Conta de Usuário](winenv-uac.md).

### <a name="default-values"></a>Valores padrão

-   **As configurações em uma janela de propriedade devem refletir o estado atual do aplicativo, objeto ou coleção de objetos.** Fazer o contrário seria enganoso e possivelmente levar a resultados indesejáveis. Por exemplo, se as configurações refletirem as recomendações, mas não o estado atual, os usuários poderão clicar em Cancelar em vez de fazer alterações, pensando que nenhuma alteração é necessária.
-   **Escolha o mais seguro (para evitar perda de dados ou acesso ao sistema) e o estado inicial mais seguro.** Suponha que a maioria dos usuários não altere as configurações.
-   **Se a segurança e a segurança não são fatores, escolha o estado inicial mais provável ou conveniente.**

## <a name="text"></a>Texto

### <a name="commands"></a>Comandos

-   Para exibir as opções do programa, use "Opções".
-   Para exibir a janela de propriedades de um objeto, use "Propriedades".
-   Para exibir um resumo das configurações de personalização de programa comumente usadas, use "[Personalizar](glossary.md)."
-   Não use "Configurações" ou "Preferências".
-   Não use re [elipses para](ctrl-command-buttons.md) esses comandos.

### <a name="property-sheet-titles"></a>Títulos da folha de propriedades

-   Para um único objeto, use " \[ propriedades de nome de \] objeto".
    -   Se o objeto não tiver nome, use o nome do tipo do objeto. (Por exemplo, Propriedades da Conta de Usuário.)
-   Para vários objetos, use " \[ first object name , \] ... Propriedades."
    -   Se os objetos não têm nomes, use o nome do tipo dos objetos. (Por exemplo, Propriedades de Contas de Usuário.)
    -   Se os objetos têm tipos diferentes, use "Propriedades de Seleção".
-   Use [a capitalização de estilo de título](glossary.md).
-   Não use pontuação final.
-   Não use hifens, como " \[ nome do objeto – \] Propriedades".

### <a name="property-inspector-titles"></a>Títulos do inspetor de propriedade

-   Use "Propriedades".
-   Use a capitalização de estilo de título.
-   Não use pontuação final.

### <a name="options-dialog-box-titles"></a>Títulos da caixa de diálogo Opções

-   Use "Opções".
-   Use a capitalização de estilo de título.
-   Não use pontuação final.

### <a name="property-page-tab-names"></a>Nomes de guias da página de propriedades

-   **Use rótulos de guia concisos.** Use uma ou duas palavras que descrevem claramente o conteúdo da página. O uso de nomes de tabulação mais longos resulta em um uso ineficiente do espaço na tela, especialmente quando os nomes de tabulação são localizados.
-   **Use rótulos de tabulação específicos e significativos.** Evite rótulos de guia genéricos que podem ser aplicados a qualquer guia, como Geral, Avançado ou Configurações.
-   Escreva o rótulo como uma frase de uma ou duas palavras e não use nenhuma pontuação final.
-   Use [a capitalização de estilo de frase](glossary.md).
-   Não atribua uma chave de [acesso exclusiva.](glossary.md)

### <a name="property-page-text"></a>Texto da página de propriedades

-   Evite grandes blocos de texto.
-   Forneça espaço suficiente para o texto expandir 30% se ele for localizado.
-   Não use texto formulado como um comando nas janelas de propriedades. Como os usuários podem querer simplesmente exibir as configurações, você não deseja solicitar que eles alterem as configurações.
-   Use a capitalização de estilo de frase e a pontuação final.

## <a name="documentation"></a>Documentação

Ao fazer referência às janelas de propriedades:

-   Na programação e em outras documentações técnicas, consulte folhas de propriedades e caixas de diálogo de opções como folhas de propriedades. Em qualquer outro lugar, use a caixa de diálogo, especialmente na documentação do usuário.
-   Use o texto de título exato, incluindo sua capitalização.
-   Para descrever a interação do usuário, use abrir e fechar.
-   Quando possível, forja o título usando texto em negrito. Caso contrário, coloque o título entre aspas somente se necessário para evitar confusão.

Ao fazer referência a páginas de propriedades:

-   Na programação e em outras documentações técnicas, consulte páginas de propriedades como páginas de propriedades. Em qualquer outro lugar, use a guia, especialmente na documentação do usuário.
-   Use o texto de título exato, incluindo sua capitalização.
-   Para descrever a interação do usuário, use clique para se referir a clicar em uma guia.
-   Quando possível, forja o nome usando texto em negrito. Caso contrário, coloque o nome entre aspas somente se necessário para evitar confusão.

 

 