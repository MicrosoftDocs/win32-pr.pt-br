---
description: Recupera as coordenadas de textura (u, v) de cada Texel.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: 'Método ID3DXTextureGutterHelper:: GetTexelMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298649"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a><span data-ttu-id="f0149-103">Método ID3DXTextureGutterHelper:: GetTexelMap</span><span class="sxs-lookup"><span data-stu-id="f0149-103">ID3DXTextureGutterHelper::GetTexelMap method</span></span>

<span data-ttu-id="f0149-104">Recupera as coordenadas de textura (u, v) de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="f0149-104">Retrieves the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0149-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0149-105">Syntax</span></span>


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="f0149-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0149-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0149-107">*pTexelData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f0149-107">*pTexelData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0149-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f0149-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f0149-109">Ponteiro para o local em coordenadas de textura de pixel (u, v) onde cada Texel está localizado.</span><span class="sxs-lookup"><span data-stu-id="f0149-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0149-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0149-110">Return value</span></span>

<span data-ttu-id="f0149-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0149-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0149-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f0149-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f0149-113">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="f0149-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="f0149-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0149-114">Remarks</span></span>

<span data-ttu-id="f0149-115">Para a [**classe 2 e 4 texels**](id3dxtexturegutterhelper.md), as coordenadas de textura retornadas (u, v) correspondem ao ponto mais próximo no triângulo mais próximo.</span><span class="sxs-lookup"><span data-stu-id="f0149-115">For [**class 2 and 4 texels**](id3dxtexturegutterhelper.md), the returned (u, v) texture coordinates correspond to the closest point on the closest triangle.</span></span>

<span data-ttu-id="f0149-116">O aplicativo deve alocar e gerenciar pTexelData.</span><span class="sxs-lookup"><span data-stu-id="f0149-116">The application must allocate and manage pTexelData.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0149-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0149-117">Requirements</span></span>



| <span data-ttu-id="f0149-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0149-118">Requirement</span></span> | <span data-ttu-id="f0149-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f0149-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0149-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0149-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f0149-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0149-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f0149-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0149-122">Library</span></span><br/> | <dl> <span data-ttu-id="f0149-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0149-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f0149-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0149-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0149-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="f0149-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




