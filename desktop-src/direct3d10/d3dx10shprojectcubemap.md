---
description: Projeta uma função representada em um mapa de cubo em harmônicas esféricas.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: Função D3DX10SHProjectCubeMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761311"
---
# <a name="d3dx10shprojectcubemap-function"></a><span data-ttu-id="45df1-103">Função D3DX10SHProjectCubeMap</span><span class="sxs-lookup"><span data-stu-id="45df1-103">D3DX10SHProjectCubeMap function</span></span>

<span data-ttu-id="45df1-104">Projeta uma função representada em um mapa de cubo em harmônicas esféricas.</span><span class="sxs-lookup"><span data-stu-id="45df1-104">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="45df1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45df1-105">Syntax</span></span>


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="45df1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45df1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45df1-107">*Ordem*</span><span class="sxs-lookup"><span data-stu-id="45df1-107">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="45df1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45df1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45df1-109">Ordem da avaliação SH, gera a ordem ^ 2 coefs, o grau é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="45df1-109">Order of the SH evaluation, generates Order^2 coefs, degree is Order-1.</span></span>

</dd> <dt>

<span data-ttu-id="45df1-110">*pCubeMap*</span><span class="sxs-lookup"><span data-stu-id="45df1-110">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="45df1-111">Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="45df1-111">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="45df1-112">Cubemap que vai ser projetado em harmônicas esféricas.</span><span class="sxs-lookup"><span data-stu-id="45df1-112">Cubemap that is going to be projected into spherical harmonics.</span></span> <span data-ttu-id="45df1-113">Consulte [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span><span class="sxs-lookup"><span data-stu-id="45df1-113">See [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span></span>

</dd> <dt>

<span data-ttu-id="45df1-114">*pROut*</span><span class="sxs-lookup"><span data-stu-id="45df1-114">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="45df1-115">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="45df1-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="45df1-116">Vetor SH de saída para vermelho.</span><span class="sxs-lookup"><span data-stu-id="45df1-116">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="45df1-117">*pGOut*</span><span class="sxs-lookup"><span data-stu-id="45df1-117">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="45df1-118">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="45df1-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="45df1-119">Gerar vetor de saída para verde.</span><span class="sxs-lookup"><span data-stu-id="45df1-119">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="45df1-120">*pBOut*</span><span class="sxs-lookup"><span data-stu-id="45df1-120">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="45df1-121">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="45df1-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="45df1-122">Vetor SH de saída para azul.</span><span class="sxs-lookup"><span data-stu-id="45df1-122">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45df1-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45df1-123">Return value</span></span>

<span data-ttu-id="45df1-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="45df1-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="45df1-125">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="45df1-125">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="45df1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45df1-126">Requirements</span></span>



| <span data-ttu-id="45df1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="45df1-127">Requirement</span></span> | <span data-ttu-id="45df1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="45df1-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45df1-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45df1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="45df1-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="45df1-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="45df1-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45df1-131">Library</span></span><br/> | <dl> <span data-ttu-id="45df1-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45df1-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="45df1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="45df1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45df1-134">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="45df1-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
