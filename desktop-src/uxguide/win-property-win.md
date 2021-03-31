---
title: Janelas de propriedades
description: A janela de propriedades é o nome coletivo para os seguintes tipos de folha de propriedades de interfaces do usuário (UIs) usado para exibir e alterar propriedades de um objeto ou coleção de objetos em uma caixa de diálogo. O Inspetor de propriedades usado para exibir e alterar as propriedades de um objeto ou de uma coleção de objetos em um painel. Opções caixa de diálogo usadas para exibir e alterar as opções de um aplicativo.
ms.assetid: 18fc04da-9f84-4a44-9f3d-a9e29b121e7c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c255d638f236b4bc4a4f1a6c923eac24421cfe9d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103663727"
---
# <a name="property-windows"></a>Janelas de propriedades

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

A janela de propriedades é o nome coletivo para os seguintes tipos de interfaces de usuário (UIs):

-   Folha de propriedades: usada para **Exibir e alterar as propriedades de um objeto ou de uma coleção de objetos em uma caixa de diálogo**.
-   Inspetor de propriedades: usado para **Exibir e alterar as propriedades de um objeto ou de uma coleção de objetos em um painel**.
-   Caixa de diálogo opções: usada para **Exibir e alterar as opções de um aplicativo**.

Uma propriedade para um objeto é uma das seguintes:

-   Uma configuração que os usuários podem alterar (como o nome de um arquivo e o atributo somente leitura).
-   Um atributo de um objeto que os usuários não podem alterar diretamente (como o tamanho de um arquivo e a data de criação).

Ao contrário das caixas de diálogo (diferente de opções de caixa de diálogo) e assistentes, as janelas de propriedades normalmente dão suporte a várias tarefas em vez de uma única tarefa.

As janelas de propriedades geralmente são organizadas em páginas, que são acessadas por meio de guias. As janelas de propriedades geralmente são associadas a guias (e vice-versa), mas as **guias não são essenciais para janelas de propriedades**.

![captura de tela da folha de propriedades propriedades do documento ](images/win-property-win-image1.png)

Uma folha de propriedades típica.

**Observação:** As diretrizes relacionadas ao [layout](vis-layout.md) e às [guias](ctrl-tabs.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

-   **A definição das propriedades exige que os usuários executem uma sequência de etapas fixa e não trivial?** Nesse caso, use um [Assistente](win-wizards.md) ou [fluxo de tarefas](glossary.md) em vez disso.
-   **O conteúdo é apenas as opções de um aplicativo?** Nesse caso, use uma caixa de diálogo opções.
-   **O conteúdo é apenas os atributos de um aplicativo?** Nesse caso, use uma [caixa sobre](glossary.md).
-   **O conteúdo é principalmente as propriedades de um objeto (suas configurações ou atributos)?** Caso contrário, use um [caixa de diálogo](win-dialog-box.md) padrão ou caixa de [diálogo com guias](glossary.md).
-   Os usuários **provavelmente exibirão ou alterarão Propriedades com frequência ou por um longo período de tempo?** Nesse caso, use um inspetor de propriedades; caso contrário, use uma folha de propriedades.
-   Os usuários **provavelmente exibirão ou alterarão Propriedades de vários objetos diferentes por vez?** Nesse caso, use um inspetor de propriedades; caso contrário, use uma folha de propriedades.

**Folhas de propriedades e inspetores de propriedades não são exclusivos.** Você pode exibir as propriedades acessadas com mais frequência em um inspetor de propriedades e o conjunto completo na folha de propriedades.

## <a name="design-concepts"></a>Conceitos de design

**As janelas de propriedades geralmente se tornam uma base de despejo para uma variedade estranha de configurações baseadas em tecnologia de baixo nível.** Muitas vezes, essas propriedades são organizadas em guias, mas além daquelas não projetadas para tarefas ou usuários específicos. Como resultado, quando os usuários enfrentam uma tarefa em uma janela de propriedades, eles geralmente não sabem o que fazer.

Para garantir que suas janelas de propriedades sejam úteis e utilizáveis, siga estas etapas:

-   Verifique se as propriedades são necessárias.
-   Apresente as propriedades em termos de metas do usuário, e não da tecnologia.
-   Apresente as propriedades no nível certo.
-   Páginas de design para tarefas específicas.
-   Páginas de design para usuários específicos, especialmente usuários limitados (não administradores).
-   Organize as páginas de propriedades com eficiência.

**Se você fizer apenas uma coisa...**

Apresente as propriedades em termos de metas do usuário, e não da tecnologia. Finja que você está explicando a propriedade e por que ela é útil para um amigo. Como você o explicaria? Qual linguagem você usaria? Esse é o idioma a ser usado em suas páginas de propriedades.

## <a name="usage-patterns"></a>Padrões de uso

As janelas de propriedades têm vários padrões de uso.

-   Folhas de propriedades. As propriedades de um único objeto são exibidas em uma caixa de diálogo sem janela restrita.
-   Folhas de propriedades de vários objetos. As propriedades de vários objetos são exibidas em uma caixa de diálogo sem janela restrita.
-   Folhas de propriedades de configurações efetivas. As propriedades efetivas de um único objeto são exibidas em uma caixa de diálogo sem janela restrita.
-   Caixas de diálogo de opções. As propriedades de um aplicativo são exibidas em uma caixa de diálogo modal.
-   Inspetores de propriedades. As propriedades da seleção atual (um único objeto ou grupo de objetos) são exibidas em um painel de janela não restrita ou em janela desencaixada.

Todos os padrões de janela de propriedade, exceto inspetores de propriedade, usam uma confirmação atrasada, o que significa que as alterações entram em vigor somente quando os usuários clicam em OK ou Os inspetores de Propriedades usam uma confirmação imediata (as propriedades são alteradas assim que os usuários fazem alterações), portanto, não há necessidade de botões OK, cancelar e aplicar.

## <a name="guidelines"></a>Diretrizes

### <a name="property-sheets"></a>Folhas de propriedade

-   **Exibir uma folha de propriedades quando os usuários:**
    -   Selecione o comando Propriedades de um objeto.
    -   Defina o foco de entrada em um objeto e pressione Alt + Enter.

**Folhas de propriedades de objetos múltiplos**

-   **Exibe as propriedades comuns de todos os objetos selecionados.** Quando os valores de propriedade forem diferentes, exiba os controles associados a esses valores usando um estado misto. (Consulte as respectivas diretrizes de controle para usar valores de estado misto.)
-   Se o objeto selecionado for uma coleção de vários objetos discretos (como uma pasta de arquivo), **exiba as propriedades do único objeto agrupado em vez de uma folha de propriedades de vários objetos para os objetos discretos.**

### <a name="options-dialog-boxes"></a>Caixas de diálogo de opções

-   **Não separe as opções de personalização.** Ou seja, não têm um comando de opções e um comando de personalização. Os usuários costumam confundir essa separação. Em vez disso, acesse a personalização por meio de opções.

### <a name="property-pages"></a>Páginas de propriedades

-   **Siga estas diretrizes para a ordem de página:**
    -   Torne a página Geral ou sua equivalente à primeira página.
    -   Torne a página avançado ou seu equivalente à última página.
    -   Para as páginas restantes:
        -   Organize-os em grupos de páginas relacionadas.
        -   Ordene os grupos pela probabilidade de seu uso.
        -   Dentro de cada grupo, ordene as páginas por suas relações ou pela probabilidade de seu uso.
        -   Você não deve ter tantas páginas que precise exibi-las em ordem alfabética.
-   **Torne as páginas coerentes relacionando todas as propriedades em cada página a uma finalidade única, específica e baseada em tarefa.**
-   **Se o espaço permitir, explique a finalidade da janela de propriedades na parte superior da página, caso não seja óbvio para os usuários de destino.** Se a página for usada para executar apenas uma única tarefa, **frase o texto como uma instrução clara sobre como executar essa tarefa**. Use frases completas, terminando com um ponto.

    ![captura de tela da folha de propriedade Propriedades do firewall ](images/win-property-win-image2.png)

    Neste exemplo, a finalidade do firewall do Microsoft Windows é explicada na parte superior da página geral.

-   **Torne conteúdo semelhante consistente nas páginas usando nomes de controle e locais consistentes.** Por exemplo, se várias páginas tiverem caixas de nome, tente colocá-las no mesmo local na página e usar rótulos consistentes. O conteúdo semelhante não deve saltar de uma página para uma página.
-   **Coloque a mesma propriedade na mesma página em todo o aplicativo.** Por exemplo, não coloque uma propriedade de expiração na guia geral para um tipo de objeto e, na guia Avançado, para outro tipo.
-   **Se os usuários provavelmente começarem com a última página exibida, faça com que a guia de página persista e selecione-a por padrão.** Fazer com que as configurações persistam em uma janela por propriedade, por usuário. Caso contrário, selecione a primeira página por padrão.
-   **Não faça as configurações em uma página dependente das configurações em outras páginas.** Em vez disso, coloque as configurações dependentes em uma única página. A alteração de uma configuração em uma página nunca deve alterar automaticamente as configurações em outras páginas.
    -   **Exceção:** Se as configurações dependentes estiverem em duas janelas de propriedades diferentes, use rótulos de texto estáticos para explicar essa relação em ambos os locais.
-   **Não role as páginas de propriedades.** As guias e as barras de rolagem são usadas para aumentar a área efetiva de uma janela, mas um mecanismo deve ser suficiente. Em vez de usar barras de rolagem, torne as páginas de propriedades maiores e deite as páginas com eficiência.

**Primeiras páginas**

-   Para propriedades de objeto, **Coloque o nome do objeto na primeira página.**
-   Se você estiver associando [ícones](vis-icons.md) (opcionais) a seus objetos, **exiba o ícone apropriado no canto superior esquerdo** da primeira página.

**Páginas gerais**

-   **Evite páginas gerais.** Não é necessário ter uma página geral. Use uma página Geral somente se:
    -   As propriedades se aplicam a várias tarefas e são significativas para a maioria dos usuários. Não coloque propriedades especializadas ou avançadas em uma página geral, mas você pode torná-las acessíveis por meio de um botão de comando na página geral.
    -   As propriedades não se ajustam a uma categoria mais específica. Em vez disso, use esse nome para a página.

**Páginas avançadas**

-   **Evite páginas avançadas.** Use uma página avançada somente se:
    -   As propriedades se aplicam a tarefas não comuns e são significativas principalmente para usuários avançados.
    -   As propriedades não se ajustam a uma categoria mais específica. Em vez disso, use esse nome para a página.
-   **Não chame Propriedades avançadas com base apenas em medidas tecnológicas.** Por exemplo, uma opção de grampeamento de impressora pode ser um recurso avançado de impressora, mas é significativo para todos os usuários, portanto, ela não deve estar em uma página avançada.

### <a name="owned-property-windows"></a>Janelas de propriedades de propriedade

-   **Não exibir mais de uma janela de propriedades de propriedade de uma janela de propriedades.** Exibir mais de um torna o significado dos botões OK e cancelar difícil de entender. Você pode exibir outros tipos de caixas de diálogo auxiliares (como seletores de objetos), conforme necessário.

    **Incorreto:**

    ![captura de tela de três janelas de propriedades pertencentes ](images/win-property-win-image3.png)

    Neste exemplo, a caixa de diálogo opções do proprietário tem três níveis de janelas de propriedade pertencentes. Como resultado, os significados OK e cancelar são confusos.

-   Para janelas de propriedades que usam um modelo de confirmação atrasada, verifique **se os usuários podem cancelar as alterações feitas em uma janela de propriedades de propriedade clicando em cancelar na janela do proprietário.**
-   Se uma janela de propriedade pertencente exigir uma confirmação imediata, **indique que as alterações foram confirmadas renomeando o botão Cancelar na janela do proprietário para fechar.** Reverta o botão de volta para cancelar se o usuário clicar em aplicar.

    ![captura de tela da janela de propriedades com OK e fechar ](images/win-property-win-image4.png)

    Neste exemplo, as alterações em dicionários personalizados e configurações de gramática não podem ser canceladas. Você pode fornecer comentários aos usuários alterando cancelar para fechar.

**Outras janelas de propriedade**

-   Se uma janela de propriedade for usada para executar uma tarefa auxiliar, **não renomeie o botão Cancelar.** As diretrizes anteriores aplicam-se apenas às janelas de propriedade pertencentes, não às caixas de diálogo usadas para executar tarefas auxiliares.

    ![captura de tela da janela do proprietário e limpeza de disco ](images/win-property-win-image5.png)

    Neste exemplo, a limpeza de disco é uma tarefa auxiliar, portanto as diretrizes anteriores não se aplicam. Por exemplo, o botão Cancelar na janela do proprietário não deve ser alterado para fechar.

-   Se a janela de propriedade for usada para executar uma tarefa auxiliar, **não feche a janela de propriedades do proprietário quando o botão de comando for clicado.** Fazer isso é a orientação e pressupõe que o único motivo pelo qual o usuário exibiu a janela de propriedades era executar esse comando.

    **Incorreto:**

    ![captura de tela da caixa de diálogo opções ](images/win-property-win-image6.png)

    Neste exemplo, clicar em **proteger documento** fecha incorretamente a caixa de diálogo opções.

### <a name="tabs"></a>Guias

-   **Use rótulos de guias concisos.** Use uma ou duas palavras que descrevam claramente o conteúdo da página. Rótulos mais longos resultam em um uso ineficiente do espaço da tela, especialmente quando os rótulos são localizados.
-   **Use rótulos de guias específicos e significativos.** Evite rótulos de guia genéricos que possam se aplicar a qualquer guia, como geral, avançado ou configurações.
-   **Use guias horizontais se:**
    -   A janela de propriedades tem sete ou menos guias (incluindo qualquer extensão de terceiros).
    -   **Todas as guias se ajustam em uma linha, mesmo quando a interface do usuário é localizada.**
    -   Você usa guias horizontais nas outras janelas de propriedades em seu aplicativo.
-   **Use as guias verticais se:**

    -   A janela de propriedades tem oito ou mais guias (incluindo qualquer extensão de terceiros).
    -   **O uso de guias horizontais exigiria mais de uma linha.**
    -   Você usa guias verticais nas outras janelas de propriedades em seu aplicativo.

    ![captura de tela da janela de propriedades com guias verticais ](images/win-property-win-image7.png)

    Neste exemplo, as guias verticais são usadas para acomodar oito ou mais guias.

-   **Para os inspetores de propriedades, para conservar o espaço, considere usar uma lista suspensa em vez de guias**, especialmente se a guia atual raramente for alterada pelo usuário.
-   **Se uma guia não se aplicar ao contexto atual e os usuários não esperarem, remova a guia.** Fazer isso simplifica a interface do usuário e os usuários não perdem isso.

    **Incorreto:**

    ![captura de tela da guia locais de arquivos esmaecidos ](images/win-property-win-image8.png)

    Neste exemplo, a guia locais de arquivo é desabilitada incorretamente quando o Microsoft Word 2003 é usado como um editor de email. A página deve ser removida porque os usuários não esperam exibir ou alterar locais de arquivo neste contexto.

-   **Se uma guia não se aplicar ao contexto atual e os usuários puderem esperar isso:**

    -   **Exiba a guia.**
    -   **Desabilite os controles na página.**
    -   **Incluir texto explicando por que os controles estão desabilitados.**

    Não desabilite a guia porque isso não é auto-explicativo e proíbe a exploração. Além disso, os usuários que procuram uma propriedade específica seriam forçados a examinar todas as outras guias.

    ![captura de tela de controles de exibição esmaecidos ](images/win-property-win-image9.png)

    Neste exemplo do Word 2003, nenhuma das opções de exibição se aplica ao layout de leitura. No entanto, os usuários podem esperar que eles se apliquem com base no rótulo da guia, portanto, a página é exibida, mas as opções são desabilitadas.

-   **Não atribua efeitos às guias de alteração.** A alteração da guia atual nunca deve ter efeitos colaterais, aplicar configurações ou resultar em uma mensagem de erro.
-   **Não aninhe tabulações ou combine guias horizontais com guias verticais.** Em vez disso, reduza o número de guias, use apenas guias verticais ou use outro controle, como uma lista suspensa.
-   **Não use guias se uma janela de propriedades tiver apenas uma única guia e não for extensível.** Use uma caixa de diálogo normal com OK, cancelar e um botão de aplicação opcional em vez disso. As janelas de propriedade extensível (que podem ser estendidas por terceiros) sempre precisam usar guias.
-   **Não coloque ícones nas guias.** Os ícones geralmente adicionam uma desordem Visual desnecessária, consomem espaço na tela e geralmente não melhoram a compreensão do usuário. Somente adicione ícones que auxiliem na compreensão, como símbolos padrão.

    **Incorreto:**

    ![captura de tela de rótulos de guia com ícones ](images/win-property-win-image10.png)

    Neste exemplo, os elementos gráficos adicionam resíduos visuais desnecessários e fazem pouco para melhorar a compreensão do usuário.

-   **Não use logotipos de produtos para gráficos de guias.** As guias não são para identidade visual.
-   **Não role as guias horizontais.** A rolagem horizontal não é prontamente detectável. No entanto, você pode rolar guias verticais.

    **Incorreto:**

    ![captura de tela do rótulo de guia horizontal truncado ](images/win-property-win-image11.png)

    Neste exemplo, as guias horizontais são roladas.

### <a name="command-buttons"></a>Botões de comando

-   **Coloque os botões de comando que se aplicam a todas as páginas de propriedades na parte inferior da janela de propriedades.** Alinhar os botões à direita e usar esta ordem (da esquerda para a direita): OK, cancelar e aplicar.
-   **Coloque os botões de comando que se aplicam somente a páginas de propriedades individuais diretamente na página de propriedades.**

### <a name="commit-buttons"></a>Botões de confirmação

**Botões OK**

-   **Para as janelas de propriedades do proprietário, o botão OK significa aplicar as alterações pendentes (feitas desde que a janela foi aberta ou a última aplicação) e fechar a janela.**
-   **Para janelas de propriedade pertencentes, o botão OK significa manter as alterações, fechar a janela e aplicar as alterações quando as alterações da janela do proprietário forem aplicadas.**
-   **Não renomeie o botão OK.** Ao contrário de outras caixas de diálogo, as janelas de propriedades não são usadas para executar uma tarefa específica. Se fizer sentido renomear o botão OK (para imprimir, por exemplo), a janela não será uma janela de propriedades.
-   **Não atribua uma chave de acesso.**

**Botões cancelar**

-   **O botão Cancelar significa descartar todas as alterações pendentes (feitas desde que a janela foi aberta ou a última aplicação) e fechar a janela.**
-   **Se todas as alterações pendentes não puderem ser abandonadas, renomeie o botão Cancelar para fechar.** Clicar em cancelar deve abandonar todas as alterações pendentes.
-   **Se a janela de Propriedade do proprietário exigir uma confirmação imediata, renomeie o botão Cancelar na janela do proprietário para fechar e mostrar que as alterações foram confirmadas.**
-   **Não atribua uma chave de acesso.**

**Aplicar botões**

-   **Para folhas de propriedades do proprietário, o botão Aplicar significa aplicar as alterações pendentes (feitas desde que a janela foi aberta ou a última aplicação), mas deixar a janela aberta.** Isso permite que os usuários avaliem as alterações antes de fechar a folha de propriedades.
-   **Para folhas de propriedades de propriedade, não use.** Usar um botão aplicar em uma folha de propriedades de propriedade faz com que o significado dos botões de confirmação na folha de propriedades do proprietário seja difícil de entender.
-   **Forneça um botão aplicar somente se a folha de propriedades tiver configurações (pelo menos uma) com efeitos que os usuários podem avaliar de maneira significativa.** Normalmente, os botões aplicar são usados quando as configurações fazem alterações visíveis. Os usuários devem ser capazes de aplicar uma alteração, avaliar a alteração e fazer outras alterações com base nessa avaliação. Caso contrário, remova o botão aplicar em vez de desabilitá-lo.

    **Incorreto:**

    ![captura de tela das propriedades do sistema com o botão aplicar ](images/win-property-win-image12.png)

    Neste exemplo, nenhuma das propriedades do sistema tem um efeito visual, portanto, o botão Aplicar não tem nenhum valor e deve ser removido.

-   **Coloque todas as configurações que os usuários podem querer aplicar nas páginas do proprietário.** Não use os botões aplicar em folhas de propriedades de propriedade, pois isso é confuso.
-   **Use os botões aplicar somente com folhas de propriedades, não com as caixas de diálogo opções.**
-   **Habilitar o botão aplicar somente quando houver alterações pendentes**; caso contrário, desabilite-o.
-   **Atribua "A" como a chave de acesso.**

**Botões de fechamento**

-   **Se todas as alterações pendentes não puderem ser abandonadas, renomeie o botão Cancelar para fechar.** Clicar em cancelar deve abandonar todas as alterações pendentes.
-   **Não confirme se os usuários descartam suas alterações.**
    -   **Exceção:** Se a janela de propriedades tiver configurações que exigem um esforço significativo para definir e o usuário tiver feito alterações, você poderá exibir uma [confirmação](mess-confirm.md) se o usuário clicar no botão fechar na barra de título. O motivo é que alguns usuários assumem erroneamente que o botão fechar na barra de título tem o mesmo efeito que o botão OK.
-   **Com exceção da mensagem de confirmação, verifique se o botão fechar na barra de título tem o mesmo efeito que cancelar ou fechar.**

### <a name="page-contents"></a>Conteúdo da página

-   **Verifique se as propriedades são necessárias.** Não contorne suas páginas com propriedades desnecessárias apenas para evitar tomar decisões de design rígido.
-   **Apresente as propriedades em termos de metas do usuário, e não da tecnologia.** Só porque uma propriedade configura uma tecnologia específica não significa que você deve apresentar a propriedade em termos dessa tecnologia.
    -   Se você precisar apresentar as configurações em termos de tecnologia (talvez porque seus usuários reconheçam o nome da tecnologia), inclua uma breve descrição de como o usuário se beneficia dessa configuração.
-   **Apresente as propriedades no nível certo.** Você não precisa apresentar configurações individuais de baixo nível em uma página de propriedades, portanto, apresente as propriedades em um nível que faça sentido para os usuários.
-   **Criar páginas de propriedades para tarefas específicas.** Determine as tarefas que os usuários executarão e verifique se há um caminho claro para executar essas tarefas.
-   **Organize as páginas de propriedades com eficiência** reduzindo o número de guias, decidindo o que vai em uma página com base no agrupamento lógico e coerência e simplificando a apresentação da página.

<!-- -->

-   **Se uma opção for altamente recomendável, considere adicionar "(recomendado)" ao rótulo.**
-   **Forneça um botão de comando restaurar padrões para uma página de propriedades ou a janela de propriedades inteira quando:**

    -   Os usuários provavelmente considerarão as configurações complexas e difíceis de entender.
    -   Ter configurações incorretas pode resultar na interrupção da funcionalidade, mas os padrões podem restaurar a funcionalidade.
    -   É mais fácil para os usuários começarem quando o objeto estiver configurado incorretamente.

    ![captura de tela de guia com o botão restaurar padrões ](images/win-property-win-image13.png)

    Neste exemplo, as configurações do firewall do Windows são complexas e podem resultar em funcionalidade quebrada. Se houver um problema, geralmente é mais fácil para os usuários recomeçarem clicando em restaurar padrões.

-   Confirme o comando restaurar padrões se seu efeito não for óbvio ou se as configurações forem complexas. Indique a confirmação usando [reticências](ctrl-command-buttons.md).
-   **Quando apropriado, exiba uma visualização dos resultados de uma configuração.**

    ![captura de tela de exemplos de ponteiro de propriedades do mouse ](images/win-property-win-image14.png)

    Neste exemplo, a página exibe uma visualização dos esquemas de ponteiro. Ao clicar em aplicar também mostra uma visualização, ter uma visualização na página é mais eficiente para os usuários.

    ![captura de tela da visualização dos resultados das configurações de fonte ](images/win-property-win-image15.png)

    Neste exemplo, a caixa de visualização mostra os resultados das configurações de fonte. Este exemplo mostra que você pode visualizar as configurações que não são gráficas.

### <a name="help"></a>Ajuda

-   Ao fornecer assistência ao usuário, **Considere o uso das seguintes opções** (listadas na ordem de preferência):
    -   Forneça rótulos autoexplicativos aos controles interativos. Os usuários têm mais probabilidade de ler os rótulos em controles interativos do que qualquer outro texto.
    -   Forneça explicações no contexto usando rótulos de texto estáticos.
    -   Forneça um [link](ctrl-links.md) específico para um tópico de ajuda relevante.
-   **Localize os links de ajuda na parte inferior de cada página.** Se uma página tiver vários grupos distintos de configurações que têm um tópico da ajuda (talvez dentro das caixas de grupo), localize o link ajuda na parte inferior do grupo.
-   **Não use links de tópicos de ajuda gerais ou vagas ou botões de ajuda genéricos.** Os usuários geralmente ignoram a ajuda genérica.

Para obter mais informações e exemplos, consulte [a ajuda](winenv-help.md).

### <a name="standard-users-and-protected-administrators"></a>Usuários padrão e administradores protegidos

**Muitas configurações exigem privilégios de administrador para serem alteradas.** Se um processo exigir privilégios de administrador, o Windows e posteriores exigirão que [usuários padrão](glossary.md) e [Administradores protegidos](glossary.md) elevem seus privilégios explicitamente. Isso ajuda a impedir que códigos mal-intencionados sejam executados com privilégios de administrador.

Para obter mais informações e exemplos, consulte [controle de conta de usuário](winenv-uac.md).

### <a name="default-values"></a>Valores padrão

-   **As configurações em uma janela de propriedades devem refletir o estado atual do aplicativo, objeto ou coleção de objetos.** Caso contrário, seria enganoso e, possivelmente, resultaria em resultados indesejados. Por exemplo, se as configurações refletirem as recomendações, mas não o estado atual, os usuários poderão clicar em Cancelar em vez de fazer alterações, pensando que nenhuma alteração é necessária.
-   **Escolha o mais seguro (para evitar a perda de dados ou acesso ao sistema) e o estado inicial mais seguro.** Suponha que a maioria dos usuários não alterará as configurações.
-   **Se não houver fatores de segurança e segurança, escolha o estado inicial mais provável ou conveniente.**

## <a name="text"></a>Texto

### <a name="commands"></a>Comandos

-   Para exibir as opções do programa, use "opções".
-   Para exibir a janela de propriedades de um objeto, use "Propriedades".
-   Para exibir um resumo das configurações de personalização do programa usadas com frequência, use "[Personalizar](glossary.md)".
-   Não use "configurações" ou "Preferências".
-   Não use [reticências](ctrl-command-buttons.md) para esses comandos.

### <a name="property-sheet-titles"></a>Títulos da folha de propriedades

-   Para um único objeto, use " \[ Propriedades do nome do objeto" \] .
    -   Se o objeto não tiver nenhum nome, use o nome do tipo do objeto. (Por exemplo, propriedades de conta de usuário.)
-   Para vários objetos, use " \[ nome do primeiro objeto \] ,... Propriedades ".
    -   Se os objetos não tiverem nomes, use o nome do tipo dos objetos. (Por exemplo, propriedades de contas de usuário.)
    -   Se os objetos tiverem tipos diferentes, use "Propriedades de seleção".
-   Use [a capitalização de estilo de título](glossary.md).
-   Não use pontuação final.
-   Não use hifens, como " \[ nome do objeto \] -Propriedades".

### <a name="property-inspector-titles"></a>Títulos do Inspetor de propriedades

-   Use "Propriedades".
-   Use a capitalização de estilo de título.
-   Não use pontuação final.

### <a name="options-dialog-box-titles"></a>Títulos da caixa de diálogo opções

-   Use "opções".
-   Use a capitalização de estilo de título.
-   Não use pontuação final.

### <a name="property-page-tab-names"></a>Nomes de guias da página de propriedades

-   **Use rótulos de guias concisos.** Use uma ou duas palavras que descrevam claramente o conteúdo da página. O uso de nomes de guias mais longos resulta em um uso ineficiente do espaço da tela, especialmente quando os nomes das guias são localizados.
-   **Use rótulos de guias específicos e significativos.** Evite rótulos de guia genéricos que possam se aplicar a qualquer guia, como geral, avançado ou configurações.
-   Escreva o rótulo como uma frase de uma ou duas palavras e não use pontuação final.
-   Use [a capitalização no estilo de frase](glossary.md).
-   Não atribua uma [chave de acesso](glossary.md)exclusiva.

### <a name="property-page-text"></a>Texto da página de propriedades

-   Evite grandes blocos de texto.
-   Forneça espaço suficiente para o texto expandir 30 por cento se ele for localizado.
-   Não use frase de texto como um comando nas janelas de propriedades. Como os usuários talvez queiram simplesmente exibir as configurações, você não deseja solicitar que eles alterem as configurações.
-   Use maiúsculas e minúsculas no estilo de sentença e pontuação final.

## <a name="documentation"></a>Documentação

Ao fazer referência a janelas de propriedades:

-   Em programação e outras documentações técnicas, consulte as caixas de diálogo folhas de propriedades e opções como folhas de propriedades. Em qualquer outra parte, use a caixa de diálogo, especialmente na documentação do usuário.
-   Use o texto do título exato, incluindo sua capitalização.
-   Para descrever a interação do usuário, use abrir e fechar.
-   Quando possível, formate o título usando texto em negrito. Caso contrário, coloque o título entre aspas somente se necessário para evitar confusão.

Ao fazer referência a páginas de propriedades:

-   Em programação e outras documentações técnicas, consulte páginas de propriedades como páginas de propriedades. Em qualquer outro lugar, use Tab, especialmente na documentação do usuário.
-   Use o texto do título exato, incluindo sua capitalização.
-   Para descrever a interação do usuário, use clique para se referir a clicar em uma guia.
-   Quando possível, formate o nome usando texto em negrito. Caso contrário, coloque o nome entre aspas somente se necessário para evitar confusão.

 

 