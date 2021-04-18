---
description: Cria uma nova malha e a preenche com os dados de uma malha carregada anteriormente.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'Método ID3DX10Mesh:: CloneMesh (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791611"
---
# <a name="id3dx10meshclonemesh-method"></a><span data-ttu-id="66f05-103">Método ID3DX10Mesh:: CloneMesh</span><span class="sxs-lookup"><span data-stu-id="66f05-103">ID3DX10Mesh::CloneMesh method</span></span>

<span data-ttu-id="66f05-104">Cria uma nova malha e a preenche com os dados de uma malha carregada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="66f05-104">Creates a new mesh and fills it with the data of a previously loaded mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f05-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66f05-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="66f05-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66f05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66f05-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="66f05-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f05-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f05-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f05-109">Sinalizadores de criação a serem aplicados à nova malha.</span><span class="sxs-lookup"><span data-stu-id="66f05-109">Creation flags to be applied to the new mesh.</span></span> <span data-ttu-id="66f05-110">Consulte [**\_ malha D3DX10**](d3dx10-mesh.md).</span><span class="sxs-lookup"><span data-stu-id="66f05-110">See [**D3DX10\_MESH**](d3dx10-mesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="66f05-111">*pPosSemantic* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66f05-111">*pPosSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f05-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f05-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f05-113">O nome semântico dos dados da posição.</span><span class="sxs-lookup"><span data-stu-id="66f05-113">The semantic name for the position data.</span></span>

</dd> <dt>

<span data-ttu-id="66f05-114">*pDesc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66f05-114">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f05-115">Tipo: **const [**d3d10 \_ de \_ elemento \_ de entrada desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="66f05-115">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="66f05-116">Matriz de \_ estruturas desc de elemento de entrada d3d10 \_ \_ , que descreve o formato de vértice para a malha retornada.</span><span class="sxs-lookup"><span data-stu-id="66f05-116">Array of D3D10\_INPUT\_ELEMENT\_DESC structures, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="66f05-117">Consulte [**o \_ elemento de entrada d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="66f05-117">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="66f05-118">*DeclCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66f05-118">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66f05-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="66f05-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="66f05-120">O número de elementos na matriz pDesc.</span><span class="sxs-lookup"><span data-stu-id="66f05-120">The number of elements in the pDesc array.</span></span>

</dd> <dt>

<span data-ttu-id="66f05-121">*ppCloneMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="66f05-121">*ppCloneMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66f05-122">Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="66f05-122">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="66f05-123">A nova malha.</span><span class="sxs-lookup"><span data-stu-id="66f05-123">The new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66f05-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66f05-124">Return value</span></span>

<span data-ttu-id="66f05-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="66f05-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="66f05-126">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="66f05-126">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66f05-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f05-127">Requirements</span></span>



| <span data-ttu-id="66f05-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f05-128">Requirement</span></span> | <span data-ttu-id="66f05-129">Valor</span><span class="sxs-lookup"><span data-stu-id="66f05-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66f05-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66f05-130">Header</span></span><br/>  | <dl> <span data-ttu-id="66f05-131"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f05-131"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="66f05-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66f05-132">Library</span></span><br/> | <dl> <span data-ttu-id="66f05-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66f05-133"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66f05-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="66f05-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f05-135">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="66f05-135">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="66f05-136">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="66f05-136">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
