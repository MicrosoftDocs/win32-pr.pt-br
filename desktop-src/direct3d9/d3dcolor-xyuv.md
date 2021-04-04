---
description: Inicializa uma cor com os valores (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: Macro D3DCOLOR_XYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 12d539e44528c5e54a54209763e4cbe262cd16f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837923"
---
# <a name="d3dcolor_xyuv-macro"></a><span data-ttu-id="00cb7-103">\_Macro D3DCOLOR XYUV</span><span class="sxs-lookup"><span data-stu-id="00cb7-103">D3DCOLOR\_XYUV macro</span></span>

<span data-ttu-id="00cb7-104">Inicializa uma cor com os valores (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="00cb7-104">Initializes a color with the (y, u, v) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="00cb7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00cb7-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a><span data-ttu-id="00cb7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00cb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00cb7-107">*y*</span><span class="sxs-lookup"><span data-stu-id="00cb7-107">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="00cb7-108">Componente de luminância da cor.</span><span class="sxs-lookup"><span data-stu-id="00cb7-108">Luminance component of the color.</span></span> <span data-ttu-id="00cb7-109">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="00cb7-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="00cb7-110">*u*</span><span class="sxs-lookup"><span data-stu-id="00cb7-110">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="00cb7-111">Brilho azul da cor.</span><span class="sxs-lookup"><span data-stu-id="00cb7-111">Blue brightness of the color.</span></span> <span data-ttu-id="00cb7-112">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="00cb7-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="00cb7-113">*l*</span><span class="sxs-lookup"><span data-stu-id="00cb7-113">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="00cb7-114">Brilho vermelho da cor.</span><span class="sxs-lookup"><span data-stu-id="00cb7-114">Red brightness of the color.</span></span> <span data-ttu-id="00cb7-115">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="00cb7-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00cb7-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00cb7-116">Return value</span></span>

<span data-ttu-id="00cb7-117">Retorna o valor de [**D3DCOLOR**](d3dcolor.md) que corresponde aos valores fornecidos (y, u, v).</span><span class="sxs-lookup"><span data-stu-id="00cb7-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied (y, u, v) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="00cb7-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="00cb7-118">Remarks</span></span>

<span data-ttu-id="00cb7-119">Uma cor RGB pode ser reduzida para 16 bits por pixel por conversão para diferenças de luminosidade e cor com as seguintes equações:</span><span class="sxs-lookup"><span data-stu-id="00cb7-119">An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:</span></span>


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a><span data-ttu-id="00cb7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00cb7-120">Requirements</span></span>



| <span data-ttu-id="00cb7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="00cb7-121">Requirement</span></span> | <span data-ttu-id="00cb7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="00cb7-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00cb7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00cb7-123">Header</span></span><br/> | <dl> <span data-ttu-id="00cb7-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="00cb7-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00cb7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="00cb7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00cb7-126">Macros</span><span class="sxs-lookup"><span data-stu-id="00cb7-126">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="00cb7-127">**\_ARGB D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="00cb7-127">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="00cb7-128">**D3DCOLOR \_ AYUV**</span><span class="sxs-lookup"><span data-stu-id="00cb7-128">**D3DCOLOR\_AYUV**</span></span>](d3dcolor-ayuv.md)
</dt> </dl>

 

 




