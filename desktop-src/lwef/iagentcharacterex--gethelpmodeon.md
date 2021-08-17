---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb78cf535fbfd7e28ab797c887c8e1548d3fd18dce03fb6b64d888c7e304c0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750781"
---
# <a name="iagentcharacterexgethelpmodeon"></a>IAgentCharacterEx::GetHelpModeOn

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

Recupera se o modo de Ajuda contexttivo está em para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*
</dt> <dd>

Endereço de uma variável que receberá **True se o** modo de Ajuda estiver em para o caractere e **False** se não.

</dd> </dl>

Quando essa propriedade é definida como **True**, o ponteiro do mouse muda para a imagem de Ajuda contextitivo quando movido sobre o caractere ou sobre o menu pop-up para o caractere. Quando o usuário clica ou arrasta o caractere ou clica em um item no menu pop-up do caractere, o servidor dispara o evento [**IAgentNotifySinkEx::HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) e sai do modo de Ajuda.

No modo de Ajuda, o servidor não envia os eventos [**IAgentNotifySink::Click**](iagentnotifysink--click.md), [**IAgentNotifySink::D ragStart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::D ragComplete**](iagentnotifysink--dragcomplete.md)e [**IAgentNotifySink::Command,**](iagentnotifysink--command.md) a menos que a propriedade [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) retorne **True.** Nesse caso, o servidor enviará o evento **IAgentNotifySink::Click** (não sai do modo ajuda), mas apenas para o botão direito do mouse para permitir que você exibe o menu pop-up.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)


 

 




