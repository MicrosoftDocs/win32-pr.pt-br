---
description: Se o bit de controle CDROMVolume for definido, o controle mostrará todos os volumes na instalação atual, além de todos os volumes de CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Atributo de controle CDROMVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749593"
---
# <a name="cdromvolume-control-attribute"></a><span data-ttu-id="2de5e-103">Atributo de controle CDROMVolume</span><span class="sxs-lookup"><span data-stu-id="2de5e-103">CDROMVolume Control Attribute</span></span>

<span data-ttu-id="2de5e-104">Se o bit de controle CDROMVolume for definido, o controle mostrará todos os volumes na instalação atual, além de todos os volumes de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="2de5e-104">If the CDROMVolume Control bit is set, the control shows all the volumes in the current installation plus all the CD-ROM volumes.</span></span>

<span data-ttu-id="2de5e-105">Se esse bit não estiver definido, o controle mostrará todos os volumes na instalação atual.</span><span class="sxs-lookup"><span data-stu-id="2de5e-105">If this bit is not set, the control shows all the volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="2de5e-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="2de5e-106">Valid Controls</span></span>

[<span data-ttu-id="2de5e-107">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="2de5e-107">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="2de5e-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="2de5e-108">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="2de5e-109">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="2de5e-109">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="2de5e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2de5e-110">Value</span></span>



| <span data-ttu-id="2de5e-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="2de5e-111">Decimal</span></span> | <span data-ttu-id="2de5e-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="2de5e-112">Hexadecimal</span></span> | <span data-ttu-id="2de5e-113">Constante</span><span class="sxs-lookup"><span data-stu-id="2de5e-113">Constant</span></span>                              |
|---------|-------------|---------------------------------------|
| <span data-ttu-id="2de5e-114">524288</span><span class="sxs-lookup"><span data-stu-id="2de5e-114">524288</span></span>  | <span data-ttu-id="2de5e-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="2de5e-115">0x00080000</span></span>  | <span data-ttu-id="2de5e-116">**msidbControlAttributesCDROMVolume**</span><span class="sxs-lookup"><span data-stu-id="2de5e-116">**msidbControlAttributesCDROMVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2de5e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2de5e-117">Remarks</span></span>

<span data-ttu-id="2de5e-118">Para definir esse atributo em um controle, inclua o bit CDROMVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="2de5e-118">To set this attribute on a control, include the CDROMVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="2de5e-119">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="2de5e-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



