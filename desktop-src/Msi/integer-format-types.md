---
description: Os tipos de formato inteiro de dados configuráveis podem ser usados nos campos texto ou banco de dados inteiro. O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido. NULL nunca é um valor válido para este tipo.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Tipos de formato de inteiro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662333"
---
# <a name="integer-format-types"></a><span data-ttu-id="69c2e-105">Tipos de formato de inteiro</span><span class="sxs-lookup"><span data-stu-id="69c2e-105">Integer Format Types</span></span>

<span data-ttu-id="69c2e-106">Os tipos de formato inteiro de dados configuráveis podem ser usados nos campos texto ou banco de dados inteiro.</span><span class="sxs-lookup"><span data-stu-id="69c2e-106">The Integer Format Types of configurable data may be used in either text or integer database fields.</span></span> <span data-ttu-id="69c2e-107">O atributo msmConfigItemNonNullable é implícito nesse formato de dados e não precisa ser definido.</span><span class="sxs-lookup"><span data-stu-id="69c2e-107">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="69c2e-108">NULL nunca é um valor válido para este tipo.</span><span class="sxs-lookup"><span data-stu-id="69c2e-108">Null is never a valid value for this type.</span></span>

<span data-ttu-id="69c2e-109">O tipo de formato inteiro a seguir existe.</span><span class="sxs-lookup"><span data-stu-id="69c2e-109">The following Integer Format type exists.</span></span>

[<span data-ttu-id="69c2e-110">Tipo de inteiro arbitrário</span><span class="sxs-lookup"><span data-stu-id="69c2e-110">Arbitrary Integer Type</span></span>](arbitrary-integer-type.md)

<span data-ttu-id="69c2e-111">Os itens configuráveis do tipo de formato inteiro são usados em colunas de texto ou de inteiro e, em geral, podem ser substituídos por qualquer inteiro positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="69c2e-111">Configurable items of the Integer Format Type are used in either text or integer columns and in general could be replaced by any positive or negative integer.</span></span> <span data-ttu-id="69c2e-112">No entanto, determinados itens configuráveis também podem ter restrições semânticas de características.</span><span class="sxs-lookup"><span data-stu-id="69c2e-112">However, particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="69c2e-113">Por exemplo, um item configurável específico necessário para ser um inteiro entre 0 e 100 tem uma restrição semântica adicional.</span><span class="sxs-lookup"><span data-stu-id="69c2e-113">For example, a particular configurable item required to be an integer between 0 and 100 has and additional semantic restriction.</span></span> <span data-ttu-id="69c2e-114">Essas restrições não são impostas por Mergemod.dll e, portanto, os autores de módulo devem estar preparados para lidar com qualquer cadeia de caracteres que satisfaça o tipo de formato inteiro especificado.</span><span class="sxs-lookup"><span data-stu-id="69c2e-114">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Integer Format type.</span></span>

 

 



