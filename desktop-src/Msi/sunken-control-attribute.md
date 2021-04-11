---
description: Se esse bit for definido, o controle será exibido com uma aparência de baixo relevo, tridimensional.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Atributo de controle de baixo-relevo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c6852a2f32880a427016e41ce9f68314a4a4ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090933"
---
# <a name="sunken-control-attribute"></a><span data-ttu-id="477ee-103">Atributo de controle de baixo-relevo</span><span class="sxs-lookup"><span data-stu-id="477ee-103">Sunken Control Attribute</span></span>

<span data-ttu-id="477ee-104">Se esse bit for definido, o controle será exibido com uma aparência de baixo relevo, tridimensional.</span><span class="sxs-lookup"><span data-stu-id="477ee-104">If this bit is set, the control is displayed with a sunken, three dimensional look.</span></span> <span data-ttu-id="477ee-105">O efeito desse tipo de bit é diferente em diferentes controles e versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="477ee-105">The effect of this style bit is different on different controls and versions of Windows.</span></span> <span data-ttu-id="477ee-106">Em alguns controles, ele não tem efeito visível.</span><span class="sxs-lookup"><span data-stu-id="477ee-106">On some controls it has no visible effect.</span></span> <span data-ttu-id="477ee-107">Se o sistema não oferecer suporte ao atributo de controle de baixo relevo, o controle será exibido no estilo visual padrão.</span><span class="sxs-lookup"><span data-stu-id="477ee-107">If the system does not support the Sunken control attribute, the control is displayed in the default visual style.</span></span> <span data-ttu-id="477ee-108">Se esse bit não for definido, o controle será exibido com o estilo visual padrão.</span><span class="sxs-lookup"><span data-stu-id="477ee-108">If this bit is not set, the control is displayed with the default visual style.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="477ee-109">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="477ee-109">Valid Controls</span></span>

<span data-ttu-id="477ee-110">Todos os controles.</span><span class="sxs-lookup"><span data-stu-id="477ee-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="477ee-111">Valor</span><span class="sxs-lookup"><span data-stu-id="477ee-111">Value</span></span>



| <span data-ttu-id="477ee-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="477ee-112">Decimal</span></span> | <span data-ttu-id="477ee-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="477ee-113">Hexadecimal</span></span> | <span data-ttu-id="477ee-114">Constante</span><span class="sxs-lookup"><span data-stu-id="477ee-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="477ee-115">4</span><span class="sxs-lookup"><span data-stu-id="477ee-115">4</span></span>       | <span data-ttu-id="477ee-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="477ee-116">0x00000004</span></span>  | <span data-ttu-id="477ee-117">**msidbControlAttributesSunken**</span><span class="sxs-lookup"><span data-stu-id="477ee-117">**msidbControlAttributesSunken**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="477ee-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="477ee-118">Remarks</span></span>

<span data-ttu-id="477ee-119">Para definir esse atributo em um controle, inclua o bit de baixo e baixo na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="477ee-119">To set this attribute on a control, include the Sunken bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="477ee-120">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="477ee-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



