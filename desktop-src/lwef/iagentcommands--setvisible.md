---
title: IAgentCommands setVisible
description: IAgentCommands setVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105812044"
---
# <a name="iagentcommandssetvisible"></a>IAgentCommands:: setVisible

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

Define o valor da propriedade [**Visible**](visible-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Um valor booliano que determina a propriedade [**visível**](visible-property.md) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . **Verdadeiro** define a [**legenda**](caption-property.md) da coleção de **comandos** como visível quando o menu pop-up do caractere é exibido; *False* não exibe.

</dd> </dl>

Uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) deve ter sua propriedade [**Caption**](caption-property.md) definida e sua propriedade [**Visible**](visible-property.md) definida como **true** para aparecer no menu pop-up do caractere. A propriedade **Visible** também deve ser definida como **true** para que os comandos na coleção apareçam quando o aplicativo cliente está na entrada-ativo.

## <a name="see-also"></a>Consulte Também

[**IAgentCommands:: getvisível**](iagentcommands--getvisible.md), [ **IAgentCommand:: SetCaption**](iagentcommand--setcaption.md)


 

 