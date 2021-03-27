---
title: Registro de entrada
description: Registro de entrada
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916416"
---
# <a name="input-register"></a><span data-ttu-id="29613-103">Registro de entrada</span><span class="sxs-lookup"><span data-stu-id="29613-103">Input Register</span></span>

<span data-ttu-id="29613-104">Registro de entrada do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="29613-104">Vertex shader input register.</span></span>

<span data-ttu-id="29613-105">Os dados de cada vértice (usando um ou mais fluxos de vértice de entrada) são carregados nos registros de entrada de vértice antes da execução do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="29613-105">Data from each vertex (using one or more input vertex streams) is loaded into the vertex input registers before the vertex shader is run.</span></span> <span data-ttu-id="29613-106">Os registros de entrada consistem em vetores de ponto flutuante de 16 4 componentes, designados como V0 por meio de v15.</span><span class="sxs-lookup"><span data-stu-id="29613-106">The input registers consist of 16 four-component floating-point vectors, designated as v0 through v15.</span></span> <span data-ttu-id="29613-107">Esses registros são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="29613-107">These registers are read-only.</span></span> <span data-ttu-id="29613-108">Um registro de entrada é associado a dados de vértice por meio de uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="29613-108">An input register is bound to vertex data through a vertex declaration.</span></span>

<span data-ttu-id="29613-109">As propriedades de registro a seguir controlam como cada registro se comporta:</span><span class="sxs-lookup"><span data-stu-id="29613-109">The following register properties control how each register behaves:</span></span>



| <span data-ttu-id="29613-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="29613-110">Property</span></span>        | <span data-ttu-id="29613-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="29613-111">Description</span></span>                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="29613-112">Name</span><span class="sxs-lookup"><span data-stu-id="29613-112">Name</span></span>            | <span data-ttu-id="29613-113">v \[ n \] -n é um número de registro opcional.</span><span class="sxs-lookup"><span data-stu-id="29613-113">v\[n\] - n is an optional register number.</span></span> <span data-ttu-id="29613-114">0 é o valor padrão usado, se for omitido.</span><span class="sxs-lookup"><span data-stu-id="29613-114">0 is the default value used, if it is omitted.</span></span>     |
| <span data-ttu-id="29613-115">Contagem</span><span class="sxs-lookup"><span data-stu-id="29613-115">Count</span></span>           | <span data-ttu-id="29613-116">Um máximo de 16 registros, V0-v15.</span><span class="sxs-lookup"><span data-stu-id="29613-116">A maximum of 16 registers, v0 - v15.</span></span>                                                          |
| <span data-ttu-id="29613-117">Permissões de e/s</span><span class="sxs-lookup"><span data-stu-id="29613-117">I/O permissions</span></span> | <span data-ttu-id="29613-118">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="29613-118">Read-only.</span></span> <span data-ttu-id="29613-119">Esse registro não pode ser gravado pela API ou dentro do sombreador.</span><span class="sxs-lookup"><span data-stu-id="29613-119">This register cannot be written by the API or within the shader.</span></span>                   |
| <span data-ttu-id="29613-120">Portas de leitura</span><span class="sxs-lookup"><span data-stu-id="29613-120">Read ports</span></span>      | <span data-ttu-id="29613-121">1. este é o número de vezes que um registro pode ser lido em uma única instrução.</span><span class="sxs-lookup"><span data-stu-id="29613-121">1. This is the number of times a register can be read within a single instruction.</span></span> <span data-ttu-id="29613-122">Veja abaixo.</span><span class="sxs-lookup"><span data-stu-id="29613-122">See below.</span></span> |



 

<span data-ttu-id="29613-123">Qualquer instrução única pode acessar apenas um registro de entrada de vértice.</span><span class="sxs-lookup"><span data-stu-id="29613-123">Any single instruction can access only one vertex input register.</span></span> <span data-ttu-id="29613-124">No entanto, cada fonte na instrução pode Swizzler e negar de forma independente o vetor conforme ele é lido.</span><span class="sxs-lookup"><span data-stu-id="29613-124">However, each source in the instruction can independently swizzle and negate that vector as it is read.</span></span>

## <a name="example"></a><span data-ttu-id="29613-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="29613-125">Example</span></span>

<span data-ttu-id="29613-126">Aqui está um exemplo que usa uma declaração de vértice para associar dados de posição de vértice 2D para registrar V0.</span><span class="sxs-lookup"><span data-stu-id="29613-126">Here is an example using a vertex declaration to bind 2D vertex position data to register v0.</span></span>

<span data-ttu-id="29613-127">A declaração de vértice pertence ao aplicativo:</span><span class="sxs-lookup"><span data-stu-id="29613-127">The vertex declaration belongs in the application:</span></span>


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



<span data-ttu-id="29613-128">Aqui está a declaração de sombreador de vértice correspondente:</span><span class="sxs-lookup"><span data-stu-id="29613-128">Here is the corresponding vertex shader declaration:</span></span>


```
dcl_position v0
```





| <span data-ttu-id="29613-129">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="29613-129">Vertex shader versions</span></span> | <span data-ttu-id="29613-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="29613-130">1\_1</span></span> | <span data-ttu-id="29613-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="29613-131">2\_0</span></span> | <span data-ttu-id="29613-132">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="29613-132">2\_sw</span></span> | <span data-ttu-id="29613-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="29613-133">2\_x</span></span> | <span data-ttu-id="29613-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="29613-134">3\_0</span></span> | <span data-ttu-id="29613-135">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="29613-135">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="29613-136">Registro de posição</span><span class="sxs-lookup"><span data-stu-id="29613-136">Position Register</span></span>      | <span data-ttu-id="29613-137">x</span><span class="sxs-lookup"><span data-stu-id="29613-137">x</span></span>    | <span data-ttu-id="29613-138">x</span><span class="sxs-lookup"><span data-stu-id="29613-138">x</span></span>    | <span data-ttu-id="29613-139">x</span><span class="sxs-lookup"><span data-stu-id="29613-139">x</span></span>     | <span data-ttu-id="29613-140">x</span><span class="sxs-lookup"><span data-stu-id="29613-140">x</span></span>    | <span data-ttu-id="29613-141">x</span><span class="sxs-lookup"><span data-stu-id="29613-141">x</span></span>    | <span data-ttu-id="29613-142">x</span><span class="sxs-lookup"><span data-stu-id="29613-142">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="29613-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29613-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29613-144">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="29613-144">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




