---
title: 'Função RWTexture2D:: Load (int, uint)'
description: 'Lê os dados de textura e retorna o status sobre a operação. | Função RWTexture2D:: Load (int, uint)'
ms.assetid: E61E1EFD-BDD1-4415-9993-0CD7203B5BDC
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
ms.openlocfilehash: dcc8619caea715f1e752ba2768cca1d4e5f330ac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968443"
---
# <a name="rwtexture2dloadintuint-function"></a><span data-ttu-id="4a9ea-105">Função RWTexture2D:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="4a9ea-105">RWTexture2D::Load(int,uint) function</span></span>

<span data-ttu-id="4a9ea-106">Lê os dados de textura e retorna o status sobre a operação.</span><span class="sxs-lookup"><span data-stu-id="4a9ea-106">Reads texture data and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a9ea-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a9ea-107">Syntax</span></span>


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="4a9ea-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a9ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a9ea-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4a9ea-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a9ea-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="4a9ea-110">Type: **int**</span></span>

<span data-ttu-id="4a9ea-111">O local da textura.</span><span class="sxs-lookup"><span data-stu-id="4a9ea-111">The location of the texture.</span></span>

</dd> <dt>

<span data-ttu-id="4a9ea-112">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="4a9ea-112">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a9ea-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4a9ea-113">Type: **uint**</span></span>

<span data-ttu-id="4a9ea-114">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="4a9ea-114">The status of the operation.</span></span> <span data-ttu-id="4a9ea-115">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="4a9ea-115">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4a9ea-116">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="4a9ea-116">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4a9ea-117">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="4a9ea-117">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a9ea-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a9ea-118">Return value</span></span>

<span data-ttu-id="4a9ea-119">Tipo:</span><span class="sxs-lookup"><span data-stu-id="4a9ea-119">Type:</span></span>

<span data-ttu-id="4a9ea-120">O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWTexture2D**](sm5-object-rwtexture2d.md) .</span><span class="sxs-lookup"><span data-stu-id="4a9ea-120">The return type matches the type in the declaration for the [**RWTexture2D**](sm5-object-rwtexture2d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a9ea-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a9ea-121">Remarks</span></span>

<span data-ttu-id="4a9ea-122">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4a9ea-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="4a9ea-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="4a9ea-123">Vertex</span></span> | <span data-ttu-id="4a9ea-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4a9ea-124">Hull</span></span> | <span data-ttu-id="4a9ea-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="4a9ea-125">Domain</span></span> | <span data-ttu-id="4a9ea-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="4a9ea-126">Geometry</span></span> | <span data-ttu-id="4a9ea-127">16x16</span><span class="sxs-lookup"><span data-stu-id="4a9ea-127">Pixel</span></span> | <span data-ttu-id="4a9ea-128">Computação</span><span class="sxs-lookup"><span data-stu-id="4a9ea-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="4a9ea-129">x</span><span class="sxs-lookup"><span data-stu-id="4a9ea-129">x</span></span>     | <span data-ttu-id="4a9ea-130">x</span><span class="sxs-lookup"><span data-stu-id="4a9ea-130">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4a9ea-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a9ea-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a9ea-132">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="4a9ea-132">Load methods</span></span>](rwtexture2d-load.md)
</dt> </dl>

 

 
