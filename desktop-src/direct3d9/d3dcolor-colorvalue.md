---
description: Inicializa uma cor com os valores de ponto flutuante de vermelho, verde, azul e alfa fornecidos.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: Macro D3DCOLOR_COLORVALUE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663974"
---
# <a name="d3dcolor_colorvalue-macro"></a><span data-ttu-id="20f82-103">\_Macro D3DCOLOR ColorValue</span><span class="sxs-lookup"><span data-stu-id="20f82-103">D3DCOLOR\_COLORVALUE macro</span></span>

<span data-ttu-id="20f82-104">Inicializa uma cor com os valores de ponto flutuante de vermelho, verde, azul e alfa fornecidos.</span><span class="sxs-lookup"><span data-stu-id="20f82-104">Initializes a color with the supplied red, green, blue, and alpha floating-point values.</span></span>

## <a name="syntax"></a><span data-ttu-id="20f82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20f82-105">Syntax</span></span>


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a><span data-ttu-id="20f82-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20f82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20f82-107">*r*</span><span class="sxs-lookup"><span data-stu-id="20f82-107">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="20f82-108">Componente vermelho da cor.</span><span class="sxs-lookup"><span data-stu-id="20f82-108">Red component of the color.</span></span> <span data-ttu-id="20f82-109">Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="20f82-109">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="20f82-110">*m*</span><span class="sxs-lookup"><span data-stu-id="20f82-110">*g*</span></span> 
</dt> <dd>

<span data-ttu-id="20f82-111">Componente verde da cor.</span><span class="sxs-lookup"><span data-stu-id="20f82-111">Green component of the color.</span></span> <span data-ttu-id="20f82-112">Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="20f82-112">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="20f82-113">*b*</span><span class="sxs-lookup"><span data-stu-id="20f82-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="20f82-114">Componente azul da cor.</span><span class="sxs-lookup"><span data-stu-id="20f82-114">Blue component of the color.</span></span> <span data-ttu-id="20f82-115">Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="20f82-115">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="20f82-116">*um*</span><span class="sxs-lookup"><span data-stu-id="20f82-116">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="20f82-117">Componente alfa da cor.</span><span class="sxs-lookup"><span data-stu-id="20f82-117">Alpha component of the color.</span></span> <span data-ttu-id="20f82-118">Esse valor deve ser um valor de ponto flutuante no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="20f82-118">This value must be a floating-point value in the range 0.0 through 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20f82-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20f82-119">Return value</span></span>

<span data-ttu-id="20f82-120">Retorna o valor [**D3DCOLOR**](d3dcolor.md) que corresponde aos valores RGBA fornecidos.</span><span class="sxs-lookup"><span data-stu-id="20f82-120">Returns the [**D3DCOLOR**](d3dcolor.md) value that corresponds to the supplied RGBA values.</span></span>

## <a name="requirements"></a><span data-ttu-id="20f82-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20f82-121">Requirements</span></span>



| <span data-ttu-id="20f82-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="20f82-122">Requirement</span></span> | <span data-ttu-id="20f82-123">Valor</span><span class="sxs-lookup"><span data-stu-id="20f82-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20f82-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20f82-124">Header</span></span><br/> | <dl> <span data-ttu-id="20f82-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="20f82-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20f82-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="20f82-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20f82-127">Macros</span><span class="sxs-lookup"><span data-stu-id="20f82-127">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




