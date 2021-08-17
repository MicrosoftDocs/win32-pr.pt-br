---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7fbe4cbba7eaed22f49865e1a0f0994c512867fb6f233ef2bbfa01dcaafcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609866"
---
# <a name="iagentcharactergetttsspeed"></a>IAgentCharacter::GetTTSSpeed

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

Recupera a configuração de velocidade de saída do TTS do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*
</dt> <dd>

Endereço de uma variável que recebe a velocidade de saída do caractere em palavras por minuto.

</dd> </dl>

Embora seu aplicativo não possa gravar esse valor, você pode incluir marcas de velocidade no texto de saída que acelerarão temporariamente a saída de um enunciado específico.

Essa propriedade retorna a configuração de velocidade de saída de fala atual para o caractere. Para caracteres que usam a saída TTS, a propriedade retorna a saída TTS real para o caractere. Se o TTS não estiver habilitado ou o caractere não tiver suporte para a saída do TTS, a configuração refletirá a configuração do usuário para a velocidade de saída.

 

 




