---
description: Recebe um valor de classe Texel que indica a classe Texel de acordo com o local de cada Texel.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'Método ID3DXTextureGutterHelper:: GetGutterMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105751365"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a><span data-ttu-id="dda52-103">Método ID3DXTextureGutterHelper:: GetGutterMap</span><span class="sxs-lookup"><span data-stu-id="dda52-103">ID3DXTextureGutterHelper::GetGutterMap method</span></span>

<span data-ttu-id="dda52-104">Recebe um valor de classe Texel que indica a classe Texel de acordo com o local de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="dda52-104">Receives a texel class value that indicates texel class according to each texel's location.</span></span>

## <a name="syntax"></a><span data-ttu-id="dda52-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dda52-105">Syntax</span></span>


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a><span data-ttu-id="dda52-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dda52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda52-107">*pGutterData* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="dda52-107">*pGutterData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dda52-108">Tipo: **[ **byte**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dda52-108">Type: **[**BYTE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dda52-109">Ponteiro para a classe Texel.</span><span class="sxs-lookup"><span data-stu-id="dda52-109">Pointer to the texel class.</span></span> <span data-ttu-id="dda52-110">As classes Texel possíveis são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="dda52-110">Possible texel classes are as follows.</span></span> <span data-ttu-id="dda52-111">Não há nenhuma classe de Texel 3.</span><span class="sxs-lookup"><span data-stu-id="dda52-111">There is no texel class 3.</span></span>



| <span data-ttu-id="dda52-112">Classe Texel</span><span class="sxs-lookup"><span data-stu-id="dda52-112">Texel Class</span></span> | <span data-ttu-id="dda52-113">Local Texel</span><span class="sxs-lookup"><span data-stu-id="dda52-113">Texel Location</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dda52-114">0</span><span class="sxs-lookup"><span data-stu-id="dda52-114">0</span></span>           | <span data-ttu-id="dda52-115">Ponto inválido; Texel não será usado.</span><span class="sxs-lookup"><span data-stu-id="dda52-115">Invalid point; texel will not be used.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="dda52-116">1</span><span class="sxs-lookup"><span data-stu-id="dda52-116">1</span></span>           | <span data-ttu-id="dda52-117">Triângulo interno.</span><span class="sxs-lookup"><span data-stu-id="dda52-117">Inside triangle.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="dda52-118">2</span><span class="sxs-lookup"><span data-stu-id="dda52-118">2</span></span>           | <span data-ttu-id="dda52-119">Dentro da medianiz.</span><span class="sxs-lookup"><span data-stu-id="dda52-119">Inside gutter.</span></span>                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="dda52-120">4</span><span class="sxs-lookup"><span data-stu-id="dda52-120">4</span></span>           | <span data-ttu-id="dda52-121">Na medianiz; Texel será avaliado como um exemplo completo nos métodos [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)ou [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) .</span><span class="sxs-lookup"><span data-stu-id="dda52-121">Inside gutter; texel will be evaluated as a full sample in the [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md), or [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) methods.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dda52-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dda52-122">Return value</span></span>

<span data-ttu-id="dda52-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dda52-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dda52-124">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dda52-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dda52-125">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="dda52-125">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="dda52-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="dda52-126">Remarks</span></span>

<span data-ttu-id="dda52-127">O aplicativo deve alocar e gerenciar pGutterData, com o tamanho fornecido por:</span><span class="sxs-lookup"><span data-stu-id="dda52-127">The application must allocate and manage pGutterData, with size given by:</span></span>


```
texture width * texture height * sizeof(BYTE)
```



<span data-ttu-id="dda52-128">A largura e a altura da textura são retornadas por [**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md) e [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md).</span><span class="sxs-lookup"><span data-stu-id="dda52-128">Texture width and height are returned by [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) and [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dda52-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dda52-129">Requirements</span></span>



| <span data-ttu-id="dda52-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="dda52-130">Requirement</span></span> | <span data-ttu-id="dda52-131">Valor</span><span class="sxs-lookup"><span data-stu-id="dda52-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dda52-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dda52-132">Header</span></span><br/>  | <dl> <span data-ttu-id="dda52-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dda52-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dda52-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dda52-134">Library</span></span><br/> | <dl> <span data-ttu-id="dda52-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dda52-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dda52-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="dda52-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda52-137">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="dda52-137">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
