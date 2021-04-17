---
description: Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes remotos. Se esse bit não estiver definido, o controle listará os volumes na instalação atual.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Atributo de controle RemoteVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787071"
---
# <a name="remotevolume-control-attribute"></a><span data-ttu-id="08f60-104">Atributo de controle RemoteVolume</span><span class="sxs-lookup"><span data-stu-id="08f60-104">RemoteVolume Control Attribute</span></span>

<span data-ttu-id="08f60-105">Se esse bit for definido, o controle mostrará todos os volumes envolvidos na instalação atual, além de todos os volumes remotos.</span><span class="sxs-lookup"><span data-stu-id="08f60-105">If this bit is set, the control shows all the volumes involved in the current installation plus all the remote volumes.</span></span> <span data-ttu-id="08f60-106">Se esse bit não estiver definido, o controle listará os volumes na instalação atual.</span><span class="sxs-lookup"><span data-stu-id="08f60-106">If this bit is not set, the control lists volumes in the current installation.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="08f60-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="08f60-107">Valid Controls</span></span>

[<span data-ttu-id="08f60-108">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="08f60-108">DirectoryCombo</span></span>](directorycombo-control.md)

[<span data-ttu-id="08f60-109">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="08f60-109">VolumeCostList</span></span>](volumecostlist-control.md)

[<span data-ttu-id="08f60-110">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="08f60-110">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="08f60-111">Valor</span><span class="sxs-lookup"><span data-stu-id="08f60-111">Value</span></span>



| <span data-ttu-id="08f60-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="08f60-112">Decimal</span></span> | <span data-ttu-id="08f60-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="08f60-113">Hexadecimal</span></span> | <span data-ttu-id="08f60-114">Constante</span><span class="sxs-lookup"><span data-stu-id="08f60-114">Constant</span></span>                               |
|---------|-------------|----------------------------------------|
| <span data-ttu-id="08f60-115">262144</span><span class="sxs-lookup"><span data-stu-id="08f60-115">262144</span></span>  | <span data-ttu-id="08f60-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="08f60-116">0x00040000</span></span>  | <span data-ttu-id="08f60-117">**msidbControlAttributesRemoteVolume**</span><span class="sxs-lookup"><span data-stu-id="08f60-117">**msidbControlAttributesRemoteVolume**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="08f60-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="08f60-118">Remarks</span></span>

<span data-ttu-id="08f60-119">Para definir esse atributo em um controle, inclua o bit RemoteVolume na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="08f60-119">To set this attribute on a control, include the RemoteVolume bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="08f60-120">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="08f60-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



