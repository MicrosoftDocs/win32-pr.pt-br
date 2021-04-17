---
description: Obtém um ponteiro para a matriz de constantes na tabela de constantes.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'Método ID3DXTextureShader:: GetConstantDesc (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780294"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a><span data-ttu-id="8067b-103">Método ID3DXTextureShader:: GetConstantDesc</span><span class="sxs-lookup"><span data-stu-id="8067b-103">ID3DXTextureShader::GetConstantDesc method</span></span>

<span data-ttu-id="8067b-104">Obtém um ponteiro para a matriz de constantes na tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="8067b-104">Gets a pointer to the array of constants in the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="8067b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8067b-105">Syntax</span></span>


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="8067b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8067b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8067b-107">*hConstant* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8067b-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8067b-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8067b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8067b-109">Identificador exclusivo para uma constante.</span><span class="sxs-lookup"><span data-stu-id="8067b-109">Unique identifier to a constant.</span></span> <span data-ttu-id="8067b-110">Consulte [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="8067b-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="8067b-111">*pDesc* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8067b-111">*pDesc* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8067b-112">Tipo: **[ **D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="8067b-112">Type: **[**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md)\***</span></span>

<span data-ttu-id="8067b-113">Retorna um ponteiro para uma matriz de descrições.</span><span class="sxs-lookup"><span data-stu-id="8067b-113">Returns a pointer to an array of descriptions.</span></span> <span data-ttu-id="8067b-114">Consulte [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md).</span><span class="sxs-lookup"><span data-stu-id="8067b-114">See [**D3DXCONSTANT\_DESC**](d3dxconstant-desc.md).</span></span>

</dd> <dt>

<span data-ttu-id="8067b-115">*pCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8067b-115">*pCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8067b-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8067b-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8067b-117">A entrada fornecida deve ser o tamanho máximo da matriz.</span><span class="sxs-lookup"><span data-stu-id="8067b-117">The input supplied must be the maximum size of the array.</span></span> <span data-ttu-id="8067b-118">A saída é o número de elementos que são preenchidos na matriz quando a função retorna.</span><span class="sxs-lookup"><span data-stu-id="8067b-118">The output is the number of elements that are filled in the array when the function returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8067b-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8067b-119">Return value</span></span>

<span data-ttu-id="8067b-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8067b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8067b-121">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8067b-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8067b-122">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="8067b-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="8067b-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="8067b-123">Remarks</span></span>

<span data-ttu-id="8067b-124">Os exemplos podem aparecer mais de uma vez em uma tabela constante, portanto, esse método pode retornar uma matriz de descrições, cada uma com um índice de registro diferente.</span><span class="sxs-lookup"><span data-stu-id="8067b-124">Samplers can appear more than once in a constant table, therefore, this method can return an array of descriptions each with a different register index.</span></span>

## <a name="requirements"></a><span data-ttu-id="8067b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8067b-125">Requirements</span></span>



| <span data-ttu-id="8067b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8067b-126">Requirement</span></span> | <span data-ttu-id="8067b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8067b-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8067b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8067b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8067b-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8067b-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8067b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8067b-130">Library</span></span><br/> | <dl> <span data-ttu-id="8067b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8067b-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8067b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8067b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8067b-133">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="8067b-133">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> <dt>

[<span data-ttu-id="8067b-134">**ID3DXTextureShader:: GetDesc**</span><span class="sxs-lookup"><span data-stu-id="8067b-134">**ID3DXTextureShader::GetDesc**</span></span>](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
