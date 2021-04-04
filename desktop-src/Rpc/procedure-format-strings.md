---
title: Cadeias de caracteres de formato de procedimento
description: A seguir está uma descrição completa da cadeia de caracteres de formato. Ele monta todas as camadas relacionadas a diferentes estágios da evolução do intérprete.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917539"
---
# <a name="procedure-format-strings"></a><span data-ttu-id="74139-104">Cadeias de caracteres de formato de procedimento</span><span class="sxs-lookup"><span data-stu-id="74139-104">Procedure Format Strings</span></span>

<span data-ttu-id="74139-105">A seguir está uma descrição completa da cadeia de caracteres de formato.</span><span class="sxs-lookup"><span data-stu-id="74139-105">The following is a complete format string description.</span></span> <span data-ttu-id="74139-106">Ele monta todas as camadas relacionadas a diferentes estágios da evolução do intérprete.</span><span class="sxs-lookup"><span data-stu-id="74139-106">It assembles all layers related to different stages of the interpreter evolution.</span></span>

## <a name="procedure-descriptor-overview"></a><span data-ttu-id="74139-107">Visão geral do descritor de procedimento</span><span class="sxs-lookup"><span data-stu-id="74139-107">Procedure Descriptor Overview</span></span>

<span data-ttu-id="74139-108">Um descritor de procedimento consiste nos descritores de cabeçalho e nos descritores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="74139-108">A procedure descriptor consists of the header descriptors and the parameter descriptors.</span></span> <span data-ttu-id="74139-109">A descrição do estilo [**– Oi**](/windows/desktop/Midl/-oi) é considerada desatualizada, em termos de uso comum na programação de RPC atual.</span><span class="sxs-lookup"><span data-stu-id="74139-109">The [**–Oi**](/windows/desktop/Midl/-oi) style description is considered outdated, in terms of common usage in current RPC programming.</span></span> <span data-ttu-id="74139-110">O **– OIF** é considerado mais atual.</span><span class="sxs-lookup"><span data-stu-id="74139-110">The **–Oif** is considered more current.</span></span>

## <a name="the-oi-style-description"></a><span data-ttu-id="74139-111">A descrição do estilo – Oi</span><span class="sxs-lookup"><span data-stu-id="74139-111">The –Oi Style Description</span></span>

<span data-ttu-id="74139-112">Essa descrição consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="74139-112">This description consists of the following:</span></span>

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

<span data-ttu-id="74139-113">O cabeçalho teria de 6 a 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="74139-113">The header would have from 6 to 16 bytes.</span></span>

<span data-ttu-id="74139-114">A descrição completa é gerada durante a compilação no modo [**– Oi**](/windows/desktop/Midl/-oi) .</span><span class="sxs-lookup"><span data-stu-id="74139-114">The complete description is generated when compiling in [**–Oi**](/windows/desktop/Midl/-oi) mode.</span></span> <span data-ttu-id="74139-115">No [**– modo do sistema operacional**](/windows/desktop/Midl/-os) , somente os descritores de parâmetro são gerados, que são usados para conversão.</span><span class="sxs-lookup"><span data-stu-id="74139-115">In [**–Os**](/windows/desktop/Midl/-os) mode, only the parameter descriptors are generated, which are used for conversion.</span></span> <span data-ttu-id="74139-116">O intérprete de seleção usa descritores de parâmetro de estilo antigo.</span><span class="sxs-lookup"><span data-stu-id="74139-116">The pickling interpreter uses old style parameter descriptors.</span></span>

## <a name="the-oif-style-description"></a><span data-ttu-id="74139-117">A descrição do estilo – OIF</span><span class="sxs-lookup"><span data-stu-id="74139-117">The –Oif Style Description</span></span>

<span data-ttu-id="74139-118">A descrição consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="74139-118">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

<span data-ttu-id="74139-119">O descritor do cabeçalho de estilo [**– OIF**](/windows/desktop/Midl/-oi) consiste em</span><span class="sxs-lookup"><span data-stu-id="74139-119">The [**–Oif**](/windows/desktop/Midl/-oi) style header descriptor consists of</span></span>

<span data-ttu-id="74139-120">A descrição do estilo – OIF é gerada durante a compilação no modo [**– OIF**](/windows/desktop/Midl/-oi) ou **– Oicf** do compilador.</span><span class="sxs-lookup"><span data-stu-id="74139-120">The –Oif style description is generated when compiling in [**–Oif**](/windows/desktop/Midl/-oi) or **–Oicf** mode of the compiler.</span></span>

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

<span data-ttu-id="74139-121">Alguns recursos mais recentes, como pipe, Async e [**/robust**](/windows/desktop/Midl/-robust) , forçam o modo [**– Oicf**](/windows/desktop/Midl/-oi) do compilador, quando usado.</span><span class="sxs-lookup"><span data-stu-id="74139-121">Some more recent features like pipe, async, and [**/robust**](/windows/desktop/Midl/-robust) force the [**–Oicf**](/windows/desktop/Midl/-oi) mode of the compiler, when used.</span></span>

## <a name="the-extended-oif-description"></a><span data-ttu-id="74139-122">A descrição estendida – OIF</span><span class="sxs-lookup"><span data-stu-id="74139-122">The Extended –Oif Description</span></span>

<span data-ttu-id="74139-123">A descrição consiste no seguinte:</span><span class="sxs-lookup"><span data-stu-id="74139-123">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 