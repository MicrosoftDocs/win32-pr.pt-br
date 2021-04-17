---
title: Propriedade Speed
description: Propriedade Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798405"
---
# <a name="speed-property"></a><span data-ttu-id="da9a4-103">Propriedade Speed</span><span class="sxs-lookup"><span data-stu-id="da9a4-103">Speed Property</span></span>

<span data-ttu-id="da9a4-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="da9a4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="da9a4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="da9a4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="da9a4-106">Retorna um inteiro longo que especifica a velocidade atual da saída de fala do caractere.</span><span class="sxs-lookup"><span data-stu-id="da9a4-106">Returns a Long integer that specifies the current speed of the character's speech output.</span></span>

</dd> <dt>

<span data-ttu-id="da9a4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="da9a4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="da9a4-108">*agente do ***. Caracteres ("*** characterid \* \* *"). Rápida**</span><span class="sxs-lookup"><span data-stu-id="da9a4-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speed*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da9a4-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="da9a4-109">Remarks</span></span>

<span data-ttu-id="da9a4-110">Essa propriedade retorna a configuração de velocidade de saída de fala atual para o caractere.</span><span class="sxs-lookup"><span data-stu-id="da9a4-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="da9a4-111">Para caracteres que usam a saída de TTS, a propriedade retorna a configuração de saída de TTS real para o caractere.</span><span class="sxs-lookup"><span data-stu-id="da9a4-111">For characters using TTS output, the property returns the actual TTS output setting for the character.</span></span> <span data-ttu-id="da9a4-112">Se a TTS não estiver habilitada ou o caractere não oferecer suporte à saída de TTS, a configuração refletirá a configuração de usuário para a velocidade de saída.</span><span class="sxs-lookup"><span data-stu-id="da9a4-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

<span data-ttu-id="da9a4-113">Embora seu aplicativo não possa gravar esse valor, você pode incluir marcas **SPD** (Speed) no texto de saída que acelerará temporariamente a saída para um determinado expressão.</span><span class="sxs-lookup"><span data-stu-id="da9a4-113">Although your application cannot write this value, you can include **Spd** (speed) tags in your output text that will temporarily speed up the output for a particular utterance.</span></span> <span data-ttu-id="da9a4-114">No entanto, usar a marca **SPD** para alterar a saída falada do caractere não afeta a configuração da propriedade **Speed** .</span><span class="sxs-lookup"><span data-stu-id="da9a4-114">However, using the **Spd** tag to change the character's spoken output does not affect the **Speed** property setting.</span></span> <span data-ttu-id="da9a4-115">Para obter mais informações, consulte [marcas de saída de fala](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="da9a4-115">For further information, see [Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




