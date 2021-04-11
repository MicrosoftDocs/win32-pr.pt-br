---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160323"
---
# <a name="iagentcharacterexgethelpmodeon"></a>IAgentCharacterEx::GetHelpModeOn

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

Recupera se o modo de ajuda sensível ao contexto está ativado para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*
</dt> <dd>

Endereço de uma variável que recebe **true** se o modo de ajuda estiver ativado para o caractere e **false** se não.

</dd> </dl>

Quando essa propriedade é definida como **true**, o ponteiro do mouse muda para a imagem de ajuda contextual quando movido sobre o caractere ou sobre o menu pop-up para o caractere. Quando o usuário clica ou arrasta o caractere ou clica em um item no menu pop-up do caractere, o servidor dispara o evento [**IAgentNotifySinkEx:: HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) e sai do modo de ajuda.

No modo de ajuda, o servidor não envia os eventos [**IAgentNotifySink:: Click**](iagentnotifysink--click.md), [**IAgentNotifySink::D ragstart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::D Ragcomplete**](iagentnotifysink--dragcomplete.md)e [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) , a menos que [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) Propriedade retorne **true**. Nesse caso, o servidor enviará o evento **IAgentNotifySink:: Click** (não sai do modo de ajuda), mas apenas para o botão direito do mouse para permitir que você exiba o menu pop-up.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)


 

 




