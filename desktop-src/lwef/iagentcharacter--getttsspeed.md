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
# <a name="iagentcharactergetttsspeed"></a><span data-ttu-id="f5f07-103">IAgentCharacter::GetTTSSpeed</span><span class="sxs-lookup"><span data-stu-id="f5f07-103">IAgentCharacter::GetTTSSpeed</span></span>

<span data-ttu-id="f5f07-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5f07-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

<span data-ttu-id="f5f07-105">Recupera a configuração de velocidade de saída TTS do caractere.</span><span class="sxs-lookup"><span data-stu-id="f5f07-105">Retrieves the character's TTS output speed setting.</span></span>

-   <span data-ttu-id="f5f07-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f5f07-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f5f07-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span><span class="sxs-lookup"><span data-stu-id="f5f07-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="f5f07-108">Endereço de uma variável que recebe a velocidade de saída do caractere em palavras por minuto.</span><span class="sxs-lookup"><span data-stu-id="f5f07-108">Address of a variable that receives the output speed of the character in words per minute.</span></span>

</dd> </dl>

<span data-ttu-id="f5f07-109">Embora seu aplicativo não possa gravar esse valor, você pode incluir marcas de velocidade no texto de saída que acelerará temporariamente a saída para um determinado expressão.</span><span class="sxs-lookup"><span data-stu-id="f5f07-109">Although your application cannot write this value, you can include speed tags in your output text that will temporarily speed up the output for a particular utterance.</span></span>

<span data-ttu-id="f5f07-110">Essa propriedade retorna a configuração de velocidade de saída de fala atual para o caractere.</span><span class="sxs-lookup"><span data-stu-id="f5f07-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="f5f07-111">Para caracteres que usam a saída de TTS, a propriedade retorna a saída de TTS real para o caractere.</span><span class="sxs-lookup"><span data-stu-id="f5f07-111">For characters using TTS output, the property returns the actual TTS output for the character.</span></span> <span data-ttu-id="f5f07-112">Se a TTS não estiver habilitada ou o caractere não oferecer suporte à saída de TTS, a configuração refletirá a configuração de usuário para a velocidade de saída.</span><span class="sxs-lookup"><span data-stu-id="f5f07-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

 

 




