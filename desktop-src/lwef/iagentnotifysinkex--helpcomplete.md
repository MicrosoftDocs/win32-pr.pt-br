---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6ad0cc7212a7e7bedbcb968f9b9d2a658f520f1a3593595ff03091b03ba32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749558"
---
# <a name="iagentnotifysinkexhelpcomplete"></a>IAgentNotifySinkEx::HelpComplete

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

Notifica um aplicativo cliente quando o usuário seleciona um comando ou caractere para concluir o modo de Ajuda.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere para o qual o modo de Ajuda foi concluído.

</dd> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*Dwcommandid*
</dt> <dd>

Identificador do comando selecionado pelo usuário.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

A causa do evento, que pode ser os seguintes valores:



| Valor                                                                         | Descrição                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **CSHELPCAUSE \_ COMMAND = 1;**<br/>             | O usuário selecionou um comando fornecido pelo seu aplicativo.                            |
| **const unsigned short** **CSHELPCAUSE \_ OTHERPROGRAM = 2;**<br/>        | O usuário selecionou [**o objeto Comandos**](/windows/desktop/lwef/the-commands-collection-object) de outro cliente. |
| **const unsigned short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3;**<br/>  | O usuário selecionou o comando Abrir Comandos de Voz.                                   |
| **const unsigned short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4;**<br/> | O usuário selecionou o comando Fechar Comandos de Voz.                                  |
| **const unsigned short** **CSHELPCAUSE \_ SHOWCHARACTER = 5;**<br/>       | O usuário selecionou o *comando Mostrar CharacterName.*                                  |
| **const unsigned short** **CSHELPCAUSE \_ HIDECHARACTER = 6;**<br/>       | O usuário selecionou o *comando Ocultar CharacterName.*                                  |
| **const unsigned short** **CSHELPCAUSE \_ CHARACTER = 7;**<br/>           | O usuário selecionou (clicou) o caractere.                                           |



 

</dd> </dl>

Normalmente, o modo de Ajuda é concluído quando o usuário clica ou arrasta o caractere ou seleciona um comando no menu pop-up do caractere. Clicar em outro caractere ou em outro lugar na tela não cancela o modo de Ajuda. O cliente que definir o modo de Ajuda para o caractere pode cancelar o modo de Ajuda definindo [**IAgentCharacter::HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) como **False.** (Isso não dispara o **evento IAgentNotifySinkEx::HelpComplete.)**

Quando o usuário seleciona um comando no menu pop-up do caractere no modo ajuda, o servidor remove o menu, chama Ajuda com o [**HelpContextID**](helpcontextid-property.md)especificado do comando e envia esse evento. O contextitivo (também conhecido como O que é isso?) A janela ajuda é exibida no local do ponteiro. Se o usuário selecionar o comando por entrada de voz, a janela Ajuda será exibida sobre o caractere. Se o caractere estiver fora da tela, a janela será exibida na tela mais próxima da posição atual do caractere.

Se o servidor retornar *dwCommandID* como uma cadeia de caracteres vazia (""), isso indicará que o usuário selecionou um comando fornecido pelo servidor.

Esse evento é enviado somente para o aplicativo cliente que coloca o caractere no modo de Ajuda.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)


 

