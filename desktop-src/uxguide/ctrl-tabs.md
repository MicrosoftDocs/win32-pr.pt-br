---
title: Guias
description: As guias fornecem uma maneira de apresentar informações relacionadas em páginas rotuladas separadas.
ms.assetid: d90228ce-aa95-4359-be8e-ea2014d71ae6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b2649862885e55bdfe10fdca7f34b7618d976a38
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104565953"
---
# <a name="tabs"></a>Guias

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

As guias fornecem uma maneira de apresentar informações relacionadas em páginas rotuladas separadas.

![captura de tela de cinco guias ](images/ctrl-tabs-image1.png)

Um conjunto típico de guias.

As guias geralmente são associadas às janelas de Propriedades (e vice-versa), mas as guias podem ser usadas em qualquer tipo de janela.

Os controles guia representam as pastas Manila com guias usadas para organizar informações em gabinetes de arquivamento geralmente encontradas no Estados Unidos. (As pastas Manila não são usadas no mundo todo.)

> [!Note]  
> As diretrizes relacionadas ao [layout](vis-layout.md), aos [menus de guias](cmd-menus.md), às caixas de [diálogo](win-dialog-box.md)e às janelas de [Propriedades](win-property-win.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **Os controles podem se ajustar confortavelmente a uma única página de tamanho razoável?** Nesse caso, use uma única página.
-   **Há apenas uma guia?** Nesse caso, use uma única página.
-   **As guias estão relacionadas entre si de alguma maneira óbvia?** Caso contrário, considere dividir as informações em janelas separadas de informações relacionadas.
-   **Se for usado para configurações, as configurações em páginas diferentes serão completamente independentes?** A alteração de uma configuração em uma página afeta as configurações em outras páginas? Se não forem independentes, use as páginas de tarefas ou um [Assistente](win-wizards.md) em vez disso.
-   **As guias são basicamente os pares uns dos outros, ou há uma relação hierárquica?** Se hierárquico, considere o uso de caixas de [diálogo](win-dialog-box.md) de divulgação progressiva ou filho para mostrar informações relacionadas.
-   **As guias são usadas para exibir as etapas em uma tarefa?** Você poderá usar "guias" para exibir as etapas em uma tarefa somente se elas forem apresentadas como etapas, e houver uma maneira óbvia e alternativa para chegar à etapa de texto, como um botão Avançar. Caso contrário, se as etapas forem necessárias, use páginas em um fluxo de página ou um [Assistente](win-wizards.md). Se as etapas forem opcionais, exiba as etapas opcionais usando [caixas de diálogo](win-dialog-box.md) modais em vez disso.
-   **As guias são diferentes exibições dos mesmos dados?** Nesse caso, considere usar um [botão de divisão](ctrl-command-buttons.md) ou uma [lista suspensa](/windows/desktop/uxguide/ctrl-drop) para alterar as exibições. Embora as guias possam ser usadas com eficiência para alterar as exibições, as alternativas são mais leves.

## <a name="usage-patterns"></a>Padrões de uso

As guias têm vários padrões de uso:



|                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Superfície de janela dinâmica**<br/> como barras de rolagem, as guias podem ser usadas para aumentar a área de superfície da janela para mostrar informações relacionadas.<br/>                                                    | Com esse padrão, o uso de guias é conceitualmente semelhante a colocar todas as informações nas guias linearmente em uma única superfície rolável, com os rótulos da guia como títulos. <br/> ![captura de tela de cinco guias ](images/ctrl-tabs-image1.png)<br/> Neste exemplo, as guias aumentam efetivamente a área da superfície da janela.<br/>                          |
| **Várias exibições**<br/> como botões de divisão ou listas suspensas, as guias podem ser usadas para mostrar exibições diferentes da mesma ou de informações relacionadas. <br/>                                           | ![captura de tela das guias design, divisão e visualização ](images/ctrl-tabs-image2.png)<br/> Neste exemplo, as guias alteram exibições em um documento.<br/>                                                                                                                                                                                                         |
| **Vários documentos**<br/> como várias janelas, as guias podem ser usadas para mostrar documentos diferentes em uma única janela. <br/>                                                                   | ![captura de tela de três guias para documentos diferentes ](images/ctrl-tabs-image3.png)<br/> ![Figura de guias para meses diferentes ](images/ctrl-tabs-image4.png)<br/> Nesses exemplos, as guias mostram documentos diferentes em uma única janela de aplicativo.<br/>                                                                                       |
| **Opções exclusivas**<br/> como botões de opção, as guias podem ser usadas para apresentar várias opções exclusivas. nesse padrão, somente a guia selecionada se aplica e todas as outras guias são ignoradas. <br/> | ![captura de tela das guias local, dados e mensagens ](images/ctrl-tabs-image5.png)<br/> Neste exemplo, as guias são usadas (incorretamente) como um substituto para botões de opção.<br/> **Esse padrão não é recomendado** porque ele usa um comportamento não padrão. As guias se comportam como uma configuração, em vez de puramente uma maneira de navegar dentro da janela. <br/> |



 

**Se você fizer apenas uma coisa...**

Verifique se as informações nas guias estão relacionadas, mas as configurações em páginas diferentes são independentes. A última guia selecionada não deve ter um significado especial.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Use guias horizontais se:**
    -   A janela tem sete ou menos guias.
    -   **Todas as guias se ajustam em uma linha, mesmo quando a interface do usuário é localizada.**
-   **Use as guias verticais se:**
    -   A janela de propriedades tem oito ou mais guias.
    -   **O uso de guias horizontais exigiria mais de uma linha.**

        ![captura de tela da janela de propriedades com onze opções ](images/ctrl-tabs-image6.png)

        Neste exemplo, as guias verticais acomodam oito ou mais guias.

-   **Não aninhe tabulações ou combine guias horizontais com guias verticais.** Em vez disso, reduza o número de guias, use apenas guias verticais ou use outro controle, como uma lista suspensa.
-   **Não role as guias horizontais.** A rolagem horizontal não é prontamente detectável. No entanto, você pode rolar guias verticais.

    **Incorreto:**

    ![captura de tela do rótulo de guia horizontal truncado ](images/ctrl-tabs-image7.png)

    Neste exemplo, as guias horizontais são roladas.

-   Para guias em uma janela ou painel redimensionável, coloque uma barra de rolagem, quando necessário, na página, não na janela ou no painel. As guias devem estar sempre visíveis e não rolar para fora da exibição.

    ![captura de tela da página de guias vertical com barra de rolagem ](images/ctrl-tabs-image8.png)

    Neste exemplo, a página da guia tem a barra de rolagem, não o painel.

-   **Verifique se as guias se parecem com guias e não outro tipo de controle.**

    **Incorreto:**

    ![captura de tela da janela com botões para guias ](images/ctrl-tabs-image9.png)

    Neste exemplo, essas guias são semelhantes a botões de comando.

### <a name="interaction"></a>Interação

-   **Quando os controles se aplicam somente a uma página, coloque-os dentro da borda da página com guias.**
-   **Quando os controles se aplicam a toda a janela, coloque-os fora da página com guias.**
-   **Não atribua efeitos às guias de alteração.** As guias devem ser acessíveis em qualquer ordem. A alteração da guia atual nunca deve ter efeitos colaterais, aplicar configurações ou resultar em uma mensagem de erro.
-   **Não atribua um significado especial à última guia selecionada.** A seleção de guia é para navegação a última seleção de guia do usuário não é uma configuração.
-   **Não faça as configurações em uma página dependente das configurações em outras páginas.** Em vez disso, coloque as configurações dependentes na mesma página.
-   **Se os usuários provavelmente começarem com a última guia exibida, faça com que a guia persista e selecione-a por padrão.** Fazer com que as configurações persistam por janela por usuário. Caso contrário, selecione a primeira página por padrão.

### <a name="icons"></a>Ícones

-   **Não coloque ícones nas guias.** Os ícones geralmente adicionam uma desordem Visual desnecessária, consomem espaço na tela e geralmente não melhoram a compreensão do usuário. Somente adicione ícones que auxiliem na compreensão, como símbolos padrão.

    **Incorreto:**

    ![captura de tela da janela com ícones em guias ](images/ctrl-tabs-image10.png)

    Neste exemplo, os ícones adicionam resíduos visuais e fazem pouco para melhorar a compreensão do usuário.

    **Exceção:** Você pode usar ícones claramente reconhecíveis se pode haver espaço insuficiente para exibir rótulos significativos:

    **Correto:**

    ![captura de tela de guias com ícones e rótulos resumida ](images/ctrl-tabs-image11.png)

    Neste exemplo, a janela é tão estreita que os ícones comunicam melhor as guias do que os rótulos.

-   **Não use logotipos de produtos para gráficos de guias.** As guias não são para [identidade visual](exper-branding.md).

### <a name="dynamic-window-surface-pattern"></a>Padrão de superfície de janela dinâmica

-   **Não use barras de rolagem em páginas da guia.** As guias funcionam de forma semelhante às barras de rolagem para aumentar a área efetiva de uma janela. Um mecanismo deve ser suficiente.
-   **Use rótulos de guias concisos.** Use uma ou duas palavras que descrevam claramente o conteúdo da página. Rótulos mais longos consomem espaço na tela, especialmente quando os rótulos são localizados.
-   **Use rótulos de guias específicos e significativos.** Evite rótulos de guia genéricos que possam se aplicar a qualquer guia, como geral, avançado ou configurações.
-   **Se uma guia não se aplicar ao contexto atual e os usuários não esperarem, remova-o.** Fazer isso simplifica a interface do usuário e os usuários não perdem isso.

    **Incorreto:**

    ![captura de tela da janela de opções com o nome de guia esmaecido ](images/ctrl-tabs-image12.png)

    Neste exemplo, a guia locais de arquivo é desabilitada incorretamente quando o Microsoft Word é usado como um editor de email. Em vez de desabilitar essa guia, ela deve ser removida porque os usuários não esperam exibir ou alterar os locais de arquivo neste contexto.

-   **Se uma guia não se aplicar ao contexto atual e os usuários puderem esperar isso:**

    -   Exiba a guia.
    -   Desabilite os controles na página.
    -   Incluir texto explicando por que os controles estão desabilitados.

    Não desabilite a guia, pois isso não é auto-explicativo e proíbe a exploração. Os usuários que procuram um valor específico seriam forçados a examinar todas as outras guias.

    ![captura de tela da janela com as opções da guia Exibir esmaecidas ](images/ctrl-tabs-image13.png)

    Neste exemplo, nenhuma das opções de exibição se aplica ao layout de leitura. No entanto, os usuários podem esperar que eles se apliquem com base no rótulo da guia, portanto, a página é exibida, mas as opções são desabilitadas.

### <a name="multiple-views-and-documents-patterns"></a>Vários padrões de exibições e documentos

-   **Use os nomes de exibição ou documento nos rótulos de guia.**
-   **Evite nomes de guias excessivamente longos.** Se necessário, tenha um tamanho máximo de nome ou truncar o rótulo de guia exibido usando reticências. Rótulos mais longos consomem espaço na tela, especialmente quando os rótulos são localizados.
-   **Se uma Tabulação não se aplicar ao contexto atual, remova a guia.**

### <a name="exclusive-options-pattern"></a>Padrão de opções exclusivas

-   **Não use esse padrão!** Use botões de opção ou uma lista suspensa em vez disso.

    **Incorreto:**

    ![captura de tela de janela com duas guias "criar" ](images/ctrl-tabs-image14.png)

    Neste exemplo, as guias são usadas incorretamente como um substituto para botões de opção.

    **Correto:**

    ![captura de tela da janela com dois botões de opção ](images/ctrl-tabs-image15.png)

    Neste exemplo, os botões de opção são usados corretamente em seu lugar.

## <a name="labels"></a>Rótulos

-   Rotular guias com base em seu padrão. Use substantivos em vez de verbos, sem pontuação final. Consulte as diretrizes de padrões anteriores para obter mais informações.
-   Use a capitalização com estilo de frase.
-   Não atribua uma chave de acesso. As guias podem ser acessadas por meio de suas teclas de atalho (Ctrl + Tab, Ctrl + Shift + Tab, CTRL + PgUp, CTRL + PgDn). Há uma deficiência de boas opções de chave de acesso, portanto, não atribuir chaves de acesso às guias facilita a atribuição a outros controles.

## <a name="documentation"></a>Documentação

Ao fazer referência a guias:

-   Use o texto exato do rótulo, incluindo suas maiúsculas e minúsculas, e inclua a palavra guia.
-   Para descrever a interação do usuário, use clique.
-   Quando possível, formate o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.
-   Como vários usos podem ser ambíguos, especialmente para um público mundial, use a guia substantivo sozinha para se referir apenas a um controle guia. Para outros usos, esclareça o significado com um descritor: a tecla Tab, uma parada de tabulação ou uma marca de tabulação na régua.

Exemplo: no menu **ferramentas** , clique em **Opções** e, em seguida, clique na guia **Exibir** .

