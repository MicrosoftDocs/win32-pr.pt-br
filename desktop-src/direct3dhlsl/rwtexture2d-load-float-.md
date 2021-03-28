---
title: 'Função RWTexture2D:: Load (int)'
description: 'Lê dados de textura. | Função RWTexture2D:: Load (int)'
ms.assetid: AEBB9C78-BE4B-4121-93CC-EE03B9925CF0
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
ms.openlocfilehash: ab5f8d755ad4af3127a0c238defc9f1c422061bc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989204"
---
# <a name="rwtexture2dloadint-function"></a><span data-ttu-id="b7317-105">Função RWTexture2D:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="b7317-105">RWTexture2D::Load(int) function</span></span>

<span data-ttu-id="b7317-106">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="b7317-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7317-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7317-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="b7317-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7317-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7317-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b7317-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7317-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="b7317-110">Type: **int**</span></span>

<span data-ttu-id="b7317-111">O local da textura.</span><span class="sxs-lookup"><span data-stu-id="b7317-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7317-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7317-112">Return value</span></span>

<span data-ttu-id="b7317-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="b7317-113">Type:</span></span>

<span data-ttu-id="b7317-114">O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWTexture2D**](sm5-object-rwtexture2d.md) .</span><span class="sxs-lookup"><span data-stu-id="b7317-114">The return type matches the type in the declaration for the [**RWTexture2D**](sm5-object-rwtexture2d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7317-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7317-115">Remarks</span></span>

<span data-ttu-id="b7317-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b7317-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b7317-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="b7317-117">Vertex</span></span> | <span data-ttu-id="b7317-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b7317-118">Hull</span></span> | <span data-ttu-id="b7317-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="b7317-119">Domain</span></span> | <span data-ttu-id="b7317-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="b7317-120">Geometry</span></span> | <span data-ttu-id="b7317-121">16x16</span><span class="sxs-lookup"><span data-stu-id="b7317-121">Pixel</span></span> | <span data-ttu-id="b7317-122">Computação</span><span class="sxs-lookup"><span data-stu-id="b7317-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b7317-123">x</span><span class="sxs-lookup"><span data-stu-id="b7317-123">x</span></span>     | <span data-ttu-id="b7317-124">x</span><span class="sxs-lookup"><span data-stu-id="b7317-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b7317-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7317-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7317-126">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="b7317-126">Load methods</span></span>](rwtexture2d-load.md)
</dt> </dl>

 

 




