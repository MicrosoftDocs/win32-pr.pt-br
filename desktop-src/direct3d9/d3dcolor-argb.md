---
description: Inicializa uma cor com os valores Alfa, vermelho, verde e azul fornecidos.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: Macro D3DCOLOR_ARGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298534"
---
# <a name="d3dcolor_argb-macro"></a><span data-ttu-id="73d87-103">\_Macro ARGB D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="73d87-103">D3DCOLOR\_ARGB macro</span></span>

<span data-ttu-id="73d87-104">Inicializa uma cor com os valores Alfa, vermelho, verde e azul fornecidos.</span><span class="sxs-lookup"><span data-stu-id="73d87-104">Initializes a color with the supplied alpha, red, green, and blue values.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d87-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73d87-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a><span data-ttu-id="73d87-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73d87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73d87-107">*um*</span><span class="sxs-lookup"><span data-stu-id="73d87-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="73d87-108">Componente alfa da cor.</span><span class="sxs-lookup"><span data-stu-id="73d87-108">Alpha component of the color.</span></span> <span data-ttu-id="73d87-109">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="73d87-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="73d87-110">*r*</span><span class="sxs-lookup"><span data-stu-id="73d87-110">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="73d87-111">Componente vermelho da cor.</span><span class="sxs-lookup"><span data-stu-id="73d87-111">Red component of the color.</span></span> <span data-ttu-id="73d87-112">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="73d87-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="73d87-113">*m*</span><span class="sxs-lookup"><span data-stu-id="73d87-113">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="73d87-114">Componente verde da cor.</span><span class="sxs-lookup"><span data-stu-id="73d87-114">Green component of the color.</span></span> <span data-ttu-id="73d87-115">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="73d87-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="73d87-116">*b*</span><span class="sxs-lookup"><span data-stu-id="73d87-116">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="73d87-117">Componente azul da cor.</span><span class="sxs-lookup"><span data-stu-id="73d87-117">Blue component of the color.</span></span> <span data-ttu-id="73d87-118">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="73d87-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73d87-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73d87-119">Return value</span></span>

<span data-ttu-id="73d87-120">Retorna o valor de [D3DCOLOR](d3dcolor.md) que corresponde aos valores ARGB fornecidos.</span><span class="sxs-lookup"><span data-stu-id="73d87-120">Returns the [D3DCOLOR](d3dcolor.md) value that corresponds to the supplied ARGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="73d87-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73d87-121">Requirements</span></span>



| <span data-ttu-id="73d87-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="73d87-122">Requirement</span></span> | <span data-ttu-id="73d87-123">Valor</span><span class="sxs-lookup"><span data-stu-id="73d87-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73d87-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73d87-124">Header</span></span><br/> | <dl> <span data-ttu-id="73d87-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="73d87-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73d87-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="73d87-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d87-127">Macros</span><span class="sxs-lookup"><span data-stu-id="73d87-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="73d87-128">**\_RGBA D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="73d87-128">**D3DCOLOR\_RGBA**</span></span>](d3dcolor-rgba.md)
</dt> <dt>

[<span data-ttu-id="73d87-129">**D3DCOLOR \_ XRGB**</span><span class="sxs-lookup"><span data-stu-id="73d87-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




