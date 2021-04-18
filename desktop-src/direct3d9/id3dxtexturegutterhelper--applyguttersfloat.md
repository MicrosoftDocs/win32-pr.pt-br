---
description: Aplica medianizes a um buffer de textura flutuante.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'Método ID3DXTextureGutterHelper:: ApplyGuttersFloat (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00ee6eac7328ee5f6adceb5b3966c222509237b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802067"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a><span data-ttu-id="78f3e-103">Método ID3DXTextureGutterHelper:: ApplyGuttersFloat</span><span class="sxs-lookup"><span data-stu-id="78f3e-103">ID3DXTextureGutterHelper::ApplyGuttersFloat method</span></span>

<span data-ttu-id="78f3e-104">Aplica medianizes a um buffer de textura flutuante.</span><span class="sxs-lookup"><span data-stu-id="78f3e-104">Applies gutters to a FLOAT texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="78f3e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78f3e-105">Syntax</span></span>


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a><span data-ttu-id="78f3e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78f3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f3e-107">*pDataIn* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78f3e-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78f3e-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78f3e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78f3e-109">Ponteiro para um buffer de dados de textura FLOAT.</span><span class="sxs-lookup"><span data-stu-id="78f3e-109">Pointer to a buffer of FLOAT texture data.</span></span>

</dd> <dt>

<span data-ttu-id="78f3e-110">*NumCoeffs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78f3e-110">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78f3e-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78f3e-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78f3e-112">Número de escalares por canal de cor usado na memória para armazenar amostras.</span><span class="sxs-lookup"><span data-stu-id="78f3e-112">Number of scalars per color channel used in memory to store samples.</span></span> <span data-ttu-id="78f3e-113">Cada Texel contém valores FLOAT NumCoeffs.</span><span class="sxs-lookup"><span data-stu-id="78f3e-113">Each texel contains NumCoeffs FLOAT values.</span></span>

</dd> <dt>

<span data-ttu-id="78f3e-114">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78f3e-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78f3e-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78f3e-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78f3e-116">Largura da textura, em pixels, Obtida de [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span><span class="sxs-lookup"><span data-stu-id="78f3e-116">Width of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md).</span></span>

</dd> <dt>

<span data-ttu-id="78f3e-117">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78f3e-117">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78f3e-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78f3e-118">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78f3e-119">Altura da textura, em pixels, Obtida de [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md).</span><span class="sxs-lookup"><span data-stu-id="78f3e-119">Height of the texture, in pixels, obtained from [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f3e-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78f3e-120">Return value</span></span>

<span data-ttu-id="78f3e-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78f3e-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78f3e-122">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="78f3e-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="78f3e-123">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="78f3e-123">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="78f3e-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="78f3e-124">Remarks</span></span>

<span data-ttu-id="78f3e-125">A [**classe 2 texels**](id3dxtexturegutterhelper.md) são geradas pela reamostração da classe 1 e 4 texels.</span><span class="sxs-lookup"><span data-stu-id="78f3e-125">[**Class 2 texels**](id3dxtexturegutterhelper.md) are generated by resampling class 1 and 4 texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="78f3e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78f3e-126">Requirements</span></span>



| <span data-ttu-id="78f3e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="78f3e-127">Requirement</span></span> | <span data-ttu-id="78f3e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="78f3e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78f3e-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78f3e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="78f3e-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="78f3e-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="78f3e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78f3e-131">Library</span></span><br/> | <dl> <span data-ttu-id="78f3e-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78f3e-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78f3e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="78f3e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f3e-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="78f3e-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
