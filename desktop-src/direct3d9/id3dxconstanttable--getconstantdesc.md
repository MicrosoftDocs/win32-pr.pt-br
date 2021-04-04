---
description: Obtém um ponteiro para uma matriz de descrições constantes na tabela de constantes.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'Método ID3DXConstantTable:: GetConstantDesc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930616"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a><span data-ttu-id="33782-103">Método ID3DXConstantTable:: GetConstantDesc</span><span class="sxs-lookup"><span data-stu-id="33782-103">ID3DXConstantTable::GetConstantDesc method</span></span>

<span data-ttu-id="33782-104">Obtém um ponteiro para uma matriz de descrições constantes na tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="33782-104">Gets a pointer to an array of constant descriptions in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="33782-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33782-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="33782-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33782-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33782-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33782-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33782-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="33782-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="33782-109">Identificador exclusivo para uma constante.</span><span class="sxs-lookup"><span data-stu-id="33782-109">Unique identifier to a constant.</span></span> <span data-ttu-id="33782-110">Consulte [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span><span class="sxs-lookup"><span data-stu-id="33782-110">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="33782-111">*pDesc* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="33782-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="33782-112">Tipo: **[ **D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="33782-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="33782-113">Retorna um ponteiro para uma matriz de descrições.</span><span class="sxs-lookup"><span data-stu-id="33782-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="33782-114">Consulte [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="33782-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="33782-115">*pCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="33782-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="33782-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="33782-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="33782-117">A entrada fornecida deve ser o tamanho máximo da matriz.</span><span class="sxs-lookup"><span data-stu-id="33782-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="33782-118">A saída é o número de elementos que são preenchidos na matriz quando a função retorna.</span><span class="sxs-lookup"><span data-stu-id="33782-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33782-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33782-119">Return value</span></span>

<span data-ttu-id="33782-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33782-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33782-121">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="33782-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="33782-122">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="33782-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="33782-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="33782-123">Remarks</span></span>

<span data-ttu-id="33782-124">**ID3DXConstantTable:: GetConstantDesc** às vezes retornará um [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md) com uma \_ contagem de registro de 0.</span><span class="sxs-lookup"><span data-stu-id="33782-124">**ID3DXConstantTable::GetConstantDesc** will sometimes return a [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md) with a Register\_Count of 0.</span></span> <span data-ttu-id="33782-125">Isso ocorrerá com uma constante exibida em mais de um conjunto de registros \_ , mas não tem espaço no conjunto de registros alocado.</span><span class="sxs-lookup"><span data-stu-id="33782-125">This will happen with a constant appears in more than one Register\_Set but does not have space in that register set allocated.</span></span>

<span data-ttu-id="33782-126">Como um amostra pode aparecer mais de uma vez em uma tabela constante, esse método pode retornar uma matriz de descrições, cada uma com um índice de registro diferente.</span><span class="sxs-lookup"><span data-stu-id="33782-126">Because a sampler can appear more than once in a constant table, this method can return an array of descriptions, each one with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="33782-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33782-127">Requirements</span></span>



| <span data-ttu-id="33782-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="33782-128">Requirement</span></span> | <span data-ttu-id="33782-129">Valor</span><span class="sxs-lookup"><span data-stu-id="33782-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33782-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33782-130">Header</span></span><br/>  | <dl> <span data-ttu-id="33782-131"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="33782-131"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="33782-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33782-132">Library</span></span><br/> | <dl> <span data-ttu-id="33782-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33782-133"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="33782-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="33782-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33782-135">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="33782-135">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="33782-136">**ID3DXConstantTable:: GetDesc**</span><span class="sxs-lookup"><span data-stu-id="33782-136">**ID3DXConstantTable::GetDesc**</span></span>](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
