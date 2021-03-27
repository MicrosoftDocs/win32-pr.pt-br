---
title: Registro de coordenadas de textura (referência do HLSL PS)
description: Registro de entrada do sombreador de pixel contendo coordenadas de textura.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104967140"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a><span data-ttu-id="c59cc-103">Registro de coordenadas de textura (referência do HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="c59cc-103">Texture coordinate register (HLSL PS reference)</span></span>

<span data-ttu-id="c59cc-104">Registro de entrada do sombreador de pixel contendo coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c59cc-104">Pixel shader input register containing texture coordinates.</span></span>



| <span data-ttu-id="c59cc-105">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c59cc-105">Pixel shader versions</span></span>       | <span data-ttu-id="c59cc-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="c59cc-106">1\_1</span></span> | <span data-ttu-id="c59cc-107">1\_2</span><span class="sxs-lookup"><span data-stu-id="c59cc-107">1\_2</span></span> | <span data-ttu-id="c59cc-108">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c59cc-108">1\_3</span></span> | <span data-ttu-id="c59cc-109">1\_4</span><span class="sxs-lookup"><span data-stu-id="c59cc-109">1\_4</span></span> | <span data-ttu-id="c59cc-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c59cc-110">2\_0</span></span> | <span data-ttu-id="c59cc-111">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c59cc-111">2\_sw</span></span> | <span data-ttu-id="c59cc-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c59cc-112">2\_x</span></span> | <span data-ttu-id="c59cc-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c59cc-113">3\_0</span></span> | <span data-ttu-id="c59cc-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c59cc-114">3\_sw</span></span> |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="c59cc-115">Registro de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="c59cc-115">Texture Coordinate Register</span></span> |      |      |      |      | <span data-ttu-id="c59cc-116">x</span><span class="sxs-lookup"><span data-stu-id="c59cc-116">x</span></span>    | <span data-ttu-id="c59cc-117">x</span><span class="sxs-lookup"><span data-stu-id="c59cc-117">x</span></span>     | <span data-ttu-id="c59cc-118">x</span><span class="sxs-lookup"><span data-stu-id="c59cc-118">x</span></span>    | <span data-ttu-id="c59cc-119">x</span><span class="sxs-lookup"><span data-stu-id="c59cc-119">x</span></span>    | <span data-ttu-id="c59cc-120">x</span><span class="sxs-lookup"><span data-stu-id="c59cc-120">x</span></span>     |



 

<span data-ttu-id="c59cc-121">Um registro de coordenadas de textura contém dados de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c59cc-121">A texture coordinate register contains texture coordinate data.</span></span> <span data-ttu-id="c59cc-122">Antes que um registro de coordenadas de textura seja usado, ele deve ser declarado por uma declaração de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="c59cc-122">Before a texture coordinate register is used, it must be declared by a pixel shader declaration.</span></span> <span data-ttu-id="c59cc-123">Para obter detalhes sobre como declarar um registro de textura, consulte [DCL-(SM2, SM3-PS ASM)](dcl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="c59cc-123">For details about how to declare a texture register, see [dcl - (sm2, sm3 - ps asm)](dcl---ps.md).</span></span>

<span data-ttu-id="c59cc-124">Além disso, aqui estão algumas outras propriedades de registros de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c59cc-124">In addition, here are some other properties of texture coordinate registers.</span></span>

-   <span data-ttu-id="c59cc-125">Há oito registros de coordenadas de textura de sombreador de pixel, T0 a T7.</span><span class="sxs-lookup"><span data-stu-id="c59cc-125">There are eight pixel-shader texture coordinate registers, t0 to t7.</span></span>
-   <span data-ttu-id="c59cc-126">Esses são registros somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c59cc-126">These are read-only registers.</span></span>
-   <span data-ttu-id="c59cc-127">Eles contêm valores RGBA de quatro componentes iterados a partir de vértices de entrada.</span><span class="sxs-lookup"><span data-stu-id="c59cc-127">They contain four-component RGBA values iterated from input vertices.</span></span>
-   <span data-ttu-id="c59cc-128">Eles contêm alta precisão, altos valores de dados de intervalo dinâmico interpolados dos dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="c59cc-128">They contain high precision, high dynamic range data values interpolated from the vertex data.</span></span> <span data-ttu-id="c59cc-129">Os valores são gerados com a interpolação de perspectiva correta.</span><span class="sxs-lookup"><span data-stu-id="c59cc-129">Values are generated with perspective-correct interpolation.</span></span> <span data-ttu-id="c59cc-130">Os dados são precisão de ponto flutuante e são assinados.</span><span class="sxs-lookup"><span data-stu-id="c59cc-130">Data is floating-point precision, and is signed.</span></span>
-   <span data-ttu-id="c59cc-131">Há um máximo de uma em uma única instrução.</span><span class="sxs-lookup"><span data-stu-id="c59cc-131">There is a maximum of one in a single instruction.</span></span>
-   <span data-ttu-id="c59cc-132">Várias leituras de um registro de coordenadas de textura em um sombreador devem usar [máscara de gravação de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)idêntica.</span><span class="sxs-lookup"><span data-stu-id="c59cc-132">Multiple reads of a texture coordinate register within a shader must use identical [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="c59cc-133">O modificador de precisão parcial opcional \[ \_ PP \] se aplica às leituras dependentes.</span><span class="sxs-lookup"><span data-stu-id="c59cc-133">The optional partial precision modifier \[\_pp\] applies to dependent reads.</span></span> <span data-ttu-id="c59cc-134">Isso ocorre porque a precisão parcial afeta as operações aritméticas que envolvem o registro de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c59cc-134">This is because partial precision affects arithmetic operations involving the texture coordinate register.</span></span> <span data-ttu-id="c59cc-135">Ele não afetará a precisão das instruções de endereço de textura porque não afeta os iteradores de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c59cc-135">It will not affect the precision of texture address instructions because it does not affect the texture coordinate iterators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c59cc-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c59cc-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c59cc-137">Register</span><span class="sxs-lookup"><span data-stu-id="c59cc-137">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




