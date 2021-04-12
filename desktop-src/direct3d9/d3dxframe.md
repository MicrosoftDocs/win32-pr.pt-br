---
description: Encapsula um quadro de transformação em uma hierarquia de quadros de transformação.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: Estrutura D3DXFRAME (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173002"
---
# <a name="d3dxframe-structure"></a><span data-ttu-id="63008-103">Estrutura D3DXFRAME</span><span class="sxs-lookup"><span data-stu-id="63008-103">D3DXFRAME structure</span></span>

<span data-ttu-id="63008-104">Encapsula um quadro de transformação em uma hierarquia de quadros de transformação.</span><span class="sxs-lookup"><span data-stu-id="63008-104">Encapsulates a transform frame in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="63008-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63008-105">Syntax</span></span>


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a><span data-ttu-id="63008-106">Membros</span><span class="sxs-lookup"><span data-stu-id="63008-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="63008-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="63008-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="63008-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="63008-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="63008-109">Nome do quadro.</span><span class="sxs-lookup"><span data-stu-id="63008-109">Name of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="63008-110">**TransformationMatrix**</span><span class="sxs-lookup"><span data-stu-id="63008-110">**TransformationMatrix**</span></span>
</dt> <dd>

<span data-ttu-id="63008-111">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="63008-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63008-112">Matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="63008-112">Transformation matrix.</span></span>

</dd> <dt>

<span data-ttu-id="63008-113">**pMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="63008-113">**pMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="63008-114">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="63008-114">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

</dd> <dd>

<span data-ttu-id="63008-115">Ponteiro para o contêiner de malha.</span><span class="sxs-lookup"><span data-stu-id="63008-115">Pointer to the mesh container.</span></span>

</dd> <dt>

<span data-ttu-id="63008-116">**pFrameSibling**</span><span class="sxs-lookup"><span data-stu-id="63008-116">**pFrameSibling**</span></span>
</dt> <dd>

<span data-ttu-id="63008-117">Tipo: \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="63008-117">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="63008-118">Ponteiro para um quadro irmão.</span><span class="sxs-lookup"><span data-stu-id="63008-118">Pointer to a sibling frame.</span></span>

</dd> <dt>

<span data-ttu-id="63008-119">**pFrameFirstChild**</span><span class="sxs-lookup"><span data-stu-id="63008-119">**pFrameFirstChild**</span></span>
</dt> <dd>

<span data-ttu-id="63008-120">Tipo: \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="63008-120">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="63008-121">Ponteiro para um quadro filho.</span><span class="sxs-lookup"><span data-stu-id="63008-121">Pointer to a child frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63008-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="63008-122">Remarks</span></span>

<span data-ttu-id="63008-123">Um aplicativo pode derivar dessa estrutura para adicionar outros dados.</span><span class="sxs-lookup"><span data-stu-id="63008-123">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="63008-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63008-124">Requirements</span></span>



| <span data-ttu-id="63008-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="63008-125">Requirement</span></span> | <span data-ttu-id="63008-126">Valor</span><span class="sxs-lookup"><span data-stu-id="63008-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63008-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63008-127">Header</span></span><br/> | <dl> <span data-ttu-id="63008-128"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="63008-128"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63008-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="63008-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63008-130">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="63008-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




