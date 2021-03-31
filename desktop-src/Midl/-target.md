---
title: opção /target
description: A opção/target permite que o compilador MIDL habilite otimizações disponíveis somente em versões recentes do Windows. A opção/target ativa automaticamente opções adicionais.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- /Target switch MIDL
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 43c17c6bb06eca94a1738ddc71255cd7cd441c5c
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104011892"
---
# <a name="target-switch"></a><span data-ttu-id="65e50-105">opção /target</span><span class="sxs-lookup"><span data-stu-id="65e50-105">/target switch</span></span>

<span data-ttu-id="65e50-106">A opção **/target** permite que o compilador MIDL habilite otimizações disponíveis somente em versões recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="65e50-106">The **/target** switch enables the MIDL compiler to enable optimizations available only on recent versions of Windows.</span></span> <span data-ttu-id="65e50-107">A opção **/target** ativa automaticamente opções adicionais.</span><span class="sxs-lookup"><span data-stu-id="65e50-107">The **/target** switch automatically activates additional switches.</span></span>

``` syntax
midl /target level
```

## <a name="switch-options"></a><span data-ttu-id="65e50-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="65e50-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="65e50-109">*level*</span><span class="sxs-lookup"><span data-stu-id="65e50-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="65e50-110">Especifica o nível de destino, como NT50, NT51, NT60, NT61, NT62 ou NT100.</span><span class="sxs-lookup"><span data-stu-id="65e50-110">Specifies the target level, such as NT50, NT51, NT60, NT61, NT62, or NT100.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65e50-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="65e50-111">Remarks</span></span>

<span data-ttu-id="65e50-112">A opção **/target** ativa automaticamente opções adicionais, com base no sistema operacional, conforme especificado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="65e50-112">The **/target** switch automatically activates additional switches, based on the operating system, as specified in the following table:</span></span>



| <span data-ttu-id="65e50-113">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="65e50-113">Operating system</span></span> | <span data-ttu-id="65e50-114">nível de/Target</span><span class="sxs-lookup"><span data-stu-id="65e50-114">/target level</span></span> | <span data-ttu-id="65e50-115">Opções ativadas</span><span class="sxs-lookup"><span data-stu-id="65e50-115">Switches Activated</span></span>                     |
|------------------|---------------|----------------------------------------|
| <span data-ttu-id="65e50-116">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="65e50-116">Windows 2000</span></span>     | <span data-ttu-id="65e50-117">NT50</span><span class="sxs-lookup"><span data-stu-id="65e50-117">NT50</span></span>          | <span data-ttu-id="65e50-118">/Oicf/Error All/robust</span><span class="sxs-lookup"><span data-stu-id="65e50-118">/Oicf /error all /robust</span></span>               |
| <span data-ttu-id="65e50-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="65e50-119">Windows XP</span></span>       | <span data-ttu-id="65e50-120">NT51</span><span class="sxs-lookup"><span data-stu-id="65e50-120">NT51</span></span>          | <span data-ttu-id="65e50-121">/Oicf/Error All/robust/Protocol</span><span class="sxs-lookup"><span data-stu-id="65e50-121">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="65e50-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65e50-122">Windows Vista</span></span>    | <span data-ttu-id="65e50-123">NT60</span><span class="sxs-lookup"><span data-stu-id="65e50-123">NT60</span></span>          | <span data-ttu-id="65e50-124">/Oicf/Error All/robust/Protocol</span><span class="sxs-lookup"><span data-stu-id="65e50-124">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="65e50-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="65e50-125">Windows 7</span></span>        | <span data-ttu-id="65e50-126">NT61</span><span class="sxs-lookup"><span data-stu-id="65e50-126">NT61</span></span>          | <span data-ttu-id="65e50-127">/Oicf/Error All/robust/Protocol</span><span class="sxs-lookup"><span data-stu-id="65e50-127">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="65e50-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="65e50-128">Windows 8</span></span>        | <span data-ttu-id="65e50-129">NT62</span><span class="sxs-lookup"><span data-stu-id="65e50-129">NT62</span></span>          | <span data-ttu-id="65e50-130">/Oicf/Error All/robust/Protocol</span><span class="sxs-lookup"><span data-stu-id="65e50-130">/Oicf /error all /robust /protocol all</span></span> |
| <span data-ttu-id="65e50-131">Windows 10</span><span class="sxs-lookup"><span data-stu-id="65e50-131">Windows 10</span></span>       | <span data-ttu-id="65e50-132">NT100</span><span class="sxs-lookup"><span data-stu-id="65e50-132">NT100</span></span>         | <span data-ttu-id="65e50-133">/Oicf/Error All/robust/Protocol</span><span class="sxs-lookup"><span data-stu-id="65e50-133">/Oicf /error all /robust /protocol all</span></span> |
 

<span data-ttu-id="65e50-134">Para garantir que um stub seja executado no sistema especificado pela opção **/target** , o MIDL emite um erro quando um recurso disponível somente em uma versão mais recente do Windows estiver presente.</span><span class="sxs-lookup"><span data-stu-id="65e50-134">To ensure a stub runs on the system specified by the **/target** switch, MIDL issues an error when a feature available only on a more recent version of Windows is present.</span></span> <span data-ttu-id="65e50-135">A tabela a seguir especifica o nível de **/target** mínimo necessário para habilitar o recurso.</span><span class="sxs-lookup"><span data-stu-id="65e50-135">The following table specifies the minimum **/target** level required to enable the feature.</span></span> <span data-ttu-id="65e50-136">Níveis de destino mais altos incluem todos os recursos de níveis de destino inferiores.</span><span class="sxs-lookup"><span data-stu-id="65e50-136">Higher target levels include all features from lower target levels.</span></span>



| <span data-ttu-id="65e50-137">Nível de/Target necessário mínimo</span><span class="sxs-lookup"><span data-stu-id="65e50-137">Minimum required /target level</span></span> | <span data-ttu-id="65e50-138">Recursos</span><span class="sxs-lookup"><span data-stu-id="65e50-138">Features</span></span>                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65e50-139">NT50</span><span class="sxs-lookup"><span data-stu-id="65e50-139">NT50</span></span>                           | <span data-ttu-id="65e50-140">/robust</span><span class="sxs-lookup"><span data-stu-id="65e50-140">/robust</span></span><br/> <span data-ttu-id="65e50-141">\[message\]</span><span class="sxs-lookup"><span data-stu-id="65e50-141">\[message\]</span></span><br/> <span data-ttu-id="65e50-142">\[async\]</span><span class="sxs-lookup"><span data-stu-id="65e50-142">\[async\]</span></span><br/> <span data-ttu-id="65e50-143">\[\_UUID assíncrono\]</span><span class="sxs-lookup"><span data-stu-id="65e50-143">\[async\_uuid\]</span></span><br/> <span data-ttu-id="65e50-144">\[notificar \] no modo/Oicf</span><span class="sxs-lookup"><span data-stu-id="65e50-144">\[notify\] in /Oicf mode</span></span><br/> <span data-ttu-id="65e50-145">\[codificar \] ou \[ decodificar \] no modo/Oicf</span><span class="sxs-lookup"><span data-stu-id="65e50-145">\[encode\] or \[decode\] in /Oicf mode</span></span><br/>                   |
| <span data-ttu-id="65e50-146">NT51</span><span class="sxs-lookup"><span data-stu-id="65e50-146">NT51</span></span>                           | <span data-ttu-id="65e50-147">suporte a/Protocol de 64 bits</span><span class="sxs-lookup"><span data-stu-id="65e50-147">/protocol 64-bit support</span></span><br/> <span data-ttu-id="65e50-148">\[\_ignorar parcial\]</span><span class="sxs-lookup"><span data-stu-id="65e50-148">\[partial\_ignore\]</span></span><br/> <span data-ttu-id="65e50-149">\[forçar \_ alocação\]</span><span class="sxs-lookup"><span data-stu-id="65e50-149">\[force\_allocate\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="65e50-150">NT60</span><span class="sxs-lookup"><span data-stu-id="65e50-150">NT60</span></span>                           | <span data-ttu-id="65e50-151">Marshalling de estrutura complexa forçada</span><span class="sxs-lookup"><span data-stu-id="65e50-151">Forced complex structure marshalling</span></span><br/> <span data-ttu-id="65e50-152">Identificadores de contexto em uma matriz ou estrutura</span><span class="sxs-lookup"><span data-stu-id="65e50-152">Context handles in an array or structure</span></span><br/> <span data-ttu-id="65e50-153">\[\]suporte de intervalo para cadeias de caracteres sem tamanho</span><span class="sxs-lookup"><span data-stu-id="65e50-153">\[range\] support for unsized strings</span></span><br/> <span data-ttu-id="65e50-154">\[tipo \_ de \_ identificador de contexto estrito \_\]</span><span class="sxs-lookup"><span data-stu-id="65e50-154">\[type\_strict\_context\_handle\]</span></span><br/> |
| <span data-ttu-id="65e50-155">NT61</span><span class="sxs-lookup"><span data-stu-id="65e50-155">NT61</span></span>                           | <span data-ttu-id="65e50-156">As chamadas diretas de stub de COM para interfaces com menos de 32 métodos exigem a vinculação de stubs com com **OLE32.DLL**.</span><span class="sxs-lookup"><span data-stu-id="65e50-156">Direct COM stub calls for interfaces with less than 32 methods requires linking COM stubs with **OLE32.DLL**.</span></span><br/>                                                                          |
| <span data-ttu-id="65e50-157">NT62</span><span class="sxs-lookup"><span data-stu-id="65e50-157">NT62</span></span>                           | <span data-ttu-id="65e50-158">Suporte a ARM</span><span class="sxs-lookup"><span data-stu-id="65e50-158">ARM support</span></span><br/> <span data-ttu-id="65e50-159">Suporte do WinRT</span><span class="sxs-lookup"><span data-stu-id="65e50-159">WinRT support</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="65e50-160">NT100</span><span class="sxs-lookup"><span data-stu-id="65e50-160">NT100</span></span>                          | <span data-ttu-id="65e50-161">\[suporte a system_handle \]</span><span class="sxs-lookup"><span data-stu-id="65e50-161">\[system_handle\] support</span></span><br /> |


 

## <a name="examples"></a><span data-ttu-id="65e50-162">Exemplos</span><span class="sxs-lookup"><span data-stu-id="65e50-162">Examples</span></span>

<span data-ttu-id="65e50-163">**MIDL/Target NT50**</span><span class="sxs-lookup"><span data-stu-id="65e50-163">**midl /target NT50**</span></span>

## <a name="see-also"></a><span data-ttu-id="65e50-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="65e50-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e50-165">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="65e50-165">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="65e50-166">**/osf**</span><span class="sxs-lookup"><span data-stu-id="65e50-166">**/osf**</span></span>](-osf.md)
</dt> </dl>
