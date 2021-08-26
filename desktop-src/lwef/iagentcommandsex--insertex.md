---
title: IAgentCommandsEx InsertEx
description: IAgentCommandsEx InsertEx
ms.assetid: 037c47df-f026-42dc-8c37-2704518d3fd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b43a9e449e16a3be3017a67082da20cb31eb1352a81f699908b0b94267ea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961816"
---
# <a name="iagentcommandsexinsertex"></a>IAgentCommandsEx::InsertEx

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT InsertEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long dwRefID,          // reference Command for insertion
   long dBefore,          // insertion position flag
   long * pdwID           // address for variable for Command ID
);
```

Insere um [**objeto Command**](/windows/desktop/lwef/the-command-object) em uma [**coleção De**](/windows/desktop/lwef/the-commands-collection-object) comandos.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Um BSTR que especifica o valor do texto [**Legenda**](caption-property.md) exibido para o [**Comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Um BSTR que especifica o valor da [**configuração**](voice-property.md) de texto Voz para um [**Comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

Uma BSTR que especifica o valor do texto [**VoiceCaption**](voicecaption-property.md) exibido para um [**Comando**](/windows/desktop/lwef/the-command-object) em uma [**coleção comandos.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Uma expressão booliana que especifica a [**configuração Habilitado**](enabled-property.md) para um [**Comando**](/windows/desktop/lwef/the-command-object). Se o parâmetro for **True**, **o comando** estará habilitado e poderá ser selecionado; se **False**, o **Comando** será desabilitado.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Uma expressão booliana que especifica a [**configuração Visível**](visible-property.md) para um [**Comando**](/windows/desktop/lwef/the-command-object). Se o parâmetro for **True**, **o comando** ficará visível no menu pop-up do caractere (se a propriedade [**Legenda**](caption-property.md) também estiver definida).

</dd> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

O número de contexto do tópico de ajuda associado ao [**objeto Command;**](/windows/desktop/lwef/the-command-object) usado para fornecer Ajuda contextul para o comando.

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*
</dt> <dd>

A ID de um [**comando**](/windows/desktop/lwef/the-command-object) usado como uma referência para a inserção relativa do novo **Comando**.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*
</dt> <dd>

Uma expressão booliana que especifica onde colocar o [**Comando**](/windows/desktop/lwef/the-command-object). Se esse parâmetro for **True,** o novo **Comando** será inserido antes do comando **referenciado**; se **False**, o **novo Comando** será colocado após o Comando **referenciado.**

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Endereço de uma variável que recebe a ID do Comando [**inserido.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

[**IAgentCommandsEx::InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) estende [**IAgentCommands::Insert**](iagentcommands--insert.md) incluindo a [**propriedade HelpContextID.**](helpcontextid-property.md) Você também pode definir a propriedade usando [ **IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)


 

 