---
description: Se esse bit for definido em um controle de edição, o instalador criará um controle de edição de várias linhas com uma barra de rolagem vertical.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Atributo de controle de várias linhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165354"
---
# <a name="multiline-control-attribute"></a><span data-ttu-id="ab5d9-103">Atributo de controle de várias linhas</span><span class="sxs-lookup"><span data-stu-id="ab5d9-103">MultiLine Control Attribute</span></span>

<span data-ttu-id="ab5d9-104">Se esse bit for definido em um [controle de edição](edit-control.md), o instalador criará um controle de edição de várias linhas com uma barra de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="ab5d9-104">If this bit is set on an [Edit control](edit-control.md), the installer creates a multiple line edit control with a vertical scroll bar.</span></span>

<span data-ttu-id="ab5d9-105">Se esse bit não for definido, ele especificará a exibição de um controle de edição normal.</span><span class="sxs-lookup"><span data-stu-id="ab5d9-105">If this bit is not set, it specifies displaying a normal edit control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="ab5d9-106">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="ab5d9-106">Valid Controls</span></span>

<span data-ttu-id="ab5d9-107">[Controle de edição](edit-control.md).</span><span class="sxs-lookup"><span data-stu-id="ab5d9-107">[Edit control](edit-control.md).</span></span>



| <span data-ttu-id="ab5d9-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="ab5d9-108">Decimal</span></span> | <span data-ttu-id="ab5d9-109">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="ab5d9-109">Hexadecimal</span></span> | <span data-ttu-id="ab5d9-110">Constante</span><span class="sxs-lookup"><span data-stu-id="ab5d9-110">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="ab5d9-111">65536</span><span class="sxs-lookup"><span data-stu-id="ab5d9-111">65536</span></span>   | <span data-ttu-id="ab5d9-112">0x00010000</span><span class="sxs-lookup"><span data-stu-id="ab5d9-112">0x00010000</span></span>  | <span data-ttu-id="ab5d9-113">**msidbControlAttributesMultiline**</span><span class="sxs-lookup"><span data-stu-id="ab5d9-113">**msidbControlAttributesMultiline**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ab5d9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab5d9-114">Remarks</span></span>

<span data-ttu-id="ab5d9-115">Para definir esse atributo em um controle, inclua o bit multilinha na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab5d9-115">To set this attribute on a control, include the MultiLine bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="ab5d9-116">Consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="ab5d9-116">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



