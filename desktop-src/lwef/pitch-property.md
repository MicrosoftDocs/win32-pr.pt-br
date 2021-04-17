---
title: Propriedade pitch
description: Propriedade pitch
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364453"
---
# <a name="pitch-property"></a><span data-ttu-id="2bfae-103">Propriedade pitch</span><span class="sxs-lookup"><span data-stu-id="2bfae-103">Pitch Property</span></span>

<span data-ttu-id="2bfae-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2bfae-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2bfae-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="2bfae-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Description**</span></span> 
</dt> <dd>

<span data-ttu-id="2bfae-106">Retorna um inteiro longo para a configuração de Tom de saída de fala (TTS) do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="2bfae-106">Returns a Long integer for the specified character's speech output (TTS) pitch setting.</span></span>

</dd> <dt>

<span data-ttu-id="2bfae-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="2bfae-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2bfae-108">*agente do ***. Caracteres ("*** characterid \* \* *"). Zumbi**</span><span class="sxs-lookup"><span data-stu-id="2bfae-108">*agent ***.Characters ("*** CharacterID\*\*\*").Pitch*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bfae-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bfae-109">Remarks</span></span>

<span data-ttu-id="2bfae-110">Essa propriedade só se aplica a caracteres configurados para saída de TTS.</span><span class="sxs-lookup"><span data-stu-id="2bfae-110">This property applies only to characters configured for TTS output.</span></span> <span data-ttu-id="2bfae-111">Se o caractere não oferecer suporte à saída de TTS, essa propriedade retornará zero (0).</span><span class="sxs-lookup"><span data-stu-id="2bfae-111">If the character does not support TTS output, this property returns zero (0).</span></span>

<span data-ttu-id="2bfae-112">Embora seu aplicativo não possa gravar esse valor, você pode incluir marcas **Pit** (Pitch) no texto de saída que aumentarão temporariamente o timbre de um determinado expressão.</span><span class="sxs-lookup"><span data-stu-id="2bfae-112">Although your application cannot write this value, you can include **Pit** (pitch) tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="2bfae-113">No entanto, usar a marca **Pit** para alterar a densidade não alterará a configuração da propriedade **pitch** .</span><span class="sxs-lookup"><span data-stu-id="2bfae-113">However, using the **Pit** tag to change the pitch will not change the **Pitch** property setting.</span></span> <span data-ttu-id="2bfae-114">Para obter mais informações, consulte [marcas de saída de fala](pit-tag.md).</span><span class="sxs-lookup"><span data-stu-id="2bfae-114">For further information, see [Speech Output Tags](pit-tag.md).</span></span>

 

 




