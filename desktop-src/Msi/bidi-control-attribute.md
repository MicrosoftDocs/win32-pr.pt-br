---
description: Essa é uma combinação da ordem de leitura da direita para a esquerda RTLRO, os atributos RightAligned e LeftScroll.
ms.assetid: 4eaec16f-ee1c-437b-8b76-7ebbdc4e2f71
title: Atributo de controle BiDi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556195c1b3170983083473598f69acb99cdcfaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752862"
---
# <a name="bidi-control-attribute"></a><span data-ttu-id="ff22a-103">Atributo de controle BiDi</span><span class="sxs-lookup"><span data-stu-id="ff22a-103">BiDi Control Attribute</span></span>

<span data-ttu-id="ff22a-104">Essa é uma combinação da ordem de leitura da direita para a esquerda [RTLRO](rtlro-control-attribute.md), os atributos [RightAligned](rightaligned-control-attribute.md)e [LeftScroll](leftscroll-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ff22a-104">This is a combination of the right-to-left reading order [RTLRO](rtlro-control-attribute.md), the [RightAligned](rightaligned-control-attribute.md), and [LeftScroll](leftscroll-control-attribute.md) attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="ff22a-105">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="ff22a-105">Valid Controls</span></span>

[<span data-ttu-id="ff22a-106">ScrollableText</span><span class="sxs-lookup"><span data-stu-id="ff22a-106">ScrollableText</span></span>](scrollabletext-control.md)

 

[<span data-ttu-id="ff22a-107">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="ff22a-107">VolumeCostList</span></span>](volumecostlist-control.md)

 

[<span data-ttu-id="ff22a-108">ComboBox</span><span class="sxs-lookup"><span data-stu-id="ff22a-108">ComboBox</span></span>](combobox-control.md)

 

[<span data-ttu-id="ff22a-109">Directorylist</span><span class="sxs-lookup"><span data-stu-id="ff22a-109">DirectoryList</span></span>](directorylist-control.md)

 

[<span data-ttu-id="ff22a-110">DirectoryCombo</span><span class="sxs-lookup"><span data-stu-id="ff22a-110">DirectoryCombo</span></span>](directorycombo-control.md)

 

[<span data-ttu-id="ff22a-111">Editar</span><span class="sxs-lookup"><span data-stu-id="ff22a-111">Edit</span></span>](edit-control.md)

 

[<span data-ttu-id="ff22a-112">ListBox</span><span class="sxs-lookup"><span data-stu-id="ff22a-112">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="ff22a-113">ListView</span><span class="sxs-lookup"><span data-stu-id="ff22a-113">ListView</span></span>](listview-control.md)

 

[<span data-ttu-id="ff22a-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="ff22a-114">SelectionTree</span></span>](selectiontree-control.md)

 

[<span data-ttu-id="ff22a-115">VolumeSelectCombo</span><span class="sxs-lookup"><span data-stu-id="ff22a-115">VolumeSelectCombo</span></span>](volumeselectcombo-control.md)

## <a name="value"></a><span data-ttu-id="ff22a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ff22a-116">Value</span></span>



| <span data-ttu-id="ff22a-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="ff22a-117">Decimal</span></span> | <span data-ttu-id="ff22a-118">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="ff22a-118">Hexadecimal</span></span> | <span data-ttu-id="ff22a-119">Constante</span><span class="sxs-lookup"><span data-stu-id="ff22a-119">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="ff22a-120">224</span><span class="sxs-lookup"><span data-stu-id="ff22a-120">224</span></span>     | <span data-ttu-id="ff22a-121">0x000000E0</span><span class="sxs-lookup"><span data-stu-id="ff22a-121">0x000000E0</span></span>  | <span data-ttu-id="ff22a-122">**msidbControlAttributesBiDi**</span><span class="sxs-lookup"><span data-stu-id="ff22a-122">**msidbControlAttributesBiDi**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ff22a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff22a-123">Remarks</span></span>

<span data-ttu-id="ff22a-124">Para definir esse atributo em um controle, inclua o bit BiDi na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ff22a-124">To set this attribute on a control, include the BiDi bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="ff22a-125">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="ff22a-125">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



