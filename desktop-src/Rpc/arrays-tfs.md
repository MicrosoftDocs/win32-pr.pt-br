---
title: Matrizes (RPC)
description: As categorias de matriz de chamada de procedimento remoto (RPC) incluem tamanho fixo, compatível, variável, variável e complexa.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b2c06d8fd5c80294e130424fbf91093145100b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103917926"
---
# <a name="arrays-rpc"></a><span data-ttu-id="7d301-103">Matrizes (RPC)</span><span class="sxs-lookup"><span data-stu-id="7d301-103">Arrays (RPC)</span></span>

<span data-ttu-id="7d301-104">Várias categorias de matriz foram definidas com base em suas características de desempenho, principalmente se a matriz pode ser copiada em bloco.</span><span class="sxs-lookup"><span data-stu-id="7d301-104">Several array categories have been defined based on their performance characteristics, primarily whether the array can be block-copied.</span></span>

<span data-ttu-id="7d301-105">Para algumas categorias, como uma matriz de tamanho fixo, existem dois tipos de descritores de matriz; Eles são indicados por um em correção no nome do token FC à esquerda.</span><span class="sxs-lookup"><span data-stu-id="7d301-105">For some categories, such as a fixed-size array, two types of array descriptors exist; they are indicated by an in-fix in the name of the leading FC token.</span></span>



| <span data-ttu-id="7d301-106">Formatar caractere</span><span class="sxs-lookup"><span data-stu-id="7d301-106">Format character</span></span> | <span data-ttu-id="7d301-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d301-107">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="7d301-108">SM</span><span class="sxs-lookup"><span data-stu-id="7d301-108">SM</span></span>               | <span data-ttu-id="7d301-109">O tamanho total do tipo pode ser representado em um int sem sinal de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7d301-109">The type's total size can be represented in a 16-bit unsigned int.</span></span>    |
| <span data-ttu-id="7d301-110">LG</span><span class="sxs-lookup"><span data-stu-id="7d301-110">LG</span></span>               | <span data-ttu-id="7d301-111">O tamanho total do tipo precisa de um longo de 32 bits sem sinal para ser representado.</span><span class="sxs-lookup"><span data-stu-id="7d301-111">The type's total size needs a 32-bit unsigned long to be represented.</span></span> |



 

<span data-ttu-id="7d301-112">Campos comuns a matrizes:</span><span class="sxs-lookup"><span data-stu-id="7d301-112">Fields common to arrays:</span></span>

-   <span data-ttu-id="7d301-113">\_Tamanho total</span><span class="sxs-lookup"><span data-stu-id="7d301-113">total\_size</span></span>

    <span data-ttu-id="7d301-114">Tamanho total da matriz na memória, em bytes.</span><span class="sxs-lookup"><span data-stu-id="7d301-114">Total size of the array in memory, in bytes.</span></span> <span data-ttu-id="7d301-115">Isso é o mesmo que o tamanho da conexão após o alinhamento.</span><span class="sxs-lookup"><span data-stu-id="7d301-115">This is the same as wire size after alignment.</span></span> <span data-ttu-id="7d301-116">O tamanho total é calculado para categorias para as quais o problema de preenchimento não existe e o tamanho é o tamanho real da matriz.</span><span class="sxs-lookup"><span data-stu-id="7d301-116">The total size is calculated for categories for which the padding issue does not exist and the size is actual array size.</span></span>

-   <span data-ttu-id="7d301-117">tamanho do elemento \_</span><span class="sxs-lookup"><span data-stu-id="7d301-117">element\_size</span></span>

    <span data-ttu-id="7d301-118">Tamanho total na memória de um único elemento da matriz, incluindo o preenchimento (isso pode acontecer apenas para matrizes complexas).</span><span class="sxs-lookup"><span data-stu-id="7d301-118">Total size in memory of a single element of the array, including padding (this may happen for complex arrays only).</span></span>

-   <span data-ttu-id="7d301-119">Descrição do elemento \_</span><span class="sxs-lookup"><span data-stu-id="7d301-119">element\_description</span></span>

    <span data-ttu-id="7d301-120">Descrição do tipo de elemento da matriz.</span><span class="sxs-lookup"><span data-stu-id="7d301-120">Description of the array element type.</span></span>

-   <span data-ttu-id="7d301-121">layout do ponteiro \_</span><span class="sxs-lookup"><span data-stu-id="7d301-121">pointer\_layout</span></span>

    <span data-ttu-id="7d301-122">Consulte o tópico [layout do ponteiro](pointer-layout-tfs.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="7d301-122">See the [Pointer Layout](pointer-layout-tfs.md) topic for more information.</span></span>

## <a name="fixed-sized-arrays"></a><span data-ttu-id="7d301-123">Matrizes de tamanho fixo</span><span class="sxs-lookup"><span data-stu-id="7d301-123">Fixed-sized Arrays</span></span>

<span data-ttu-id="7d301-124">Uma cadeia de formato de matriz de tamanho fixo é gerada para matrizes que têm um tamanho conhecido e, portanto, podem ser copiadas em bloco para o buffer de marshaling.</span><span class="sxs-lookup"><span data-stu-id="7d301-124">A fixed-sized array format string is generated for arrays that have a known size, and therefore may be block-copied to the marshaling buffer.</span></span> <span data-ttu-id="7d301-125">Os dois formatos de descritor de matriz fixos são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="7d301-125">The two fixed array descriptor formats are as follows.</span></span>

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

<span data-ttu-id="7d301-126">e</span><span class="sxs-lookup"><span data-stu-id="7d301-126">and</span></span>

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a><span data-ttu-id="7d301-127">Matriz de conformidade</span><span class="sxs-lookup"><span data-stu-id="7d301-127">Conformant Array</span></span>

<span data-ttu-id="7d301-128">Uma matriz compatível pode ser copiada em bloco depois que o tamanho da matriz é conhecido.</span><span class="sxs-lookup"><span data-stu-id="7d301-128">A conformant array can be block-copied once the size of the array is known.</span></span>

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="7d301-129">A descrição de conformidade \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.</span><span class="sxs-lookup"><span data-stu-id="7d301-129">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="conformant-varying-array"></a><span data-ttu-id="7d301-130">Matriz de variação em conformidade</span><span class="sxs-lookup"><span data-stu-id="7d301-130">Conformant Varying Array</span></span>

<span data-ttu-id="7d301-131">Uma matriz de variação em conformidade também pode ser copiada em bloco.</span><span class="sxs-lookup"><span data-stu-id="7d301-131">A conformant varying array can also be block-copied.</span></span>

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="7d301-132">A descrição de conformidade \_<> e a descrição da variância \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.</span><span class="sxs-lookup"><span data-stu-id="7d301-132">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="varying-array"></a><span data-ttu-id="7d301-133">Matriz variável</span><span class="sxs-lookup"><span data-stu-id="7d301-133">Varying Array</span></span>

<span data-ttu-id="7d301-134">As matrizes variantes têm duas possibilidades, dependendo do tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="7d301-134">The varying arrays have two possibilities depending on the size of the array.</span></span>

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="7d301-135">A descrição da variância \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo do [**/robust**](/windows/desktop/Midl/-robust) que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="7d301-135">The variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on the [**/robust**](/windows/desktop/Midl/-robust) being used.</span></span>

<span data-ttu-id="7d301-136">Para matrizes variáveis inseridas dentro de uma estrutura, o campo deslocamento<2> da \_ Descrição da variância<> é um deslocamento relativo da posição da matriz variável na estrutura até a variação que descreve o campo.</span><span class="sxs-lookup"><span data-stu-id="7d301-136">For varying arrays embedded inside of a structure, the offset<2> field of the variance\_description<> is a relative offset from the varying array's position in the structure to the variance describing field.</span></span> <span data-ttu-id="7d301-137">Normalmente, o deslocamento é relativo ao início da estrutura.</span><span class="sxs-lookup"><span data-stu-id="7d301-137">The offset is typically relative to the beginning of the structure.</span></span>

## <a name="complex-arrays"></a><span data-ttu-id="7d301-138">Matrizes complexas</span><span class="sxs-lookup"><span data-stu-id="7d301-138">Complex Arrays</span></span>

<span data-ttu-id="7d301-139">Uma matriz complexa é qualquer matriz com um elemento que impede que ele seja copiado em bloco e, dessa forma, uma ação adicional precisa ser executada.</span><span class="sxs-lookup"><span data-stu-id="7d301-139">A complex array is any array with an element that prevents it from being block-copied, and as such, additional action needs to be taken.</span></span> <span data-ttu-id="7d301-140">Esses elementos tornam uma matriz complexa:</span><span class="sxs-lookup"><span data-stu-id="7d301-140">These elements make an array complex:</span></span>

-   <span data-ttu-id="7d301-141">tipos simples: ENUM16, \_ \_ INT3264 (somente em plataformas de 64 bits), um integral com \[ [ **intervalo**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="7d301-141">simple types: ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="7d301-142">ponteiros de referência e de interface (todos os ponteiros em plataformas de 64 bits)</span><span class="sxs-lookup"><span data-stu-id="7d301-142">reference and interface pointers (all pointers on 64-bit platforms)</span></span>
-   <span data-ttu-id="7d301-143">uniões</span><span class="sxs-lookup"><span data-stu-id="7d301-143">unions</span></span>
-   <span data-ttu-id="7d301-144">estruturas complexas (consulte o tópico de descrição de estrutura complexa para obter uma lista completa de motivos para uma estrutura ser complexa)</span><span class="sxs-lookup"><span data-stu-id="7d301-144">complex structures (see the Complex Structure Description topic for a full list of reasons for a structure to be complex)</span></span>
-   <span data-ttu-id="7d301-145">elementos definidos com \[ [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] , \[ [**\_ Marshal do usuário**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="7d301-145">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="7d301-146">Todas as matrizes multidimensionais com pelo menos uma dimensão de conformidade e/ou variável são complexas, independentemente do tipo de elemento subjacente.</span><span class="sxs-lookup"><span data-stu-id="7d301-146">All multidimensional arrays with at least one conformant and/or varying dimension are complex regardless of the underlying element type.</span></span>

<span data-ttu-id="7d301-147">A descrição complexa da matriz é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="7d301-147">The complex array description is as follows:</span></span>

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

<span data-ttu-id="7d301-148">O número \_ de \_ elementos<2> campo será zero se a matriz for compatível.</span><span class="sxs-lookup"><span data-stu-id="7d301-148">The number\_of\_elements<2> field is zero if the array is conformant.</span></span>

<span data-ttu-id="7d301-149">A descrição de conformidade \_<> e a descrição da variância \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.</span><span class="sxs-lookup"><span data-stu-id="7d301-149">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="7d301-150">Se a matriz tiver conformidade e/ou variação, a descrição de conformidade \_<> e/ou a descrição da variação \_<> campo (s) terá descrições válidas, caso contrário, os quatro primeiros bytes do descritor de correlação serão definidos como 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="7d301-150">If the array has conformance and/or variance then the conformance\_description<> and/or variance\_description<> field(s) have valid descriptions, otherwise the first 4 bytes of the correlation descriptor are set to 0xFFFFFFFF.</span></span> <span data-ttu-id="7d301-151">Os sinalizadores, quando presentes, são definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="7d301-151">The flags, when present, are set to zero.</span></span>

 

 
