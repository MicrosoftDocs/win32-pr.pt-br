---
description: Localiza o quadro filho de um quadro raiz.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: Função D3DXFrameFind (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764998"
---
# <a name="d3dxframefind-function"></a><span data-ttu-id="4e480-103">Função D3DXFrameFind</span><span class="sxs-lookup"><span data-stu-id="4e480-103">D3DXFrameFind function</span></span>

<span data-ttu-id="4e480-104">Localiza o quadro filho de um quadro raiz.</span><span class="sxs-lookup"><span data-stu-id="4e480-104">Finds the child frame of a root frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e480-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e480-105">Syntax</span></span>


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a><span data-ttu-id="4e480-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e480-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e480-107">*pFrameRoot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e480-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e480-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e480-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="4e480-109">Ponteiro para o quadro raiz.</span><span class="sxs-lookup"><span data-stu-id="4e480-109">Pointer to the root frame.</span></span> <span data-ttu-id="4e480-110">Consulte [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e480-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e480-111">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4e480-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e480-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e480-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e480-113">Nome do quadro filho a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="4e480-113">Name of the child frame to find.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e480-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e480-114">Return value</span></span>

<span data-ttu-id="4e480-115">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="4e480-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="4e480-116">Retorna o quadro filho se ele for encontrado ou **NULL** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4e480-116">Returns the child frame if it is found, or **NULL** otherwise.</span></span> <span data-ttu-id="4e480-117">Consulte [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e480-117">See [**D3DXFRAME**](d3dxframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e480-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e480-118">Requirements</span></span>



| <span data-ttu-id="4e480-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e480-119">Requirement</span></span> | <span data-ttu-id="4e480-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4e480-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e480-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e480-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4e480-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e480-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4e480-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e480-123">Library</span></span><br/> | <dl> <span data-ttu-id="4e480-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e480-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e480-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e480-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e480-126">Funções de animação</span><span class="sxs-lookup"><span data-stu-id="4e480-126">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
