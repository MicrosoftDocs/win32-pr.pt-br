---
description: Define as dimensões de janela de uma superfície de destino de renderização na qual os projetos de volume 3D.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: Estrutura D3DVIEWPORT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815577"
---
# <a name="d3dviewport9-structure"></a><span data-ttu-id="89234-103">Estrutura D3DVIEWPORT9</span><span class="sxs-lookup"><span data-stu-id="89234-103">D3DVIEWPORT9 structure</span></span>

<span data-ttu-id="89234-104">Define as dimensões de janela de uma superfície de destino de renderização na qual os projetos de volume 3D.</span><span class="sxs-lookup"><span data-stu-id="89234-104">Defines the window dimensions of a render-target surface onto which a 3D volume projects.</span></span>

## <a name="syntax"></a><span data-ttu-id="89234-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89234-105">Syntax</span></span>


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a><span data-ttu-id="89234-106">Membros</span><span class="sxs-lookup"><span data-stu-id="89234-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="89234-107">**X**</span><span class="sxs-lookup"><span data-stu-id="89234-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="89234-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89234-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="89234-109">Coordenada de pixel do canto superior esquerdo do visor na superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="89234-109">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="89234-110">A menos que você queira renderizar para um subconjunto da superfície, esse membro pode ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="89234-110">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="89234-111">**S**</span><span class="sxs-lookup"><span data-stu-id="89234-111">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="89234-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89234-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="89234-113">Coordenada de pixel do canto superior esquerdo do visor na superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="89234-113">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="89234-114">A menos que você queira renderizar para um subconjunto da superfície, esse membro pode ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="89234-114">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="89234-115">**Largura**</span><span class="sxs-lookup"><span data-stu-id="89234-115">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="89234-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89234-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="89234-117">Dimensão de largura do volume do clipe, em pixels.</span><span class="sxs-lookup"><span data-stu-id="89234-117">Width dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="89234-118">A menos que você esteja renderizando apenas para um subconjunto da superfície, esse membro deve ser definido como a dimensão de largura da superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="89234-118">Unless you are rendering only to a subset of the surface, this member should be set to the width dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="89234-119">**Altura**</span><span class="sxs-lookup"><span data-stu-id="89234-119">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="89234-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89234-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="89234-121">Dimensão de altura do volume do clipe, em pixels.</span><span class="sxs-lookup"><span data-stu-id="89234-121">Height dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="89234-122">A menos que você esteja renderizando apenas para um subconjunto da superfície, esse membro deve ser definido como a dimensão de altura da superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="89234-122">Unless you are rendering only to a subset of the surface, this member should be set to the height dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="89234-123">**MinZ**</span><span class="sxs-lookup"><span data-stu-id="89234-123">**MinZ**</span></span>
</dt> <dd>

<span data-ttu-id="89234-124">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="89234-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="89234-125">Junto com MaxZ, o valor que descreve o intervalo de valores de profundidade no qual uma cena deve ser renderizada, os valores mínimo e máximo do volume do clipe.</span><span class="sxs-lookup"><span data-stu-id="89234-125">Together with MaxZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="89234-126">A maioria dos aplicativos define esse valor como 0,0.</span><span class="sxs-lookup"><span data-stu-id="89234-126">Most applications set this value to 0.0.</span></span> <span data-ttu-id="89234-127">O recorte é executado após a aplicação da matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="89234-127">Clipping is performed after applying the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="89234-128">**MaxZ**</span><span class="sxs-lookup"><span data-stu-id="89234-128">**MaxZ**</span></span>
</dt> <dd>

<span data-ttu-id="89234-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="89234-129">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="89234-130">Junto com MinZ, o valor que descreve o intervalo de valores de profundidade no qual uma cena deve ser renderizada, os valores mínimo e máximo do volume do clipe.</span><span class="sxs-lookup"><span data-stu-id="89234-130">Together with MinZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="89234-131">A maioria dos aplicativos define esse valor como 1,0.</span><span class="sxs-lookup"><span data-stu-id="89234-131">Most applications set this value to 1.0.</span></span> <span data-ttu-id="89234-132">O recorte é executado após a aplicação da matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="89234-132">Clipping is performed after applying the projection matrix.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89234-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="89234-133">Remarks</span></span>

<span data-ttu-id="89234-134">Os membros X, Y, Width e Height descrevem a posição e as dimensões do visor na superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="89234-134">The X, Y, Width, and Height members describe the position and dimensions of the viewport on the render-target surface.</span></span> <span data-ttu-id="89234-135">Normalmente, os aplicativos são renderizados para toda a superfície de destino; ao renderizar em uma superfície 640 x 480, esses membros devem ser 0, 0, 640 e 480, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="89234-135">Usually, applications render to the entire target surface; when rendering on a 640 x 480 surface, these members should be 0, 0, 640, and 480, respectively.</span></span> <span data-ttu-id="89234-136">Os MinZ e MaxZ normalmente são definidos como 0,0 e 1,0, mas podem ser definidos como outros valores para obter efeitos específicos.</span><span class="sxs-lookup"><span data-stu-id="89234-136">The MinZ and MaxZ are typically set to 0.0 and 1.0 but can be set to other values to achieve specific effects.</span></span> <span data-ttu-id="89234-137">Por exemplo, você pode defini-los como 0,0 para forçar o sistema a renderizar objetos no primeiro plano de uma cena ou ambos para 1,0 para forçar os objetos em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="89234-137">For example, you might set them both to 0.0 to force the system to render objects to the foreground of a scene, or both to 1.0 to force the objects into the background.</span></span>

<span data-ttu-id="89234-138">Quando os parâmetros do visor de um dispositivo são alterados (devido a uma chamada para o método [**setviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) ), o driver cria uma nova matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="89234-138">When the viewport parameters for a device change (because of a call to the [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) method), the driver builds a new transformation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="89234-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89234-139">Requirements</span></span>



| <span data-ttu-id="89234-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="89234-140">Requirement</span></span> | <span data-ttu-id="89234-141">Valor</span><span class="sxs-lookup"><span data-stu-id="89234-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89234-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89234-142">Header</span></span><br/> | <dl> <span data-ttu-id="89234-143"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="89234-143"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89234-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="89234-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89234-145">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="89234-145">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="89234-146">**Getviewport**</span><span class="sxs-lookup"><span data-stu-id="89234-146">**GetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[<span data-ttu-id="89234-147">**Setviewport**</span><span class="sxs-lookup"><span data-stu-id="89234-147">**SetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
