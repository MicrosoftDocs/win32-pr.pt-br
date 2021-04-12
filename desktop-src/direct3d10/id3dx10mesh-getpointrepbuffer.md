---
description: Obtenha o buffer do representante do ponto da malha.
ms.assetid: 4be7bee5-15ea-496f-83c2-a3a9bafd97c6
title: 'Método ID3DX10Mesh:: GetPointRepBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetPointRepBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 131094792f35b21fd230b66bda6a43fb104b65ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091971"
---
# <a name="id3dx10meshgetpointrepbuffer-method"></a><span data-ttu-id="7c0c6-103">Método ID3DX10Mesh:: GetPointRepBuffer</span><span class="sxs-lookup"><span data-stu-id="7c0c6-103">ID3DX10Mesh::GetPointRepBuffer method</span></span>

<span data-ttu-id="7c0c6-104">Obtenha o buffer do representante do ponto da malha.</span><span class="sxs-lookup"><span data-stu-id="7c0c6-104">Get the mesh's point rep buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c0c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c0c6-105">Syntax</span></span>


```C++
HRESULT GetPointRepBuffer(
  [out] ID3DX10MeshBuffer **ppPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="7c0c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c0c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c0c6-107">*ppPointReps* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7c0c6-107">*ppPointReps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c0c6-108">Tipo: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7c0c6-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="7c0c6-109">Ponteiro para um buffer de malha que contém os dados do representante de ponto da malha.</span><span class="sxs-lookup"><span data-stu-id="7c0c6-109">Pointer to a mesh buffer containing the mesh's point rep data.</span></span> <span data-ttu-id="7c0c6-110">Consulte [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="7c0c6-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c0c6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c0c6-111">Return value</span></span>

<span data-ttu-id="7c0c6-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c0c6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c0c6-113">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7c0c6-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c0c6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c0c6-114">Requirements</span></span>



| <span data-ttu-id="7c0c6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c0c6-115">Requirement</span></span> | <span data-ttu-id="7c0c6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7c0c6-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0c6-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c0c6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7c0c6-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c0c6-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c0c6-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c0c6-119">Library</span></span><br/> | <dl> <span data-ttu-id="7c0c6-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c0c6-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c0c6-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c0c6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0c6-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="7c0c6-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="7c0c6-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="7c0c6-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




