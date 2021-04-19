---
description: Defina dados de vértice em um dos buffers de vértice da malha.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'Método ID3DX10Mesh:: SetVertexData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 68d54c6868e44517d42e0b53159f7a23ef45a05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785048"
---
# <a name="id3dx10meshsetvertexdata-method"></a><span data-ttu-id="352d2-103">Método ID3DX10Mesh:: SetVertexData</span><span class="sxs-lookup"><span data-stu-id="352d2-103">ID3DX10Mesh::SetVertexData method</span></span>

<span data-ttu-id="352d2-104">Defina dados de vértice em um dos buffers de vértice da malha.</span><span class="sxs-lookup"><span data-stu-id="352d2-104">Set vertex data into one of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="352d2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="352d2-105">Syntax</span></span>


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a><span data-ttu-id="352d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="352d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="352d2-107">*iBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="352d2-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352d2-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="352d2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="352d2-109">O buffer de vértice a ser preenchido com pData.</span><span class="sxs-lookup"><span data-stu-id="352d2-109">The vertex buffer to be filled with pData.</span></span>

</dd> <dt>

<span data-ttu-id="352d2-110">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="352d2-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352d2-111">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="352d2-111">Type: **const void\***</span></span>

<span data-ttu-id="352d2-112">Os dados de vértice a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="352d2-112">The vertex data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="352d2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="352d2-113">Return value</span></span>

<span data-ttu-id="352d2-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="352d2-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="352d2-115">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="352d2-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="352d2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="352d2-116">Requirements</span></span>



| <span data-ttu-id="352d2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="352d2-117">Requirement</span></span> | <span data-ttu-id="352d2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="352d2-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="352d2-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="352d2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="352d2-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="352d2-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="352d2-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="352d2-121">Library</span></span><br/> | <dl> <span data-ttu-id="352d2-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="352d2-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="352d2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="352d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352d2-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="352d2-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="352d2-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="352d2-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
