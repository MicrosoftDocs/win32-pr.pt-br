---
description: 'Método ID3DXConstantTable:: getconstant – Obtém uma constante pesquisando seu índice.'
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: 'Método ID3DXConstantTable:: getconstant (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 664a1b1a214b49eb731a3a0766a255e5f5acadd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115264"
---
# <a name="id3dxconstanttablegetconstant-method"></a><span data-ttu-id="2cbe7-103">Método ID3DXConstantTable:: getconstant</span><span class="sxs-lookup"><span data-stu-id="2cbe7-103">ID3DXConstantTable::GetConstant method</span></span>

<span data-ttu-id="2cbe7-104">Obtém uma constante procurando seu índice.</span><span class="sxs-lookup"><span data-stu-id="2cbe7-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cbe7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cbe7-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="2cbe7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cbe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cbe7-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cbe7-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbe7-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2cbe7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2cbe7-109">Identificador exclusivo para a estrutura de dados pai.</span><span class="sxs-lookup"><span data-stu-id="2cbe7-109">Unique identifier to the parent data structure.</span></span> <span data-ttu-id="2cbe7-110">Se a constante for um parâmetro de nível superior (não há nenhuma estrutura de dados pai), use **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2cbe7-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2cbe7-111">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2cbe7-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cbe7-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2cbe7-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2cbe7-113">Índice de base zero da constante.</span><span class="sxs-lookup"><span data-stu-id="2cbe7-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cbe7-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2cbe7-114">Return value</span></span>

<span data-ttu-id="2cbe7-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2cbe7-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2cbe7-116">Retorna um identificador exclusivo para a constante.</span><span class="sxs-lookup"><span data-stu-id="2cbe7-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cbe7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cbe7-117">Remarks</span></span>

<span data-ttu-id="2cbe7-118">Para obter uma constante de uma matriz de constantes, use [**ID3DXConstantTable:: Getconstantelement**](id3dxconstanttable--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="2cbe7-118">To get a constant from an array of constants, use [**ID3DXConstantTable::GetConstantElement**](id3dxconstanttable--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cbe7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cbe7-119">Requirements</span></span>



| <span data-ttu-id="2cbe7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cbe7-120">Requirement</span></span> | <span data-ttu-id="2cbe7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2cbe7-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbe7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2cbe7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2cbe7-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cbe7-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2cbe7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2cbe7-124">Library</span></span><br/> | <dl> <span data-ttu-id="2cbe7-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cbe7-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2cbe7-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2cbe7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbe7-127">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="2cbe7-127">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
