---
description: Conjuntos predefinidos de estado de pipeline usados por blocos de estado (consulte estado de salvamento e restauração de blocos de estado (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Enumeração D3DSTATEBLOCKTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104569467"
---
# <a name="d3dstateblocktype-enumeration"></a><span data-ttu-id="a7ce7-103">Enumeração D3DSTATEBLOCKTYPE</span><span class="sxs-lookup"><span data-stu-id="a7ce7-103">D3DSTATEBLOCKTYPE enumeration</span></span>

<span data-ttu-id="a7ce7-104">Conjuntos predefinidos de estado de pipeline usados por blocos de estado (consulte [estado de salvamento e restauração de blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="a7ce7-104">Predefined sets of pipeline state used by state blocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ce7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7ce7-105">Syntax</span></span>


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a><span data-ttu-id="a7ce7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a7ce7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a7ce7-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ tudo**</span><span class="sxs-lookup"><span data-stu-id="a7ce7-107"><span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="a7ce7-108">Capturar o estado atual do [dispositivo](saving-all-device-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="a7ce7-108">Capture the current [device state](saving-all-device-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7ce7-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ pixelstate**</span><span class="sxs-lookup"><span data-stu-id="a7ce7-109"><span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT\_PIXELSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="a7ce7-110">Capturar o estado atual do [pixel](saving-pixel-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="a7ce7-110">Capture the current [pixel state](saving-pixel-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7ce7-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ vérticestate**</span><span class="sxs-lookup"><span data-stu-id="a7ce7-111"><span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT\_VERTEXSTATE**</span></span>
</dt> <dd>

<span data-ttu-id="a7ce7-112">Capturar o estado atual do [vértice](saving-vertex-states-with-a-stateblock.md).</span><span class="sxs-lookup"><span data-stu-id="a7ce7-112">Capture the current [vertex state](saving-vertex-states-with-a-stateblock.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7ce7-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a7ce7-113"><span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a7ce7-114">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a7ce7-115">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a7ce7-116">Não use esse valor.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-116">Do not use this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7ce7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7ce7-117">Remarks</span></span>

<span data-ttu-id="a7ce7-118">Como mostra o diagrama a seguir, o vértice e o estado do pixel são subconjuntos do estado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-118">As the following diagram shows, vertex and pixel state are both subsets of device state.</span></span>

![diagrama de estado do dispositivo, com estado de vértice e estado de pixel como subconjuntos](images/statesets.png)

<span data-ttu-id="a7ce7-120">Há apenas alguns Estados que são considerados vértice e estado de pixel.</span><span class="sxs-lookup"><span data-stu-id="a7ce7-120">There are only a few states that are considered both vertex and pixel state.</span></span> <span data-ttu-id="a7ce7-121">Esses estados são:</span><span class="sxs-lookup"><span data-stu-id="a7ce7-121">These states are:</span></span>

-   <span data-ttu-id="a7ce7-122">Estado de renderização: D3DRS \_ FOGDENSITY</span><span class="sxs-lookup"><span data-stu-id="a7ce7-122">Render state: D3DRS\_FOGDENSITY</span></span>
-   <span data-ttu-id="a7ce7-123">Estado de renderização: D3DRS \_ FOGSTART</span><span class="sxs-lookup"><span data-stu-id="a7ce7-123">Render state: D3DRS\_FOGSTART</span></span>
-   <span data-ttu-id="a7ce7-124">Estado de renderização: D3DRS \_ FOGEND</span><span class="sxs-lookup"><span data-stu-id="a7ce7-124">Render state: D3DRS\_FOGEND</span></span>
-   <span data-ttu-id="a7ce7-125">Estado de textura: D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="a7ce7-125">Texture state: D3DTSS\_TEXCOORDINDEX</span></span>
-   <span data-ttu-id="a7ce7-126">Estado de textura: D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="a7ce7-126">Texture state: D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>

## <a name="requirements"></a><span data-ttu-id="a7ce7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7ce7-127">Requirements</span></span>



| <span data-ttu-id="a7ce7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7ce7-128">Requirement</span></span> | <span data-ttu-id="a7ce7-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a7ce7-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ce7-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7ce7-130">Header</span></span><br/> | <dl> <span data-ttu-id="a7ce7-131"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7ce7-131"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7ce7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7ce7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ce7-133">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="a7ce7-133">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="a7ce7-134">**IDirect3DDevice9::CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="a7ce7-134">**IDirect3DDevice9::CreateStateBlock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

<span data-ttu-id="a7ce7-135">**IDirect3DDevice9::CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="a7ce7-135">**IDirect3DDevice9::CreateStateBlock**</span></span>
</dt> </dl>

 

 
