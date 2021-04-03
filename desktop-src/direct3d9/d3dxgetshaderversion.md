---
description: Retorna a versão do sombreador compilado.
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: Função D3DXGetShaderVersion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c4a65db8706f6d8648096cf0822654e562687a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091965"
---
# <a name="d3dxgetshaderversion-function"></a><span data-ttu-id="428e9-103">Função D3DXGetShaderVersion</span><span class="sxs-lookup"><span data-stu-id="428e9-103">D3DXGetShaderVersion function</span></span>

<span data-ttu-id="428e9-104">Retorna a versão do sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="428e9-104">Returns the shader version of the compiled shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="428e9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="428e9-105">Syntax</span></span>


```C++
DWORD D3DXGetShaderVersion(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a><span data-ttu-id="428e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="428e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="428e9-107">*pFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="428e9-107">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="428e9-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="428e9-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="428e9-109">Ponteiro para a função de fluxo DWORD.</span><span class="sxs-lookup"><span data-stu-id="428e9-109">Pointer to the function DWORD stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="428e9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="428e9-110">Return value</span></span>

<span data-ttu-id="428e9-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="428e9-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="428e9-112">Retorna a versão do sombreador fornecido ou zero se a função de sombreador for **nula**.</span><span class="sxs-lookup"><span data-stu-id="428e9-112">Returns the shader version of the given shader, or zero if the shader function is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="428e9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="428e9-113">Requirements</span></span>



| <span data-ttu-id="428e9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="428e9-114">Requirement</span></span> | <span data-ttu-id="428e9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="428e9-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="428e9-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="428e9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="428e9-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="428e9-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="428e9-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="428e9-118">Library</span></span><br/> | <dl> <span data-ttu-id="428e9-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="428e9-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="428e9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="428e9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="428e9-121">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="428e9-121">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
