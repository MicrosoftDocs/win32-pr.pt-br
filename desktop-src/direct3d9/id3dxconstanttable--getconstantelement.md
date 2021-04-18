---
description: Obtém uma constante de uma matriz de constantes. Uma matriz é composta de elementos.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'Método ID3DXConstantTable:: getconstantelement (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793836"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a><span data-ttu-id="6df38-104">Método ID3DXConstantTable:: getconstantelement</span><span class="sxs-lookup"><span data-stu-id="6df38-104">ID3DXConstantTable::GetConstantElement method</span></span>

<span data-ttu-id="6df38-105">Obtém uma constante de uma matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="6df38-105">Gets a constant from an array of constants.</span></span> <span data-ttu-id="6df38-106">Uma matriz é composta de elementos.</span><span class="sxs-lookup"><span data-stu-id="6df38-106">An array is made up of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df38-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6df38-107">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="6df38-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6df38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df38-109">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6df38-109">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df38-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6df38-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6df38-111">Identificador exclusivo para a matriz de constantes.</span><span class="sxs-lookup"><span data-stu-id="6df38-111">Unique identifier to the array of constants.</span></span> <span data-ttu-id="6df38-112">Esse valor não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6df38-112">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6df38-113">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="6df38-113">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df38-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6df38-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6df38-115">Índice de base zero do elemento na matriz.</span><span class="sxs-lookup"><span data-stu-id="6df38-115">Zero-based index of the element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df38-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6df38-116">Return value</span></span>

<span data-ttu-id="6df38-117">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6df38-117">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6df38-118">Retorna um identificador exclusivo para a constante do elemento.</span><span class="sxs-lookup"><span data-stu-id="6df38-118">Returns a unique identifier to the element constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="6df38-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6df38-119">Remarks</span></span>

<span data-ttu-id="6df38-120">Para obter uma constante que não faz parte de uma matriz, use [**ID3DXConstantTable:: getconstant**](id3dxconstanttable--getconstant.md) ou [**ID3DXConstantTable:: GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span><span class="sxs-lookup"><span data-stu-id="6df38-120">To get a constant that is not part of an array, use [**ID3DXConstantTable::GetConstant**](id3dxconstanttable--getconstant.md) or [**ID3DXConstantTable::GetConstantByName**](id3dxconstanttable--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6df38-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6df38-121">Requirements</span></span>



| <span data-ttu-id="6df38-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6df38-122">Requirement</span></span> | <span data-ttu-id="6df38-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6df38-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df38-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6df38-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6df38-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6df38-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6df38-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6df38-126">Library</span></span><br/> | <dl> <span data-ttu-id="6df38-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6df38-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6df38-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6df38-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df38-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="6df38-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
