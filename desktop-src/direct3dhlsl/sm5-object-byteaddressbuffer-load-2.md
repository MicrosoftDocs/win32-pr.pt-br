---
title: 'Função ByteAddressBuffer:: Load (int, uint)'
description: Obtém um valor e o status da operação.
ms.assetid: 8F90671B-CEEB-4F8C-9469-D85940568872
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
ms.openlocfilehash: 319daad35da0256a4d36ef4580df62fd4d295854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085047"
---
# <a name="byteaddressbufferloadint-uint-function"></a><span data-ttu-id="5070b-104">Função ByteAddressBuffer:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="5070b-104">ByteAddressBuffer::Load(int, uint) function</span></span>

<span data-ttu-id="5070b-105">Obtém um valor e o status da operação.</span><span class="sxs-lookup"><span data-stu-id="5070b-105">Gets one value and the status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5070b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5070b-106">Syntax</span></span>

``` syntax
uint Load(
  in  int Location,
  out uint Status
);
```

## <a name="parameters"></a><span data-ttu-id="5070b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5070b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5070b-108">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5070b-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5070b-109">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="5070b-109">Type: **int**</span></span>

<span data-ttu-id="5070b-110">O endereço de entrada em bytes, que deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="5070b-110">The input address in bytes, which must be a multiple of 4.</span></span>

</dd> <dt>

<span data-ttu-id="5070b-111">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="5070b-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5070b-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5070b-112">Type: **uint**</span></span>

<span data-ttu-id="5070b-113">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="5070b-113">The status of the operation.</span></span> <span data-ttu-id="5070b-114">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="5070b-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5070b-115">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="5070b-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5070b-116">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="5070b-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5070b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5070b-117">Return value</span></span>

<span data-ttu-id="5070b-118">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="5070b-118">Type: **uint**</span></span>

<span data-ttu-id="5070b-119">Um valor.</span><span class="sxs-lookup"><span data-stu-id="5070b-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5070b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="5070b-120">Remarks</span></span>

<span data-ttu-id="5070b-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="5070b-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5070b-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="5070b-122">Vertex</span></span> | <span data-ttu-id="5070b-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="5070b-123">Hull</span></span> | <span data-ttu-id="5070b-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="5070b-124">Domain</span></span> | <span data-ttu-id="5070b-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="5070b-125">Geometry</span></span> | <span data-ttu-id="5070b-126">16x16</span><span class="sxs-lookup"><span data-stu-id="5070b-126">Pixel</span></span> | <span data-ttu-id="5070b-127">Computação</span><span class="sxs-lookup"><span data-stu-id="5070b-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5070b-128">x</span><span class="sxs-lookup"><span data-stu-id="5070b-128">x</span></span>      | <span data-ttu-id="5070b-129">x</span><span class="sxs-lookup"><span data-stu-id="5070b-129">x</span></span>    | <span data-ttu-id="5070b-130">x</span><span class="sxs-lookup"><span data-stu-id="5070b-130">x</span></span>      | <span data-ttu-id="5070b-131">x</span><span class="sxs-lookup"><span data-stu-id="5070b-131">x</span></span>        | <span data-ttu-id="5070b-132">x</span><span class="sxs-lookup"><span data-stu-id="5070b-132">x</span></span>     | <span data-ttu-id="5070b-133">x</span><span class="sxs-lookup"><span data-stu-id="5070b-133">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5070b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5070b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5070b-135">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="5070b-135">Load methods</span></span>](byteaddressbuffer-load.md)
</dt> <dt>

[<span data-ttu-id="5070b-136">**ByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="5070b-136">**ByteAddressBuffer**</span></span>](sm5-object-byteaddressbuffer.md)
</dt> </dl>

 

 
