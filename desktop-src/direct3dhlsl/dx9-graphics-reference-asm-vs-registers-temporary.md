---
title: Registro temporário (referência do HLSL VS)
description: Um registro temporário de sombreador de vértice é usado para manter resultados intermediários.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104293612"
---
# <a name="temporary-register-hlsl-vs-reference"></a><span data-ttu-id="7ed38-103">Registro temporário (referência do HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="7ed38-103">Temporary Register (HLSL VS reference)</span></span>

<span data-ttu-id="7ed38-104">Um registro temporário de sombreador de vértice é usado para manter resultados intermediários.</span><span class="sxs-lookup"><span data-stu-id="7ed38-104">A vertex shader temporary register is used to hold intermediate results.</span></span>

<span data-ttu-id="7ed38-105">Um registro temporário deve ser inicializado antes de ser usado.</span><span class="sxs-lookup"><span data-stu-id="7ed38-105">A temporary register must be initialized before it is used.</span></span> <span data-ttu-id="7ed38-106">Cada registro temporário tem acesso de gravação única e de leitura tripla.</span><span class="sxs-lookup"><span data-stu-id="7ed38-106">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="7ed38-107">Isso significa que uma única instrução de sombreador pode usar até três registros temporários como entradas.</span><span class="sxs-lookup"><span data-stu-id="7ed38-107">This means that a single shader instruction can use as many as three temporary registers as inputs.</span></span>

<span data-ttu-id="7ed38-108">Os valores em um registro temporário que permanecem de invocações anteriores do sombreador de vértice não podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="7ed38-108">Values in a temporary register that remain from preceding invocations of the vertex shader cannot be used.</span></span>

<span data-ttu-id="7ed38-109">Um registro consiste em propriedades que determinam se o registro se comporta.</span><span class="sxs-lookup"><span data-stu-id="7ed38-109">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="7ed38-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7ed38-110">Property</span></span>        | <span data-ttu-id="7ed38-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ed38-111">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed38-112">Name</span><span class="sxs-lookup"><span data-stu-id="7ed38-112">Name</span></span>            | <span data-ttu-id="7ed38-113">r \[ n \] .</span><span class="sxs-lookup"><span data-stu-id="7ed38-113">r\[n\].</span></span> <span data-ttu-id="7ed38-114">n é um número de registro opcional.</span><span class="sxs-lookup"><span data-stu-id="7ed38-114">n is an optional register number.</span></span> <span data-ttu-id="7ed38-115">O padrão é 0 e é o valor usado se nenhum valor for especificado.</span><span class="sxs-lookup"><span data-stu-id="7ed38-115">The default is 0, and is the value used if no value is specified.</span></span>                                                                                 |
| <span data-ttu-id="7ed38-116">Contagem</span><span class="sxs-lookup"><span data-stu-id="7ed38-116">Count</span></span>           | <span data-ttu-id="7ed38-117">Um máximo de 12 registros.</span><span class="sxs-lookup"><span data-stu-id="7ed38-117">A maximum of 12 registers.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="7ed38-118">Permissões de e/s</span><span class="sxs-lookup"><span data-stu-id="7ed38-118">I/O permissions</span></span> | <span data-ttu-id="7ed38-119">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7ed38-119">Read/write.</span></span> <span data-ttu-id="7ed38-120">Esse registro pode ser lido ou gravado pela API ou pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="7ed38-120">This register can be read or written by the API or by the shader.</span></span>                                                                                                               |
| <span data-ttu-id="7ed38-121">Portas de leitura</span><span class="sxs-lookup"><span data-stu-id="7ed38-121">Read ports</span></span>      | <span data-ttu-id="7ed38-122">O número de vezes que um registro pode ser lido em uma única instrução é 3.</span><span class="sxs-lookup"><span data-stu-id="7ed38-122">The number of times a register can be read within a single instruction is 3.</span></span> <span data-ttu-id="7ed38-123">Um registro temporário é o único registro que pode ser lido e gravado mais de uma vez em uma única instrução.</span><span class="sxs-lookup"><span data-stu-id="7ed38-123">A temporary register is the only register that can be read and written more than once in a single instruction.</span></span> |



 

<span data-ttu-id="7ed38-124">Cada registro temporário tem acesso de gravação única e de leitura tripla.</span><span class="sxs-lookup"><span data-stu-id="7ed38-124">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="7ed38-125">Portanto, uma instrução pode ter até três registros temporários em seu conjunto de operandos de origem de entrada.</span><span class="sxs-lookup"><span data-stu-id="7ed38-125">Therefore, an instruction can have as many as three temporary registers in its set of input source operands.</span></span>

<span data-ttu-id="7ed38-126">Nenhum valor em um registro temporário que permaneça de invocações precedentes do sombreador de vértice pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="7ed38-126">No values in a temporary register that remain from preceding invocations of the vertex shader can be used.</span></span> <span data-ttu-id="7ed38-127">Os sombreadores de vértice que lêem um valor de um registro temporário antes de gravar nele falharão na chamada à API do Direct3D para criar o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="7ed38-127">Vertex shaders that read a value from a temporary register before writing to it will fail the Direct3D API call to create the vertex shader.</span></span>

## <a name="example"></a><span data-ttu-id="7ed38-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7ed38-128">Example</span></span>

<span data-ttu-id="7ed38-129">Aqui está um exemplo usando um registro temporário:</span><span class="sxs-lookup"><span data-stu-id="7ed38-129">Here is an example using a temporary register:</span></span>


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| <span data-ttu-id="7ed38-130">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7ed38-130">Vertex shader versions</span></span> | <span data-ttu-id="7ed38-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="7ed38-131">1\_1</span></span> | <span data-ttu-id="7ed38-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ed38-132">2\_0</span></span> | <span data-ttu-id="7ed38-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7ed38-133">2\_sw</span></span> | <span data-ttu-id="7ed38-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7ed38-134">2\_x</span></span> | <span data-ttu-id="7ed38-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ed38-135">3\_0</span></span> | <span data-ttu-id="7ed38-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7ed38-136">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="7ed38-137">Registro temporário</span><span class="sxs-lookup"><span data-stu-id="7ed38-137">Temporary Register</span></span>     | <span data-ttu-id="7ed38-138">x</span><span class="sxs-lookup"><span data-stu-id="7ed38-138">x</span></span>    | <span data-ttu-id="7ed38-139">x</span><span class="sxs-lookup"><span data-stu-id="7ed38-139">x</span></span>    | <span data-ttu-id="7ed38-140">x</span><span class="sxs-lookup"><span data-stu-id="7ed38-140">x</span></span>     | <span data-ttu-id="7ed38-141">x</span><span class="sxs-lookup"><span data-stu-id="7ed38-141">x</span></span>    | <span data-ttu-id="7ed38-142">x</span><span class="sxs-lookup"><span data-stu-id="7ed38-142">x</span></span>    | <span data-ttu-id="7ed38-143">x</span><span class="sxs-lookup"><span data-stu-id="7ed38-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="7ed38-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ed38-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed38-145">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7ed38-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




