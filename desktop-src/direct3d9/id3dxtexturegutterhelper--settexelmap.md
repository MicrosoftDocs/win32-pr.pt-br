---
description: Define as coordenadas de textura (u, v) de cada Texel.
ms.assetid: b1f8f5d6-568f-4868-87c9-9d6b1034d898
title: 'Método ID3DXTextureGutterHelper:: SetTexelMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee00394e81dadf147d54dffe0dc02199b2274e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771272"
---
# <a name="id3dxtexturegutterhelpersettexelmap-method"></a><span data-ttu-id="3fb07-103">Método ID3DXTextureGutterHelper:: SetTexelMap</span><span class="sxs-lookup"><span data-stu-id="3fb07-103">ID3DXTextureGutterHelper::SetTexelMap method</span></span>

<span data-ttu-id="3fb07-104">Define as coordenadas de textura (u, v) de cada Texel.</span><span class="sxs-lookup"><span data-stu-id="3fb07-104">Sets the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fb07-105">Syntax</span></span>


```C++
HRESULT SetTexelMap(
  [in] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="3fb07-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fb07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb07-107">*pTexelData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3fb07-107">*pTexelData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb07-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="3fb07-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="3fb07-109">Ponteiro para o local em coordenadas de textura de pixel (u, v) onde cada Texel está localizado.</span><span class="sxs-lookup"><span data-stu-id="3fb07-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb07-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3fb07-110">Return value</span></span>

<span data-ttu-id="3fb07-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3fb07-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3fb07-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3fb07-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3fb07-113">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="3fb07-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb07-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fb07-114">Requirements</span></span>



| <span data-ttu-id="3fb07-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb07-115">Requirement</span></span> | <span data-ttu-id="3fb07-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3fb07-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb07-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fb07-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3fb07-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fb07-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3fb07-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fb07-119">Library</span></span><br/> | <dl> <span data-ttu-id="3fb07-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fb07-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3fb07-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fb07-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb07-122">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="3fb07-122">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




