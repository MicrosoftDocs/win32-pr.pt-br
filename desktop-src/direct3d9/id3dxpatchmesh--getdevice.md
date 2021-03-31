---
description: Obtém o dispositivo que criou a malha.
ms.assetid: b03dadda-ca54-4a55-a0a5-cf5ccdb55a72
title: 'Método ID3DXPatchMesh:: GetDevice (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a026398b719bf3ba9a9c02082105cbc7dd299013
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930730"
---
# <a name="id3dxpatchmeshgetdevice-method"></a><span data-ttu-id="fe3d4-103">Método ID3DXPatchMesh:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="fe3d4-103">ID3DXPatchMesh::GetDevice method</span></span>

<span data-ttu-id="fe3d4-104">Obtém o dispositivo que criou a malha.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-104">Gets the device that created the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3d4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe3d4-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="fe3d4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe3d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe3d4-107">*ppDevice* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fe3d4-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe3d4-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="fe3d4-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="fe3d4-109">Ponteiro para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-109">Pointer to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe3d4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe3d4-110">Return value</span></span>

<span data-ttu-id="fe3d4-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe3d4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe3d4-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe3d4-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe3d4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe3d4-114">Requirements</span></span>



| <span data-ttu-id="fe3d4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe3d4-115">Requirement</span></span> | <span data-ttu-id="fe3d4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fe3d4-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3d4-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe3d4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fe3d4-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe3d4-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fe3d4-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe3d4-119">Library</span></span><br/> | <dl> <span data-ttu-id="fe3d4-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe3d4-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe3d4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe3d4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3d4-122">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="fe3d4-122">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
