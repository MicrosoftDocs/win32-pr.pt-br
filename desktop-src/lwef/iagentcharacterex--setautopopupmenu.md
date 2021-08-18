---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a616bd95836d8f8131aaccabe0bb6db4f35a5caf22c480c17908935d80f2b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477954"
---
# <a name="iagentcharacterexsetautopopupmenu"></a>IAgentCharacterEx::SetAutoPopupMenu

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

Define se o servidor exibe automaticamente o menu pop-up do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*
</dt> <dd>

O sinalizador de exibição de menu pop-up automático. Se esse parâmetro for **True,** o Microsoft Agent exibirá automaticamente o menu pop-up do caractere quando o usuário clicar com o botão direito do mouse no ícone da barra de tarefas do caractere ou do caractere.

</dd> </dl>

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

Ao definir essa propriedade como **False,** você pode criar seu próprio comportamento de manipulação de menu. Para exibir o menu depois de definir essa propriedade como **False,** use o [**método IAgentCharacterEx::ShowPopupMenu.**](iagentcharacterex--showpopupmenu.md)

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx::GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 




