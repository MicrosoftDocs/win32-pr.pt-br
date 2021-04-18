---
title: 'Função StructuredBuffer:: Load (int)'
description: 'Lê dados de buffer. | Função StructuredBuffer:: Load (int)'
ms.assetid: ef08d360-0494-49f7-9481-cb802e14aeee
keywords:
- Carregar função HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 883d483044a27e35848457e70e22888dd5ad6320
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968487"
---
# <a name="structuredbufferloadint-function"></a><span data-ttu-id="07de7-105">Função StructuredBuffer:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="07de7-105">StructuredBuffer::Load(int) function</span></span>

<span data-ttu-id="07de7-106">Lê dados de buffer.</span><span class="sxs-lookup"><span data-stu-id="07de7-106">Reads buffer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="07de7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07de7-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="07de7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07de7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07de7-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="07de7-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07de7-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="07de7-110">Type: **int**</span></span>

<span data-ttu-id="07de7-111">O local do buffer.</span><span class="sxs-lookup"><span data-stu-id="07de7-111">The location of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07de7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07de7-112">Return value</span></span>

<span data-ttu-id="07de7-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="07de7-113">Type:</span></span>

<span data-ttu-id="07de7-114">O tipo de retorno corresponde ao tipo na declaração para o objeto [**StructuredBuffer**](sm5-object-structuredbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="07de7-114">The return type matches the type in the declaration for the [**StructuredBuffer**](sm5-object-structuredbuffer.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="07de7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="07de7-115">Remarks</span></span>

<span data-ttu-id="07de7-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="07de7-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="07de7-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="07de7-117">Vertex</span></span> | <span data-ttu-id="07de7-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="07de7-118">Hull</span></span> | <span data-ttu-id="07de7-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="07de7-119">Domain</span></span> | <span data-ttu-id="07de7-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="07de7-120">Geometry</span></span> | <span data-ttu-id="07de7-121">16x16</span><span class="sxs-lookup"><span data-stu-id="07de7-121">Pixel</span></span> | <span data-ttu-id="07de7-122">Computação</span><span class="sxs-lookup"><span data-stu-id="07de7-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="07de7-123">x</span><span class="sxs-lookup"><span data-stu-id="07de7-123">x</span></span>     | <span data-ttu-id="07de7-124">x</span><span class="sxs-lookup"><span data-stu-id="07de7-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="07de7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="07de7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07de7-126">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="07de7-126">Load methods</span></span>](structuredbuffer-load.md)
</dt> </dl>

 

 




