---
description: Retorna um Declarador de um código de formato de vértice flexível (FVF).
ms.assetid: 0272239c-0873-4a5c-b046-541f4ba603f4
title: Função D3DXDeclaratorFromFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDeclaratorFromFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de5360c7f9bd28d4c97184f985f06e48ca0002d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105784686"
---
# <a name="d3dxdeclaratorfromfvf-function"></a><span data-ttu-id="af35b-103">Função D3DXDeclaratorFromFVF</span><span class="sxs-lookup"><span data-stu-id="af35b-103">D3DXDeclaratorFromFVF function</span></span>

<span data-ttu-id="af35b-104">Retorna um Declarador de um código de formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="af35b-104">Returns a declarator from a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="af35b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af35b-105">Syntax</span></span>


```C++
HRESULT D3DXDeclaratorFromFVF(
  _In_    DWORD             FVF,
  _Inout_ D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="af35b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af35b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af35b-107">*FVF* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af35b-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af35b-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af35b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af35b-109">Combinação de [D3DFVF](d3dfvf.md) que descreve o FVF do qual gerar a matriz de Declarador retornado.</span><span class="sxs-lookup"><span data-stu-id="af35b-109">Combination of [D3DFVF](d3dfvf.md) that describes the FVF from which to generate the returned declarator array.</span></span>

</dd> <dt>

<span data-ttu-id="af35b-110">*Declaração* \[ de entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="af35b-110">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="af35b-111">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="af35b-111">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="af35b-112">Uma matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) que descreve o formato de vértice dos vértices de malha.</span><span class="sxs-lookup"><span data-stu-id="af35b-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="af35b-113">O limite superior dessa matriz de Declarador é o [**tamanho máximo de \_ \_ DECL \_ FVF**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="af35b-113">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af35b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af35b-114">Return value</span></span>

<span data-ttu-id="af35b-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af35b-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af35b-116">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af35b-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="af35b-117">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DXERR \_ INVALIDMESH.</span><span class="sxs-lookup"><span data-stu-id="af35b-117">If the function fails, the return value can be one of the following: D3DXERR\_INVALIDMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="af35b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af35b-118">Requirements</span></span>



| <span data-ttu-id="af35b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="af35b-119">Requirement</span></span> | <span data-ttu-id="af35b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="af35b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af35b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af35b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="af35b-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="af35b-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="af35b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af35b-123">Library</span></span><br/> | <dl> <span data-ttu-id="af35b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af35b-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af35b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="af35b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af35b-126">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="af35b-126">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="af35b-127">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="af35b-127">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
