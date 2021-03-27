---
title: Função D3DX11SHProjectCubeMap (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca matemática de harmônicas esféricas, SHProjectCubeMap.
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- Função D3DX11SHProjectCubeMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989331"
---
# <a name="d3dx11shprojectcubemap-function"></a><span data-ttu-id="99971-105">Função D3DX11SHProjectCubeMap</span><span class="sxs-lookup"><span data-stu-id="99971-105">D3DX11SHProjectCubeMap function</span></span>

> [!Note]  
> <span data-ttu-id="99971-106">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="99971-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="99971-107">Em vez de usar essa função, recomendamos que você use a biblioteca [matemática de harmônicas esféricas](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) , **SHProjectCubeMap**.</span><span class="sxs-lookup"><span data-stu-id="99971-107">Instead of using this function, we recommend that you use the [Spherical Harmonics Math](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) library, **SHProjectCubeMap**.</span></span>

 

<span data-ttu-id="99971-108">Projeta uma função representada em um mapa de cubo em harmônicas esféricas.</span><span class="sxs-lookup"><span data-stu-id="99971-108">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="99971-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99971-109">Syntax</span></span>


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="99971-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99971-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99971-111">*pContext*</span><span class="sxs-lookup"><span data-stu-id="99971-111">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="99971-112">Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="99971-112">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="99971-113">Um ponteiro para um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="99971-113">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="99971-114">*Ordem*</span><span class="sxs-lookup"><span data-stu-id="99971-114">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="99971-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="99971-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="99971-116">Ordem da avaliação SH, gera coeficientes de ordem ^ 2 cujo grau é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="99971-116">Order of the SH evaluation, generates Order^2 coefficients whose degree is Order-1.</span></span> <span data-ttu-id="99971-117">O intervalo válido está entre 2 e 6.</span><span class="sxs-lookup"><span data-stu-id="99971-117">Valid range is between 2 and 6.</span></span>

</dd> <dt>

<span data-ttu-id="99971-118">*pCubeMap*</span><span class="sxs-lookup"><span data-stu-id="99971-118">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="99971-119">Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="99971-119">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="99971-120">Um ponteiro para um [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) que representa um cubemap que vai ser projetado em harmônicas esféricas.</span><span class="sxs-lookup"><span data-stu-id="99971-120">A pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) that represents a cubemap that is going to be projected into spherical harmonics.</span></span>

</dd> <dt>

<span data-ttu-id="99971-121">*pROut*</span><span class="sxs-lookup"><span data-stu-id="99971-121">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="99971-122">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="99971-122">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="99971-123">Vetor SH de saída para vermelho.</span><span class="sxs-lookup"><span data-stu-id="99971-123">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="99971-124">*pGOut*</span><span class="sxs-lookup"><span data-stu-id="99971-124">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="99971-125">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="99971-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="99971-126">Gerar vetor de saída para verde.</span><span class="sxs-lookup"><span data-stu-id="99971-126">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="99971-127">*pBOut*</span><span class="sxs-lookup"><span data-stu-id="99971-127">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="99971-128">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="99971-128">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="99971-129">Vetor SH de saída para azul.</span><span class="sxs-lookup"><span data-stu-id="99971-129">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99971-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99971-130">Return value</span></span>

<span data-ttu-id="99971-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99971-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99971-132">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="99971-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99971-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99971-133">Requirements</span></span>



| <span data-ttu-id="99971-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="99971-134">Requirement</span></span> | <span data-ttu-id="99971-135">Valor</span><span class="sxs-lookup"><span data-stu-id="99971-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99971-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99971-136">Header</span></span><br/>  | <dl> <span data-ttu-id="99971-137"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="99971-137"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="99971-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99971-138">Library</span></span><br/> | <dl> <span data-ttu-id="99971-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99971-139"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="99971-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="99971-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99971-141">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="99971-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

