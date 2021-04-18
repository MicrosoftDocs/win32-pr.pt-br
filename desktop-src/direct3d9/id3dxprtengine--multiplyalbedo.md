---
description: Multiplica cada vetor de PRT (transferência radiante em pré-computação) pelo albedo por vértice.
ms.assetid: 2b3e4b19-7778-4240-ac79-3237fda2ed96
title: 'Método ID3DXPRTEngine:: MultiplyAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.MultiplyAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a282605789644382f39fd8fff9ce8bb47d6dfc7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771500"
---
# <a name="id3dxprtenginemultiplyalbedo-method"></a><span data-ttu-id="3a6c2-103">Método ID3DXPRTEngine:: MultiplyAlbedo</span><span class="sxs-lookup"><span data-stu-id="3a6c2-103">ID3DXPRTEngine::MultiplyAlbedo method</span></span>

<span data-ttu-id="3a6c2-104">Multiplica cada vetor de PRT (transferência radiante em pré-computação) pelo albedo por vértice.</span><span class="sxs-lookup"><span data-stu-id="3a6c2-104">Multiplies each precomputed radiance transfer (PRT) vector by the per-vertex albedo.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a6c2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a6c2-105">Syntax</span></span>


```C++
HRESULT MultiplyAlbedo(
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="3a6c2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a6c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a6c2-107">*pDataOut* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3a6c2-107">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a6c2-108">Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="3a6c2-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="3a6c2-109">Ponteiro para um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de saída que conterá vetores de PRT multiplicado pelo albedo por vértice.</span><span class="sxs-lookup"><span data-stu-id="3a6c2-109">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will contain PRT vectors multiplied by the per-vertex albedo.</span></span> <span data-ttu-id="3a6c2-110">Se esse buffer de saída for um objeto de textura, deve-se tomar cuidado para armazenar o albedo da textura na mesma resolução que o buffer de simulação.</span><span class="sxs-lookup"><span data-stu-id="3a6c2-110">If this output buffer is a texture object, then care must be taken to store the albedo of the texture at the same resolution as the simulation buffer.</span></span> <span data-ttu-id="3a6c2-111">Você pode definir a resolução apropriada no albedo com [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), aplicando regiões de medianiz de textura, se apropriado.</span><span class="sxs-lookup"><span data-stu-id="3a6c2-111">You can set the proper resolution on the albedo with [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md), applying texture gutter regions if appropriate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a6c2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a6c2-112">Return value</span></span>

<span data-ttu-id="3a6c2-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a6c2-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a6c2-114">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a6c2-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3a6c2-115">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3a6c2-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a6c2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a6c2-116">Remarks</span></span>

<span data-ttu-id="3a6c2-117">Os métodos ID3DXPRTEngine:: Computexxx calculam os buffers de saída nos quais o sinal leve não foi multiplicado por albedo.</span><span class="sxs-lookup"><span data-stu-id="3a6c2-117">The ID3DXPRTEngine::Computexxx methods compute output buffers in which the light signal has not been multiplied by albedo.</span></span> <span data-ttu-id="3a6c2-118">Ao não multiplicar o albedo, você pode modelar a variação de albedo em uma escala mais fina do que a radiante de origem, gerando assim resultados mais precisos da compactação.</span><span class="sxs-lookup"><span data-stu-id="3a6c2-118">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="3a6c2-119">Para incluir albedo no modelo de leve renderizado, chame esse método após um dos métodos Computexxx.</span><span class="sxs-lookup"><span data-stu-id="3a6c2-119">To include albedo in the rendered-light model, call this method after one of the Computexxx methods.</span></span>

<span data-ttu-id="3a6c2-120">[**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) deve ser chamado antes de chamar este método.</span><span class="sxs-lookup"><span data-stu-id="3a6c2-120">[**ID3DXPRTEngine::SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md) should be called before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a6c2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a6c2-121">Requirements</span></span>



| <span data-ttu-id="3a6c2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a6c2-122">Requirement</span></span> | <span data-ttu-id="3a6c2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3a6c2-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6c2-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a6c2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3a6c2-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a6c2-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3a6c2-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a6c2-126">Library</span></span><br/> | <dl> <span data-ttu-id="3a6c2-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a6c2-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3a6c2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a6c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a6c2-129">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="3a6c2-129">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="3a6c2-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span><span class="sxs-lookup"><span data-stu-id="3a6c2-130">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> </dl>

 

 




