---
title: Suporte ao menu pop-up
description: Suporte ao menu pop-up
ms.assetid: a8a1cf91-c18a-497f-89a7-b47536eaca0a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890d7eab6595200cb00e8422644b10f39807bab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294027"
---
# <a name="pop-up-menu-support"></a>Suporte ao menu pop-up

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O Microsoft Agent inclui um menu pop-up (também conhecido como um menu contextual) para cada caractere. O servidor exibe esse menu pop-up automaticamente quando um usuário clica com o botão direito do mouse no caractere. Você pode adicionar comandos para o seu aplicativo cliente no menu definindo uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Para cada comando na coleção que você define, você pode especificar a [**legenda**](caption-property.md) e as propriedades [**visíveis**](visible-property.md) . A **legenda** é o texto que aparece no menu quando a propriedade **Visible** é definida como **true**. Você também pode usar a propriedade [**Enabled**](enabled-property.md) para exibir o comando no menu como desabilitado e o [**HelpContextId**](helpcontextid-property.md) para dar suporte à ajuda de suporte para a propriedade. Defina a chave de acesso para o texto do menu, incluindo um e comercial (&) antes do caractere de texto da configuração de texto da **legenda** .

O servidor adiciona automaticamente aos comandos de menu para abrir a janela de comandos de voz e ocultar o caractere, bem como as legendas de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) de outros clientes do caractere para permitir que os usuários alternem entre clientes. O servidor adiciona automaticamente um separador ao menu entre suas entradas de menu e as definidas pelo cliente. Os separadores aparecem somente quando há itens no menu a serem separados.

Para remover comandos de um menu, use o método [**Remove**](remove-method.md) . Observe que as entradas de menu não são alteradas enquanto o menu é exibido. Se você adicionar ou remover comandos ou alterar suas propriedades, o menu exibirá as alterações quando o usuário reexibir o menu.

Se preferir fornecer seus próprios serviços de menu pop-up para um caractere, você poderá usar a propriedade [**AutoPopupMenu**](autopopupmenu-property.md) para desativar a manipulação de servidor da ação de clique com o botão direito do mouse. Você pode usar a notificação de evento de [**clique**](click-event.md) para criar seu próprio comportamento de manipulação de menu.

Quando o usuário seleciona um comando no menu pop-up de um caractere ou na janela de comandos de voz, o servidor dispara o evento de [**comando**](command-event.md) do cliente associado e retorna os parâmetros da entrada usando o objeto [**userinput**](/windows/desktop/lwef/iagentuserinput) .

O servidor também fornece um menu pop-up para o ícone da barra de tarefas do caractere. Quando o caractere estiver visível, clicar com o botão direito do mouse nesse menu exibirá os mesmos comandos exibidos ao clicar com o botão direito do mouse no caractere. No entanto, quando o caractere está oculto, somente os comandos fornecidos pelo servidor são incluídos.

 

 