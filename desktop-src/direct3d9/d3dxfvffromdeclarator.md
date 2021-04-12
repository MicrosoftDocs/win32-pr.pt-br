---
description: Retorna um código de formato de vértice flexível (FVF) de um Declarador.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: Função D3DXFVFFromDeclarator (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fdaf6f80340a08562ed644ee44ac92c42874d149
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298617"
---
# <a name="d3dxfvffromdeclarator-function"></a><span data-ttu-id="806e8-103">Função D3DXFVFFromDeclarator</span><span class="sxs-lookup"><span data-stu-id="806e8-103">D3DXFVFFromDeclarator function</span></span>

<span data-ttu-id="806e8-104">Retorna um código de formato de vértice flexível (FVF) de um Declarador.</span><span class="sxs-lookup"><span data-stu-id="806e8-104">Returns a flexible vertex format (FVF) code from a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="806e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="806e8-105">Syntax</span></span>


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a><span data-ttu-id="806e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="806e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="806e8-107">*pDeclaration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="806e8-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="806e8-108">Tipo: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="806e8-108">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="806e8-109">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que descreve o código FVF.</span><span class="sxs-lookup"><span data-stu-id="806e8-109">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the FVF code.</span></span>

</dd> <dt>

<span data-ttu-id="806e8-110">*pFVF* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="806e8-110">*pFVF* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="806e8-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="806e8-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="806e8-112">Ponteiro para um valor DWORD, que representa a combinação retornada de [D3DFVF](d3dfvf.md) que descreve o formato de vértice retornado do Declarador.</span><span class="sxs-lookup"><span data-stu-id="806e8-112">Pointer to a DWORD value, representing the returned combination of [D3DFVF](d3dfvf.md) that describes the vertex format returned from the declarator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="806e8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="806e8-113">Return value</span></span>

<span data-ttu-id="806e8-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="806e8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="806e8-115">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="806e8-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="806e8-116">Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="806e8-116">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="806e8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="806e8-117">Remarks</span></span>

<span data-ttu-id="806e8-118">Essa função falhará para qualquer Declarador que não mapeie diretamente para um FVF.</span><span class="sxs-lookup"><span data-stu-id="806e8-118">This function will fail for any declarator that does not map directly to an FVF.</span></span>

## <a name="requirements"></a><span data-ttu-id="806e8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="806e8-119">Requirements</span></span>



| <span data-ttu-id="806e8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="806e8-120">Requirement</span></span> | <span data-ttu-id="806e8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="806e8-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="806e8-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="806e8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="806e8-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="806e8-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="806e8-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="806e8-124">Library</span></span><br/> | <dl> <span data-ttu-id="806e8-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="806e8-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="806e8-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="806e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="806e8-127">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="806e8-127">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="806e8-128">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="806e8-128">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
