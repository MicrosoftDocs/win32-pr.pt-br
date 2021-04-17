---
description: Estrutura D3DXSHPRTSPLITMESHCLUSTERDATA
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: Estrutura D3DXSHPRTSPLITMESHCLUSTERDATA (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7b1bc23606dbf08f5a924860e12c9c09d719287
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812391"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a><span data-ttu-id="b387e-103">Estrutura D3DXSHPRTSPLITMESHCLUSTERDATA</span><span class="sxs-lookup"><span data-stu-id="b387e-103">D3DXSHPRTSPLITMESHCLUSTERDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="b387e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b387e-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a><span data-ttu-id="b387e-105">Membros</span><span class="sxs-lookup"><span data-stu-id="b387e-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="b387e-106">**uVertStart**</span><span class="sxs-lookup"><span data-stu-id="b387e-106">**uVertStart**</span></span>
</dt> <dd>

<span data-ttu-id="b387e-107">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b387e-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b387e-108">Vértice inicial na matriz de vértice remapeada.</span><span class="sxs-lookup"><span data-stu-id="b387e-108">Initial vertex into remapped vertex array.</span></span>

</dd> <dt>

<span data-ttu-id="b387e-109">**uVertLength**</span><span class="sxs-lookup"><span data-stu-id="b387e-109">**uVertLength**</span></span>
</dt> <dd>

<span data-ttu-id="b387e-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b387e-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b387e-111">Número de vértices neste supercluster.</span><span class="sxs-lookup"><span data-stu-id="b387e-111">Number of vertices in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="b387e-112">**uFaceStart**</span><span class="sxs-lookup"><span data-stu-id="b387e-112">**uFaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="b387e-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b387e-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b387e-114">Índice inicial na matriz de face.</span><span class="sxs-lookup"><span data-stu-id="b387e-114">Initial index into face array.</span></span>

</dd> <dt>

<span data-ttu-id="b387e-115">**uFaceLength**</span><span class="sxs-lookup"><span data-stu-id="b387e-115">**uFaceLength**</span></span>
</dt> <dd>

<span data-ttu-id="b387e-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b387e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b387e-117">Número de rostos neste supercluster.</span><span class="sxs-lookup"><span data-stu-id="b387e-117">Number of faces in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="b387e-118">**uClusterStart**</span><span class="sxs-lookup"><span data-stu-id="b387e-118">**uClusterStart**</span></span>
</dt> <dd>

<span data-ttu-id="b387e-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b387e-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b387e-120">Índice inicial na matriz de cluster.</span><span class="sxs-lookup"><span data-stu-id="b387e-120">Initial index into cluster array.</span></span>

</dd> <dt>

<span data-ttu-id="b387e-121">**uClusterLength**</span><span class="sxs-lookup"><span data-stu-id="b387e-121">**uClusterLength**</span></span>
</dt> <dd>

<span data-ttu-id="b387e-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b387e-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b387e-123">Número de clusters nesta matriz de supercluster.</span><span class="sxs-lookup"><span data-stu-id="b387e-123">Number of clusters in this supercluster array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b387e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b387e-124">Requirements</span></span>



| <span data-ttu-id="b387e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b387e-125">Requirement</span></span> | <span data-ttu-id="b387e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b387e-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b387e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b387e-127">Header</span></span><br/> | <dl> <span data-ttu-id="b387e-128"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b387e-128"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b387e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b387e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b387e-130">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="b387e-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="b387e-131">**D3DXSHPRTCompSplitMeshSC**</span><span class="sxs-lookup"><span data-stu-id="b387e-131">**D3DXSHPRTCompSplitMeshSC**</span></span>](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
