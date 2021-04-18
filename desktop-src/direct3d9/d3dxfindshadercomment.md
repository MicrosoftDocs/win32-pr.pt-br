---
description: Pesquisa em um sombreador um comentário específico. O comentário é identificado por um código de quatro caracteres (FOURCC) na primeira DWORD do comentário.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: Função D3DXFindShaderComment (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771641"
---
# <a name="d3dxfindshadercomment-function"></a><span data-ttu-id="7f9b8-104">Função D3DXFindShaderComment</span><span class="sxs-lookup"><span data-stu-id="7f9b8-104">D3DXFindShaderComment function</span></span>

<span data-ttu-id="7f9b8-105">Pesquisa em um sombreador um comentário específico.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-105">Searches through a shader for a particular comment.</span></span> <span data-ttu-id="7f9b8-106">O comentário é identificado por um código de quatro caracteres (FOURCC) na primeira DWORD do comentário.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-106">The comment is identified by a four-character code (FOURCC) in the first DWORD of the comment.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9b8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f9b8-107">Syntax</span></span>


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a><span data-ttu-id="7f9b8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f9b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f9b8-109">*pFunction* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f9b8-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f9b8-110">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7f9b8-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7f9b8-111">Ponteiro para o fluxo DWORD da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="7f9b8-112">*FOURCC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f9b8-112">*FourCC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f9b8-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f9b8-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f9b8-114">Código FOURCC que identifica o bloco de comentários.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-114">FOURCC code that identifies the comment block.</span></span> <span data-ttu-id="7f9b8-115">Consulte [formatos FOURCC](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="7f9b8-115">See [FourCC Formats](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f9b8-116">*ppData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7f9b8-116">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f9b8-117">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f9b8-117">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7f9b8-118">Retorna um ponteiro para os dados de comentário (sem incluir o token de comentário e o código FOURCC).</span><span class="sxs-lookup"><span data-stu-id="7f9b8-118">Returns a pointer to the comment data (not including the comment token and FOURCC code).</span></span> <span data-ttu-id="7f9b8-119">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9b8-120">*pSizeInBytes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7f9b8-120">*pSizeInBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f9b8-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f9b8-121">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7f9b8-122">Retorna o tamanho dos dados de comentário em bytes.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-122">Returns the size of the comment data in bytes.</span></span> <span data-ttu-id="7f9b8-123">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-123">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f9b8-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f9b8-124">Return value</span></span>

<span data-ttu-id="7f9b8-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f9b8-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f9b8-126">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7f9b8-127">Se o comentário não for encontrado e nenhum outro erro tiver ocorrido, S \_ false será retornado.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-127">If the comment is not found, and no other error has occurred, S\_FALSE is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f9b8-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f9b8-128">Requirements</span></span>



| <span data-ttu-id="7f9b8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f9b8-129">Requirement</span></span> | <span data-ttu-id="7f9b8-130">Valor</span><span class="sxs-lookup"><span data-stu-id="7f9b8-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9b8-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f9b8-131">Header</span></span><br/>  | <dl> <span data-ttu-id="7f9b8-132"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f9b8-132"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7f9b8-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f9b8-133">Library</span></span><br/> | <dl> <span data-ttu-id="7f9b8-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f9b8-134"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7f9b8-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f9b8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f9b8-136">Funções de sombreador</span><span class="sxs-lookup"><span data-stu-id="7f9b8-136">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
