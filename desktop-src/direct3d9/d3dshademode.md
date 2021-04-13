---
description: Define constantes que descrevem os modos de sombreamento com suporte.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Enumeração D3DSHADEMODE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298557"
---
# <a name="d3dshademode-enumeration"></a><span data-ttu-id="53896-103">Enumeração D3DSHADEMODE</span><span class="sxs-lookup"><span data-stu-id="53896-103">D3DSHADEMODE enumeration</span></span>

<span data-ttu-id="53896-104">Define constantes que descrevem os modos de sombreamento com suporte.</span><span class="sxs-lookup"><span data-stu-id="53896-104">Defines constants that describe the supported shading modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="53896-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53896-105">Syntax</span></span>


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a><span data-ttu-id="53896-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="53896-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="53896-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ simples**</span><span class="sxs-lookup"><span data-stu-id="53896-107"><span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE\_FLAT**</span></span>
</dt> <dd>

<span data-ttu-id="53896-108">Modo de sombreamento simples.</span><span class="sxs-lookup"><span data-stu-id="53896-108">Flat shading mode.</span></span> <span data-ttu-id="53896-109">A cor e o componente especular do primeiro vértice no triângulo são usados para determinar a cor e o componente especular da face.</span><span class="sxs-lookup"><span data-stu-id="53896-109">The color and specular component of the first vertex in the triangle are used to determine the color and specular component of the face.</span></span> <span data-ttu-id="53896-110">Essas cores permanecem constantes em todo o triângulo; ou seja, eles não são interpolados.</span><span class="sxs-lookup"><span data-stu-id="53896-110">These colors remain constant across the triangle; that is, they are not interpolated.</span></span> <span data-ttu-id="53896-111">O alfa especular é interpolado.</span><span class="sxs-lookup"><span data-stu-id="53896-111">The specular alpha is interpolated.</span></span> <span data-ttu-id="53896-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="53896-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="53896-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ GOURAUD**</span><span class="sxs-lookup"><span data-stu-id="53896-113"><span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE\_GOURAUD**</span></span>
</dt> <dd>

<span data-ttu-id="53896-114">Modo de sombreamento Gouraud.</span><span class="sxs-lookup"><span data-stu-id="53896-114">Gouraud shading mode.</span></span> <span data-ttu-id="53896-115">Os componentes de cor e especulação da face são determinados por uma interpolação linear entre os três vértices do triângulo.</span><span class="sxs-lookup"><span data-stu-id="53896-115">The color and specular components of the face are determined by a linear interpolation between all three of the triangle's vertices.</span></span>

</dd> <dt>

<span data-ttu-id="53896-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ PHONG**</span><span class="sxs-lookup"><span data-stu-id="53896-116"><span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE\_PHONG**</span></span>
</dt> <dd>

<span data-ttu-id="53896-117">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="53896-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="53896-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="53896-118"><span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="53896-119">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="53896-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="53896-120">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="53896-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="53896-121">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="53896-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53896-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="53896-122">Remarks</span></span>

<span data-ttu-id="53896-123">O primeiro vértice de um triângulo para o modo de sombreamento simples é definido da maneira a seguir.</span><span class="sxs-lookup"><span data-stu-id="53896-123">The first vertex of a triangle for flat shading mode is defined in the following manner.</span></span>

-   <span data-ttu-id="53896-124">Para uma lista de triângulos, o primeiro vértice do triângulo i é \* 3.</span><span class="sxs-lookup"><span data-stu-id="53896-124">For a triangle list, the first vertex of the triangle i is i \* 3.</span></span>
-   <span data-ttu-id="53896-125">Para uma faixa de triângulo, o primeiro vértice do triângulo i é o vértice i.</span><span class="sxs-lookup"><span data-stu-id="53896-125">For a triangle strip, the first vertex of the triangle i is vertex i.</span></span>
-   <span data-ttu-id="53896-126">Para um ventilador de triângulo, o primeiro vértice do triângulo i é o vértice i + 1.</span><span class="sxs-lookup"><span data-stu-id="53896-126">For a triangle fan, the first vertex of the triangle i is vertex i + 1.</span></span>

<span data-ttu-id="53896-127">Os membros desse tipo enumerado definem o valores para o \_ estado de RENDERIZAÇÃO D3DRS shadmode.</span><span class="sxs-lookup"><span data-stu-id="53896-127">The members of this enumerated type define the vales for the D3DRS\_SHADEMODE render state.</span></span>

## <a name="requirements"></a><span data-ttu-id="53896-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53896-128">Requirements</span></span>



| <span data-ttu-id="53896-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="53896-129">Requirement</span></span> | <span data-ttu-id="53896-130">Valor</span><span class="sxs-lookup"><span data-stu-id="53896-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53896-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53896-131">Header</span></span><br/> | <dl> <span data-ttu-id="53896-132"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="53896-132"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53896-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="53896-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53896-134">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="53896-134">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="53896-135">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="53896-135">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
