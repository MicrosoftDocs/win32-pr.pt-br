---
title: Barras de status (noções básicas de design)
description: Uma barra de status é uma área na parte inferior de uma janela primária que exibe informações sobre o estado da janela atual (como o que está sendo exibido e como), tarefas em segundo plano (como impressão, verificação e formatação) ou outras informações contextuais (como seleção e estado do teclado).
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: fa76563adbd3810b48339cc49014441512e3d76a0ac7484ff632f64f635b4cf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934143"
---
# <a name="status-bars-design-basics"></a>Barras de status (noções básicas de design)

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Uma barra de status é uma área na parte inferior de uma janela primária que exibe informações sobre o estado da janela atual (como o que está sendo exibido e como), tarefas em segundo plano (como impressão, verificação e formatação) ou outras informações contextuais (como seleção e estado do teclado).

As barras de status normalmente indicam o status por meio de texto e ícones, mas também podem ter indicadores de progresso, bem como menus para comandos e opções relacionadas ao status.

![captura de tela da barra de status típica ](images/ctrl-status-bars-image1.png)

Uma barra de status típica.

> [!Note]  
> As diretrizes relacionadas [à área de notificação](winenv-notification.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir, considere estas perguntas:

-   **O status é relevante quando os usuários estão usando ativamente outros programas?** Em caso afirmado, use [ícones de área de notificação](winenv-notification.md).
-   **O item de status precisa exibir notificações?** Se sim, você deve usar um ícone de área de notificação.
-   **A janela é uma janela primária?** Caso não, não use uma barra de status. Caixas de diálogo, assistentes, painéis de controle e folhas de propriedades não devem ter barras de status.
-   **As informações são principalmente o status?** Caso não, não use uma barra de status. As barras de status não devem ser usadas como uma barra de [menus secundária ou](cmd-menus.md) [barra de ferramentas](cmd-toolbars.md).
-   **As informações explicam como usar o controle selecionado?** Em caso afirmacional, exibe as informações ao lado do controle associado usando uma explicação complementar ou um rótulo de instrução.
-   **O status é útil e relevante? Ou seja, os usuários provavelmente alterarão seu comportamento como resultado dessas informações?** Caso não seja, não exibe o status ou coloca-o em um arquivo de log.
-   **O status é crítico? A ação imediata é necessária?** Nesse caso, exibe as informações em um formulário que exige atenção [](win-dialog-box.md) e não pode ser facilmente ignorada, como uma caixa de diálogo ou dentro da própria janela primária.

    ![captura de tela da barra de status "erro de certificado" vermelha ](images/ctrl-status-bars-image2.png)

    Uma barra de endereços vermelhos Windows Internet Explorer.

-   **O programa destina-se principalmente a usuários iniciantes?** Em geral, os usuários não estão cientes das barras de status, portanto, remente o uso de barras de status nesse caso.

## <a name="design-concepts"></a>Conceitos de design

As barras de status são uma ótima maneira de fornecer informações de status sem interromper os usuários ou interromper seu fluxo. No entanto, as barras de status são fáceis de ignorar. Tão fácil, na verdade, que muitos usuários não notam barras de status.

A solução para esse problema não é exigir a atenção do usuário usando ícones de cor, animação ou piscar, mas projetar para essa limitação. É possível fazer isso da seguinte maneira:

-   **Certifique-se de que as informações de status são úteis e relevantes.** Caso não, não forneça uma barra de status.
-   **Não usar barras de status para obter informações cruciais.** Os usuários nunca devem ter que saber o que está na barra de status. Se os usuários precisam vê-lo, não coloque-o em uma barra de status.

**Se você fizer apenas uma coisa...**

Certifique-se de que as informações da barra de status são úteis e relevantes, mas não cruciais.

## <a name="usage-patterns"></a>Padrões de uso

As barras de status têm vários padrões de uso:



|   Uso                                                                                                                                 |    Exemplo                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Status da janela atual**<br/> Mostrar a origem do que está sendo exibido junto com os modos de exibição <br/>              | ![captura de tela de uma barra de status 'location' ](images/ctrl-status-bars-image3.png)<br/> Neste exemplo, a barra de status exibe o caminho para o documento.<br/>                                                         |
| **Progresso**<br/> Mostre o progresso das tarefas em segundo plano, seja com uma barra de progresso determinada ou uma animação. <br/> | ![captura de tela da barra de status com a barra de progresso ](images/ctrl-status-bars-image4.png)<br/> Neste exemplo, a barra de status inclui uma barra de progresso para mostrar o carregamento da página da Web em uma Internet Explorer janela.<br/> |
| **Informações contextuais**<br/> Mostrar informações contextuais sobre o que o usuário está fazendo no momento. <br/>              | ![captura de tela da barra de status mostrando o número de pixels ](images/ctrl-status-bars-image5.png)<br/> Neste exemplo, Microsoft Paint mostra o tamanho da seleção em pixels.<br/>                                           |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   Considere fornecer um comando Exibir Barra de Status se apenas alguns usuários precisarem das informações da barra de status. Ocultar a barra de status por padrão se a maioria dos usuários não precisar dela.
-   Não use a barra de status para explicar os itens da barra de menus. Esse padrão de ajuda não é descobrivel.

### <a name="presentation"></a>Apresentação

-   Desabilite o status modal que não se aplica. O status modal inclui estados de teclado e documento.
-   Remova o status não modal que não se aplica.
-   Apresente informações de status na seguinte ordem: status da janela atual; progresso; e informações contextuais.

### <a name="icons"></a>Ícones

-   Escolha designs de ícone de status facilmente reconhecíveis. Prefira ícones com contornos exclusivos em vez de ícones em forma de quadrado ou retangular.
-   Use apenas as cores vermelho, amarelo e verde puros para comunicar informações de status. Caso contrário, esses ícones são confusos.

    **Correto:**

    ![captura de tela da barra de status com ícones azuis ](images/ctrl-status-bars-image6.png)

    **Incorreto:**

    ![captura de tela da barra de status com um ícone vermelho ](images/ctrl-status-bars-image7.png)

    No exemplo incorreto, o ícone vermelho sugere um erro sem querer, criando confusão.

-   Use variações de ícone ou sobreposições para indicar alterações de status ou status. Use variações de ícone para mostrar alterações em quantidades ou pontos fortes. Para outros tipos de status, use estas sobreposições padrão: 

    | Sobreposição                 | Status            |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | ![captura de tela do ícone de aviso ](images/ctrl-status-bars-image8.png)<br/>                | Aviso<br/>               |
    | ![captura de tela do ícone de erro ](images/ctrl-status-bars-image9.png)<br/>                  | Erro<br/>                 |
    | ![captura de tela do ícone desabilitado/desconectado ](images/ctrl-status-bars-image10.png)<br/> | Desabilitado/Desconectado<br/> |
    | ![captura de tela do ícone bloqueado/offline ](images/ctrl-status-bars-image11.png)<br/>       | Bloqueado/Offline<br/>       |

    

     

-   Não altere o status com muita frequência. Os ícones da barra de status não devem parecer barulhentos, instável ou exigir atenção. O olho é sensível a alterações no campo periférico da visão, portanto, as alterações de status precisam ser sutis.
-   Para ícones que fornecem informações de status importantes, prefira rótulos in-place.
-   Os ícones da barra de status sem rótulo devem ter dicas de ferramenta.

Para obter mais informações, consulte [ícones](vis-icons.md).

### <a name="interaction"></a>Interação

-   Tornar uma área de barra de status interativa para permitir que os usuários acessem diretamente os comandos e opções relacionados.
    -   Use um controle que pareça e se comporta como um [botão de menu](ctrl-command-buttons.md) ou um botão de divisão. Essas áreas de barra de status devem ter uma seta suspensa para indicar que são clicáveis.
    -   Exiba o menu ao clicar com o botão esquerdo do mouse para baixo e não para o mouse.
    -   Não dê suporte ao clique com o botão direito do mouse ou clique duas vezes em. Os usuários não esperam tais interações em uma barra de status, portanto, não são prováveis de tentar.
-   Exibir dicas de ferramentas ao focalizar.

## <a name="text"></a>Texto

-   Em geral, use rótulos concisos. Recorte qualquer texto que possa ser eliminado.
-   Prefira fragmentos de sentença, sem pontuação final. Use frases completas (com pontuação final) somente quando os fragmentos de frase não forem significativamente menores.
-   Para rótulos de progresso opcionais, indique o que a operação está fazendo com um rótulo que começa com um verbo (formulário gerund) e termina com uma elipse. Por exemplo: "copiando...". Esse rótulo pode ser alterado dinamicamente se a operação tiver várias etapas ou estiver processando vários objetos.
-   Não use cores, negrito ou itálico para enfatizar o texto da barra de status.
-   Para obter diretrizes de formulação de dica de ferramenta, consulte [tooltips e Infotips](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Documentação

Consulte barras de status como barras de status, não linhas de status ou outras variações. Exemplo: "o número da página atual é exibido na barra de status".

 

