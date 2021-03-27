---
title: 'Função RWTexture1D:: Load (int)'
description: 'Lê dados de textura. | Função RWTexture1D:: Load (int)'
ms.assetid: AA5E324E-A2C0-45C5-92A8-E4DBC4EB684C
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
ms.openlocfilehash: e78cd12502ada91e48df1ce88be6a19fb714327f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298272"
---
# <a name="rwtexture1dloadint-function"></a><span data-ttu-id="184ca-105">Função RWTexture1D:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="184ca-105">RWTexture1D::Load(int) function</span></span>

<span data-ttu-id="184ca-106">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="184ca-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="184ca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="184ca-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="184ca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="184ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="184ca-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="184ca-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184ca-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="184ca-110">Type: **int**</span></span>

<span data-ttu-id="184ca-111">O local da textura.</span><span class="sxs-lookup"><span data-stu-id="184ca-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="184ca-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="184ca-112">Return value</span></span>

<span data-ttu-id="184ca-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="184ca-113">Type:</span></span>

<span data-ttu-id="184ca-114">O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWTexture1D**](sm5-object-rwtexture1d.md) .</span><span class="sxs-lookup"><span data-stu-id="184ca-114">The return type matches the type in the declaration for the [**RWTexture1D**](sm5-object-rwtexture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="184ca-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="184ca-115">Remarks</span></span>

<span data-ttu-id="184ca-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="184ca-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="184ca-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="184ca-117">Vertex</span></span> | <span data-ttu-id="184ca-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="184ca-118">Hull</span></span> | <span data-ttu-id="184ca-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="184ca-119">Domain</span></span> | <span data-ttu-id="184ca-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="184ca-120">Geometry</span></span> | <span data-ttu-id="184ca-121">16x16</span><span class="sxs-lookup"><span data-stu-id="184ca-121">Pixel</span></span> | <span data-ttu-id="184ca-122">Computação</span><span class="sxs-lookup"><span data-stu-id="184ca-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="184ca-123">x</span><span class="sxs-lookup"><span data-stu-id="184ca-123">x</span></span>     | <span data-ttu-id="184ca-124">x</span><span class="sxs-lookup"><span data-stu-id="184ca-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="184ca-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="184ca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="184ca-126">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="184ca-126">Load methods</span></span>](rwtexture1d-load.md)
</dt> </dl>

 

 




