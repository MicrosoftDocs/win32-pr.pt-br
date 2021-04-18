---
description: Acesse o buffer de atributo da malha.
ms.assetid: 01ebb592-1e0d-4d93-b3f5-ad5f1e0225d0
title: 'Método ID3DX10Mesh:: GetAttributeBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 161711cd28dae790fd25ff8dd192945a366e9dd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763933"
---
# <a name="id3dx10meshgetattributebuffer-method"></a><span data-ttu-id="6db39-103">Método ID3DX10Mesh:: GetAttributeBuffer</span><span class="sxs-lookup"><span data-stu-id="6db39-103">ID3DX10Mesh::GetAttributeBuffer method</span></span>

<span data-ttu-id="6db39-104">Acesse o buffer de atributo da malha.</span><span class="sxs-lookup"><span data-stu-id="6db39-104">Access the mesh's attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db39-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6db39-105">Syntax</span></span>


```C++
HRESULT GetAttributeBuffer(
  [out] ID3DX10MeshBuffer **ppAttributeBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="6db39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6db39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6db39-107">*ppAttributeBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6db39-107">*ppAttributeBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6db39-108">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6db39-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="6db39-109">O buffer de atributo.</span><span class="sxs-lookup"><span data-stu-id="6db39-109">The attribute buffer.</span></span> <span data-ttu-id="6db39-110">Consulte [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="6db39-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6db39-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6db39-111">Return value</span></span>

<span data-ttu-id="6db39-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6db39-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6db39-113">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6db39-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6db39-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6db39-114">Requirements</span></span>



| <span data-ttu-id="6db39-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6db39-115">Requirement</span></span> | <span data-ttu-id="6db39-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6db39-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6db39-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6db39-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6db39-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6db39-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6db39-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6db39-119">Library</span></span><br/> | <dl> <span data-ttu-id="6db39-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6db39-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db39-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6db39-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db39-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="6db39-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="6db39-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="6db39-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




