---
description: Recupera os dados em um buffer de índice.
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: 'Método ID3DX10Mesh:: GetIndexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c2777a9d530ac7217b1cc0f3c0f148998cc70ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370957"
---
# <a name="id3dx10meshgetindexbuffer-method"></a><span data-ttu-id="fcbc0-103">Método ID3DX10Mesh:: GetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="fcbc0-103">ID3DX10Mesh::GetIndexBuffer method</span></span>

<span data-ttu-id="fcbc0-104">Recupera os dados em um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="fcbc0-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcbc0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcbc0-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="fcbc0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fcbc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcbc0-107">*ppIndexBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fcbc0-107">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbc0-108">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="fcbc0-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="fcbc0-109">Endereço de um ponteiro para uma interface ID3DX10MeshBuffer, representando o buffer de índice associado à malha.</span><span class="sxs-lookup"><span data-stu-id="fcbc0-109">Address of a pointer to a ID3DX10MeshBuffer interface, representing the index buffer associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcbc0-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fcbc0-110">Return value</span></span>

<span data-ttu-id="fcbc0-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fcbc0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fcbc0-112">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fcbc0-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcbc0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcbc0-113">Requirements</span></span>



| <span data-ttu-id="fcbc0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcbc0-114">Requirement</span></span> | <span data-ttu-id="fcbc0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fcbc0-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbc0-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fcbc0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fcbc0-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcbc0-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fcbc0-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcbc0-118">Library</span></span><br/> | <dl> <span data-ttu-id="fcbc0-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcbc0-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcbc0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcbc0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcbc0-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="fcbc0-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="fcbc0-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="fcbc0-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




