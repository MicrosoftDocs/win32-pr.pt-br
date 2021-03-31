---
description: Se o bit de controle FixedVolume for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os discos rígidos internos fixos.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Atributo de controle FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827605"
---
# <a name="fixedvolume-control-attribute"></a><span data-ttu-id="5113a-103">Atributo de controle FixedVolume</span><span class="sxs-lookup"><span data-stu-id="5113a-103">FixedVolume Control Attribute</span></span>

<span data-ttu-id="5113a-104">Se o bit de controle FixedVolume for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os discos rígidos internos fixos.</span><span class="sxs-lookup"><span data-stu-id="5113a-104">If the FixedVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the fixed internal hard drives.</span></span>

<span data-ttu-id="5113a-105">Se esse bit não estiver definido, o controle listará os volumes na instalação atual.</span><span class="sxs-lookup"><span data-stu-id="5113a-105">If this bit is not set, the control lists the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="5113a-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="5113a-106">Valid Controls</span></span>

[<span data-ttu-id="5113a-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="5113a-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="5113a-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="5113a-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="5113a-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="5113a-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)



| <span data-ttu-id="5113a-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="5113a-110">Decimal</span></span> | <span data-ttu-id="5113a-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="5113a-111">Hexadecimal</span></span> | <span data-ttu-id="5113a-112">Constante</span><span class="sxs-lookup"><span data-stu-id="5113a-112">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="5113a-113">131072</span><span class="sxs-lookup"><span data-stu-id="5113a-113">131072</span></span>  | <span data-ttu-id="5113a-114">0x00020000</span><span class="sxs-lookup"><span data-stu-id="5113a-114">0x00020000</span></span>  | <span data-ttu-id="5113a-115">**msidbControlAttributesFixedVolume**</span><span class="sxs-lookup"><span data-stu-id="5113a-115">**msidbControlAttributesFixedVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5113a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5113a-116">Remarks</span></span>

<span data-ttu-id="5113a-117">Para definir esse atributo em um controle, inclua o bit FixedVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="5113a-117">To set this attribute on a control, include the FixedVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="5113a-118">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="5113a-118">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



