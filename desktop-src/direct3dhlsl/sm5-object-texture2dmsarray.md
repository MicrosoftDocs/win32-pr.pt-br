---
title: Texture2DMSArray
description: Texture2DMSArray
ms.assetid: 4200eba8-a9e5-41ba-b04c-4ac7b20274d2
keywords:
- Texture2DMSArray HLSL
topic_type:
- apiref
api_name:
- Texture2DMSArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: effe4819c674a7909cc445b9e9f7b5322fae7676
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104172446"
---
# <a name="texture2dmsarray"></a><span data-ttu-id="8959c-104">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="8959c-104">Texture2DMSArray</span></span>

<span data-ttu-id="8959c-105">Tipo de Texture2DMSArray (como ele existe no modelo de sombreador 4) mais variáveis de recurso.</span><span class="sxs-lookup"><span data-stu-id="8959c-105">Texture2DMSArray type (as it exists in Shader Model 4) plus resource variables.</span></span>



| <span data-ttu-id="8959c-106">Método</span><span class="sxs-lookup"><span data-stu-id="8959c-106">Method</span></span>                                                                             | <span data-ttu-id="8959c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8959c-107">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="8959c-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="8959c-108">**GetDimensions**</span></span>](sm5-object-texture2dmsarray-getdimensions.md)                  | <span data-ttu-id="8959c-109">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="8959c-109">Gets the resource dimensions.</span></span>                      |
| [<span data-ttu-id="8959c-110">**GetSamplePosition**</span><span class="sxs-lookup"><span data-stu-id="8959c-110">**GetSamplePosition**</span></span>](sm5-object-texture2dmsarray-getsampleposition.md)          | <span data-ttu-id="8959c-111">Obtém a posição do exemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="8959c-111">Gets the position of the specified sample.</span></span>         |
| [<span data-ttu-id="8959c-112">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="8959c-112">**Load**</span></span>](texture2dmsarray-load.md)                                               | <span data-ttu-id="8959c-113">Obtém um valor.</span><span class="sxs-lookup"><span data-stu-id="8959c-113">Gets one value.</span></span>                                    |
| <span data-ttu-id="8959c-114">[**Nova. Operador\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="8959c-114">[**sample.Operator\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span></span>  | <span data-ttu-id="8959c-115">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8959c-115">Gets a read-only resource variable.</span></span>                |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8959c-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8959c-116">Minimum Shader Model</span></span>

<span data-ttu-id="8959c-117">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8959c-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="8959c-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8959c-118">Shader Model</span></span>                                                                | <span data-ttu-id="8959c-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8959c-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8959c-120">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="8959c-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="8959c-121">sim</span><span class="sxs-lookup"><span data-stu-id="8959c-121">yes</span></span>       |



 

<span data-ttu-id="8959c-122">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8959c-122">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="8959c-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="8959c-123">Vertex</span></span> | <span data-ttu-id="8959c-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="8959c-124">Hull</span></span> | <span data-ttu-id="8959c-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="8959c-125">Domain</span></span> | <span data-ttu-id="8959c-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="8959c-126">Geometry</span></span> | <span data-ttu-id="8959c-127">16x16</span><span class="sxs-lookup"><span data-stu-id="8959c-127">Pixel</span></span> | <span data-ttu-id="8959c-128">Computação</span><span class="sxs-lookup"><span data-stu-id="8959c-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8959c-129">x</span><span class="sxs-lookup"><span data-stu-id="8959c-129">x</span></span>      | <span data-ttu-id="8959c-130">x</span><span class="sxs-lookup"><span data-stu-id="8959c-130">x</span></span>    | <span data-ttu-id="8959c-131">x</span><span class="sxs-lookup"><span data-stu-id="8959c-131">x</span></span>      | <span data-ttu-id="8959c-132">x</span><span class="sxs-lookup"><span data-stu-id="8959c-132">x</span></span>        | <span data-ttu-id="8959c-133">x</span><span class="sxs-lookup"><span data-stu-id="8959c-133">x</span></span>     | <span data-ttu-id="8959c-134">x</span><span class="sxs-lookup"><span data-stu-id="8959c-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8959c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="8959c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8959c-136">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="8959c-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




