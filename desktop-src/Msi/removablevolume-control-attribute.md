---
description: Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes removíveis. Se esse bit não estiver definido, o controle listará os volumes na instalação atual.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Atributo de controle RemovableVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a91a464eb55ee965f12eae9885849eb2080996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647056"
---
# <a name="removablevolume-control-attribute"></a><span data-ttu-id="320fe-104">Atributo de controle RemovableVolume</span><span class="sxs-lookup"><span data-stu-id="320fe-104">RemovableVolume Control Attribute</span></span>

<span data-ttu-id="320fe-105">Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes removíveis.</span><span class="sxs-lookup"><span data-stu-id="320fe-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the removable volumes.</span></span> <span data-ttu-id="320fe-106">Se esse bit não estiver definido, o controle listará os volumes na instalação atual.</span><span class="sxs-lookup"><span data-stu-id="320fe-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="320fe-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="320fe-107">Valid Controls</span></span>

[<span data-ttu-id="320fe-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="320fe-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="320fe-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="320fe-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="320fe-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="320fe-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="320fe-111">Valor</span><span class="sxs-lookup"><span data-stu-id="320fe-111">Value</span></span>



| <span data-ttu-id="320fe-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="320fe-112">Decimal</span></span> | <span data-ttu-id="320fe-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="320fe-113">Hexadecimal</span></span> | <span data-ttu-id="320fe-114">Constante</span><span class="sxs-lookup"><span data-stu-id="320fe-114">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="320fe-115">65536</span><span class="sxs-lookup"><span data-stu-id="320fe-115">65536</span></span>   | <span data-ttu-id="320fe-116">0x00010000</span><span class="sxs-lookup"><span data-stu-id="320fe-116">0x00010000</span></span>  | <span data-ttu-id="320fe-117">**msidbControlAttributesRemovableVolume**</span><span class="sxs-lookup"><span data-stu-id="320fe-117">**msidbControlAttributesRemovableVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="320fe-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="320fe-118">Remarks</span></span>

<span data-ttu-id="320fe-119">Para definir esse atributo em um controle, inclua o bit RemovableVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="320fe-119">To set this attribute on a control, include the RemovableVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="320fe-120">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="320fe-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



