---
title: Registro de posição
description: Este registro de saída do sombreador de vértice contém dados de posição por vértice.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636097"
---
# <a name="position-register"></a><span data-ttu-id="63ae7-103">Registro de posição</span><span class="sxs-lookup"><span data-stu-id="63ae7-103">Position Register</span></span>

<span data-ttu-id="63ae7-104">Este registro de saída do sombreador de vértice contém dados de posição por vértice.</span><span class="sxs-lookup"><span data-stu-id="63ae7-104">This vertex shader output register contains per-vertex position data.</span></span>



| <span data-ttu-id="63ae7-105">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="63ae7-105">Vertex shader versions</span></span> | <span data-ttu-id="63ae7-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="63ae7-106">1\_1</span></span> | <span data-ttu-id="63ae7-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63ae7-107">2\_0</span></span> | <span data-ttu-id="63ae7-108">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="63ae7-108">2\_sw</span></span> | <span data-ttu-id="63ae7-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="63ae7-109">2\_x</span></span> | <span data-ttu-id="63ae7-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63ae7-110">3\_0</span></span> | <span data-ttu-id="63ae7-111">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="63ae7-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="63ae7-112">Registro de posição</span><span class="sxs-lookup"><span data-stu-id="63ae7-112">Position Register</span></span>      | <span data-ttu-id="63ae7-113">x</span><span class="sxs-lookup"><span data-stu-id="63ae7-113">x</span></span>    | <span data-ttu-id="63ae7-114">x</span><span class="sxs-lookup"><span data-stu-id="63ae7-114">x</span></span>    | <span data-ttu-id="63ae7-115">x</span><span class="sxs-lookup"><span data-stu-id="63ae7-115">x</span></span>     | <span data-ttu-id="63ae7-116">x</span><span class="sxs-lookup"><span data-stu-id="63ae7-116">x</span></span>    | <span data-ttu-id="63ae7-117">x</span><span class="sxs-lookup"><span data-stu-id="63ae7-117">x</span></span>    | <span data-ttu-id="63ae7-118">x</span><span class="sxs-lookup"><span data-stu-id="63ae7-118">x</span></span>     |



 

<span data-ttu-id="63ae7-119">Um registro consiste em propriedades que determinam se o registro se comporta.</span><span class="sxs-lookup"><span data-stu-id="63ae7-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="63ae7-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="63ae7-120">Property</span></span>        | <span data-ttu-id="63ae7-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="63ae7-121">Description</span></span> |
|-----------------|-------------|
| <span data-ttu-id="63ae7-122">Name</span><span class="sxs-lookup"><span data-stu-id="63ae7-122">Name</span></span>            | <span data-ttu-id="63ae7-123">oPos</span><span class="sxs-lookup"><span data-stu-id="63ae7-123">oPos</span></span>        |
| <span data-ttu-id="63ae7-124">Contagem</span><span class="sxs-lookup"><span data-stu-id="63ae7-124">Count</span></span>           | <span data-ttu-id="63ae7-125">1 vetor</span><span class="sxs-lookup"><span data-stu-id="63ae7-125">1 vector</span></span>    |
| <span data-ttu-id="63ae7-126">Permissões de e/s</span><span class="sxs-lookup"><span data-stu-id="63ae7-126">I/O permissions</span></span> | <span data-ttu-id="63ae7-127">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="63ae7-127">Write-only.</span></span> |



 

<span data-ttu-id="63ae7-128">O valor é a posição no espaço de recorte homogêneo.</span><span class="sxs-lookup"><span data-stu-id="63ae7-128">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="63ae7-129">Esse valor deve ser gravado pelo sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="63ae7-129">This value must be written by the vertex shader.</span></span>

<span data-ttu-id="63ae7-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="63ae7-130">Example</span></span>


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a><span data-ttu-id="63ae7-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63ae7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63ae7-132">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="63ae7-132">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




