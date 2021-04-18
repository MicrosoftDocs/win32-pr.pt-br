---
description: Desmontar um sombreador.
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: Função D3DXDisassembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6192b77c190ed73dc6e5038c9119152836eca375
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781621"
---
# <a name="d3dxdisassembleshader-function"></a><span data-ttu-id="2d18c-103">Função D3DXDisassembleShader</span><span class="sxs-lookup"><span data-stu-id="2d18c-103">D3DXDisassembleShader function</span></span>

<span data-ttu-id="2d18c-104">Desmontar um sombreador.</span><span class="sxs-lookup"><span data-stu-id="2d18c-104">Disassemble a shader.</span></span>

> [!Note]  
> <span data-ttu-id="2d18c-105">Em vez de usar essa função herdada, recomendamos que você use a API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="2d18c-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2d18c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d18c-106">Syntax</span></span>


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="2d18c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d18c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d18c-108">*pShader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d18c-108">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18c-109">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d18c-109">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2d18c-110">Ponteiro para um buffer de memória que contém os dados do sombreador.</span><span class="sxs-lookup"><span data-stu-id="2d18c-110">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="2d18c-111">*EnableColorCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d18c-111">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18c-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d18c-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d18c-113">Habilite o código de cor para facilitar a leitura da desmontagem.</span><span class="sxs-lookup"><span data-stu-id="2d18c-113">Enable color code to make it easier to read the disassembly.</span></span>

</dd> <dt>

<span data-ttu-id="2d18c-114">*pComments* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d18c-114">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18c-115">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d18c-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d18c-116">Uma cadeia de caracteres de comentário opcional com terminação nula.</span><span class="sxs-lookup"><span data-stu-id="2d18c-116">An optional NULL-terminated comment string.</span></span> <span data-ttu-id="2d18c-117">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2d18c-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2d18c-118">*ppDisassembly* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2d18c-118">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18c-119">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d18c-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2d18c-120">Retorna um buffer que contém o sombreador desmontado.</span><span class="sxs-lookup"><span data-stu-id="2d18c-120">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="2d18c-121">Consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="2d18c-121">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d18c-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d18c-122">Return value</span></span>

<span data-ttu-id="2d18c-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2d18c-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2d18c-124">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2d18c-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2d18c-125">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2d18c-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d18c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d18c-126">Requirements</span></span>



| <span data-ttu-id="2d18c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d18c-127">Requirement</span></span> | <span data-ttu-id="2d18c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2d18c-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d18c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d18c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2d18c-130"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d18c-130"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2d18c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d18c-131">Library</span></span><br/> | <dl> <span data-ttu-id="2d18c-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d18c-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2d18c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d18c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d18c-134">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="2d18c-134">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
