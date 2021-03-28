---
title: Buffer
description: Buffer
ms.assetid: 7f552b9b-c5fb-4bc2-a7ae-61983379db38
keywords:
- HLSL de buffer
topic_type:
- apiref
api_name:
- Buffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1754272fd90cedc5a806543dd83a99cdcd9455
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364941"
---
# <a name="buffer"></a><span data-ttu-id="28684-104">Buffer</span><span class="sxs-lookup"><span data-stu-id="28684-104">Buffer</span></span>

<span data-ttu-id="28684-105">Tipo de buffer como ele existe no sombreador modelo 4, além de variáveis de recurso e informações de buffer.</span><span class="sxs-lookup"><span data-stu-id="28684-105">Buffer type as it exists in Shader Model 4 plus resource variables and buffer info.</span></span>



| <span data-ttu-id="28684-106">Método</span><span class="sxs-lookup"><span data-stu-id="28684-106">Method</span></span>                                                   | <span data-ttu-id="28684-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="28684-107">Description</span></span>                         |
|----------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="28684-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="28684-108">**GetDimensions**</span></span>](sm5-object-buffer-getdimensions.md) | <span data-ttu-id="28684-109">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="28684-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="28684-110">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="28684-110">**Load**</span></span>](buffer-load.md)                              | <span data-ttu-id="28684-111">Lê dados de buffer.</span><span class="sxs-lookup"><span data-stu-id="28684-111">Reads buffer data.</span></span>                  |
| <span data-ttu-id="28684-112">[**Operador\[\]**](sm5-object-buffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="28684-112">[**Operator\[\]**](sm5-object-buffer-operatorindex.md)</span></span>  | <span data-ttu-id="28684-113">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="28684-113">Gets a read-only resource variable.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="28684-114">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="28684-114">Minimum Shader Model</span></span>

<span data-ttu-id="28684-115">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="28684-115">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="28684-116">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="28684-116">Shader Model</span></span>                                                                | <span data-ttu-id="28684-117">Com suporte</span><span class="sxs-lookup"><span data-stu-id="28684-117">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="28684-118">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="28684-118">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="28684-119">sim</span><span class="sxs-lookup"><span data-stu-id="28684-119">yes</span></span>       |



 

<span data-ttu-id="28684-120">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="28684-120">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="28684-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="28684-121">Vertex</span></span> | <span data-ttu-id="28684-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="28684-122">Hull</span></span> | <span data-ttu-id="28684-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="28684-123">Domain</span></span> | <span data-ttu-id="28684-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="28684-124">Geometry</span></span> | <span data-ttu-id="28684-125">16x16</span><span class="sxs-lookup"><span data-stu-id="28684-125">Pixel</span></span> | <span data-ttu-id="28684-126">Computação</span><span class="sxs-lookup"><span data-stu-id="28684-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="28684-127">x</span><span class="sxs-lookup"><span data-stu-id="28684-127">x</span></span>      | <span data-ttu-id="28684-128">x</span><span class="sxs-lookup"><span data-stu-id="28684-128">x</span></span>    | <span data-ttu-id="28684-129">x</span><span class="sxs-lookup"><span data-stu-id="28684-129">x</span></span>      | <span data-ttu-id="28684-130">x</span><span class="sxs-lookup"><span data-stu-id="28684-130">x</span></span>        | <span data-ttu-id="28684-131">x</span><span class="sxs-lookup"><span data-stu-id="28684-131">x</span></span>     | <span data-ttu-id="28684-132">x</span><span class="sxs-lookup"><span data-stu-id="28684-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="28684-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="28684-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28684-134">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="28684-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




