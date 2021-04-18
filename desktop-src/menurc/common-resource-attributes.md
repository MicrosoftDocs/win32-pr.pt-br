---
title: Atributos de recursos comuns
description: As instruções de definição de recurso com suporte no Windows de 16 bits incluem uma opção Load-mem que especifica as características de carga e memória do recurso.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813590"
---
# <a name="common-resource-attributes"></a><span data-ttu-id="ff3b0-103">Atributos de recursos comuns</span><span class="sxs-lookup"><span data-stu-id="ff3b0-103">Common Resource Attributes</span></span>

<span data-ttu-id="ff3b0-104">As instruções de definição de recurso com suporte no Windows de 16 bits incluem uma opção *Load-mem* que especifica as características de carga e memória do recurso.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-104">The resource-definition statements supported on 16-bit Windows include a *load-mem* option that specifies the loading and memory characteristics of the resource.</span></span> <span data-ttu-id="ff3b0-105">Esses atributos são permitidos em scripts de recurso para compatibilidade com versões anteriores, mas são ignorados.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-105">These attributes are permitted in resource scripts for backward compatibility, but they are ignored.</span></span> <span data-ttu-id="ff3b0-106">Os recursos do Windows são carregados quando o módulo correspondente é carregado e liberados quando o módulo é descarregado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-106">Windows resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

## <a name="load-attributes"></a><span data-ttu-id="ff3b0-107">Carregar atributos</span><span class="sxs-lookup"><span data-stu-id="ff3b0-107">Load Attributes</span></span>

<span data-ttu-id="ff3b0-108">Os atributos de carregamento especificam quando o recurso deve ser carregado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-108">The load attributes specify when the resource is to be loaded.</span></span> <span data-ttu-id="ff3b0-109">O parâmetro de carregamento deve ser um dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-109">The load parameter must be one of the following attributes.</span></span>



| <span data-ttu-id="ff3b0-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="ff3b0-110">Attribute</span></span>      | <span data-ttu-id="ff3b0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff3b0-111">Description</span></span>                                                                  |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ff3b0-112">**CARREGAMENTO**</span><span class="sxs-lookup"><span data-stu-id="ff3b0-112">**PRELOAD**</span></span>    | <span data-ttu-id="ff3b0-113">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-113">Ignored.</span></span> <span data-ttu-id="ff3b0-114">No Windows de 16 bits, o recurso é carregado com o arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-114">In 16-bit Windows, the resource is loaded with the executable file.</span></span> |
| <span data-ttu-id="ff3b0-115">**LOADONCALL**</span><span class="sxs-lookup"><span data-stu-id="ff3b0-115">**LOADONCALL**</span></span> | <span data-ttu-id="ff3b0-116">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-116">Ignored.</span></span> <span data-ttu-id="ff3b0-117">No Windows de 16 bits, o recurso é carregado quando chamado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-117">In 16-bit Windows, the resource is loaded when called.</span></span>              |



 

## <a name="memory-attributes"></a><span data-ttu-id="ff3b0-118">Atributos de memória</span><span class="sxs-lookup"><span data-stu-id="ff3b0-118">Memory Attributes</span></span>

<span data-ttu-id="ff3b0-119">Os atributos de memória especificam se o recurso é fixo ou móvel, se é Descartado e se é puro.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-119">The memory attributes specify whether the resource is fixed or movable, whether it is discardable, and whether it is pure.</span></span> <span data-ttu-id="ff3b0-120">O parâmetro de memória pode ser um ou mais dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-120">The memory parameter can be one or more of the following attributes.</span></span>



| <span data-ttu-id="ff3b0-121">Atributo</span><span class="sxs-lookup"><span data-stu-id="ff3b0-121">Attribute</span></span>       | <span data-ttu-id="ff3b0-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff3b0-122">Description</span></span>                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff3b0-123">**FIXED**</span><span class="sxs-lookup"><span data-stu-id="ff3b0-123">**FIXED**</span></span>       | <span data-ttu-id="ff3b0-124">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-124">Ignored.</span></span> <span data-ttu-id="ff3b0-125">No Windows de 16 bits, o recurso permanece em um local de memória fixa.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-125">In 16-bit Windows, the resource remains at a fixed memory location.</span></span>                                                              |
| <span data-ttu-id="ff3b0-126">**MÓVEL**</span><span class="sxs-lookup"><span data-stu-id="ff3b0-126">**MOVEABLE**</span></span>    | <span data-ttu-id="ff3b0-127">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-127">Ignored.</span></span> <span data-ttu-id="ff3b0-128">No Windows de 16 bits, o recurso pode ser movido, se necessário, para compactar a memória.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-128">In 16-bit Windows, the resource can be moved if necessary to compact memory.</span></span>                                                     |
| <span data-ttu-id="ff3b0-129">**Descartado**</span><span class="sxs-lookup"><span data-stu-id="ff3b0-129">**DISCARDABLE**</span></span> | <span data-ttu-id="ff3b0-130">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-130">Ignored.</span></span> <span data-ttu-id="ff3b0-131">No Windows de 16 bits, o recurso poderá ser Descartado se não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-131">In 16-bit Windows, the resource can be discarded if no longer needed.</span></span>                                                            |
| <span data-ttu-id="ff3b0-132">**MERO**</span><span class="sxs-lookup"><span data-stu-id="ff3b0-132">**PURE**</span></span>        | <span data-ttu-id="ff3b0-133">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-133">Ignored.</span></span> <span data-ttu-id="ff3b0-134">Aceito para compatibilidade com scripts de recursos existentes.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-134">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="ff3b0-135">**IMPUROS**</span><span class="sxs-lookup"><span data-stu-id="ff3b0-135">**IMPURE**</span></span>      | <span data-ttu-id="ff3b0-136">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-136">Ignored.</span></span> <span data-ttu-id="ff3b0-137">Aceito para compatibilidade com scripts de recursos existentes.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-137">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="ff3b0-138">**COMPARTILHADO**</span><span class="sxs-lookup"><span data-stu-id="ff3b0-138">**SHARED**</span></span>      | <span data-ttu-id="ff3b0-139">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-139">Ignored.</span></span> <span data-ttu-id="ff3b0-140">No Windows de 16 bits, SHARED é ignorado para módulos regulares.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-140">In 16-bit Windows, SHARED is ignored for regular modules.</span></span> <span data-ttu-id="ff3b0-141">Para um recurso de um módulo de ROM do Windows, a memória é compartilhada.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-141">For a resource from a ROM Windows module, the memory is shared.</span></span>        |
| <span data-ttu-id="ff3b0-142">**Não compartilhado**</span><span class="sxs-lookup"><span data-stu-id="ff3b0-142">**NONSHARED**</span></span>   | <span data-ttu-id="ff3b0-143">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-143">Ignored.</span></span> <span data-ttu-id="ff3b0-144">No Windows de 16 bits, não compartilhado é ignorado para módulos regulares.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-144">In 16-bit Windows, NONSHARED is ignored for regular modules.</span></span> <span data-ttu-id="ff3b0-145">Para um recurso de um módulo de ROM do Windows, a memória não é compartilhada.</span><span class="sxs-lookup"><span data-stu-id="ff3b0-145">For a resource from a ROM Windows module, the memory is not shared.</span></span> |



 

 

 




