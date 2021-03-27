---
title: texdp3-PS
description: Executa um produto de três componentes de ponto entre os dados no número de registro de textura e o conjunto de coordenadas de textura correspondente ao número de registro de destino.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64cc14ee66123ea3e25941579b9838977a753174
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293552"
---
# <a name="texdp3---ps"></a><span data-ttu-id="c69aa-103">texdp3-PS</span><span class="sxs-lookup"><span data-stu-id="c69aa-103">texdp3 - ps</span></span>

<span data-ttu-id="c69aa-104">Executa um produto de três componentes de ponto entre os dados no número de registro de textura e o conjunto de coordenadas de textura correspondente ao número de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="c69aa-104">Performs a three-component dot product between data in the texture register number and the texture coordinate set corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c69aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c69aa-105">Syntax</span></span>



| <span data-ttu-id="c69aa-106">texdp3 DST, src</span><span class="sxs-lookup"><span data-stu-id="c69aa-106">texdp3 dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="c69aa-107">onde</span><span class="sxs-lookup"><span data-stu-id="c69aa-107">where</span></span>

-   <span data-ttu-id="c69aa-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="c69aa-108">dst is the destination register.</span></span>
-   <span data-ttu-id="c69aa-109">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="c69aa-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c69aa-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c69aa-110">Remarks</span></span>



| <span data-ttu-id="c69aa-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c69aa-111">Pixel shader versions</span></span> | <span data-ttu-id="c69aa-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="c69aa-112">1\_1</span></span> | <span data-ttu-id="c69aa-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="c69aa-113">1\_2</span></span> | <span data-ttu-id="c69aa-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c69aa-114">1\_3</span></span> | <span data-ttu-id="c69aa-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="c69aa-115">1\_4</span></span> | <span data-ttu-id="c69aa-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c69aa-116">2\_0</span></span> | <span data-ttu-id="c69aa-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c69aa-117">2\_x</span></span> | <span data-ttu-id="c69aa-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c69aa-118">2\_sw</span></span> | <span data-ttu-id="c69aa-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c69aa-119">3\_0</span></span> | <span data-ttu-id="c69aa-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c69aa-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c69aa-121">texdp3</span><span class="sxs-lookup"><span data-stu-id="c69aa-121">texdp3</span></span>                |      | <span data-ttu-id="c69aa-122">x</span><span class="sxs-lookup"><span data-stu-id="c69aa-122">x</span></span>    | <span data-ttu-id="c69aa-123">x</span><span class="sxs-lookup"><span data-stu-id="c69aa-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="c69aa-124">Os registros de textura devem usar a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="c69aa-124">Texture registers must use the following sequence.</span></span>


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



<span data-ttu-id="c69aa-125">Veja mais detalhes sobre como o produto dot é realizado.</span><span class="sxs-lookup"><span data-stu-id="c69aa-125">Here is more detail about how the dot product is accomplished.</span></span>

<span data-ttu-id="c69aa-126">A instrução texdp3 executa um produto de três componentes e o Replica para todos os quatro canais de cores.</span><span class="sxs-lookup"><span data-stu-id="c69aa-126">The texdp3 instruction performs a three-component dot product and replicates it to all four color channels.</span></span>

<span data-ttu-id="c69aa-127">t (m)<sub>RGBA</sub> = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="c69aa-127">t(m)<sub>RGBA</sub> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

## <a name="related-topics"></a><span data-ttu-id="c69aa-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c69aa-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c69aa-129">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="c69aa-129">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




