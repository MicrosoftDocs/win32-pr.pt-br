---
title: Barras de status (noções básicas de Design)
description: Uma barra de status é uma área na parte inferior de uma janela primária que exibe informações sobre o estado da janela atual (como o que está sendo exibido e como), tarefas em segundo plano (como impressão, verificação e formatação) ou outras informações contextuais (como a seleção e o estado do teclado).
ms.assetid: 09dc03d9-d730-4f03-86a8-7b39d9a55369
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8f65d104f59cd0aec0c242d623f83c410c22f48d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104172423"
---
# <a name="status-bars-design-basics"></a>Barras de status (noções básicas de Design)

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Uma barra de status é uma área na parte inferior de uma janela primária que exibe informações sobre o estado da janela atual (como o que está sendo exibido e como), tarefas em segundo plano (como impressão, verificação e formatação) ou outras informações contextuais (como a seleção e o estado do teclado).

Barras de status normalmente indicam o status por meio de texto e ícones, mas também podem ter indicadores de progresso, bem como menus para comandos e opções relacionadas ao status.

![captura de tela da barra de status típica ](images/ctrl-status-bars-image1.png)

Uma barra de status típica.

> [!Note]  
> As diretrizes relacionadas à [área de notificação](winenv-notification.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir, considere estas perguntas:

-   **O status é relevante quando os usuários estão usando ativamente outros programas?** Nesse caso, use os [ícones da área de notificação](winenv-notification.md).
-   **O item de status precisa exibir notificações?** Nesse caso, você deve usar um ícone da área de notificação.
-   **A janela é uma janela principal?** Caso contrário, não use uma barra de status. Caixas de diálogo, assistentes, painéis de controle e folhas de propriedades não devem ter barras de status.
-   **As informações são principalmente o status?** Caso contrário, não use uma barra de status. As barras de status não devem ser usadas como [barra de menus](cmd-menus.md) ou barra de [ferramentas](cmd-toolbars.md)secundária.
-   **As informações explicam como usar o controle selecionado?** Nesse caso, exiba as informações ao lado do controle associado usando uma explicação suplementar ou rótulo de instrução em vez disso.
-   **O status é útil e relevante? Ou seja, os usuários provavelmente podem alterar seu comportamento como resultado dessas informações?** Caso contrário, não exiba o status ou coloque-o em um arquivo de log.
-   **O status é crítico? A ação imediata é necessária?** Nesse caso, exiba as informações em um formulário que exija atenção e não pode ser facilmente ignorada, como uma [caixa de diálogo](win-dialog-box.md) ou dentro da própria janela principal.

    ![captura de tela da barra de status vermelho "erro de certificado" ](images/ctrl-status-bars-image2.png)

    Uma barra de endereços vermelha no Windows Internet Explorer.

-   **O programa destina-se principalmente a usuários iniciantes?** Os usuários inexperientes geralmente não sabem das barras de status; portanto, reconsidere o uso de barras de status nesse caso.

## <a name="design-concepts"></a>Conceitos de design

Barras de status são uma ótima maneira de fornecer informações de status sem interromper os usuários ou interromper seu fluxo. No entanto, as barras de status são fáceis de serem ignoradas. Muito fácil, de fato, que muitos usuários não percebam barras de status.

A solução para esse problema não é exigir a atenção do usuário usando ícones extravagantes, animações ou piscar, mas para criar essa limitação. É possível fazer isso da seguinte maneira:

-   **Verificar se as informações de status são úteis e relevantes.** Caso contrário, não forneça uma barra de status.
-   **Não usar barras de status para obter informações cruciais.** Os usuários nunca devem saber o que há na barra de status. Se os usuários precisarem vê-lo, não coloque-o em uma barra de status.

**Se você fizer apenas uma coisa...**

Verifique se as informações da barra de status são úteis e relevantes, mas não são cruciais.

## <a name="usage-patterns"></a>Padrões de uso

Barras de status têm vários padrões de uso:



|                                                                                                                                    |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Status da janela atual**<br/> Mostrar a origem do que está sendo exibido junto com qualquer modo de exibição <br/>              | ![captura de tela de uma barra de status ' local ' ](images/ctrl-status-bars-image3.png)<br/> Neste exemplo, a barra de status exibe o caminho para o documento.<br/>                                                         |
| **Progresso**<br/> Mostrar o andamento das tarefas em segundo plano, seja com uma barra de progresso ou uma animação de destérmino. <br/> | ![captura de tela da barra de status com barra de progresso ](images/ctrl-status-bars-image4.png)<br/> Neste exemplo, a barra de status inclui uma barra de progresso para mostrar o carregamento da página da Web em uma janela do Internet Explorer.<br/> |
| **Informações contextuais**<br/> Mostrar informações contextuais sobre o que o usuário está fazendo no momento. <br/>              | ![captura de tela da barra de status mostrando o número de pixels ](images/ctrl-status-bars-image5.png)<br/> Neste exemplo, o Microsoft Paint mostra o tamanho da seleção em pixels.<br/>                                           |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   Considere fornecer um comando exibir barra de status se apenas alguns usuários precisarem das informações da barra de status. Oculte a barra de status por padrão se a maioria dos usuários não precisar dela.
-   Não use a barra de status para explicar os itens da barra de menus. Esse padrão de ajuda não é detectável.

### <a name="presentation"></a>Apresentação

-   Desabilite o status modal que não se aplica. O status modal inclui os Estados de teclado e documento.
-   Remova o status não modal que não se aplica.
-   Apresente as informações de status na seguinte ordem: status da janela atual; andamento e informações contextuais.

### <a name="icons"></a>Ícones

-   Escolha designs de ícone de status facilmente reconhecíveis. Prefira ícones com contornos exclusivos em ícones quadrados ou retangulares.
-   Use faixas puro vermelho, amarelo e verde apenas para comunicar informações de status. Caso contrário, esses ícones são confusos.

    **Correto:**

    ![captura de tela da barra de status com ícones azuis ](images/ctrl-status-bars-image6.png)

    **Incorreto:**

    ![captura de tela da barra de status com um ícone vermelho ](images/ctrl-status-bars-image7.png)

    No exemplo incorreto, o ícone vermelho sugere um erro involuntariamente, criando confusão.

-   Use variações de ícone ou sobreposições para indicar alterações de status ou status. Use variações de ícone para mostrar as alterações em quantidades ou forças. Para outros tipos de status, use estas sobreposições padrão: 

    |                                                                                               |                                  |
    |-----------------------------------------------------------------------------------------------|----------------------------------|
    | **Sobreposição**<br/>                                                                        | **Status**<br/>            |
    | ![captura de tela do ícone de aviso ](images/ctrl-status-bars-image8.png)<br/>                | Aviso<br/>               |
    | ![captura de tela do ícone de erro ](images/ctrl-status-bars-image9.png)<br/>                  | Erro<br/>                 |
    | ![captura de tela do ícone desabilitado/desconectado ](images/ctrl-status-bars-image10.png)<br/> | Desabilitado/desconectado<br/> |
    | ![captura de tela do ícone bloqueado/offline ](images/ctrl-status-bars-image11.png)<br/>       | Bloqueado/offline<br/>       |

    

     

-   Não altere o status com muita frequência. Os ícones da barra de status não devem aparecer ruidosas, instáveis ou exigir atenção. O olho é sensível às alterações no campo periférico da visão, portanto, as alterações de status precisam ser sutis.
-   Para ícones que fornecem informações de status importantes, prefira rótulos in-loco.
-   Ícones de barra de status não rotulados devem ter dicas de ferramenta.

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

 

