---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551074e1647cffc88e0b5f9f530cea931cd21ff9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364501"
---
# <a name="iagentcharactergetttsspeed"></a>IAgentCharacter::GetTTSSpeed

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

Recupera a configuração de velocidade de saída TTS do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*
</dt> <dd>

Endereço de uma variável que recebe a velocidade de saída do caractere em palavras por minuto.

</dd> </dl>

Embora seu aplicativo não possa gravar esse valor, você pode incluir marcas de velocidade no texto de saída que acelerará temporariamente a saída para um determinado expressão.

Essa propriedade retorna a configuração de velocidade de saída de fala atual para o caractere. Para caracteres que usam a saída de TTS, a propriedade retorna a saída de TTS real para o caractere. Se a TTS não estiver habilitada ou o caractere não oferecer suporte à saída de TTS, a configuração refletirá a configuração de usuário para a velocidade de saída.

 

 




