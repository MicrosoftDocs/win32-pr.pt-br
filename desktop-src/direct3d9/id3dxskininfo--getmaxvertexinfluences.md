---
description: Obtém o número máximo de influências para qualquer vértice na malha.
ms.assetid: 012168e8-30e5-4571-b793-647ab23df068
title: 'Método ID3DXSkinInfo:: GetMaxVertexInfluences (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxVertexInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2acae5cc119df25989e6bf22692ec1609ffa9408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930536"
---
# <a name="id3dxskininfogetmaxvertexinfluences-method"></a><span data-ttu-id="cb734-103">Método ID3DXSkinInfo:: GetMaxVertexInfluences</span><span class="sxs-lookup"><span data-stu-id="cb734-103">ID3DXSkinInfo::GetMaxVertexInfluences method</span></span>

<span data-ttu-id="cb734-104">Obtém o número máximo de influências para qualquer vértice na malha.</span><span class="sxs-lookup"><span data-stu-id="cb734-104">Gets the maximum number of influences for any vertex in the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb734-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb734-105">Syntax</span></span>


```C++
HRESULT GetMaxVertexInfluences(
  [in] DWORD *maxVertexInfluences
);
```



## <a name="parameters"></a><span data-ttu-id="cb734-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb734-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb734-107">*maxVertexInfluences* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cb734-107">*maxVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb734-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb734-108">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cb734-109">Ponteiro para a influência máxima do vértice.</span><span class="sxs-lookup"><span data-stu-id="cb734-109">Pointer to the maximum vertex influence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb734-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb734-110">Return value</span></span>

<span data-ttu-id="cb734-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb734-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb734-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb734-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cb734-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cb734-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb734-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb734-114">Requirements</span></span>



| <span data-ttu-id="cb734-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb734-115">Requirement</span></span> | <span data-ttu-id="cb734-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cb734-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb734-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb734-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cb734-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb734-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cb734-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb734-119">Library</span></span><br/> | <dl> <span data-ttu-id="cb734-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb734-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cb734-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb734-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb734-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="cb734-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
