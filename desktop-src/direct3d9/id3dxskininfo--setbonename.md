---
description: Define o nome do Bone.
ms.assetid: 2eecddb8-4efa-41a3-be83-7404047a9857
title: 'Método ID3DXSkinInfo:: setossoname (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetBoneName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c9190c12eac21963d116f60d5a7aa09f97db796
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172915"
---
# <a name="id3dxskininfosetbonename-method"></a><span data-ttu-id="1658c-103">Método ID3DXSkinInfo:: setbonename</span><span class="sxs-lookup"><span data-stu-id="1658c-103">ID3DXSkinInfo::SetBoneName method</span></span>

<span data-ttu-id="1658c-104">Define o nome do Bone.</span><span class="sxs-lookup"><span data-stu-id="1658c-104">Sets the bone name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1658c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1658c-105">Syntax</span></span>


```C++
HRESULT SetBoneName(
  [in] DWORD  Bone,
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="1658c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1658c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1658c-107">*Bone* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1658c-107">*Bone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1658c-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1658c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1658c-109">Número do Bone</span><span class="sxs-lookup"><span data-stu-id="1658c-109">Bone number</span></span>

</dd> <dt>

<span data-ttu-id="1658c-110">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1658c-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1658c-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1658c-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1658c-112">Nome do Bone</span><span class="sxs-lookup"><span data-stu-id="1658c-112">Bone name</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1658c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1658c-113">Return value</span></span>

<span data-ttu-id="1658c-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1658c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1658c-115">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1658c-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1658c-116">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1658c-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1658c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1658c-117">Remarks</span></span>

<span data-ttu-id="1658c-118">Os nomes de Bone são retornados por [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span><span class="sxs-lookup"><span data-stu-id="1658c-118">Bone names are returned by [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1658c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1658c-119">Requirements</span></span>



| <span data-ttu-id="1658c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1658c-120">Requirement</span></span> | <span data-ttu-id="1658c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1658c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1658c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1658c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1658c-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1658c-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1658c-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1658c-124">Library</span></span><br/> | <dl> <span data-ttu-id="1658c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1658c-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1658c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1658c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1658c-127">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="1658c-127">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="1658c-128">**ID3DXSkinInfo:: getbonename**</span><span class="sxs-lookup"><span data-stu-id="1658c-128">**ID3DXSkinInfo::GetBoneName**</span></span>](id3dxskininfo--getbonename.md)
</dt> </dl>

 

 
