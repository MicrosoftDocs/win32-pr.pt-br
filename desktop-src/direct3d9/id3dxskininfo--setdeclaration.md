---
description: Define a declaração de vértice.
ms.assetid: cbb802ac-f0ba-41e6-8c67-a787982f975f
title: 'Método ID3DXSkinInfo:: setdeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 821801647ca1aee3deabe69d911bd1cab5f7eb4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298459"
---
# <a name="id3dxskininfosetdeclaration-method"></a><span data-ttu-id="dd30d-103">Método ID3DXSkinInfo:: setdeclaration</span><span class="sxs-lookup"><span data-stu-id="dd30d-103">ID3DXSkinInfo::SetDeclaration method</span></span>

<span data-ttu-id="dd30d-104">Define a declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="dd30d-104">Sets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd30d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd30d-105">Syntax</span></span>


```C++
HRESULT SetDeclaration(
  [in] const D3DVERTEXELEMENT9 *pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="dd30d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd30d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd30d-107">*pDeclaration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dd30d-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd30d-108">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="dd30d-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="dd30d-109">Ponteiro para uma matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="dd30d-109">Pointer to an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd30d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd30d-110">Return value</span></span>

<span data-ttu-id="dd30d-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd30d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd30d-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dd30d-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dd30d-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="dd30d-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd30d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd30d-114">Requirements</span></span>



| <span data-ttu-id="dd30d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd30d-115">Requirement</span></span> | <span data-ttu-id="dd30d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="dd30d-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd30d-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd30d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="dd30d-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd30d-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dd30d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dd30d-119">Library</span></span><br/> | <dl> <span data-ttu-id="dd30d-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd30d-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dd30d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd30d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd30d-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="dd30d-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="dd30d-123">**ID3DXSkinInfo:: getdeclaration**</span><span class="sxs-lookup"><span data-stu-id="dd30d-123">**ID3DXSkinInfo::GetDeclaration**</span></span>](id3dxskininfo--getdeclaration.md)
</dt> </dl>

 

 




