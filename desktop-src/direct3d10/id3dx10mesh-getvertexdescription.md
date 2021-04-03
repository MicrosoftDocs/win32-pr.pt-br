---
description: Acesse a descrição do vértice passada para D3DX10CreateMesh. A descrição do vértice descreve o layout dos buffers de vértice da malha.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'Método ID3DX10Mesh:: GetVertexDescription (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01888ea83f43e37951b48e03916f18af1ec6ddb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930605"
---
# <a name="id3dx10meshgetvertexdescription-method"></a><span data-ttu-id="11d7d-104">Método ID3DX10Mesh:: GetVertexDescription</span><span class="sxs-lookup"><span data-stu-id="11d7d-104">ID3DX10Mesh::GetVertexDescription method</span></span>

<span data-ttu-id="11d7d-105">Acesse a descrição do vértice passada para [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).</span><span class="sxs-lookup"><span data-stu-id="11d7d-105">Access the vertex description passed into [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md).</span></span> <span data-ttu-id="11d7d-106">A descrição do vértice descreve o layout dos buffers de vértice da malha.</span><span class="sxs-lookup"><span data-stu-id="11d7d-106">The vertex description describes the layout of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="11d7d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11d7d-107">Syntax</span></span>


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a><span data-ttu-id="11d7d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11d7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11d7d-109">*ppDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="11d7d-109">*ppDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11d7d-110">Tipo: **const [**d3d10 \_ de \_ elemento \_ de entrada desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \***</span><span class="sxs-lookup"><span data-stu-id="11d7d-110">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\*\***</span></span>

<span data-ttu-id="11d7d-111">Matriz de elementos de entrada que descrevem o layout dos buffers de vértice da malha.</span><span class="sxs-lookup"><span data-stu-id="11d7d-111">Array of input elements that describe the layout of the mesh's vertex buffers.</span></span> <span data-ttu-id="11d7d-112">Consulte [**o \_ elemento de entrada d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="11d7d-112">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="11d7d-113">*pDeclCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11d7d-113">*pDeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d7d-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="11d7d-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="11d7d-115">O número de elementos de entrada em ppDesc.</span><span class="sxs-lookup"><span data-stu-id="11d7d-115">The number of input elements in ppDesc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11d7d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11d7d-116">Return value</span></span>

<span data-ttu-id="11d7d-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="11d7d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="11d7d-118">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="11d7d-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11d7d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11d7d-119">Requirements</span></span>



| <span data-ttu-id="11d7d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="11d7d-120">Requirement</span></span> | <span data-ttu-id="11d7d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="11d7d-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11d7d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11d7d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="11d7d-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="11d7d-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="11d7d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11d7d-124">Library</span></span><br/> | <dl> <span data-ttu-id="11d7d-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11d7d-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11d7d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="11d7d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d7d-127">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="11d7d-127">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="11d7d-128">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="11d7d-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
