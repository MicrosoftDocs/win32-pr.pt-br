---
description: Função D3DXGetShaderConstantTableEx – Obtém a tabela de constante de sombreador inserida dentro de um sombreador.
ms.assetid: f7e846e4-9cb4-4634-95e3-4b2a752978a8
title: Função D3DXGetShaderConstantTableEx (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderConstantTableEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2cac525f6f6fc4f4e3b6e5900aa9b655e7c7f60d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114424"
---
# <a name="d3dxgetshaderconstanttableex-function"></a><span data-ttu-id="73f1a-103">Função D3DXGetShaderConstantTableEx</span><span class="sxs-lookup"><span data-stu-id="73f1a-103">D3DXGetShaderConstantTableEx function</span></span>

<span data-ttu-id="73f1a-104">Obtém a tabela de sombreador-constante inserida dentro de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="73f1a-104">Gets the shader-constant table embedded inside a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f1a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73f1a-105">Syntax</span></span>


```C++
HRESULT D3DXGetShaderConstantTableEx(
  _In_  const DWORD               *pFunction,
  _In_        DWORD               Flags,
  _Out_       LPD3DXCONSTANTTABLE * ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="73f1a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73f1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73f1a-107">*pFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73f1a-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73f1a-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="73f1a-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="73f1a-109">Ponteiro para a função de fluxo DWORD.</span><span class="sxs-lookup"><span data-stu-id="73f1a-109">Pointer to the function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="73f1a-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="73f1a-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73f1a-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73f1a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73f1a-112">Use o \_ sinalizador D3DXCONSTTABLE LARGEADDRESSAWARE para acessar até 4 GB de espaço de endereço virtual (em vez do padrão de 2 GB).</span><span class="sxs-lookup"><span data-stu-id="73f1a-112">Use the D3DXCONSTTABLE\_LARGEADDRESSAWARE flag to access up to 4 GB of virtual address space (instead of the default of 2 GB).</span></span> <span data-ttu-id="73f1a-113">Se você não precisar do espaço de endereço virtual adicional, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span><span class="sxs-lookup"><span data-stu-id="73f1a-113">If you do not need the additional virtual address space, use [**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md).</span></span>

</dd> <dt>

 <span data-ttu-id="73f1a-114">*ppConstantTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="73f1a-114">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73f1a-115">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="73f1a-115">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="73f1a-116">Retorna a interface da tabela de constantes (consulte [**ID3DXConstantTable**](id3dxconstanttable.md)) que gerencia a tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="73f1a-116">Returns the constant table interface (see [**ID3DXConstantTable**](id3dxconstanttable.md)) that manages the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73f1a-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="73f1a-117">Return value</span></span>

<span data-ttu-id="73f1a-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73f1a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73f1a-119">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="73f1a-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="73f1a-120">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="73f1a-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="73f1a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="73f1a-121">Remarks</span></span>

<span data-ttu-id="73f1a-122">Uma tabela constante é gerada por [**D3DXCompileShader**](d3dxcompileshader.md) e inserida no corpo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="73f1a-122">A constant table is generated by [**D3DXCompileShader**](d3dxcompileshader.md) and embedded in the shader body.</span></span>

## <a name="requirements"></a><span data-ttu-id="73f1a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73f1a-123">Requirements</span></span>



| <span data-ttu-id="73f1a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="73f1a-124">Requirement</span></span> | <span data-ttu-id="73f1a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="73f1a-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f1a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73f1a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="73f1a-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="73f1a-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="73f1a-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73f1a-128">Library</span></span><br/> | <dl> <span data-ttu-id="73f1a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73f1a-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="73f1a-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="73f1a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73f1a-131">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="73f1a-131">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
