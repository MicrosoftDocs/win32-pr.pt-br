---
description: ICE08 valida que a tabela de componentes não contém GUIDs duplicados. Cada componente deve ter um GUID exclusivo. Nenhuma validação será feita se a tabela de componentes não existir.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783270"
---
# <a name="ice08"></a><span data-ttu-id="3856f-105">ICE08</span><span class="sxs-lookup"><span data-stu-id="3856f-105">ICE08</span></span>

<span data-ttu-id="3856f-106">ICE08 valida que a [tabela de componentes](component-table.md) não contém [GUIDs](guid.md)duplicados.</span><span class="sxs-lookup"><span data-stu-id="3856f-106">ICE08 validates that the [Component table](component-table.md) contains no duplicate [GUIDs](guid.md).</span></span> <span data-ttu-id="3856f-107">Cada componente deve ter um GUID exclusivo.</span><span class="sxs-lookup"><span data-stu-id="3856f-107">Every component must have a unique GUID.</span></span> <span data-ttu-id="3856f-108">Nenhuma validação será feita se a tabela de componentes não existir.</span><span class="sxs-lookup"><span data-stu-id="3856f-108">No validation is done if the Component table does not exist.</span></span>

## <a name="result"></a><span data-ttu-id="3856f-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="3856f-109">Result</span></span>

<span data-ttu-id="3856f-110">ICE08 posta uma mensagem de erro se duas ou mais entradas na coluna ComponentID da tabela de componentes contiverem o mesmo GUID.</span><span class="sxs-lookup"><span data-stu-id="3856f-110">ICE08 posts an error message if two or more entries in the ComponentId column of the Component table contain the same GUID.</span></span>

## <a name="example"></a><span data-ttu-id="3856f-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3856f-111">Example</span></span>

<span data-ttu-id="3856f-112">No exemplo a seguir, ICE08 postaria uma mensagem informando que os componentes vermelho e verde têm GUIDs duplicados.</span><span class="sxs-lookup"><span data-stu-id="3856f-112">For the following example, ICE08 would post a message stating that components Red and Green have duplicate GUIDs.</span></span>

<span data-ttu-id="3856f-113">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3856f-113">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="3856f-114">Componente</span><span class="sxs-lookup"><span data-stu-id="3856f-114">Component</span></span> | <span data-ttu-id="3856f-115">ComponentId</span><span class="sxs-lookup"><span data-stu-id="3856f-115">ComponentId</span></span>                            |
|-----------|----------------------------------------|
| <span data-ttu-id="3856f-116">Vermelho</span><span class="sxs-lookup"><span data-stu-id="3856f-116">Red</span></span>       | <span data-ttu-id="3856f-117">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="3856f-117">{0000000A-0003-0000-0000-624474736554}</span></span> |
| <span data-ttu-id="3856f-118">Azul</span><span class="sxs-lookup"><span data-stu-id="3856f-118">Blue</span></span>      | <span data-ttu-id="3856f-119">{0000000A-0003-0000-0000-624474736354}</span><span class="sxs-lookup"><span data-stu-id="3856f-119">{0000000A-0003-0000-0000-624474736354}</span></span> |
| <span data-ttu-id="3856f-120">Verde</span><span class="sxs-lookup"><span data-stu-id="3856f-120">Green</span></span>     | <span data-ttu-id="3856f-121">{0000000A-0003-0000-0000-624474736554}</span><span class="sxs-lookup"><span data-stu-id="3856f-121">{0000000A-0003-0000-0000-624474736554}</span></span> |



 

<span data-ttu-id="3856f-122">Para corrigir esse erro, altere qualquer um dos GUIDs duplicados.</span><span class="sxs-lookup"><span data-stu-id="3856f-122">To fix this error, change either of the duplicate GUIDs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3856f-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3856f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3856f-124">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="3856f-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



