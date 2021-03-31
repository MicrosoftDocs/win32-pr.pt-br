---
title: IAgentCharacter getociosidade
description: IAgentCharacter getociosidade
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637266"
---
# <a name="iagentcharactergetidleon"></a>IAgentCharacter:: getidley

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

Indica o estado de processamento de ociosidade automático para um caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Endereço de uma variável que recebe **true** se o servidor do Microsoft Agent reproduzir automaticamente animações de estado **deixar** para um caractere e **false** se não.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: setidleion**](iagentcharacter--setidleon.md)


 

 




