---
description: Opções de soldagem em vértices.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: Enumeração D3DXWELDEPSILONSFLAGS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298657"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a><span data-ttu-id="292d9-103">Enumeração D3DXWELDEPSILONSFLAGS</span><span class="sxs-lookup"><span data-stu-id="292d9-103">D3DXWELDEPSILONSFLAGS enumeration</span></span>

<span data-ttu-id="292d9-104">Opções de soldagem em vértices.</span><span class="sxs-lookup"><span data-stu-id="292d9-104">Options for welding together vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="292d9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="292d9-105">Syntax</span></span>


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a><span data-ttu-id="292d9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="292d9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="292d9-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS \_ WELDALL**</span><span class="sxs-lookup"><span data-stu-id="292d9-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS\_WELDALL**</span></span>
</dt> <dd>

<span data-ttu-id="292d9-108">A solda em todos os vértices que estão no mesmo local.</span><span class="sxs-lookup"><span data-stu-id="292d9-108">Weld together all vertices that are at the same location.</span></span> <span data-ttu-id="292d9-109">O uso desse sinalizador evita uma comparação de Épsilon entre componentes de vértice.</span><span class="sxs-lookup"><span data-stu-id="292d9-109">Using this flag avoids an epsilon comparison between vertex components.</span></span>

</dd> <dt>

<span data-ttu-id="292d9-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS \_ WELDPARTIALMATCHES**</span><span class="sxs-lookup"><span data-stu-id="292d9-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS\_WELDPARTIALMATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="292d9-111">Se um determinado componente de vértice estiver dentro de épsilon, modifique os vértices parcialmente correspondentes para que ambos os componentes sejam idênticos.</span><span class="sxs-lookup"><span data-stu-id="292d9-111">If a given vertex component is within epsilon, modify partially matched vertices so that both components are identical.</span></span> <span data-ttu-id="292d9-112">Se todos os componentes forem iguais, remova um dos vértices.</span><span class="sxs-lookup"><span data-stu-id="292d9-112">If all components are equal, remove one of the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="292d9-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS \_ DONOTREMOVEVERTICES**</span><span class="sxs-lookup"><span data-stu-id="292d9-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS\_DONOTREMOVEVERTICES**</span></span>
</dt> <dd>

<span data-ttu-id="292d9-114">Instrui a solda para permitir apenas modificações em vértices e não na remoção.</span><span class="sxs-lookup"><span data-stu-id="292d9-114">Instructs the weld to allow only modifications to vertices and not removal.</span></span> <span data-ttu-id="292d9-115">Esse sinalizador só será válido se D3DXWELDEPSILONS \_ WELDPARTIALMATCHES for definido.</span><span class="sxs-lookup"><span data-stu-id="292d9-115">This flag is valid only if D3DXWELDEPSILONS\_WELDPARTIALMATCHES is set.</span></span> <span data-ttu-id="292d9-116">É útil modificar vértices para que sejam iguais, mas não permitir que os vértices sejam removidos.</span><span class="sxs-lookup"><span data-stu-id="292d9-116">It is useful to modify vertices to be equal, but not to allow vertices to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="292d9-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="292d9-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="292d9-118">Instrui a solda não a dividir os vértices que estão em grupos de atributos separados.</span><span class="sxs-lookup"><span data-stu-id="292d9-118">Instructs the weld not to split vertices that are in separate attribute groups.</span></span> <span data-ttu-id="292d9-119">Quando o método [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) é chamado com o \_ sinalizador D3DXMESHOPT ATTRSORT, o sinalizador D3DXMESHOPT \_ DONOTSPLIT também será definido.</span><span class="sxs-lookup"><span data-stu-id="292d9-119">When the [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) method is called with the D3DXMESHOPT\_ATTRSORT flag, then the D3DXMESHOPT\_DONOTSPLIT flag will also be set.</span></span> <span data-ttu-id="292d9-120">A definição desse sinalizador pode tornar o processamento de vértice de software lento.</span><span class="sxs-lookup"><span data-stu-id="292d9-120">Setting this flag can slow down software vertex processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="292d9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="292d9-121">Requirements</span></span>



| <span data-ttu-id="292d9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="292d9-122">Requirement</span></span> | <span data-ttu-id="292d9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="292d9-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="292d9-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="292d9-124">Header</span></span><br/> | <dl> <span data-ttu-id="292d9-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="292d9-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="292d9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="292d9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="292d9-127">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="292d9-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="292d9-128">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="292d9-128">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 




