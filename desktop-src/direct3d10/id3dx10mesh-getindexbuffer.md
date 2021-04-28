---
description: 'Método ID3DX10Mesh:: GetIndexBuffer – recupera os dados em um buffer de índice.'
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
ms.openlocfilehash: 751d6dd0376dc73f0213ddb83a19954dc154d633
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084024"
---
# <a name="id3dx10meshgetindexbuffer-method"></a><span data-ttu-id="cefcc-103">Método ID3DX10Mesh:: GetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="cefcc-103">ID3DX10Mesh::GetIndexBuffer method</span></span>

<span data-ttu-id="cefcc-104">Recupera os dados em um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="cefcc-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cefcc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cefcc-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="cefcc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cefcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cefcc-107">*ppIndexBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cefcc-107">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cefcc-108">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cefcc-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="cefcc-109">Endereço de um ponteiro para uma interface ID3DX10MeshBuffer, representando o buffer de índice associado à malha.</span><span class="sxs-lookup"><span data-stu-id="cefcc-109">Address of a pointer to a ID3DX10MeshBuffer interface, representing the index buffer associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cefcc-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cefcc-110">Return value</span></span>

<span data-ttu-id="cefcc-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cefcc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cefcc-112">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cefcc-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cefcc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cefcc-113">Requirements</span></span>



| <span data-ttu-id="cefcc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cefcc-114">Requirement</span></span> | <span data-ttu-id="cefcc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cefcc-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cefcc-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cefcc-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cefcc-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cefcc-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cefcc-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cefcc-118">Library</span></span><br/> | <dl> <span data-ttu-id="cefcc-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cefcc-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cefcc-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cefcc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cefcc-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="cefcc-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="cefcc-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="cefcc-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




