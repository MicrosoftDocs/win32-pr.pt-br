---
description: Define os valores de transformação da coordenada de textura.
ms.assetid: a91f33ce-2db5-437a-ac29-402b26b0d4e1
title: Enumeração D3DTEXTURETRANSFORMFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURETRANSFORMFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 63426c0d57dee02823ee2f37327ba7c66d421b24
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172943"
---
# <a name="d3dtexturetransformflags-enumeration"></a><span data-ttu-id="76485-103">Enumeração D3DTEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="76485-103">D3DTEXTURETRANSFORMFLAGS enumeration</span></span>

<span data-ttu-id="76485-104">Define os valores de transformação da coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="76485-104">Defines texture coordinate transformation values.</span></span>

## <a name="syntax"></a><span data-ttu-id="76485-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76485-105">Syntax</span></span>


```C++
typedef enum D3DTEXTURETRANSFORMFLAGS { 
  D3DTTFF_DISABLE      = 0,
  D3DTTFF_COUNT1       = 1,
  D3DTTFF_COUNT2       = 2,
  D3DTTFF_COUNT3       = 3,
  D3DTTFF_COUNT4       = 4,
  D3DTTFF_PROJECTED    = 256,
  D3DTTFF_FORCE_DWORD  = 0x7fffffff
} D3DTEXTURETRANSFORMFLAGS, *LPD3DTEXTURETRANSFORMFLAGS;
```



## <a name="constants"></a><span data-ttu-id="76485-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="76485-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="76485-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF \_ desabilitar**</span><span class="sxs-lookup"><span data-stu-id="76485-107"><span id="D3DTTFF_DISABLE"></span><span id="d3dttff_disable"></span>**D3DTTFF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="76485-108">As coordenadas de textura são passadas diretamente para o rasterizador.</span><span class="sxs-lookup"><span data-stu-id="76485-108">Texture coordinates are passed directly to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="76485-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF \_ COUNT1**</span><span class="sxs-lookup"><span data-stu-id="76485-109"><span id="D3DTTFF_COUNT1"></span><span id="d3dttff_count1"></span>**D3DTTFF\_COUNT1**</span></span>
</dt> <dd>

<span data-ttu-id="76485-110">O rasterizador deve esperar coordenadas de textura 1D.</span><span class="sxs-lookup"><span data-stu-id="76485-110">The rasterizer should expect 1D texture coordinates.</span></span> <span data-ttu-id="76485-111">Esse valor é usado pelo processamento de vértice de função fixa; Ele deve ser definido como 0 ao usar um sombreador de vértice programável.</span><span class="sxs-lookup"><span data-stu-id="76485-111">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="76485-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF \_ COUNT2**</span><span class="sxs-lookup"><span data-stu-id="76485-112"><span id="D3DTTFF_COUNT2"></span><span id="d3dttff_count2"></span>**D3DTTFF\_COUNT2**</span></span>
</dt> <dd>

<span data-ttu-id="76485-113">O rasterizador deve esperar coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="76485-113">The rasterizer should expect 2D texture coordinates.</span></span> <span data-ttu-id="76485-114">Esse valor é usado pelo processamento de vértice de função fixa; Ele deve ser definido como 0 ao usar um sombreador de vértice programável.</span><span class="sxs-lookup"><span data-stu-id="76485-114">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="76485-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF \_ COUNT3**</span><span class="sxs-lookup"><span data-stu-id="76485-115"><span id="D3DTTFF_COUNT3"></span><span id="d3dttff_count3"></span>**D3DTTFF\_COUNT3**</span></span>
</dt> <dd>

<span data-ttu-id="76485-116">O rasterizador deve esperar coordenadas de textura 3D.</span><span class="sxs-lookup"><span data-stu-id="76485-116">The rasterizer should expect 3D texture coordinates.</span></span> <span data-ttu-id="76485-117">Esse valor é usado pelo processamento de vértice de função fixa; Ele deve ser definido como 0 ao usar um sombreador de vértice programável.</span><span class="sxs-lookup"><span data-stu-id="76485-117">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="76485-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF \_ COUNT4**</span><span class="sxs-lookup"><span data-stu-id="76485-118"><span id="D3DTTFF_COUNT4"></span><span id="d3dttff_count4"></span>**D3DTTFF\_COUNT4**</span></span>
</dt> <dd>

<span data-ttu-id="76485-119">O rasterizador deve esperar coordenadas de textura 4D.</span><span class="sxs-lookup"><span data-stu-id="76485-119">The rasterizer should expect 4D texture coordinates.</span></span> <span data-ttu-id="76485-120">Esse valor é usado pelo processamento de vértice de função fixa; Ele deve ser definido como 0 ao usar um sombreador de vértice programável.</span><span class="sxs-lookup"><span data-stu-id="76485-120">This value is used by fixed function vertex processing; it should be set to 0 when using a programmable vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="76485-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF \_ projetado**</span><span class="sxs-lookup"><span data-stu-id="76485-121"><span id="D3DTTFF_PROJECTED"></span><span id="d3dttff_projected"></span>**D3DTTFF\_PROJECTED**</span></span>
</dt> <dd>

<span data-ttu-id="76485-122">Esse sinalizador é respeitado pelo pipeline de pixel de função fixa, bem como pelo pipeline de pixel programável nas versões PS \_ 1 \_ 1 para PS \_ 1 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="76485-122">This flag is honored by the fixed function pixel pipeline, as well as the programmable pixel pipeline in versions ps\_1\_1 to ps\_1\_3.</span></span> <span data-ttu-id="76485-123">Quando a projeção de textura está habilitada para um estágio de textura, todos os quatro valores de ponto flutuante devem ser gravados no registro de textura correspondente.</span><span class="sxs-lookup"><span data-stu-id="76485-123">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span> <span data-ttu-id="76485-124">Cada coordenada de textura é dividida pelo último elemento antes de ser passada para o rasterizador.</span><span class="sxs-lookup"><span data-stu-id="76485-124">Each texture coordinate is divided by the last element before being passed to the rasterizer.</span></span> <span data-ttu-id="76485-125">Por exemplo, se esse sinalizador for especificado com o \_ sinalizador D3DTTFF COUNT3, a primeira e a segunda coordenadas de textura serão divididas pela terceira coordenada antes de serem passadas para o rasterizador.</span><span class="sxs-lookup"><span data-stu-id="76485-125">For example, if this flag is specified with the D3DTTFF\_COUNT3 flag, the first and second texture coordinates are divided by the third coordinate before being passed to the rasterizer.</span></span>

</dd> <dt>

<span data-ttu-id="76485-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="76485-126"><span id="D3DTTFF_FORCE_DWORD"></span><span id="d3dttff_force_dword"></span>**D3DTTFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="76485-127">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="76485-127">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="76485-128">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="76485-128">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="76485-129">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="76485-129">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76485-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="76485-130">Remarks</span></span>

<span data-ttu-id="76485-131">As coordenadas de textura podem ser transformadas usando uma matriz de 4 x 4 antes que os resultados sejam passados para o rasterizador.</span><span class="sxs-lookup"><span data-stu-id="76485-131">Texture coordinates can be transformed using a 4 x 4 matrix before the results are passed to the rasterizer.</span></span> <span data-ttu-id="76485-132">As transformações de coordenadas de textura são definidas chamando [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api)e passando o \_ estado de estágio de textura D3DTSS TEXTURETRANSFORMFLAGS e um dos valores de **D3DTEXTURETRANSFORMFLAGS**.</span><span class="sxs-lookup"><span data-stu-id="76485-132">The texture coordinate transforms are set by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api), and by passing in the D3DTSS\_TEXTURETRANSFORMFLAGS texture stage state and one of the values from **D3DTEXTURETRANSFORMFLAGS**.</span></span> <span data-ttu-id="76485-133">Para obter mais informações sobre transformações de textura, consulte [transformações de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="76485-133">For more information about texture transforms, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76485-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76485-134">Requirements</span></span>



| <span data-ttu-id="76485-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="76485-135">Requirement</span></span> | <span data-ttu-id="76485-136">Valor</span><span class="sxs-lookup"><span data-stu-id="76485-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76485-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76485-137">Header</span></span><br/> | <dl> <span data-ttu-id="76485-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="76485-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76485-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="76485-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76485-140">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="76485-140">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="76485-141">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="76485-141">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
