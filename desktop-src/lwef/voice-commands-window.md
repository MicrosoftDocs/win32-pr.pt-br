---
title: Janela de comandos de voz
description: Janela de comandos de voz
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4ad0a1521e8dacc941ba5b2ce5f6c264c65a31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105761079"
---
# <a name="voice-commands-window"></a>Janela de comandos de voz

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A janela comandos de voz exibe os comandos de voz ativos atuais disponíveis para o caractere. A janela é exibida quando o comando abrir comandos da janela é escolhido ou a propriedade [**Visible**](visible-property.md) do objeto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) é definida como **true**. Se o mecanismo de fala ainda não tiver sido carregado, consultar ou definir essa propriedade fará com que o Microsoft Agent tente inicializar o mecanismo. Se o usuário desabilitar a fala, a janela ainda poderá ser exibida; no entanto, ele incluirá uma mensagem de texto informando ao usuário que a fala está atualmente desabilitada.

Os comandos de entrada-ativo do cliente aparecem na janela de comandos de voz com base nas configurações de [**legenda**](caption-property.md) [**de voz e**](voice-property.md)de propriedade de **voz** listadas em [**VoiceCaption**](voicecaption-property.md) de sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

**Figura 1. Janela de comandos de voz**

A janela comandos de voz é exibida quando o comando abrir comandos da janela é escolhido. Os comandos de entrada-ativo do cliente aparecem na janela de comandos de voz com base nas [**configurações de**](voice-property.md)[**legenda**](caption-property.md) de voz e de propriedade de **voz** listadas em **voz** da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

A janela de comandos de voz também lista o [**VoiceCaption**](voicecaption-property.md) da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) para outros clientes do caractere e os seguintes comandos de voz gerados pelo servidor para interação geral na entrada de comandos globais:



| Legenda de voz                       | Gramática de voz                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abrir \| janela fechar comandos de voz | (Open \| show) \[ a \] janela de comandos o \[ \] \| que posso dizer \[ agora\] <br/> alterna com: <br/> fechar \[ a \] janela de comandos \[\] <br/> |
| Ocultar                                | exibe \*                                                                                                                                                  |
| *Caractere de*                     | *Caractere de*\*\*                                                                                                                                      |
| Comandos globais                     | \[Mostrar \] \[ \] comandos globais                                                                                                                          |



 

\* Um caractere é listado aqui somente se estiver visível no momento.

\*\* Todos os caracteres carregados são listados.

Falar o comando de voz para a coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) de outro cliente alterna para esse cliente, e a janela de comandos de voz exibe os comandos desse cliente. Nenhuma outra entrada é expandida. Da mesma forma, se o usuário alternar caracteres, a janela de comandos de voz será alterada para exibir os comandos de seu cliente de entrada-ativo. Se o cliente já estiver em entrada-ativo, falar um de seus comandos de voz não terá nenhum efeito. (No entanto, se o usuário recolher a subárvore do cliente ativo com o mouse, falar o nome do cliente exibirá novamente a subárvore do cliente.)

Se um cliente tiver comandos de voz, mas nenhuma configuração de [**voz**](voice-property.md) para seu objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) (ou nenhuma [**legenda**](caption-property.md)de **voz**), a árvore exibirá "(comando indefinido)" como a entrada pai, mas somente quando esse cliente for entrada-ativo e o cliente tiver comandos em sua coleção que têm configurações de **legenda** e de **voz** .

O servidor exibe automaticamente os comandos do cliente de entrada-ativo atual e, se necessário, rola a janela para exibir o máximo possível dos comandos do cliente, com base no tamanho da janela. Se o caractere não tiver entradas de cliente, a entrada de comandos globais será expandida.

Se o usuário fala "comandos globais", a janela comandos de voz sempre exibe suas entradas de subárvore associadas. Se eles já estiverem exibidos, o comando não terá nenhum efeito.

Embora você também possa exibir ou ocultar a janela de comandos de voz do código do seu aplicativo usando a propriedade [**Visible**](visible-property.md) , não é possível alterar o tamanho ou o local da janela de comandos de voz. O servidor mantém as propriedades da janela de comandos de voz com base na interação do usuário com a janela. Seu local inicial é imediatamente adjacente ao ícone da barra de tarefas do caractere.

A janela de comandos de voz está incluída na ordem da janela ALT + TAB. Isso permite que um usuário alterne para a janela para rolar, redimensionar ou reposicionar a janela com o teclado.

-   [A dica de escuta](the-listening-tip.md)
-   [A janela Opções de caractere avançadas](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)

 

