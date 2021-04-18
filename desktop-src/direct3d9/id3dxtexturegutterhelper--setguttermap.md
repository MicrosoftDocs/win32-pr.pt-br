---
description: Define um valor de classe Texel que indica a classe Texel de acordo com o local de cada Texel.
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'Método ID3DXTextureGutterHelper:: SetGutterMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793343"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a><span data-ttu-id="ddff2-103">Método ID3DXTextureGutterHelper:: SetGutterMap</span><span class="sxs-lookup"><span data-stu-id="ddff2-103">ID3DXTextureGutterHelper::SetGutterMap method</span></span>

<span data-ttu-id="ddff2-104">Define um valor de classe Texel que indica a classe Texel de acordo com o local de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="ddff2-104">Sets a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddff2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ddff2-105">Syntax</span></span>


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="ddff2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddff2-107">*pGutterData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ddff2-107">*pGutterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddff2-108">Tipo: **[ **byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ddff2-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ddff2-109">Ponteiro para a classe Texel.</span><span class="sxs-lookup"><span data-stu-id="ddff2-109">Pointer to the texel class.</span></span> <span data-ttu-id="ddff2-110">As classes Texel possíveis são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="ddff2-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="ddff2-111">Não há nenhuma classe de Texel 3.</span><span class="sxs-lookup"><span data-stu-id="ddff2-111">There is no texel class 3.</span></span>



| <span data-ttu-id="ddff2-112">Classe Texel</span><span class="sxs-lookup"><span data-stu-id="ddff2-112">Texel Class</span></span> | <span data-ttu-id="ddff2-113">Local Texel</span><span class="sxs-lookup"><span data-stu-id="ddff2-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddff2-114">0</span><span class="sxs-lookup"><span data-stu-id="ddff2-114">0</span></span>           | <span data-ttu-id="ddff2-115">Ponto inválido; Texel não será usado.</span><span class="sxs-lookup"><span data-stu-id="ddff2-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ddff2-116">1</span><span class="sxs-lookup"><span data-stu-id="ddff2-116">1</span></span>           | <span data-ttu-id="ddff2-117">Triângulo interno.</span><span class="sxs-lookup"><span data-stu-id="ddff2-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="ddff2-118">2</span><span class="sxs-lookup"><span data-stu-id="ddff2-118">2</span></span>           | <span data-ttu-id="ddff2-119">Dentro da medianiz.</span><span class="sxs-lookup"><span data-stu-id="ddff2-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ddff2-120">4</span><span class="sxs-lookup"><span data-stu-id="ddff2-120">4</span></span>           | <span data-ttu-id="ddff2-121">Na medianiz; Texel será avaliado como um exemplo completo nos métodos [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="ddff2-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddff2-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ddff2-122">Return value</span></span>

<span data-ttu-id="ddff2-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ddff2-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ddff2-124">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ddff2-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ddff2-125">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="ddff2-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="ddff2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddff2-126">Requirements</span></span>



| <span data-ttu-id="ddff2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddff2-127">Requirement</span></span> | <span data-ttu-id="ddff2-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ddff2-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddff2-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ddff2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ddff2-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddff2-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ddff2-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ddff2-131">Library</span></span><br/> | <dl> <span data-ttu-id="ddff2-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddff2-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ddff2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddff2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddff2-134">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="ddff2-134">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
