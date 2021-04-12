---
title: IAgentCommands inserir
description: IAgentCommands inserir
ms.assetid: f450aae4-db6f-4326-ae14-ddb68ab0953a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f15df0c24e16a7554881cf3d0e6c41c4ee42b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365917"
---
# <a name="iagentcommandsinsert"></a>IAgentCommands:: Insert

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Insert(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long dwRefID,     // reference Command for insertion
   long dBefore,     // insertion position flag
   long * pdwID      // address for variable for Command ID
);
```

Insere um objeto de [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Um BSTR que especifica o valor do texto de [**legenda**](caption-property.md) exibido para o [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Um BSTR que especifica o valor da configuração de texto de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Uma expressão booliana que especifica a configuração [**habilitada**](enabled-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object). Se o parâmetro for **true**, o **comando** será habilitado e poderá ser selecionado; Se for **false**, o **comando** será desabilitado.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Uma expressão booliana que especifica a configuração [**visível**](visible-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object). Se o parâmetro for **true**, o **comando** ficará visível no menu pop-up do caractere (se a propriedade [**Caption**](caption-property.md) também estiver definida).

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*
</dt> <dd>

A ID de um [**comando**](/windows/desktop/lwef/the-command-object) usado como uma referência para a inserção relativa do novo **comando**.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*
</dt> <dd>

Uma expressão booliana que especifica onde posicionar o [**comando**](/windows/desktop/lwef/the-command-object). Se esse parâmetro for **true**, o novo **comando** será inserido antes do **comando** referenciado; Se for **false**, o novo **comando** será colocado após o **comando** referenciado.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Endereço de uma variável que recebe a ID do [**comando**](/windows/desktop/lwef/the-command-object)inserido.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)


 

 