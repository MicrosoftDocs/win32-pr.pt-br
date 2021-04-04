---
title: IAgentCommands adicionar
description: IAgentCommands adicionar
ms.assetid: f6be7773-77fa-4c59-8feb-c2ebf54fd2e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee56854c302a096143e58fe6c21ef75fedfbf59
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084464"
---
# <a name="iagentcommandsadd"></a>IAgentCommands:: Adicionar

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Add(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long * pdwID      // address for variable for ID
);
```

Adiciona um [**comando**](/windows/desktop/lwef/the-command-object) a uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Um BSTR que especifica o valor do texto de [**legenda**](caption-property.md) exibido para um [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Um BSTR que especifica o valor da configuração de texto de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Uma expressão booliana que especifica a configuração [**habilitada**](enabled-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Se o parâmetro for **true**, o **comando** será habilitado e poderá ser selecionado; Se for **false**, o **comando** será desabilitado.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Uma expressão booliana que especifica a configuração [**visível**](visible-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Se o parâmetro for **true**, o **comando** ficará visível no menu pop-up do caractere (se a propriedade [**Caption**](caption-property.md) também estiver definida).

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Endereço de uma variável que recebe a ID para o [**comando**](/windows/desktop/lwef/the-command-object)adicionado.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: sethabilitated**](iagentcommand--setenabled.md), [**IAgentCommand:: setvisível**](iagentcommand--setvisible.md), [**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)


 

 