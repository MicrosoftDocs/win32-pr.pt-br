---
description: Descreve um destino de renderização fora da tela usado por uma instância de ID3DXRenderToEnvMap.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: Estrutura de D3DXRTE_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 69a5957bc9338abac4441f65066a43efb7dabead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172989"
---
# <a name="d3dxrte_desc-structure"></a><span data-ttu-id="93a95-103">\_Estrutura desc de D3DXRTE</span><span class="sxs-lookup"><span data-stu-id="93a95-103">D3DXRTE\_DESC structure</span></span>

<span data-ttu-id="93a95-104">Descreve um destino de renderização fora da tela usado por uma instância de [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span><span class="sxs-lookup"><span data-stu-id="93a95-104">Describes an off-screen render target used by an instance of [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="93a95-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93a95-105">Syntax</span></span>


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a><span data-ttu-id="93a95-106">Membros</span><span class="sxs-lookup"><span data-stu-id="93a95-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="93a95-107">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="93a95-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="93a95-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93a95-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="93a95-109">Largura e altura em pixels.</span><span class="sxs-lookup"><span data-stu-id="93a95-109">Width and height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="93a95-110">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="93a95-110">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="93a95-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93a95-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="93a95-112">Número máximo de detalhes (LOD).</span><span class="sxs-lookup"><span data-stu-id="93a95-112">Maximum level of detail (LOD) number.</span></span>

</dd> <dt>

<span data-ttu-id="93a95-113">**Formato**</span><span class="sxs-lookup"><span data-stu-id="93a95-113">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="93a95-114">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="93a95-114">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="93a95-115">Formato de buffer de cores.</span><span class="sxs-lookup"><span data-stu-id="93a95-115">Color buffer format.</span></span>

</dd> <dt>

<span data-ttu-id="93a95-116">**DepthStencil**</span><span class="sxs-lookup"><span data-stu-id="93a95-116">**DepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="93a95-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93a95-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="93a95-118">Indica se o z-buffer é necessário.</span><span class="sxs-lookup"><span data-stu-id="93a95-118">Indicates if the z-buffer is needed.</span></span>

</dd> <dt>

<span data-ttu-id="93a95-119">**DepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="93a95-119">**DepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="93a95-120">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="93a95-120">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="93a95-121">Formato do buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="93a95-121">Format of the depth buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93a95-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="93a95-122">Remarks</span></span>

<span data-ttu-id="93a95-123">Esse método é usado para retornar os parâmetros de criação usados ao criar um objeto [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) .</span><span class="sxs-lookup"><span data-stu-id="93a95-123">This method is used to return the creation parameters used when creating an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="93a95-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93a95-124">Requirements</span></span>



| <span data-ttu-id="93a95-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="93a95-125">Requirement</span></span> | <span data-ttu-id="93a95-126">Valor</span><span class="sxs-lookup"><span data-stu-id="93a95-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93a95-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93a95-127">Header</span></span><br/> | <dl> <span data-ttu-id="93a95-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="93a95-128"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93a95-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="93a95-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a95-130">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="93a95-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
