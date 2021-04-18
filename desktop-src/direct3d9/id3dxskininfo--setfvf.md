---
description: Define o tipo de formato de vértice flexível (FVF).
ms.assetid: e581dcd4-7e17-4c36-aac9-c2942924cf51
title: 'Método ID3DXSkinInfo:: SetFVF (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 010385597442ba1546c20122f6551fca0cfcf81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807848"
---
# <a name="id3dxskininfosetfvf-method"></a><span data-ttu-id="17b6a-103">Método ID3DXSkinInfo:: SetFVF</span><span class="sxs-lookup"><span data-stu-id="17b6a-103">ID3DXSkinInfo::SetFVF method</span></span>

<span data-ttu-id="17b6a-104">Define o tipo de formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="17b6a-104">Sets the flexible vertex format (FVF) type.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b6a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17b6a-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="17b6a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17b6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b6a-107">*FVF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17b6a-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b6a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17b6a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17b6a-109">Formato de vértice flexível.</span><span class="sxs-lookup"><span data-stu-id="17b6a-109">Flexible vertex format.</span></span> <span data-ttu-id="17b6a-110">Consulte [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="17b6a-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b6a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17b6a-111">Return value</span></span>

<span data-ttu-id="17b6a-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17b6a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17b6a-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="17b6a-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="17b6a-114">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="17b6a-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b6a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b6a-115">Requirements</span></span>



| <span data-ttu-id="17b6a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b6a-116">Requirement</span></span> | <span data-ttu-id="17b6a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="17b6a-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17b6a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17b6a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="17b6a-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="17b6a-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="17b6a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17b6a-120">Library</span></span><br/> | <dl> <span data-ttu-id="17b6a-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17b6a-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17b6a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="17b6a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b6a-123">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="17b6a-123">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
