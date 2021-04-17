---
description: Se esse bit for definido, o texto no controle será exibido em uma única linha. Se o texto ultrapassar as margens do controle, ele será truncado e uma reticências (&\# 0034;... &\# 0034;) é inserido no final para indicar o truncamento. Se esse bit não estiver definido, o texto será quebrado.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Atributo de controle NoWrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789769"
---
# <a name="nowrap-control-attribute"></a><span data-ttu-id="6cd76-105">Atributo de controle NoWrap</span><span class="sxs-lookup"><span data-stu-id="6cd76-105">NoWrap Control Attribute</span></span>

<span data-ttu-id="6cd76-106">Se esse bit for definido, o texto no controle será exibido em uma única linha.</span><span class="sxs-lookup"><span data-stu-id="6cd76-106">If this bit is set the text in the control is displayed on a single line.</span></span> <span data-ttu-id="6cd76-107">Se o texto ultrapassar as margens do controle, ele será truncado e uma reticências ("...") será inserida no final para indicar o truncamento.</span><span class="sxs-lookup"><span data-stu-id="6cd76-107">If the text extends beyond the control's margins it is truncated and an ellipsis ("...") is inserted at the end to indicate the truncation.</span></span> <span data-ttu-id="6cd76-108">Se esse bit não estiver definido, o texto será quebrado.</span><span class="sxs-lookup"><span data-stu-id="6cd76-108">If this bit is not set, text wraps.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="6cd76-109">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="6cd76-109">Valid Controls</span></span>

[<span data-ttu-id="6cd76-110">Text</span><span class="sxs-lookup"><span data-stu-id="6cd76-110">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="6cd76-111">Valor</span><span class="sxs-lookup"><span data-stu-id="6cd76-111">Value</span></span>



| <span data-ttu-id="6cd76-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="6cd76-112">Decimal</span></span> | <span data-ttu-id="6cd76-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="6cd76-113">Hexadecimal</span></span> | <span data-ttu-id="6cd76-114">Constante</span><span class="sxs-lookup"><span data-stu-id="6cd76-114">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="6cd76-115">262144</span><span class="sxs-lookup"><span data-stu-id="6cd76-115">262144</span></span>  | <span data-ttu-id="6cd76-116">0x00040000</span><span class="sxs-lookup"><span data-stu-id="6cd76-116">0x00040000</span></span>  | <span data-ttu-id="6cd76-117">**msidbControlAttributesNoWrap**</span><span class="sxs-lookup"><span data-stu-id="6cd76-117">**msidbControlAttributesNoWrap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6cd76-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cd76-118">Remarks</span></span>

<span data-ttu-id="6cd76-119">Para definir esse atributo em um controle, inclua o bit nowrap na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="6cd76-119">To set this attribute on a control, include the NoWrap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="6cd76-120">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="6cd76-120">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



