---
title: Texture2DMS
description: Tipo de Texture2DMS (como ele existe no modelo de sombreador 4) mais variáveis de recurso.
ms.assetid: afda7324-680e-432a-a445-d90bd708e5e0
keywords:
- Texture2DMS HLSL
topic_type:
- apiref
api_name:
- Texture2DMS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c16c69a4fa0fd35ce7b12d69f880daa4b8345d02
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006428"
---
# <a name="texture2dms"></a><span data-ttu-id="12393-104">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="12393-104">Texture2DMS</span></span>

<span data-ttu-id="12393-105">Tipo de Texture2DMS (como ele existe no modelo de sombreador 4) mais variáveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="12393-105">Texture2DMS type (as it exists in Shader Model 4) plus resource variables.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="12393-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="12393-106">In this section</span></span>



| <span data-ttu-id="12393-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="12393-107">Topic</span></span>                                                                                    | <span data-ttu-id="12393-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="12393-108">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12393-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="12393-109">**GetDimensions**</span></span>](sm5-object-texture2dms-getdimensions.md)<br/>                 | <span data-ttu-id="12393-110">Retorna as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="12393-110">Returns the dimensions of the resource.</span></span><br/>                                          |
| [<span data-ttu-id="12393-111">**GetSamplePosition**</span><span class="sxs-lookup"><span data-stu-id="12393-111">**GetSamplePosition**</span></span>](sm5-object-texture2dms-getsampleposition.md)<br/>         | <span data-ttu-id="12393-112">Retorna a posição de exemplo do índice de exemplo fornecido.</span><span class="sxs-lookup"><span data-stu-id="12393-112">Returns the sample position for the sample index provided.</span></span><br/>                       |
| [<span data-ttu-id="12393-113">**Métodos de carregamento**</span><span class="sxs-lookup"><span data-stu-id="12393-113">**Load methods**</span></span>](texture2dms-load.md)<br/>                                      | <span data-ttu-id="12393-114">Recupera um valor do recurso no local e no índice de exemplo fornecidos.</span><span class="sxs-lookup"><span data-stu-id="12393-114">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="12393-115">[**Nova. Operador\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="12393-115">[**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span></span><br/> | <span data-ttu-id="12393-116">Recupera um valor do recurso no local e no índice de exemplo fornecidos.</span><span class="sxs-lookup"><span data-stu-id="12393-116">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="12393-117">[**Operador\[\]**](sm5-object-texture2dms-operator1.md)</span><span class="sxs-lookup"><span data-stu-id="12393-117">[**Operator\[\]**](sm5-object-texture2dms-operator1.md)</span></span><br/>                      | <span data-ttu-id="12393-118">Recupera um valor do recurso no local fornecido no índice de exemplo 0.</span><span class="sxs-lookup"><span data-stu-id="12393-118">Retrieves a value from the resource at the location provided at sample index 0.</span></span> <br/> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="12393-119">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="12393-119">Minimum Shader Model</span></span>

<span data-ttu-id="12393-120">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="12393-120">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="12393-121">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="12393-121">Shader Model</span></span>              | <span data-ttu-id="12393-122">Com suporte</span><span class="sxs-lookup"><span data-stu-id="12393-122">Supported</span></span> |
|---------------------------|-----------|
| <span data-ttu-id="12393-123">Modelo de sombreador 4 e superior</span><span class="sxs-lookup"><span data-stu-id="12393-123">Shader model 4 and higher</span></span> | <span data-ttu-id="12393-124">sim</span><span class="sxs-lookup"><span data-stu-id="12393-124">yes</span></span>       |



 

<span data-ttu-id="12393-125">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="12393-125">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="12393-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="12393-126">Vertex</span></span> | <span data-ttu-id="12393-127">Envoltória</span><span class="sxs-lookup"><span data-stu-id="12393-127">Hull</span></span> | <span data-ttu-id="12393-128">Domínio</span><span class="sxs-lookup"><span data-stu-id="12393-128">Domain</span></span> | <span data-ttu-id="12393-129">Geometria</span><span class="sxs-lookup"><span data-stu-id="12393-129">Geometry</span></span> | <span data-ttu-id="12393-130">16x16</span><span class="sxs-lookup"><span data-stu-id="12393-130">Pixel</span></span> | <span data-ttu-id="12393-131">Computação</span><span class="sxs-lookup"><span data-stu-id="12393-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="12393-132">x</span><span class="sxs-lookup"><span data-stu-id="12393-132">x</span></span>      | <span data-ttu-id="12393-133">x</span><span class="sxs-lookup"><span data-stu-id="12393-133">x</span></span>    | <span data-ttu-id="12393-134">x</span><span class="sxs-lookup"><span data-stu-id="12393-134">x</span></span>      | <span data-ttu-id="12393-135">x</span><span class="sxs-lookup"><span data-stu-id="12393-135">x</span></span>        | <span data-ttu-id="12393-136">x</span><span class="sxs-lookup"><span data-stu-id="12393-136">x</span></span>     | <span data-ttu-id="12393-137">x</span><span class="sxs-lookup"><span data-stu-id="12393-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="12393-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="12393-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12393-139">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="12393-139">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





