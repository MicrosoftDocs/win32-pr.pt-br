---
description: Desenha uma faixa de linha no espaço da tela com uma matriz de transformação de entrada especificada.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: 'ID3DXLine: método rawTransform de:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763980"
---
# <a name="id3dxlinedrawtransform-method"></a><span data-ttu-id="b3ad9-103">ID3DXLine: método rawTransform de:D</span><span class="sxs-lookup"><span data-stu-id="b3ad9-103">ID3DXLine::DrawTransform method</span></span>

<span data-ttu-id="b3ad9-104">Desenha uma faixa de linha no espaço da tela com uma matriz de transformação de entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-104">Draws a line strip in screen space with a specified input transformation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ad9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3ad9-105">Syntax</span></span>


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a><span data-ttu-id="b3ad9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3ad9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3ad9-107">*pVertexList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3ad9-107">*pVertexList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ad9-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3ad9-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b3ad9-109">Matriz de vértices que compõem a linha.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-109">Array of vertices that make up the line.</span></span> <span data-ttu-id="b3ad9-110">Consulte [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="b3ad9-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3ad9-111">*dwVertexListCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3ad9-111">*dwVertexListCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ad9-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3ad9-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3ad9-113">Número de vértices na lista de vértices.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-113">Number of vertices in the vertex list.</span></span>

</dd> <dt>

<span data-ttu-id="b3ad9-114">*pTransform* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3ad9-114">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ad9-115">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3ad9-115">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b3ad9-116">Uma matriz de tamanho, rotação e conversão (SRT) para transformar os pontos.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-116">A scale, rotate, and translate (SRT) matrix for transforming the points.</span></span> <span data-ttu-id="b3ad9-117">Consulte [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="b3ad9-117">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span> <span data-ttu-id="b3ad9-118">Se essa matriz for uma matriz de projeção, todas as linhas stippled serão desenhadas com um padrão stippling de perspectiva correta.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-118">If this matrix is a projection matrix, any stippled lines will be drawn with a perspective-correct stippling pattern.</span></span> <span data-ttu-id="b3ad9-119">Ou, você pode transformar os vértices e usar [**ID3DXLine::D RAW**](id3dxline--draw.md) para desenhar a linha com um padrão de Stipple que não seja de perspectiva correta.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-119">Or, you can transform the vertices and use [**ID3DXLine::Draw**](id3dxline--draw.md) to draw the line with a nonperspective-correct stipple pattern.</span></span>

</dd> <dt>

<span data-ttu-id="b3ad9-120">*Cor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b3ad9-120">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ad9-121">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="b3ad9-121">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="b3ad9-122">Cor da linha.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-122">Color of the line.</span></span> <span data-ttu-id="b3ad9-123">Consulte [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="b3ad9-123">See [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3ad9-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3ad9-124">Return value</span></span>

<span data-ttu-id="b3ad9-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3ad9-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3ad9-126">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-126">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b3ad9-127">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="b3ad9-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ad9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3ad9-128">Requirements</span></span>



| <span data-ttu-id="b3ad9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3ad9-129">Requirement</span></span> | <span data-ttu-id="b3ad9-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b3ad9-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ad9-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3ad9-131">Header</span></span><br/>  | <dl> <span data-ttu-id="b3ad9-132"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3ad9-132"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b3ad9-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3ad9-133">Library</span></span><br/> | <dl> <span data-ttu-id="b3ad9-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3ad9-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3ad9-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3ad9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ad9-136">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="b3ad9-136">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
