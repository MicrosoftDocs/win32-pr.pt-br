---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822799"
---
# <a name="iagentcharacterexshowpopupmenu"></a>IAgentCharacterEx::ShowPopupMenu

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

Exibe o menu pop-up do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="x"></span><span id="X"></span>*w.x.y.*
</dt> <dd>

A coordenada x do menu pop-up do caractere em pixels, em relação à origem da tela (superior esquerda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Iar*
</dt> <dd>

A coordenada y do menu pop-up do caractere em pixels, em relação à origem da tela (superior esquerda).

</dd> </dl>

Quando você define [**IAgentCharacterEx:: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) como **false**, o servidor não exibe mais automaticamente o menu quando o caractere ou o ícone da barra de tarefas é clicado com o botão direito do mouse. Você pode usar esse método para exibir o menu.

O menu é exibido até que o usuário selecione um comando ou exiba outro menu. Somente um menu pop-up pode ser exibido de cada vez; Portanto, as chamadas para esse método irão cancelar (remover) o menu anterior.

Esse método deve ser chamado somente quando o aplicativo cliente é o cliente ativo do caractere; caso contrário, ele falhará.

[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)

 

 




