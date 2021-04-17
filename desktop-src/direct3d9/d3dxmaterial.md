---
description: Retorna informações de material salvas em arquivos Direct3D (. x).
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: Estrutura D3DXMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763026"
---
# <a name="d3dxmaterial-structure"></a><span data-ttu-id="c48f7-103">Estrutura D3DXMATERIAL</span><span class="sxs-lookup"><span data-stu-id="c48f7-103">D3DXMATERIAL structure</span></span>

<span data-ttu-id="c48f7-104">Retorna informações de material salvas em arquivos Direct3D (. x).</span><span class="sxs-lookup"><span data-stu-id="c48f7-104">Returns material information saved in Direct3D (.x) files.</span></span>

## <a name="syntax"></a><span data-ttu-id="c48f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c48f7-105">Syntax</span></span>


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a><span data-ttu-id="c48f7-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c48f7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c48f7-107">**MatD3D**</span><span class="sxs-lookup"><span data-stu-id="c48f7-107">**MatD3D**</span></span>
</dt> <dd>

<span data-ttu-id="c48f7-108">Tipo: **[ **D3DMATERIAL9**](d3dmaterial9.md)**</span><span class="sxs-lookup"><span data-stu-id="c48f7-108">Type: **[**D3DMATERIAL9**](d3dmaterial9.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c48f7-109">Estrutura [**D3DMATERIAL9**](d3dmaterial9.md) que descreve as propriedades do material.</span><span class="sxs-lookup"><span data-stu-id="c48f7-109">[**D3DMATERIAL9**](d3dmaterial9.md) structure that describes the material properties.</span></span>

</dd> <dt>

<span data-ttu-id="c48f7-110">**pTextureFilename**</span><span class="sxs-lookup"><span data-stu-id="c48f7-110">**pTextureFilename**</span></span>
</dt> <dd>

<span data-ttu-id="c48f7-111">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="c48f7-111">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="c48f7-112">Ponteiro para uma cadeia de caracteres que especifica o nome do arquivo da textura.</span><span class="sxs-lookup"><span data-stu-id="c48f7-112">Pointer to a string that specifies the file name of the texture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c48f7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c48f7-113">Remarks</span></span>

<span data-ttu-id="c48f7-114">As funções [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) e [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) retornam uma matriz de estruturas **D3DXMATERIAL** que especificam a cor do material e o nome da textura para cada material na malha.</span><span class="sxs-lookup"><span data-stu-id="c48f7-114">The [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) and [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) functions return an array of **D3DXMATERIAL** structures that specify the material color and name of the texture for each material in the mesh.</span></span> <span data-ttu-id="c48f7-115">Em seguida, o aplicativo é necessário para carregar a textura.</span><span class="sxs-lookup"><span data-stu-id="c48f7-115">The application is then required to load the texture.</span></span>

<span data-ttu-id="c48f7-116">O tipo LPD3DXMATERIAL é definido como um ponteiro para a estrutura **D3DXMATERIAL** .</span><span class="sxs-lookup"><span data-stu-id="c48f7-116">The LPD3DXMATERIAL type is defined as a pointer to the **D3DXMATERIAL** structure.</span></span>


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a><span data-ttu-id="c48f7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c48f7-117">Requirements</span></span>



| <span data-ttu-id="c48f7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c48f7-118">Requirement</span></span> | <span data-ttu-id="c48f7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c48f7-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c48f7-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c48f7-120">Header</span></span><br/> | <dl> <span data-ttu-id="c48f7-121"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c48f7-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c48f7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c48f7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c48f7-123">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="c48f7-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="c48f7-124">**D3DXLoadMeshFromX**</span><span class="sxs-lookup"><span data-stu-id="c48f7-124">**D3DXLoadMeshFromX**</span></span>](d3dxloadmeshfromx.md)
</dt> <dt>

[<span data-ttu-id="c48f7-125">**D3DXLoadMeshFromXof**</span><span class="sxs-lookup"><span data-stu-id="c48f7-125">**D3DXLoadMeshFromXof**</span></span>](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




