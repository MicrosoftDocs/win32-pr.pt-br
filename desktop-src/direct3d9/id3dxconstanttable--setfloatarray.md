---
description: Define uma matriz de números de ponto flutuante.
ms.assetid: 7a622dd5-47ed-4166-a6df-f484b03e0b5a
title: 'Método ID3DXConstantTable:: SetFloatArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d75d4171ab51859e4095acbe5d3e86d704b1f437
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173037"
---
# <a name="id3dxconstanttablesetfloatarray-method"></a><span data-ttu-id="f6149-103">Método ID3DXConstantTable:: SetFloatArray</span><span class="sxs-lookup"><span data-stu-id="f6149-103">ID3DXConstantTable::SetFloatArray method</span></span>

<span data-ttu-id="f6149-104">Define uma matriz de números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="f6149-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6149-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6149-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const FLOAT             *pf,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="f6149-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6149-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6149-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6149-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6149-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f6149-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f6149-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="f6149-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="f6149-110">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6149-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6149-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="f6149-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="f6149-112">Identificador exclusivo para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="f6149-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="f6149-113">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f6149-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6149-114">*PF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6149-114">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6149-115">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f6149-115">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f6149-116">Matriz de números de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="f6149-116">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="f6149-117">*Contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="f6149-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6149-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6149-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6149-119">Número de valores de ponto flutuante na matriz.</span><span class="sxs-lookup"><span data-stu-id="f6149-119">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6149-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6149-120">Return value</span></span>

<span data-ttu-id="f6149-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f6149-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f6149-122">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f6149-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f6149-123">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f6149-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6149-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6149-124">Requirements</span></span>



| <span data-ttu-id="f6149-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6149-125">Requirement</span></span> | <span data-ttu-id="f6149-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f6149-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6149-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6149-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f6149-128"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6149-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="f6149-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6149-129">Library</span></span><br/> | <dl> <span data-ttu-id="f6149-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6149-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f6149-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6149-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6149-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="f6149-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
