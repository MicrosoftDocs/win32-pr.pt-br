---
title: IAgentCommandWindow GetSize
description: IAgentCommandWindow GetSize
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cf42d98f811905590209b6fed70b28a5728903
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764270"
---
# <a name="iagentcommandwindowgetsize"></a>IAgentCommandWindow::GetSize

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

Recupera o tamanho atual da janela de comandos de voz.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Endereço de uma variável que recebe a largura da janela de comandos de voz em pixels, em relação à origem da tela (superior esquerda).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Endereço de uma variável que recebe a altura da janela de comandos de voz em pixels, em relação à origem da tela (superior esquerda).

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommandWindow:: GetPosition**](iagentcommandwindow--getposition.md)


 

 




