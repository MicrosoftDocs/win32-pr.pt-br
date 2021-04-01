---
description: Se esse bit for definido em um controle de texto, a ocorrência do caractere &\# 0034; &&\# 0034; em uma cadeia de caracteres de texto será exibida como ela mesma. Se esse bit não estiver definido, o caractere seguinte &\# 0034; &&\# 0034; na cadeia de caracteres de texto será exibido como um caractere sublinhado.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: Atributo de controle NoPrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164995"
---
# <a name="noprefix-control-attribute"></a><span data-ttu-id="91ad1-104">Atributo de controle NoPrefix</span><span class="sxs-lookup"><span data-stu-id="91ad1-104">NoPrefix Control Attribute</span></span>

<span data-ttu-id="91ad1-105">Se esse bit for definido em um controle de texto, a ocorrência do caractere "&" em uma cadeia de texto será exibida como a si mesma.</span><span class="sxs-lookup"><span data-stu-id="91ad1-105">If this bit is set on a text control, the occurrence of the character "&" in a text string is displayed as itself.</span></span> <span data-ttu-id="91ad1-106">Se esse bit não estiver definido, o caractere após "&" na cadeia de texto será exibido como um caractere sublinhado.</span><span class="sxs-lookup"><span data-stu-id="91ad1-106">If this bit is not set, then the character following "&" in the text string is displayed as an underscored character.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="91ad1-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="91ad1-107">Valid Controls</span></span>

[<span data-ttu-id="91ad1-108">Text</span><span class="sxs-lookup"><span data-stu-id="91ad1-108">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="91ad1-109">Valor</span><span class="sxs-lookup"><span data-stu-id="91ad1-109">Value</span></span>



| <span data-ttu-id="91ad1-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="91ad1-110">Decimal</span></span> | <span data-ttu-id="91ad1-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="91ad1-111">Hexadecimal</span></span> | <span data-ttu-id="91ad1-112">Constante</span><span class="sxs-lookup"><span data-stu-id="91ad1-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="91ad1-113">131072</span><span class="sxs-lookup"><span data-stu-id="91ad1-113">131072</span></span>  | <span data-ttu-id="91ad1-114">0x20000</span><span class="sxs-lookup"><span data-stu-id="91ad1-114">0x20000</span></span>     | <span data-ttu-id="91ad1-115">**msidbControlAttributesNoPrefix**</span><span class="sxs-lookup"><span data-stu-id="91ad1-115">**msidbControlAttributesNoPrefix**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="91ad1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="91ad1-116">Remarks</span></span>

<span data-ttu-id="91ad1-117">Para definir esse atributo em um controle, inclua o bit NoPrefix na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="91ad1-117">To set this attribute on a control, include the NoPrefix bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="91ad1-118">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="91ad1-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



