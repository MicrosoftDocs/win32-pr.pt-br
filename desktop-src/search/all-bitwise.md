---
description: As palavras-chave todos os bits e as chaves bit a bit são usadas para testar o bit em um tipo integral.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: Todos os bits e a bit a bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709db4829f5b620bcb14e0b4261fac7e7d9a6f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501462"
---
# <a name="all-bitwise-and-some-bitwise"></a><span data-ttu-id="9ddfe-103">Todos os bits e a bit a bit</span><span class="sxs-lookup"><span data-stu-id="9ddfe-103">ALL BITWISE and SOME BITWISE</span></span>

<span data-ttu-id="9ddfe-104">As palavras-chave **todos os** **bits e as chaves bit a** bit são usadas para testar o bit em um tipo integral.</span><span class="sxs-lookup"><span data-stu-id="9ddfe-104">The **ALL BITWISE** and **SOME BITWISE** keywords are used for testing the bits in an integral type.</span></span> <span data-ttu-id="9ddfe-105">Se todos os bits de conjunto em uma propriedade corresponderem à máscara, **todos os bit a bit** serão verdadeiros.</span><span class="sxs-lookup"><span data-stu-id="9ddfe-105">If all of the set bits in a property match the mask, **ALL BITWISE** is true.</span></span> <span data-ttu-id="9ddfe-106">Se pelo menos um dos conjuntos de bits em uma propriedade corresponder à máscara, **um** valor de bit que for true será verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="9ddfe-106">If at least one of the set bits in a property matches the mask, **SOME BITWISE** is true.</span></span>

<span data-ttu-id="9ddfe-107">Os operadores podem ser aplicados a Propriedades escalares (valor único) e propriedades de vetor (valores múltiplos).</span><span class="sxs-lookup"><span data-stu-id="9ddfe-107">Operators can be applied to both scalar (single-value) properties and vector (multiple-value) properties.</span></span> <span data-ttu-id="9ddfe-108">O exemplo de código a seguir mostra como testar **valores de propriedade** com **todos os bits** e de bit a bit.</span><span class="sxs-lookup"><span data-stu-id="9ddfe-108">The following code example shows how to test property values with **ALL BITWISE** and **SOME BITWISE**.</span></span>


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a><span data-ttu-id="9ddfe-109">Operadores de comparação</span><span class="sxs-lookup"><span data-stu-id="9ddfe-109">Comparison Operators</span></span>

<span data-ttu-id="9ddfe-110">Os operadores de comparação com suporte para testes de bits BITais são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9ddfe-110">The supported comparison operators for BITWISE tests are listed in the following table.</span></span>



| <span data-ttu-id="9ddfe-111">Operador de comparação</span><span class="sxs-lookup"><span data-stu-id="9ddfe-111">Comparison operator</span></span> | <span data-ttu-id="9ddfe-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ddfe-112">Description</span></span>  |
|---------------------|--------------|
| =                   | <span data-ttu-id="9ddfe-113">Igual a</span><span class="sxs-lookup"><span data-stu-id="9ddfe-113">Equal to</span></span>     |
| <span data-ttu-id="9ddfe-114">! = ou <></span><span class="sxs-lookup"><span data-stu-id="9ddfe-114">!= or <></span></span>      | <span data-ttu-id="9ddfe-115">Não igual a</span><span class="sxs-lookup"><span data-stu-id="9ddfe-115">Not equal to</span></span> |



 

<span data-ttu-id="9ddfe-116">A lógica dos testes em bits é listada na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9ddfe-116">The logic of BITWISE tests is listed in the following table.</span></span>



| <span data-ttu-id="9ddfe-117">Teste e operador de comparação</span><span class="sxs-lookup"><span data-stu-id="9ddfe-117">BITWISE test and comparison operator</span></span> | <span data-ttu-id="9ddfe-118">Lógica</span><span class="sxs-lookup"><span data-stu-id="9ddfe-118">Logic</span></span>                   |
|--------------------------------------|-------------------------|
| <span data-ttu-id="9ddfe-119">= TODOS OS BITS</span><span class="sxs-lookup"><span data-stu-id="9ddfe-119">= ALL BITWISE</span></span>                        | <span data-ttu-id="9ddfe-120">Máscara de & de propriedade = máscara</span><span class="sxs-lookup"><span data-stu-id="9ddfe-120">Property & Mask = Mask</span></span>  |
| <span data-ttu-id="9ddfe-121">= ALGUNS BITS</span><span class="sxs-lookup"><span data-stu-id="9ddfe-121">= SOME BITWISE</span></span>                       | <span data-ttu-id="9ddfe-122">Máscara de & de propriedade! = 0</span><span class="sxs-lookup"><span data-stu-id="9ddfe-122">Property & Mask != 0</span></span>    |
| <span data-ttu-id="9ddfe-123"><> TODOS OS BITS</span><span class="sxs-lookup"><span data-stu-id="9ddfe-123"><> ALL BITWISE</span></span>                 | <span data-ttu-id="9ddfe-124">Máscara de & de propriedade! = máscara</span><span class="sxs-lookup"><span data-stu-id="9ddfe-124">Property & Mask != Mask</span></span> |
| <span data-ttu-id="9ddfe-125"><> ALGUNS BITS</span><span class="sxs-lookup"><span data-stu-id="9ddfe-125"><> SOME BITWISE</span></span>                | <span data-ttu-id="9ddfe-126">Máscara de & de propriedade = 0</span><span class="sxs-lookup"><span data-stu-id="9ddfe-126">Property & Mask = 0</span></span>     |



 

<span data-ttu-id="9ddfe-127">A tabela verdadeira a seguir usa valores binários e hexadecimais de exemplo para demonstrar a lógica de testes bit-a-bit.</span><span class="sxs-lookup"><span data-stu-id="9ddfe-127">The following truth table uses example binary and hex values to demonstate the logic of BITWISE tests.</span></span>



| <span data-ttu-id="9ddfe-128">Propriedade em binary (Hex)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-128">Property in binary (hex)</span></span> | <span data-ttu-id="9ddfe-129">Máscara em binário (Hex)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-129">Mask in binary (hex)</span></span> | <span data-ttu-id="9ddfe-130">Máscara de & de propriedade = binary (Hex)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-130">Property & Mask = binary (hex)</span></span> | <span data-ttu-id="9ddfe-131">= ALGUNS BITS</span><span class="sxs-lookup"><span data-stu-id="9ddfe-131">= SOME BITWISE</span></span> | <span data-ttu-id="9ddfe-132">= TODOS OS BITS</span><span class="sxs-lookup"><span data-stu-id="9ddfe-132">= ALL BITWISE</span></span> |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| <span data-ttu-id="9ddfe-133">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-133">0001 (0x1)</span></span>               | <span data-ttu-id="9ddfe-134">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-134">0001 (0x1)</span></span>           | <span data-ttu-id="9ddfe-135">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-135">0001 (0x1)</span></span>                     | <span data-ttu-id="9ddfe-136">True</span><span class="sxs-lookup"><span data-stu-id="9ddfe-136">True</span></span>           | <span data-ttu-id="9ddfe-137">True</span><span class="sxs-lookup"><span data-stu-id="9ddfe-137">True</span></span>          |
| <span data-ttu-id="9ddfe-138">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-138">0001 (0x1)</span></span>               | <span data-ttu-id="9ddfe-139">0011 (0x3)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-139">0011 (0x3)</span></span>           | <span data-ttu-id="9ddfe-140">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-140">0001 (0x1)</span></span>                     | <span data-ttu-id="9ddfe-141">True</span><span class="sxs-lookup"><span data-stu-id="9ddfe-141">True</span></span>           | <span data-ttu-id="9ddfe-142">Falso</span><span class="sxs-lookup"><span data-stu-id="9ddfe-142">False</span></span>         |
| <span data-ttu-id="9ddfe-143">0011 (0x3)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-143">0011 (0x3)</span></span>               | <span data-ttu-id="9ddfe-144">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-144">0001 (0x1)</span></span>           | <span data-ttu-id="9ddfe-145">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-145">0001 (0x1)</span></span>                     | <span data-ttu-id="9ddfe-146">True</span><span class="sxs-lookup"><span data-stu-id="9ddfe-146">True</span></span>           | <span data-ttu-id="9ddfe-147">True</span><span class="sxs-lookup"><span data-stu-id="9ddfe-147">True</span></span>          |
| <span data-ttu-id="9ddfe-148">0010 (0x2)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-148">0010 (0x2)</span></span>               | <span data-ttu-id="9ddfe-149">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-149">0001 (0x1)</span></span>           | <span data-ttu-id="9ddfe-150">0000 (0x0)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-150">0000 (0x0)</span></span>                     | <span data-ttu-id="9ddfe-151">Falso</span><span class="sxs-lookup"><span data-stu-id="9ddfe-151">False</span></span>          | <span data-ttu-id="9ddfe-152">Falso</span><span class="sxs-lookup"><span data-stu-id="9ddfe-152">False</span></span>         |
| <span data-ttu-id="9ddfe-153">11110000 (0xF0)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-153">11110000 (0xF0)</span></span>          | <span data-ttu-id="9ddfe-154">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-154">00000011 (0x03)</span></span>      | <span data-ttu-id="9ddfe-155">00000000 (0x00)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-155">00000000 (0x00)</span></span>                | <span data-ttu-id="9ddfe-156">Falso</span><span class="sxs-lookup"><span data-stu-id="9ddfe-156">False</span></span>          | <span data-ttu-id="9ddfe-157">Falso</span><span class="sxs-lookup"><span data-stu-id="9ddfe-157">False</span></span>         |
| <span data-ttu-id="9ddfe-158">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-158">11110010 (0xF2)</span></span>          | <span data-ttu-id="9ddfe-159">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-159">11110010 (0xF2)</span></span>      | <span data-ttu-id="9ddfe-160">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-160">11110010 (0xF2)</span></span>                | <span data-ttu-id="9ddfe-161">True</span><span class="sxs-lookup"><span data-stu-id="9ddfe-161">True</span></span>           | <span data-ttu-id="9ddfe-162">True</span><span class="sxs-lookup"><span data-stu-id="9ddfe-162">True</span></span>          |
| <span data-ttu-id="9ddfe-163">11110010 (0xF2)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-163">11110010 (0xF2)</span></span>          | <span data-ttu-id="9ddfe-164">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-164">00000011 (0x03)</span></span>      | <span data-ttu-id="9ddfe-165">00000010 (0x02)</span><span class="sxs-lookup"><span data-stu-id="9ddfe-165">00000010 (0x02)</span></span>                | <span data-ttu-id="9ddfe-166">True</span><span class="sxs-lookup"><span data-stu-id="9ddfe-166">True</span></span>           | <span data-ttu-id="9ddfe-167">Falso</span><span class="sxs-lookup"><span data-stu-id="9ddfe-167">False</span></span>         |



 

## <a name="example"></a><span data-ttu-id="9ddfe-168">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9ddfe-168">Example</span></span>

<span data-ttu-id="9ddfe-169">Veja a seguir um exemplo de predicado **All bit a bit** .</span><span class="sxs-lookup"><span data-stu-id="9ddfe-169">The following is an example of the **ALL BITWISE** predicate.</span></span>


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a><span data-ttu-id="9ddfe-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ddfe-170">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9ddfe-171">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="9ddfe-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ddfe-172">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="9ddfe-172">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="9ddfe-173">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="9ddfe-173">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



