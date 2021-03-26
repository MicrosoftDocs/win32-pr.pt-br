---
title: 'Função RWByteAddressBuffer:: Load (int, uint)'
description: Obtém um valor e retorna o status da operação.
ms.assetid: E3FD0FFA-6A9B-4B44-A90D-47270326F9BA
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
ms.openlocfilehash: 71f142d35ae8be3800ccf85b5e8114d5e85c44ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824088"
---
# <a name="rwbyteaddressbufferloadintuint-function"></a><span data-ttu-id="6cff3-104">Função RWByteAddressBuffer:: Load (int, uint)</span><span class="sxs-lookup"><span data-stu-id="6cff3-104">RWByteAddressBuffer::Load(int,uint) function</span></span>

<span data-ttu-id="6cff3-105">Obtém um valor e retorna o status da operação.</span><span class="sxs-lookup"><span data-stu-id="6cff3-105">Gets one value and returns status of the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cff3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cff3-106">Syntax</span></span>


``` syntax
uint Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a><span data-ttu-id="6cff3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cff3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cff3-108">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="6cff3-108">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cff3-109">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="6cff3-109">Type: **int**</span></span>

<span data-ttu-id="6cff3-110">O local do buffer.</span><span class="sxs-lookup"><span data-stu-id="6cff3-110">The location of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6cff3-111">*Status* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="6cff3-111">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cff3-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="6cff3-112">Type: **uint**</span></span>

<span data-ttu-id="6cff3-113">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="6cff3-113">The status of the operation.</span></span> <span data-ttu-id="6cff3-114">Você não pode acessar o status diretamente; em vez disso, passe o status para a função intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="6cff3-114">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="6cff3-115">**CheckAccessFullyMapped** retornará **true** se todos os valores da operação de **amostra**, **coleta** ou **carregamento** correspondente acessaram os blocos mapeados em um recurso de bloco ao [lado](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="6cff3-115">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="6cff3-116">Se qualquer valor tiver sido tirado de um bloco não mapeado, **CheckAccessFullyMapped** retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="6cff3-116">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cff3-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cff3-117">Return value</span></span>

<span data-ttu-id="6cff3-118">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="6cff3-118">Type: **uint**</span></span>

<span data-ttu-id="6cff3-119">Um valor.</span><span class="sxs-lookup"><span data-stu-id="6cff3-119">One value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cff3-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cff3-120">Remarks</span></span>

<span data-ttu-id="6cff3-121">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="6cff3-121">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="6cff3-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="6cff3-122">Vertex</span></span> | <span data-ttu-id="6cff3-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="6cff3-123">Hull</span></span> | <span data-ttu-id="6cff3-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="6cff3-124">Domain</span></span> | <span data-ttu-id="6cff3-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="6cff3-125">Geometry</span></span> | <span data-ttu-id="6cff3-126">16x16</span><span class="sxs-lookup"><span data-stu-id="6cff3-126">Pixel</span></span> | <span data-ttu-id="6cff3-127">Computação</span><span class="sxs-lookup"><span data-stu-id="6cff3-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="6cff3-128">x</span><span class="sxs-lookup"><span data-stu-id="6cff3-128">x</span></span>     | <span data-ttu-id="6cff3-129">x</span><span class="sxs-lookup"><span data-stu-id="6cff3-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="6cff3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cff3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cff3-131">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="6cff3-131">Load methods</span></span>](rwbyteaddressbuffer-load.md)
</dt> </dl>

 

 
