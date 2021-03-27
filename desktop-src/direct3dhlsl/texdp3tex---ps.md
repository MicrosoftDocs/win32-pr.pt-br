---
title: texdp3tex-PS
description: Executa um produto de três componentes e usa o resultado para fazer uma pesquisa de textura 1D.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988557"
---
# <a name="texdp3tex---ps"></a><span data-ttu-id="3c67d-103">texdp3tex-PS</span><span class="sxs-lookup"><span data-stu-id="3c67d-103">texdp3tex - ps</span></span>

<span data-ttu-id="3c67d-104">Executa um produto de três componentes e usa o resultado para fazer uma pesquisa de textura 1D.</span><span class="sxs-lookup"><span data-stu-id="3c67d-104">Performs a three-component dot product and uses the result to do a 1D texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c67d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c67d-105">Syntax</span></span>



| <span data-ttu-id="3c67d-106">texdp3tex DST, src</span><span class="sxs-lookup"><span data-stu-id="3c67d-106">texdp3tex dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="3c67d-107">onde</span><span class="sxs-lookup"><span data-stu-id="3c67d-107">where</span></span>

-   <span data-ttu-id="3c67d-108">DST é o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3c67d-108">dst is the destination register.</span></span>
-   <span data-ttu-id="3c67d-109">src é um registro de origem.</span><span class="sxs-lookup"><span data-stu-id="3c67d-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c67d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c67d-110">Remarks</span></span>



| <span data-ttu-id="3c67d-111">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3c67d-111">Pixel shader versions</span></span> | <span data-ttu-id="3c67d-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="3c67d-112">1\_1</span></span> | <span data-ttu-id="3c67d-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="3c67d-113">1\_2</span></span> | <span data-ttu-id="3c67d-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3c67d-114">1\_3</span></span> | <span data-ttu-id="3c67d-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="3c67d-115">1\_4</span></span> | <span data-ttu-id="3c67d-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c67d-116">2\_0</span></span> | <span data-ttu-id="3c67d-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3c67d-117">2\_x</span></span> | <span data-ttu-id="3c67d-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c67d-118">2\_sw</span></span> | <span data-ttu-id="3c67d-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3c67d-119">3\_0</span></span> | <span data-ttu-id="3c67d-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3c67d-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="3c67d-121">texdp3tex</span><span class="sxs-lookup"><span data-stu-id="3c67d-121">texdp3tex</span></span>             |      | <span data-ttu-id="3c67d-122">x</span><span class="sxs-lookup"><span data-stu-id="3c67d-122">x</span></span>    | <span data-ttu-id="3c67d-123">x</span><span class="sxs-lookup"><span data-stu-id="3c67d-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="3c67d-124">Os registros de textura devem usar a sequência a seguir.</span><span class="sxs-lookup"><span data-stu-id="3c67d-124">Texture registers must use the following sequence.</span></span>


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



<span data-ttu-id="3c67d-125">Veja mais detalhes sobre como o produto e a pesquisa de textura do ponto são feitos.</span><span class="sxs-lookup"><span data-stu-id="3c67d-125">Here is more detail about how the dot product and texture lookup are done.</span></span>

<span data-ttu-id="3c67d-126">A instrução texdp3tex executa um produto de três componentes, ponto.</span><span class="sxs-lookup"><span data-stu-id="3c67d-126">The texdp3tex instruction performs a three-component dot product.</span></span>

<span data-ttu-id="3c67d-127">u ' = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="3c67d-127">u' = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="3c67d-128">O resultado é usado para exemplificar a textura no estágio de textura m executando uma pesquisa 1D.</span><span class="sxs-lookup"><span data-stu-id="3c67d-128">The result is used to sample the texture at texture stage m by performing a 1D lookup.</span></span>

<span data-ttu-id="3c67d-129">t (m)<sub>RGBA</sub> = TextureSample (estágio m)<sub>RGBA</sub> usando (u ', 0, 0) como coordenadas</span><span class="sxs-lookup"><span data-stu-id="3c67d-129">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using (u',0,0) as coordinates</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c67d-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c67d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c67d-131">Instruções do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="3c67d-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




