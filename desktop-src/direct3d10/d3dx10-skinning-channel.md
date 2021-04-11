---
description: O membro da decl de vértice para fazer a subaparência do software. Isso é usado com a API ID3DX10SkinInfo::D oSoftwareSkinning.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: Estrutura de D3DX10_SKINNING_CHANNEL (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173062"
---
# <a name="d3dx10_skinning_channel-structure"></a><span data-ttu-id="491f5-104">Estrutura de canal de D3DX10 de \_ aparência \_</span><span class="sxs-lookup"><span data-stu-id="491f5-104">D3DX10\_SKINNING\_CHANNEL structure</span></span>

<span data-ttu-id="491f5-105">O membro da decl de vértice para fazer a subaparência do software.</span><span class="sxs-lookup"><span data-stu-id="491f5-105">The member of the vertex decl to do the software skinning on.</span></span> <span data-ttu-id="491f5-106">Isso é usado com a API [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) .</span><span class="sxs-lookup"><span data-stu-id="491f5-106">This is used with the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span>

## <a name="syntax"></a><span data-ttu-id="491f5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="491f5-107">Syntax</span></span>


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a><span data-ttu-id="491f5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="491f5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="491f5-109">**SrcOffset**</span><span class="sxs-lookup"><span data-stu-id="491f5-109">**SrcOffset**</span></span>
</dt> <dd>

<span data-ttu-id="491f5-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="491f5-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="491f5-111">Deslocamento do início de cada vértice de origem.</span><span class="sxs-lookup"><span data-stu-id="491f5-111">Offset from the beginning of each source vertex.</span></span>

</dd> <dt>

<span data-ttu-id="491f5-112">**DestOffset**</span><span class="sxs-lookup"><span data-stu-id="491f5-112">**DestOffset**</span></span>
</dt> <dd>

<span data-ttu-id="491f5-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="491f5-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="491f5-114">Deslocamento do início de cada vértice de destino.</span><span class="sxs-lookup"><span data-stu-id="491f5-114">Offset from the beginning of each destination vertex.</span></span>

</dd> <dt>

<span data-ttu-id="491f5-115">**IsNormal**</span><span class="sxs-lookup"><span data-stu-id="491f5-115">**IsNormal**</span></span>
</dt> <dd>

<span data-ttu-id="491f5-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="491f5-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="491f5-117">Determina qual matriz de matrizes usar na API [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) .</span><span class="sxs-lookup"><span data-stu-id="491f5-117">Determines which array of matrices to use in the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span> <span data-ttu-id="491f5-118">Se for true, o *pInverseTransposeBoneMatrices* será usado; caso contrário, *pBoneMatrices* será usado.</span><span class="sxs-lookup"><span data-stu-id="491f5-118">If this is true, the *pInverseTransposeBoneMatrices* will be used, otherwise *pBoneMatrices* will be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="491f5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="491f5-119">Requirements</span></span>



| <span data-ttu-id="491f5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="491f5-120">Requirement</span></span> | <span data-ttu-id="491f5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="491f5-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="491f5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="491f5-122">Header</span></span><br/> | <dl> <span data-ttu-id="491f5-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="491f5-123"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="491f5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="491f5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="491f5-125">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="491f5-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
