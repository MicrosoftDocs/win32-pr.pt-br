---
title: Getvoice IAgentCommand
description: Getvoice IAgentCommand
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105782663"
---
# <a name="iagentcommandgetvoice"></a>IAgentCommand:: getvoice

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

Recupera o valor da propriedade de texto de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

O endereço de um BSTR que recebe a propriedade de texto de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Um [**comando**](/windows/desktop/lwef/the-command-object) com seu conjunto de propriedades de [**voz**](voice-property.md) e sua propriedade [**Enabled**](enabled-property.md) definida como **true** serão acessíveis por voz. Se sua propriedade [**Caption**](caption-property.md) também for definida, ela aparecerá na janela comandos de voz. Se sua propriedade [**Visible**](visible-property.md) for definida como **true**, ela aparecerá no menu pop-up do caractere.

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 