---
title: IAgentCharacter GetIdleOn
description: IAgentCharacter GetIdleOn
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a5ce64b39b615325a3de55c1643004cffaeecf89e2e0a024d317bb56e32d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478353"
---
# <a name="iagentcharactergetidleon"></a>IAgentCharacter::GetIdleOn

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

Indica o estado de processamento ocioso automático de um caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Endereço de uma variável que recebe **True se** o servidor do Microsoft Agent reproduz automaticamente animações de estado de **Idling** para um caractere e **False** se não.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)


 

 




