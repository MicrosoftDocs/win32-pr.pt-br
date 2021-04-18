---
description: Sinalizadores que indicam o método que o rasterizador usa para criar uma imagem em uma superfície.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Enumeração D3DSCANLINEORDERING (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2eaed36577f881266c12b0a927cfcdc2494f0d57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788754"
---
# <a name="d3dscanlineordering-enumeration"></a><span data-ttu-id="ab61f-103">Enumeração D3DSCANLINEORDERING</span><span class="sxs-lookup"><span data-stu-id="ab61f-103">D3DSCANLINEORDERING enumeration</span></span>

<span data-ttu-id="ab61f-104">Sinalizadores que indicam o método que o rasterizador usa para criar uma imagem em uma superfície.</span><span class="sxs-lookup"><span data-stu-id="ab61f-104">Flags indicating the method the rasterizer uses to create an image on a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab61f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab61f-105">Syntax</span></span>


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a><span data-ttu-id="ab61f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ab61f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ab61f-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ progressivo**</span><span class="sxs-lookup"><span data-stu-id="ab61f-107"><span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING\_PROGRESSIVE**</span></span>
</dt> <dd>

<span data-ttu-id="ab61f-108">A imagem é criada da primeira varredura para a última sem ignorar nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ab61f-108">The image is created from the first scanline to the last without skipping any.</span></span>

</dd> <dt>

<span data-ttu-id="ab61f-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING \_ entrelaçado**</span><span class="sxs-lookup"><span data-stu-id="ab61f-109"><span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING\_INTERLACED**</span></span>
</dt> <dd>

<span data-ttu-id="ab61f-110">A imagem é criada usando o método entrelaçado no qual as linhas ímpares são desenhadas em passagens de números ímpares e até mesmo as linhas são desenhadas em passagens de número par.</span><span class="sxs-lookup"><span data-stu-id="ab61f-110">The image is created using the interlaced method in which odd-numbered lines are drawn on odd-numbered passes and even lines are drawn on even-numbered passes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab61f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab61f-111">Remarks</span></span>

<span data-ttu-id="ab61f-112">Essa enumeração é usada como um membro em [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) e [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).</span><span class="sxs-lookup"><span data-stu-id="ab61f-112">This enumeration is used as a member in [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) and [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab61f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab61f-113">Requirements</span></span>



| <span data-ttu-id="ab61f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab61f-114">Requirement</span></span> | <span data-ttu-id="ab61f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ab61f-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab61f-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab61f-116">Header</span></span><br/> | <dl> <span data-ttu-id="ab61f-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab61f-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab61f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab61f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab61f-119">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="ab61f-119">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




