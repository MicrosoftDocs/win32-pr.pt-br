---
description: Obtém os atributos do patch.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'Método ID3DXPatchMesh:: GetPatchInfo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70308857aa66551ed371dbe511acb6bd2d211bfb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105753900"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a><span data-ttu-id="3bd0b-103">Método ID3DXPatchMesh:: GetPatchInfo</span><span class="sxs-lookup"><span data-stu-id="3bd0b-103">ID3DXPatchMesh::GetPatchInfo method</span></span>

<span data-ttu-id="3bd0b-104">Obtém os atributos do patch.</span><span class="sxs-lookup"><span data-stu-id="3bd0b-104">Gets the attributes of the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd0b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bd0b-105">Syntax</span></span>


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3bd0b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bd0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd0b-107">*PatchInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3bd0b-107">*PatchInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd0b-108">Tipo: **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="3bd0b-108">Type: **[**LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span></span>

<span data-ttu-id="3bd0b-109">Ponteiro para as estruturas que contêm os atributos de patch.</span><span class="sxs-lookup"><span data-stu-id="3bd0b-109">Pointer to the structures containing the patch attributes.</span></span> <span data-ttu-id="3bd0b-110">Para obter mais informações sobre atributos de patch, consulte [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="3bd0b-110">For more information about patch attributes, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd0b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bd0b-111">Return value</span></span>

<span data-ttu-id="3bd0b-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3bd0b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3bd0b-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3bd0b-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3bd0b-114">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3bd0b-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd0b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bd0b-115">Requirements</span></span>



| <span data-ttu-id="3bd0b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bd0b-116">Requirement</span></span> | <span data-ttu-id="3bd0b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3bd0b-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd0b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bd0b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3bd0b-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bd0b-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3bd0b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3bd0b-120">Library</span></span><br/> | <dl> <span data-ttu-id="3bd0b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bd0b-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3bd0b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bd0b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd0b-123">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="3bd0b-123">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




