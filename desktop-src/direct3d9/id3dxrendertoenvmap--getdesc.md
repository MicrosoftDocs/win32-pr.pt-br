---
description: Recupera a descrição da superfície de renderização.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'Método ID3DXRenderToEnvMap:: GetDesc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663988"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a><span data-ttu-id="999a4-103">Método ID3DXRenderToEnvMap:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="999a4-103">ID3DXRenderToEnvMap::GetDesc method</span></span>

<span data-ttu-id="999a4-104">Recupera a descrição da superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="999a4-104">Retrieves the description of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="999a4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="999a4-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="999a4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="999a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="999a4-107">*pDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="999a4-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="999a4-108">Tipo: **[ **D3DXRTE \_ desc**](d3dxrte-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="999a4-108">Type: **[**D3DXRTE\_DESC**](d3dxrte-desc.md)\***</span></span>

<span data-ttu-id="999a4-109">Ponteiro para uma [**estrutura \_ desc de D3DXRTE**](d3dxrte-desc.md) que descreve a superfície de renderização.</span><span class="sxs-lookup"><span data-stu-id="999a4-109">Pointer to a [**D3DXRTE\_DESC**](d3dxrte-desc.md) structure that describes the rendering surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="999a4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="999a4-110">Return value</span></span>

<span data-ttu-id="999a4-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="999a4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="999a4-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="999a4-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="999a4-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="999a4-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="999a4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="999a4-114">Requirements</span></span>



| <span data-ttu-id="999a4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="999a4-115">Requirement</span></span> | <span data-ttu-id="999a4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="999a4-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="999a4-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="999a4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="999a4-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="999a4-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="999a4-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="999a4-119">Library</span></span><br/> | <dl> <span data-ttu-id="999a4-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="999a4-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="999a4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="999a4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="999a4-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="999a4-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




