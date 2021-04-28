---
description: Função D3DX10CreateMesh – cria um objeto de malha usando um Declarador.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: Função D3DX10CreateMesh (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc744536336a4a102bafeaeae3ba87bbad58eb97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113354"
---
# <a name="d3dx10createmesh-function"></a><span data-ttu-id="b590c-103">Função D3DX10CreateMesh</span><span class="sxs-lookup"><span data-stu-id="b590c-103">D3DX10CreateMesh function</span></span>

<span data-ttu-id="b590c-104">Cria um objeto de malha usando um Declarador.</span><span class="sxs-lookup"><span data-stu-id="b590c-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="b590c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b590c-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="b590c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b590c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b590c-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b590c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b590c-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="b590c-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="b590c-109">Ponteiro para uma [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), o objeto de dispositivo a ser associado à malha.</span><span class="sxs-lookup"><span data-stu-id="b590c-109">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b590c-110">*pDeclaration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b590c-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b590c-111">Tipo: **const [**d3d10 \_ de \_ elemento \_ de entrada desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b590c-111">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="b590c-112">Matriz de [**elementos \_ \_ \_ desc de elemento de entrada d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) , que descreve o formato de vértice para a malha retornada.</span><span class="sxs-lookup"><span data-stu-id="b590c-112">Array of [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="b590c-113">Esse parâmetro deve ser mapeado diretamente para um formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="b590c-113">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="b590c-114">*DeclCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b590c-114">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b590c-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b590c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b590c-116">O número de elementos em pDeclaration.</span><span class="sxs-lookup"><span data-stu-id="b590c-116">The number of elements in pDeclaration.</span></span>

</dd> <dt>

<span data-ttu-id="b590c-117">*pPositionSemantic* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b590c-117">*pPositionSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b590c-118">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b590c-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b590c-119">Semântica que identifica qual parte da declaração de vértice contém informações de posição.</span><span class="sxs-lookup"><span data-stu-id="b590c-119">Semantic that identifies which part of the vertex declaration contains position information.</span></span>

</dd> <dt>

<span data-ttu-id="b590c-120">*Contagemdevértice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b590c-120">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b590c-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b590c-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b590c-122">Número de vértices para a malha.</span><span class="sxs-lookup"><span data-stu-id="b590c-122">Number of vertices for the mesh.</span></span> <span data-ttu-id="b590c-123">Esse parâmetro deve ser maior que 0.</span><span class="sxs-lookup"><span data-stu-id="b590c-123">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="b590c-124">*FaceCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b590c-124">*FaceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b590c-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b590c-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b590c-126">Número de faces para a malha.</span><span class="sxs-lookup"><span data-stu-id="b590c-126">Number of faces for the mesh.</span></span> <span data-ttu-id="b590c-127">O intervalo válido para esse número é maior que 0 e um menor que o DWORD (normalmente 65534), pois o último índice é reservado.</span><span class="sxs-lookup"><span data-stu-id="b590c-127">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b590c-128">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b590c-128">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b590c-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b590c-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b590c-130">Combinação de um ou mais sinalizadores da [**\_ malha D3DX10**](d3dx10-mesh.md), especificando as opções para a malha.</span><span class="sxs-lookup"><span data-stu-id="b590c-130">Combination of one or more flags from the [**D3DX10\_MESH**](d3dx10-mesh.md), specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b590c-131">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b590c-131">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b590c-132">Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b590c-132">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="b590c-133">Endereço de um ponteiro para uma [**interface ID3DX10Mesh**](id3dx10mesh.md), que representa o objeto de malha criado.</span><span class="sxs-lookup"><span data-stu-id="b590c-133">Address of a pointer to an [**ID3DX10Mesh Interface**](id3dx10mesh.md), representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b590c-134">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b590c-134">Return value</span></span>

<span data-ttu-id="b590c-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b590c-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b590c-136">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b590c-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b590c-137">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b590c-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b590c-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b590c-138">Requirements</span></span>



| <span data-ttu-id="b590c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b590c-139">Requirement</span></span> | <span data-ttu-id="b590c-140">Valor</span><span class="sxs-lookup"><span data-stu-id="b590c-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b590c-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b590c-141">Header</span></span><br/>  | <dl> <span data-ttu-id="b590c-142"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b590c-142"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b590c-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b590c-143">Library</span></span><br/> | <dl> <span data-ttu-id="b590c-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b590c-144"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b590c-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b590c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b590c-146">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="b590c-146">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="b590c-147">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="b590c-147">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
