---
description: Usa um sistema de coordenadas à esquerda para criar uma linha.
ms.assetid: 0d2ef331-9edf-4b0a-ace4-ecb8bb2f7352
title: Função D3DXCreateLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cf7d75ca63d64be39733b36a1b7d7a1b464238e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763273"
---
# <a name="d3dxcreateline-function"></a><span data-ttu-id="adf13-103">Função D3DXCreateLine</span><span class="sxs-lookup"><span data-stu-id="adf13-103">D3DXCreateLine function</span></span>

<span data-ttu-id="adf13-104">Usa um sistema de coordenadas à esquerda para criar uma linha.</span><span class="sxs-lookup"><span data-stu-id="adf13-104">Uses a left-handed coordinate system to create a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf13-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adf13-105">Syntax</span></span>


```C++
HRESULT D3DXCreateLine(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXLINE        *ppLine
);
```



## <a name="parameters"></a><span data-ttu-id="adf13-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adf13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf13-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="adf13-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf13-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="adf13-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="adf13-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à malha da caixa criada.</span><span class="sxs-lookup"><span data-stu-id="adf13-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="adf13-110">*ppLine* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="adf13-110">*ppLine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adf13-111">Tipo: **[ **LPD3DXLINE**](id3dxline.md)\***</span><span class="sxs-lookup"><span data-stu-id="adf13-111">Type: **[**LPD3DXLINE**](id3dxline.md)\***</span></span>

<span data-ttu-id="adf13-112">Ponteiro para uma interface [**ID3DXLine**](id3dxline.md) .</span><span class="sxs-lookup"><span data-stu-id="adf13-112">Pointer to an [**ID3DXLine**](id3dxline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf13-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="adf13-113">Return value</span></span>

<span data-ttu-id="adf13-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="adf13-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="adf13-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="adf13-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="adf13-116">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="adf13-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="adf13-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="adf13-117">Remarks</span></span>

<span data-ttu-id="adf13-118">Essa função cria uma malha com a \_ opção de criação gerenciada D3DXMESH e [D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) formato de vértice flexível normal (FVF).</span><span class="sxs-lookup"><span data-stu-id="adf13-118">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) Flexible Vertex Format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="adf13-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adf13-119">Requirements</span></span>



| <span data-ttu-id="adf13-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="adf13-120">Requirement</span></span> | <span data-ttu-id="adf13-121">Valor</span><span class="sxs-lookup"><span data-stu-id="adf13-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="adf13-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="adf13-122">Header</span></span><br/>  | <dl> <span data-ttu-id="adf13-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf13-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="adf13-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="adf13-124">Library</span></span><br/> | <dl> <span data-ttu-id="adf13-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="adf13-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="adf13-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="adf13-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf13-127">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="adf13-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
