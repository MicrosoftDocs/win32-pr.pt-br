---
description: Define uma matriz de vetores 4D.
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
ms.openlocfilehash: a6c68621a3f97251cdd88836792bf55980f28311
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813647"
---
# <a name="id3dxconstanttablesetvectorarray-method"></a><span data-ttu-id="cc049-103">Método ID3DXConstantTable:: SetVectorArray</span><span class="sxs-lookup"><span data-stu-id="cc049-103">ID3DXConstantTable::SetVectorArray method</span></span>

<span data-ttu-id="cc049-104">Define uma matriz de vetores 4D.</span><span class="sxs-lookup"><span data-stu-id="cc049-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc049-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc049-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXVECTOR4       *pVector,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="cc049-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc049-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc049-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc049-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc049-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cc049-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cc049-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="cc049-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="cc049-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc049-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc049-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="cc049-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="cc049-112">Identificador exclusivo para a matriz de constantes de vetor.</span><span class="sxs-lookup"><span data-stu-id="cc049-112">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="cc049-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="cc049-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc049-114">*pVector* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc049-114">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc049-115">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc049-115">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="cc049-116">Matriz de vetores 4D.</span><span class="sxs-lookup"><span data-stu-id="cc049-116">Array of 4D vectors.</span></span>

</dd> <dt>

<span data-ttu-id="cc049-117">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="cc049-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc049-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc049-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc049-119">Número de vetores na matriz.</span><span class="sxs-lookup"><span data-stu-id="cc049-119">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc049-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc049-120">Return value</span></span>

<span data-ttu-id="cc049-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc049-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc049-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc049-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cc049-123">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cc049-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc049-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc049-124">Requirements</span></span>



| <span data-ttu-id="cc049-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc049-125">Requirement</span></span> | <span data-ttu-id="cc049-126">Valor</span><span class="sxs-lookup"><span data-stu-id="cc049-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc049-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc049-127">Header</span></span><br/>  | <dl> <span data-ttu-id="cc049-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc049-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="cc049-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc049-129">Library</span></span><br/> | <dl> <span data-ttu-id="cc049-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc049-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cc049-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc049-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc049-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="cc049-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
