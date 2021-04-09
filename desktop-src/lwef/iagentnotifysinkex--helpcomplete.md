---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3b7dbbdf272844242943d49ed86b303d220185
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007420"
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

Notifica um aplicativo cliente quando o usuário seleciona um comando ou caractere para concluir o modo de ajuda.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere para o qual o modo de ajuda foi concluído.

</dd> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificador do comando selecionado pelo usuário.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

A causa do evento, que pode ser os seguintes valores:



| Valor                                                                         | Descrição                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const CSHELPCAUSE curto não assinado** **\_ comando = 1;**<br/>             | O usuário selecionou um comando fornecido pelo seu aplicativo.                            |
| **const CSHELPCAUSE curto não assinado** **\_ OTHERPROGRAM = 2;**<br/>        | O usuário selecionou o objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) de outro cliente. |
| **const CSHELPCAUSE curto não assinado** **\_ OPENCOMMANDSWINDOW = 3;**<br/>  | O usuário selecionou o comando abrir comandos de voz.                                   |
| **const CSHELPCAUSE curto não assinado** **\_ CLOSECOMMANDSWINDOW = 4;**<br/> | O usuário selecionou o comando fechar comandos de voz.                                  |
| **const CSHELPCAUSE curto não assinado** **\_ = 5;**<br/>       | O usuário selecionou o comando Mostrar *caracterename* .                                  |
| **const CSHELPCAUSE curto não assinado** **\_ HIDECHARACTER = 6;**<br/>       | O usuário selecionou o comando Ocultar *caracterename* .                                  |
| **const CSHELPCAUSE caracteres curto não assinado** **\_ = 7;**<br/>           | O usuário selecionou (clicou) o caractere.                                           |



 

</dd> </dl>

Normalmente, o modo de ajuda é concluído quando o usuário clica ou arrasta o caractere ou seleciona um comando no menu pop-up do caractere. Clicar em outro caractere ou em outro lugar na tela não cancela o modo de ajuda. O cliente que define o modo de ajuda para o caractere pode cancelar o modo de ajuda definindo [**IAgentCharacter:: HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) como **false**. (Isso não dispara o evento **IAgentNotifySinkEx:: HelpComplete** .)

Quando o usuário seleciona um comando no menu pop-up do caractere no modo de ajuda, o servidor remove o menu, chama a ajuda com a [**HelpContextId**](helpcontextid-property.md)especificada do comando e envia esse evento. O contexto é contextual (também conhecido como o que é isso?) A janela da ajuda é exibida no local do ponteiro. Se o usuário selecionar o comando por entrada de voz, a janela da ajuda será exibida sobre o caractere. Se o caractere estiver fora da tela, a janela será exibida na tela mais próxima da posição atual do caractere.

Se o servidor retornar *dwCommandID* como uma cadeia de caracteres vazia (""), ele indicará que o usuário selecionou um comando fornecido pelo servidor.

Esse evento é enviado somente para o aplicativo cliente que coloca o caractere no modo de ajuda.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx:: setidentificaçãodocontextodaajuda**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx:: setidentificaçãodocontextodaajuda**](iagentcommandsex--sethelpcontextid.md)


 

