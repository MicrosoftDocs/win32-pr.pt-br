---
description: Inicializa uma cor com os valores vermelho, verde e azul fornecidos.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: Macro D3DCOLOR_XRGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4932e34979b0913f27874e57cfa881f18fb16364
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370931"
---
# <a name="d3dcolor_xrgb-macro"></a><span data-ttu-id="c174e-103">\_Macro D3DCOLOR XRGB</span><span class="sxs-lookup"><span data-stu-id="c174e-103">D3DCOLOR\_XRGB macro</span></span>

<span data-ttu-id="c174e-104">Inicializa uma cor com os valores vermelho, verde e azul fornecidos.</span><span class="sxs-lookup"><span data-stu-id="c174e-104">Initializes a color with the supplied red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c174e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c174e-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="c174e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c174e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c174e-107">*r*</span><span class="sxs-lookup"><span data-stu-id="c174e-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="c174e-108">Componente vermelho da cor.</span><span class="sxs-lookup"><span data-stu-id="c174e-108">Red component of the color.</span></span> <span data-ttu-id="c174e-109">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="c174e-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="c174e-110">*m*</span><span class="sxs-lookup"><span data-stu-id="c174e-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="c174e-111">Componente verde da cor.</span><span class="sxs-lookup"><span data-stu-id="c174e-111">Green component of the color.</span></span> <span data-ttu-id="c174e-112">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="c174e-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="c174e-113">*b*</span><span class="sxs-lookup"><span data-stu-id="c174e-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="c174e-114">Componente azul da cor.</span><span class="sxs-lookup"><span data-stu-id="c174e-114">Blue component of the color.</span></span> <span data-ttu-id="c174e-115">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="c174e-115">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c174e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c174e-116">Return value</span></span>

<span data-ttu-id="c174e-117">Retorna o valor de [**D3DCOLOR**](d3dcolor.md) que corresponde aos valores RGB fornecidos.</span><span class="sxs-lookup"><span data-stu-id="c174e-117">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c174e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c174e-118">Requirements</span></span>



| <span data-ttu-id="c174e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c174e-119">Requirement</span></span> | <span data-ttu-id="c174e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c174e-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c174e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c174e-121">Header</span></span><br/> | <dl> <span data-ttu-id="c174e-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c174e-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c174e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c174e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c174e-124">Macros</span><span class="sxs-lookup"><span data-stu-id="c174e-124">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="c174e-125">**\_ARGB D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="c174e-125">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="c174e-126">**\_RGBA D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="c174e-126">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> </dl>

 

 




