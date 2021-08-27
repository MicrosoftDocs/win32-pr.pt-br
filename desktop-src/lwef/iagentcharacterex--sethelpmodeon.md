---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacbdf9c0ea9737bb73ba7a99e0839e1435379e42536a82aa30c2ca034a28860
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062026"
---
# <a name="iagentcharacterexsethelpmodeon"></a>IAgentCharacterEx::SetHelpModeOn

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

Define o modo de ajuda contextual para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*
</dt> <dd>

Sinalizador de modo de ajuda. Se esse parâmetro for **true**, o Microsoft Agent ativará o modo de ajuda para o caractere.

</dd> </dl>

Quando você define essa propriedade como **true**, o ponteiro do mouse muda para a imagem de ajuda contextual quando movido sobre o caractere ou sobre o menu pop-up para o caractere. Quando o usuário clica ou arrasta o caractere ou clica em um item no menu pop-up do caractere, o servidor dispara o evento [**IAgentNotifySinkEx:: HelpComplete**](iagentnotifysinkex--helpcomplete.md) e sai do modo de ajuda.

No modo de ajuda, o servidor não envia os eventos de [**clique**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)e [**Command**](command-event.md) , a menos que a propriedade [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) retorne **true**. Nesse caso, o servidor enviará o evento de **clique** (não sai do modo de ajuda), mas apenas para o botão direito do mouse, para que você possa exibir o menu pop-up.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx:: GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [ **IAgentNotifySinkEx:: HelpComplete**](iagentnotifysinkex--helpcomplete.md)


 

 