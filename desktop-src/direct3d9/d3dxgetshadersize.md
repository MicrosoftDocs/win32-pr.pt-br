---
description: Retorna o tamanho do código de byte do sombreador, em bytes.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: Função D3DXGetShaderSize (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3017c5a5371e99bcf9e1d69827de0227d929f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785218"
---
# <a name="d3dxgetshadersize-function"></a><span data-ttu-id="17a56-103">Função D3DXGetShaderSize</span><span class="sxs-lookup"><span data-stu-id="17a56-103">D3DXGetShaderSize function</span></span>

<span data-ttu-id="17a56-104">Retorna o tamanho do código de byte do sombreador, em bytes.</span><span class="sxs-lookup"><span data-stu-id="17a56-104">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a56-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17a56-105">Syntax</span></span>


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="17a56-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17a56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17a56-107">*pFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17a56-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17a56-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="17a56-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="17a56-109">Ponteiro para a função de fluxo DWORD.</span><span class="sxs-lookup"><span data-stu-id="17a56-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17a56-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17a56-110">Return value</span></span>

<span data-ttu-id="17a56-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17a56-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17a56-112">Retorna o tamanho do código de byte do sombreador, em bytes.</span><span class="sxs-lookup"><span data-stu-id="17a56-112">Returns the size of the shader byte code, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a56-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17a56-113">Requirements</span></span>



| <span data-ttu-id="17a56-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="17a56-114">Requirement</span></span> | <span data-ttu-id="17a56-115">Valor</span><span class="sxs-lookup"><span data-stu-id="17a56-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="17a56-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17a56-116">Header</span></span><br/>  | <dl> <span data-ttu-id="17a56-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="17a56-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="17a56-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17a56-118">Library</span></span><br/> | <dl> <span data-ttu-id="17a56-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17a56-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="17a56-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="17a56-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a56-121">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="17a56-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
