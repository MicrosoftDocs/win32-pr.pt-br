---
title: IAgentCharacter GetTTSPitch
description: IAgentCharacter GetTTSPitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781092"
---
# <a name="iagentcharactergetttspitch"></a><span data-ttu-id="1297c-103">IAgentCharacter::GetTTSPitch</span><span class="sxs-lookup"><span data-stu-id="1297c-103">IAgentCharacter::GetTTSPitch</span></span>

<span data-ttu-id="1297c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1297c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

<span data-ttu-id="1297c-105">Recupera a configuração de densidade de saída TTS do caractere.</span><span class="sxs-lookup"><span data-stu-id="1297c-105">Retrieves the character's TTS output pitch setting.</span></span>

-   <span data-ttu-id="1297c-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1297c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1297c-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*</span><span class="sxs-lookup"><span data-stu-id="1297c-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*</span></span>
</dt> <dd>

<span data-ttu-id="1297c-108">Endereço de uma variável que recebe a configuração de densidade de TTS atual do caractere em Hertz.</span><span class="sxs-lookup"><span data-stu-id="1297c-108">Address of a variable that receives the character's current TTS pitch setting in Hertz.</span></span>

</dd> </dl>

<span data-ttu-id="1297c-109">Embora seu aplicativo não possa gravar esse valor, você pode incluir marcas de densidade no texto de saída que aumentarão temporariamente a inclinação de um determinado expressão.</span><span class="sxs-lookup"><span data-stu-id="1297c-109">Although your application cannot write this value, you can include pitch tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="1297c-110">Esse método se aplica somente a caracteres configurados para saída de TTS.</span><span class="sxs-lookup"><span data-stu-id="1297c-110">This method applies only to characters configured for TTS output.</span></span> <span data-ttu-id="1297c-111">Se o mecanismo de síntese de fala (TTS) não estiver habilitado (ou instalado) ou se o caractere não oferecer suporte à saída de TTS, esse método retornará zero (0).</span><span class="sxs-lookup"><span data-stu-id="1297c-111">If the speech synthesis (TTS) engine is not enabled (or installed) or the character does not support TTS output, this method returns zero (0).</span></span>

 

 




