---
description: Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes de disco de RAM. Se esse bit não estiver definido, o controle listará os volumes na instalação atual.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Atributo de controle RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768721"
---
# <a name="ramdiskvolume-control-attribute"></a><span data-ttu-id="ef577-104">Atributo de controle RAMDiskVolume</span><span class="sxs-lookup"><span data-stu-id="ef577-104">RAMDiskVolume Control Attribute</span></span>

<span data-ttu-id="ef577-105">Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes de disco de RAM.</span><span class="sxs-lookup"><span data-stu-id="ef577-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the RAM disk volumes.</span></span> <span data-ttu-id="ef577-106">Se esse bit não estiver definido, o controle listará os volumes na instalação atual.</span><span class="sxs-lookup"><span data-stu-id="ef577-106">If this bit is not set the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="ef577-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="ef577-107">Valid Controls</span></span>

[<span data-ttu-id="ef577-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="ef577-108">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="ef577-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="ef577-109">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="ef577-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="ef577-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="ef577-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ef577-111">Value</span></span>



| <span data-ttu-id="ef577-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="ef577-112">Decimal</span></span> | <span data-ttu-id="ef577-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="ef577-113">Hexadecimal</span></span> | <span data-ttu-id="ef577-114">Constante</span><span class="sxs-lookup"><span data-stu-id="ef577-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="ef577-115">1048567</span><span class="sxs-lookup"><span data-stu-id="ef577-115">1048567</span></span> | <span data-ttu-id="ef577-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="ef577-116">0x00100000</span></span>  | <span data-ttu-id="ef577-117">**msidbControlAttributesRAMDiskVolume**</span><span class="sxs-lookup"><span data-stu-id="ef577-117">**msidbControlAttributesRAMDiskVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ef577-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef577-118">Remarks</span></span>

<span data-ttu-id="ef577-119">Para definir esse atributo em um controle, inclua o bit RAMDiskVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ef577-119">To set this attribute on a control, include the RAMDiskVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="ef577-120">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="ef577-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



