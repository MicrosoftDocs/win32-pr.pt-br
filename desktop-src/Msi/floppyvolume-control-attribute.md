---
description: Se o bit de controle FloppyVolume for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes de disquete.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Atributo de controle FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502366"
---
# <a name="floppyvolume-control-attribute"></a><span data-ttu-id="80e8b-103">Atributo de controle FloppyVolume</span><span class="sxs-lookup"><span data-stu-id="80e8b-103">FloppyVolume Control Attribute</span></span>

<span data-ttu-id="80e8b-104">Se o bit de controle FloppyVolume for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes de disquete.</span><span class="sxs-lookup"><span data-stu-id="80e8b-104">If the FloppyVolume Control bit is set, the control shows all the volumes involved in the current installation plus all the floppy volumes.</span></span>

<span data-ttu-id="80e8b-105">Se esse bit não estiver definido, o controle listará os volumes na instalação atual.</span><span class="sxs-lookup"><span data-stu-id="80e8b-105">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="80e8b-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="80e8b-106">Valid Controls</span></span>

[<span data-ttu-id="80e8b-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="80e8b-107">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="80e8b-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="80e8b-108">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="80e8b-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="80e8b-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="80e8b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="80e8b-110">Value</span></span>



| <span data-ttu-id="80e8b-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="80e8b-111">Decimal</span></span> | <span data-ttu-id="80e8b-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="80e8b-112">Hexadecimal</span></span> | <span data-ttu-id="80e8b-113">Constante</span><span class="sxs-lookup"><span data-stu-id="80e8b-113">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="80e8b-114">2097152</span><span class="sxs-lookup"><span data-stu-id="80e8b-114">2097152</span></span> | <span data-ttu-id="80e8b-115">0x00200000</span><span class="sxs-lookup"><span data-stu-id="80e8b-115">0x00200000</span></span>  | <span data-ttu-id="80e8b-116">**msidbControlAttributesFloppyVolume**</span><span class="sxs-lookup"><span data-stu-id="80e8b-116">**msidbControlAttributesFloppyVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="80e8b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="80e8b-117">Remarks</span></span>

<span data-ttu-id="80e8b-118">Para definir esse atributo em um controle, inclua o bit FloppyVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="80e8b-118">To set this attribute on a control, include the FloppyVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="80e8b-119">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="80e8b-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



