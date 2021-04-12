---
description: Descreve os valores de cor.
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: Estrutura D3DCOLORVALUE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1fe2f187921749207bbbf51d7fcfd75357a70858
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298531"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="06012-103">Estrutura D3DCOLORVALUE (D3D9Types. h)</span><span class="sxs-lookup"><span data-stu-id="06012-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="06012-104">Descreve os valores de cor.</span><span class="sxs-lookup"><span data-stu-id="06012-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="06012-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06012-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="06012-106">Membros</span><span class="sxs-lookup"><span data-stu-id="06012-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="06012-107">**r**</span><span class="sxs-lookup"><span data-stu-id="06012-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="06012-108">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="06012-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="06012-109">Valor de ponto flutuante que especifica o componente vermelho de uma cor.</span><span class="sxs-lookup"><span data-stu-id="06012-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="06012-110">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="06012-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="06012-111">Um valor de 0,0 indica a ausência completa do componente vermelho, enquanto um valor de 1,0 indica que o vermelho está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="06012-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="06012-112">**m**</span><span class="sxs-lookup"><span data-stu-id="06012-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="06012-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="06012-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="06012-114">Valor de ponto flutuante que especifica o componente verde de uma cor.</span><span class="sxs-lookup"><span data-stu-id="06012-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="06012-115">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="06012-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="06012-116">Um valor de 0,0 indica a ausência completa do componente verde, enquanto um valor de 1,0 indica que o verde está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="06012-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="06012-117">**b**</span><span class="sxs-lookup"><span data-stu-id="06012-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="06012-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="06012-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="06012-119">Valor de ponto flutuante que especifica o componente azul de uma cor.</span><span class="sxs-lookup"><span data-stu-id="06012-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="06012-120">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="06012-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="06012-121">Um valor de 0,0 indica a ausência completa do componente azul, enquanto um valor de 1,0 indica que o azul está totalmente presente.</span><span class="sxs-lookup"><span data-stu-id="06012-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="06012-122">**um**</span><span class="sxs-lookup"><span data-stu-id="06012-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="06012-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="06012-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="06012-124">Valor de ponto flutuante que especifica o componente alfa de uma cor.</span><span class="sxs-lookup"><span data-stu-id="06012-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="06012-125">Esse valor geralmente está no intervalo de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="06012-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="06012-126">Um valor de 0,0 indica totalmente transparente, enquanto um valor de 1,0 indica totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="06012-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06012-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="06012-127">Remarks</span></span>

<span data-ttu-id="06012-128">Você pode definir os membros dessa estrutura com valores fora do intervalo de 0 a 1 para implementar alguns efeitos incomuns.</span><span class="sxs-lookup"><span data-stu-id="06012-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="06012-129">Valores maiores que 1 produzem luzes fortes que tendem a desbotar uma cena.</span><span class="sxs-lookup"><span data-stu-id="06012-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="06012-130">Valores negativos produzem luzes escuras que realmente removem a luz de uma cena.</span><span class="sxs-lookup"><span data-stu-id="06012-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="06012-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06012-131">Requirements</span></span>



| <span data-ttu-id="06012-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="06012-132">Requirement</span></span> | <span data-ttu-id="06012-133">Valor</span><span class="sxs-lookup"><span data-stu-id="06012-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06012-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06012-134">Header</span></span><br/> | <dl> <span data-ttu-id="06012-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="06012-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06012-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="06012-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06012-137">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="06012-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




