---
description: Inicializa uma cor com os valores vermelho, verde, azul e alfa fornecidos.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: Macro D3DCOLOR_RGBA (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750117"
---
# <a name="d3dcolor_rgba-macro"></a><span data-ttu-id="9fff6-103">\_Macro D3DCOLOR RGBA</span><span class="sxs-lookup"><span data-stu-id="9fff6-103">D3DCOLOR\_RGBA macro</span></span>

<span data-ttu-id="9fff6-104">Inicializa uma cor com os valores vermelho, verde, azul e alfa fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9fff6-104">Initializes a color with the supplied red, green, blue, and alpha values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fff6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fff6-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a><span data-ttu-id="9fff6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fff6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fff6-107">*r*</span><span class="sxs-lookup"><span data-stu-id="9fff6-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="9fff6-108">Componente vermelho da cor.</span><span class="sxs-lookup"><span data-stu-id="9fff6-108">Red component of the color.</span></span> <span data-ttu-id="9fff6-109">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="9fff6-109">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="9fff6-110">*m*</span><span class="sxs-lookup"><span data-stu-id="9fff6-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="9fff6-111">Componente verde da cor.</span><span class="sxs-lookup"><span data-stu-id="9fff6-111">Green component of the color.</span></span> <span data-ttu-id="9fff6-112">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="9fff6-112">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="9fff6-113">*b*</span><span class="sxs-lookup"><span data-stu-id="9fff6-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="9fff6-114">Componente azul da cor.</span><span class="sxs-lookup"><span data-stu-id="9fff6-114">Blue component of the color.</span></span> <span data-ttu-id="9fff6-115">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="9fff6-115">This value must be in the range 0 through 255.</span></span>

</dd> <dt>

<span data-ttu-id="9fff6-116">*um*</span><span class="sxs-lookup"><span data-stu-id="9fff6-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="9fff6-117">Componente alfa da cor.</span><span class="sxs-lookup"><span data-stu-id="9fff6-117">Alpha component of the color.</span></span> <span data-ttu-id="9fff6-118">Esse valor deve estar no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="9fff6-118">This value must be in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fff6-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9fff6-119">Return value</span></span>

<span data-ttu-id="9fff6-120">Retorna o valor [**D3DCOLOR**](d3dcolor.md) que corresponde aos valores RGBA fornecidos.</span><span class="sxs-lookup"><span data-stu-id="9fff6-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fff6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fff6-121">Requirements</span></span>



| <span data-ttu-id="9fff6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fff6-122">Requirement</span></span> | <span data-ttu-id="9fff6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9fff6-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fff6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9fff6-124">Header</span></span><br/> | <dl> <span data-ttu-id="9fff6-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fff6-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fff6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fff6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fff6-127">Macros</span><span class="sxs-lookup"><span data-stu-id="9fff6-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="9fff6-128">**\_ARGB D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="9fff6-128">**D3DCOLOR\_ARGB**</span></span>](d3dcolor-argb.md)
</dt> <dt>

[<span data-ttu-id="9fff6-129">**D3DCOLOR \_ XRGB**</span><span class="sxs-lookup"><span data-stu-id="9fff6-129">**D3DCOLOR\_XRGB**</span></span>](d3dcolor-xrgb.md)
</dt> </dl>

 

 




