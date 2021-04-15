---
description: Um método implementado pelo usuário para abrir e ler o conteúdo de um arquivo de inclusão de sombreador \# .
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'Método ID3DXInclude:: Open (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761215"
---
# <a name="id3dxincludeopen-method"></a><span data-ttu-id="c3984-103">Método ID3DXInclude:: Open</span><span class="sxs-lookup"><span data-stu-id="c3984-103">ID3DXInclude::Open method</span></span>

<span data-ttu-id="c3984-104">Um método implementado pelo usuário para abrir e ler o conteúdo de um arquivo de inclusão de sombreador \# .</span><span class="sxs-lookup"><span data-stu-id="c3984-104">A user-implemented method for opening and reading the contents of a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3984-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3984-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a><span data-ttu-id="c3984-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3984-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3984-107">*Incluir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3984-107">*IncludeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3984-108">Tipo: **[ **\_ tipo de D3DXINCLUDE**](./d3dxinclude-type.md)**</span><span class="sxs-lookup"><span data-stu-id="c3984-108">Type: **[**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md)**</span></span>

<span data-ttu-id="c3984-109">O local do \# arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="c3984-109">The location of the \#include file.</span></span> <span data-ttu-id="c3984-110">Consulte [**\_ tipo de D3DXINCLUDE**](./d3dxinclude-type.md).</span><span class="sxs-lookup"><span data-stu-id="c3984-110">See [**D3DXINCLUDE\_TYPE**](./d3dxinclude-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3984-111">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3984-111">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3984-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3984-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3984-113">Nome do \# arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="c3984-113">Name of the \#include file.</span></span>

</dd> <dt>

<span data-ttu-id="c3984-114">*pParentData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3984-114">*pParentData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3984-115">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3984-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3984-116">Ponteiro para o contêiner que inclui o \# arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="c3984-116">Pointer to the container that includes the \#include file.</span></span> <span data-ttu-id="c3984-117">O compilador pode passar nulo em *pParentData*.</span><span class="sxs-lookup"><span data-stu-id="c3984-117">The compiler might pass NULL in *pParentData*.</span></span> <span data-ttu-id="c3984-118">Para obter mais informações, consulte a seção "procurando arquivos de inclusão" em [compilar um efeito (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span><span class="sxs-lookup"><span data-stu-id="c3984-118">For more information, see the "Searching for Include Files" section in [Compile an Effect (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3984-119">*ppData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c3984-119">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3984-120">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3984-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c3984-121">Ponteiro para o buffer retornado que contém as diretivas include.</span><span class="sxs-lookup"><span data-stu-id="c3984-121">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="c3984-122">Esse ponteiro permanece válido até que [**ID3DXInclude:: Close**](id3dxinclude--close.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="c3984-122">This pointer remains valid until [**ID3DXInclude::Close**](id3dxinclude--close.md) is called.</span></span>

</dd> <dt>

<span data-ttu-id="c3984-123">*pBytes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c3984-123">*pBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3984-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3984-124">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c3984-125">Número de bytes retornados em ppData.</span><span class="sxs-lookup"><span data-stu-id="c3984-125">Number of bytes returned in ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3984-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3984-126">Return value</span></span>

<span data-ttu-id="c3984-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3984-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3984-128">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3984-128">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="c3984-129">Se o retorno de chamada falhar ao ler o \# arquivo de inclusão, a API que causou o retorno de chamada será reprovada.</span><span class="sxs-lookup"><span data-stu-id="c3984-129">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="c3984-130">Ele é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="c3984-130">This is one of the following:</span></span>

-   <span data-ttu-id="c3984-131">O sombreador HLSL falhará em uma das funções do D3DXCompileShader \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="c3984-131">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="c3984-132">O sombreador de assembly falhará em uma das \* \* \* funções D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="c3984-132">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="c3984-133">O efeito falhará em uma das \* \* \* funções D3DXCreateEffect ou D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="c3984-133">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3984-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3984-134">Requirements</span></span>



| <span data-ttu-id="c3984-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3984-135">Requirement</span></span> | <span data-ttu-id="c3984-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c3984-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3984-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3984-137">Header</span></span><br/>  | <dl> <span data-ttu-id="c3984-138"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3984-138"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c3984-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3984-139">Library</span></span><br/> | <dl> <span data-ttu-id="c3984-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3984-140"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c3984-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3984-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3984-142">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="c3984-142">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="c3984-143">**ID3DXInclude:: fechar**</span><span class="sxs-lookup"><span data-stu-id="c3984-143">**ID3DXInclude::Close**</span></span>](id3dxinclude--close.md)
</dt> </dl>

 

 
