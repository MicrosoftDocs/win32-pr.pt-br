---
description: Desenha uma faixa de linha no espaço da tela. A entrada está na forma de uma matriz que define pontos (de D3DXVECTOR2) na faixa de linha.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: 'ID3DXLine: método RAW de:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813438"
---
# <a name="id3dxlinedraw-method"></a><span data-ttu-id="2ed11-104">ID3DXLine: método RAW de:D</span><span class="sxs-lookup"><span data-stu-id="2ed11-104">ID3DXLine::Draw method</span></span>

<span data-ttu-id="2ed11-105">Desenha uma faixa de linha no espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="2ed11-105">Draws a line strip in screen space.</span></span> <span data-ttu-id="2ed11-106">A entrada está na forma de uma matriz que define pontos (de [**D3DXVECTOR2**](d3dxvector2.md)) na faixa de linha.</span><span class="sxs-lookup"><span data-stu-id="2ed11-106">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ed11-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ed11-107">Syntax</span></span>


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="2ed11-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ed11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ed11-109">*pVertexList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ed11-109">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ed11-110">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ed11-110">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2ed11-111">Matriz de vértices que compõem a linha.</span><span class="sxs-lookup"><span data-stu-id="2ed11-111">Array of vertices that make up the line.</span></span> <span data-ttu-id="2ed11-112">Consulte [**D3DXVECTOR2**](d3dxvector2.md).</span><span class="sxs-lookup"><span data-stu-id="2ed11-112">See [**D3DXVECTOR2**](d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ed11-113">*dwVertexListCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ed11-113">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ed11-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ed11-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ed11-115">Número de vértices na lista de vértices.</span><span class="sxs-lookup"><span data-stu-id="2ed11-115">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="2ed11-116">*Cor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2ed11-116">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ed11-117">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2ed11-117">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="2ed11-118">Cor da linha.</span><span class="sxs-lookup"><span data-stu-id="2ed11-118">Color of the line.</span></span> <span data-ttu-id="2ed11-119">Consulte [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="2ed11-119">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ed11-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ed11-120">Return value</span></span>

<span data-ttu-id="2ed11-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ed11-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ed11-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ed11-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ed11-123">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="2ed11-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed11-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ed11-124">Requirements</span></span>



| <span data-ttu-id="2ed11-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ed11-125">Requirement</span></span> | <span data-ttu-id="2ed11-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2ed11-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed11-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ed11-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2ed11-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ed11-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="2ed11-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ed11-129">Library</span></span><br/> | <dl> <span data-ttu-id="2ed11-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ed11-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2ed11-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ed11-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed11-132">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="2ed11-132">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
