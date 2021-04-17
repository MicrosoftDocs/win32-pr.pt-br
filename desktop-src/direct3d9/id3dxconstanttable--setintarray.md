---
description: Define uma matriz de inteiros.
ms.assetid: 15add9df-966d-45aa-b29c-d4bed2a125f4
title: 'Método ID3DXConstantTable:: SetIntArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f89de7d784ce355570d369606bfa67ddd6f5acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798080"
---
# <a name="id3dxconstanttablesetintarray-method"></a><span data-ttu-id="fbd80-103">Método ID3DXConstantTable:: SetIntArray</span><span class="sxs-lookup"><span data-stu-id="fbd80-103">ID3DXConstantTable::SetIntArray method</span></span>

<span data-ttu-id="fbd80-104">Define uma matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="fbd80-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd80-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbd80-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const INT               *pn,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="fbd80-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbd80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbd80-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fbd80-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd80-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="fbd80-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="fbd80-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="fbd80-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="fbd80-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fbd80-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd80-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fbd80-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fbd80-112">Identificador exclusivo para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="fbd80-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="fbd80-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fbd80-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="fbd80-114">*PN* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fbd80-114">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd80-115">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fbd80-115">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fbd80-116">Matriz de inteiros.</span><span class="sxs-lookup"><span data-stu-id="fbd80-116">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="fbd80-117">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="fbd80-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd80-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fbd80-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fbd80-119">Número de inteiros na matriz.</span><span class="sxs-lookup"><span data-stu-id="fbd80-119">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbd80-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbd80-120">Return value</span></span>

<span data-ttu-id="fbd80-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fbd80-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fbd80-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fbd80-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fbd80-123">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fbd80-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbd80-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbd80-124">Requirements</span></span>



| <span data-ttu-id="fbd80-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbd80-125">Requirement</span></span> | <span data-ttu-id="fbd80-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fbd80-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd80-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbd80-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fbd80-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbd80-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fbd80-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fbd80-129">Library</span></span><br/> | <dl> <span data-ttu-id="fbd80-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbd80-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fbd80-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbd80-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd80-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="fbd80-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
