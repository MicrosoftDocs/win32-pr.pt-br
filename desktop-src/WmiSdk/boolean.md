---
title: booliano (WMI)
description: É um \_ parâmetro VT bool que assume o valor de Variant \_ TRUE (&\# 8211; 1) ou Variant \_ false (0).
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811573"
---
# <a name="boolean-wmi"></a><span data-ttu-id="e8bb6-103">booliano (WMI)</span><span class="sxs-lookup"><span data-stu-id="e8bb6-103">boolean (WMI)</span></span>

<span data-ttu-id="e8bb6-104">O tipo de dados booliano é um \_ parâmetro VT bool que assume o valor de Variant \_ true (– 1) ou Variant \_ false (0).</span><span class="sxs-lookup"><span data-stu-id="e8bb6-104">The boolean data type is a VT\_BOOL parameter that takes on the value of VARIANT\_TRUE (–1) or VARIANT\_FALSE (0).</span></span> <span data-ttu-id="e8bb6-105">A tabela a seguir lista a diferença entre as representações programáticas de **true** lógico em C/C++ e o tipo de automação.</span><span class="sxs-lookup"><span data-stu-id="e8bb6-105">The following table lists the difference between the programmatic representations of logical **TRUE** in C/C++ and the Automation type.</span></span>

| <span data-ttu-id="e8bb6-106">Idioma</span><span class="sxs-lookup"><span data-stu-id="e8bb6-106">Language</span></span>   | <span data-ttu-id="e8bb6-107">Valor</span><span class="sxs-lookup"><span data-stu-id="e8bb6-107">Value</span></span>         | <span data-ttu-id="e8bb6-108">Valor numérico</span><span class="sxs-lookup"><span data-stu-id="e8bb6-108">Numerical value</span></span> |
|------------|---------------|-----------------|
| <span data-ttu-id="e8bb6-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="e8bb6-109">C/C++</span></span>      | <span data-ttu-id="e8bb6-110">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="e8bb6-110">**TRUE**</span></span>      | <span data-ttu-id="e8bb6-111">1</span><span class="sxs-lookup"><span data-stu-id="e8bb6-111">1</span></span>               |
| <span data-ttu-id="e8bb6-112">Automação</span><span class="sxs-lookup"><span data-stu-id="e8bb6-112">Automation</span></span> | <span data-ttu-id="e8bb6-113">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="e8bb6-113">VARIANT\_TRUE</span></span> | <span data-ttu-id="e8bb6-114">– 1</span><span class="sxs-lookup"><span data-stu-id="e8bb6-114">–1</span></span>              |

<span data-ttu-id="e8bb6-115">Os dois tipos são diferentes de zero e, portanto, não são **falsos**, mas têm representações diferentes para **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="e8bb6-115">Both types are nonzero and therefore not **FALSE**, but have different representations for **TRUE**.</span></span>
