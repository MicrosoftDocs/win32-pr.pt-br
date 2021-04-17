---
description: Inicializa uma cor usando os valores (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: Macro D3DCOLOR_AYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752756"
---
# <a name="d3dcolor_ayuv-macro"></a><span data-ttu-id="5f737-103">\_Macro D3DCOLOR AYUV</span><span class="sxs-lookup"><span data-stu-id="5f737-103">D3DCOLOR\_AYUV macro</span></span>

<span data-ttu-id="5f737-104">Inicializa uma cor usando os valores (a, y, u, v).</span><span class="sxs-lookup"><span data-stu-id="5f737-104">Initializes a color using the (a,y,u,v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f737-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f737-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="5f737-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f737-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f737-107">*um*</span><span class="sxs-lookup"><span data-stu-id="5f737-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="5f737-108">Componente alfa da cor.</span><span class="sxs-lookup"><span data-stu-id="5f737-108">Alpha component of the color.</span></span> <span data-ttu-id="5f737-109">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="5f737-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="5f737-110">*y*</span><span class="sxs-lookup"><span data-stu-id="5f737-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="5f737-111">Componente de luminância da cor.</span><span class="sxs-lookup"><span data-stu-id="5f737-111">Luminance component of the color.</span></span> <span data-ttu-id="5f737-112">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="5f737-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="5f737-113">*u*</span><span class="sxs-lookup"><span data-stu-id="5f737-113">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="5f737-114">Brilho azul da cor.</span><span class="sxs-lookup"><span data-stu-id="5f737-114">Blue brightness of the color.</span></span> <span data-ttu-id="5f737-115">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="5f737-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="5f737-116">*l*</span><span class="sxs-lookup"><span data-stu-id="5f737-116">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="5f737-117">Brilho vermelho da cor.</span><span class="sxs-lookup"><span data-stu-id="5f737-117">Red brightness of the color.</span></span> <span data-ttu-id="5f737-118">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="5f737-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f737-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f737-119">Return value</span></span>

<span data-ttu-id="5f737-120">Retorna o valor de [D3DCOLOR](d3dcolor.md) que corresponde aos valores ARGB fornecidos.</span><span class="sxs-lookup"><span data-stu-id="5f737-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f737-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f737-121">Remarks</span></span>

<span data-ttu-id="5f737-122">Uma cor RGB pode ser reduzida para 16 bits por pixel por conversão para diferenças de luminosidade e cor com as seguintes equações:</span><span class="sxs-lookup"><span data-stu-id="5f737-122">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="5f737-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f737-123">Requirements</span></span>



| <span data-ttu-id="5f737-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f737-124">Requirement</span></span> | <span data-ttu-id="5f737-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5f737-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f737-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f737-126">Header</span></span><br/> | <dl> <span data-ttu-id="5f737-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f737-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f737-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f737-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f737-129">Macros</span><span class="sxs-lookup"><span data-stu-id="5f737-129">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="5f737-130">**\_ARGB D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="5f737-130">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="5f737-131">**D3DCOLOR \_ XYUV**</span><span class="sxs-lookup"><span data-stu-id="5f737-131">**D3DCOLOR\_XYUV**</span></span>](d3dcolor-xyuv.md)
</dt> </dl>

 

 




