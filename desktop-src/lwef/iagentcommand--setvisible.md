---
title: IAgentCommand setVisible
description: IAgentCommand setVisible
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105813509"
---
# <a name="iagentcommandsetvisible"></a>IAgentCommand:: setVisible

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

Define o valor da propriedade [**Visible**](visible-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Um valor booliano que determina a propriedade [**visível**](visible-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object). **Verdadeiro** mostra o **comando**; **False** oculta-o.

</dd> </dl>

Um [**comando**](/windows/desktop/lwef/the-command-object) deve ter sua propriedade [**visível**](visible-property.md) definida como **true** e sua propriedade [**Caption**](caption-property.md) definida como aparece no menu pop-up do caractere.

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: getvisível**](iagentcommand--getvisible.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 