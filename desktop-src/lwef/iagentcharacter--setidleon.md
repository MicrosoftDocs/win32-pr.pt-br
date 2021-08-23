---
title: IAgentCharacter setocioso
description: IAgentCharacter setocioso
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde86da6dda12744aedcd780b93d92c45fe2906dd16073bf0e3555848718e747
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665676"
---
# <a name="iagentcharactersetidleon"></a>IAgentCharacter:: setidleion

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

Define o processamento de ociosidade automático para um caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Bno*
</dt> <dd>

Sinalizador de processamento ocioso. Se esse parâmetro for **true**, o Microsoft Agent reproduzirá automaticamente animações de estado **deixar** .

</dd> </dl>

O servidor define automaticamente um tempo limite após a última animação executada para um caractere. Quando o intervalo desse temporizador for concluído, o servidor começará os Estados **deixar** de um caractere, jogando suas animações **deixar** associadas em intervalos regulares. Se você quiser gerenciar as animações de estado **deixar** por conta própria, defina a propriedade como **false**. Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: getidley**](iagentcharacter--getidleon.md)


 

 




