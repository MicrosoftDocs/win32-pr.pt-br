---
description: 'Método ID3DXConstantTable:: SetVectorArray – define uma matriz de vetores 4D.'
ms.assetid: bd453384-4f38-4017-a9a5-cac605919940
title: 'Método ID3DXConstantTable:: SetVectorArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe93ef7a75cda743399133445a5f6efd34dd5ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115004"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="6bdb8-103">Método ID3DXConstantTable:: SetVectorArray</span><span class="sxs-lookup"><span data-stu-id="6bdb8-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="6bdb8-104">Define uma matriz de vetores 4D.</span><span class="sxs-lookup"><span data-stu-id="6bdb8-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bdb8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6bdb8-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="6bdb8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6bdb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bdb8-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bdb8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bdb8-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6bdb8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6bdb8-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="6bdb8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="6bdb8-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bdb8-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bdb8-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6bdb8-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6bdb8-112">Identificador exclusivo para a matriz de constantes de vetor.</span><span class="sxs-lookup"><span data-stu-id="6bdb8-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="6bdb8-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6bdb8-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bdb8-114">*pVector* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6bdb8-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bdb8-115">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6bdb8-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6bdb8-116">Matriz de vetores 4D.</span><span class="sxs-lookup"><span data-stu-id="6bdb8-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="6bdb8-117">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="6bdb8-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bdb8-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6bdb8-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6bdb8-119">Número de vetores na matriz.</span><span class="sxs-lookup"><span data-stu-id="6bdb8-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bdb8-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6bdb8-120">Return value</span></span>

<span data-ttu-id="6bdb8-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6bdb8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6bdb8-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6bdb8-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6bdb8-123">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6bdb8-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bdb8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bdb8-124">Requirements</span></span>



| <span data-ttu-id="6bdb8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bdb8-125">Requirement</span></span> | <span data-ttu-id="6bdb8-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6bdb8-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bdb8-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bdb8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6bdb8-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bdb8-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6bdb8-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bdb8-129">Library</span></span><br/> | <dl> <span data-ttu-id="6bdb8-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bdb8-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6bdb8-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6bdb8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bdb8-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="6bdb8-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
