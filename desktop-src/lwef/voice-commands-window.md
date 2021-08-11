---
title: Janela Comandos de Voz
description: Janela Comandos de Voz
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f4e5ce02ea9a964663efacbc19a3b302d6e58f0364d705491be26229b15f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245099"
---
# <a name="voice-commands-window"></a>Janela Comandos de Voz

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A Janela Comandos de Voz exibe os comandos de voz ativos atuais disponíveis para o caractere. A janela aparece quando o comando Abrir Janela comandos é escolhido ou a propriedade [**Visible**](visible-property.md) do objeto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) é definida como **True.** Se o mecanismo de fala ainda não tiver sido carregado, consultar ou definir essa propriedade fará com que o Microsoft Agent tente inicializar o mecanismo. Se o usuário desabilitar a fala, a janela ainda poderá ser exibida; no entanto, ele incluirá uma mensagem de texto que informa ao usuário que a fala está desabilitada no momento.

Os comandos do cliente de entrada ativa aparecem na [](voice-property.md)[](caption-property.md) Janela Comandos  de Voz com base nas configurações de propriedade Legenda de Voz e Voz listadas em [**VoiceCaption**](voicecaption-property.md) de sua [**coleção De**](/windows/desktop/lwef/the-commands-collection-object) comandos.

**Figura 1. Janela Comandos de Voz**

A Janela Comandos de Voz aparece quando o comando Abrir Janela comandos é escolhido. Os comandos do cliente de entrada ativa aparecem na [](voice-property.md)[](caption-property.md) Janela Comandos  de Voz com base nas configurações de propriedade Legenda de Voz e Voz listadas em **Voz** da [**coleção Comandos.**](/windows/desktop/lwef/the-commands-collection-object)

A Janela Comandos de Voz também lista o [**VoiceCaption**](voicecaption-property.md) da coleção [**Commands**](/windows/desktop/lwef/the-commands-collection-object) para outros clientes do caractere e os seguintes comandos de voz gerados pelo servidor para interação geral na entrada Comandos Globais:



| Legenda de voz                       | Gramática de voz                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abrir \| a janela Fechar Comandos de Voz | (abrir \| mostrar) a \[ janela \] \[ comandos, o que posso dizer \] \| \[ agora\] <br/> alterna com: <br/> fechar \[ a janela \] comandos \[\] <br/> |
| Ocultar                                | Esconder \*                                                                                                                                                  |
| *CharacterName*                     | *CharacterName*\*\*                                                                                                                                      |
| Comandos globais                     | \[mostrar \] \[ comandos \] globais                                                                                                                          |



 

\* Um caractere será listado aqui somente se ele estiver visível no momento.

\*\* Todos os caracteres carregados são listados.

A fala do comando de [](/windows/desktop/lwef/the-commands-collection-object) voz para a coleção Comandos de outro cliente muda para esse cliente e a Janela Comandos de Voz exibe os comandos desse cliente. Nenhuma outra entrada é expandida. Da mesma forma, se o usuário alternar caracteres, a Janela comandos de voz será mudada para exibir os comandos de seu cliente ativo de entrada. Se o cliente já estiver ativo de entrada, falar em um de seus comandos de voz não terá nenhum efeito. (No entanto, se o usuário fechar a subárvore do cliente ativo com o mouse, falar o nome do cliente repetirá a subárvore do cliente.)

Se um cliente tiver comandos [](voice-property.md) de voz, mas nenhuma configuração de Voz para seu objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) (ou nenhuma Legenda de [**Voz),**](caption-property.md)a árvore exibirá "(comando indefinido)" como a entrada pai , mas somente quando esse cliente estiver ativo de entrada e o cliente tiver comandos em sua coleção que têm configurações de Legenda e Voz.  

O servidor exibe automaticamente os comandos do cliente ativo de entrada atual e, se necessário, rola a janela para exibir o máximo possível de comandos do cliente, com base no tamanho da janela. Se o caractere não tiver entradas de cliente, a entrada Comandos Globais será expandida.

Se o usuário falar "Comandos Globais", a Janela Comandos de Voz sempre exibirá suas entradas de subárvore associadas. Se eles já estão exibidos, o comando não tem nenhum efeito.

Embora você também possa exibir ou ocultar a Janela comandos de voz do código do aplicativo usando a propriedade [**Visible,**](visible-property.md) não é possível alterar o tamanho ou o local da Janela comandos de voz. O servidor mantém as propriedades da Janela comandos de voz com base na interação do usuário com a janela. Seu local inicial é imediatamente adjacente ao ícone da barra de tarefas do caractere.

A janela Comandos de Voz está incluída na ordem da janela ALT+TAB. Isso permite que um usuário alternar para a janela para rolar, reescalar ou reposicionar a janela com o teclado.

-   [A dica de escuta](the-listening-tip.md)
-   [A janela Opções de Caractere Avançadas](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)

 

