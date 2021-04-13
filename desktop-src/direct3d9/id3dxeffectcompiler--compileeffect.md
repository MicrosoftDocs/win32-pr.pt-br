---
description: Compile um efeito.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: 'Método ID3DXEffectCompiler:: CompileEffect (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6552d0216cd05c40c122657270c02e0886438da1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298519"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a><span data-ttu-id="77779-103">Método ID3DXEffectCompiler:: CompileEffect</span><span class="sxs-lookup"><span data-stu-id="77779-103">ID3DXEffectCompiler::CompileEffect method</span></span>

<span data-ttu-id="77779-104">Compile um efeito.</span><span class="sxs-lookup"><span data-stu-id="77779-104">Compile an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="77779-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77779-105">Syntax</span></span>


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="77779-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77779-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77779-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="77779-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77779-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77779-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77779-109">Opções de compilação identificadas por vários sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="77779-109">Compile options identified by various flags.</span></span> <span data-ttu-id="77779-110">O compilador do Direct3D 10 HLSL agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="77779-110">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="77779-111">Consulte [D3DXSHADER flags](d3dxshader-flags.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="77779-111">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="77779-112">*ppEffect* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="77779-112">*ppEffect* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="77779-113">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="77779-113">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="77779-114">Buffer que contém o efeito compilado.</span><span class="sxs-lookup"><span data-stu-id="77779-114">Buffer containing the compiled effect.</span></span> <span data-ttu-id="77779-115">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="77779-115">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="77779-116">*ppErrorMsgs* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="77779-116">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="77779-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="77779-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="77779-118">Buffer que contém pelo menos a primeira mensagem de erro de compilação que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="77779-118">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="77779-119">Isso inclui efeitos de erros de compilador e erros de compilação de linguagem de alto nível.</span><span class="sxs-lookup"><span data-stu-id="77779-119">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="77779-120">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="77779-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77779-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77779-121">Return value</span></span>

<span data-ttu-id="77779-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77779-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77779-123">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="77779-123">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="77779-124">Se os argumentos forem inválidos, o método retornará D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="77779-124">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="77779-125">Se o método falhar, o valor de retorno será E \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="77779-125">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="77779-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77779-126">Requirements</span></span>



| <span data-ttu-id="77779-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="77779-127">Requirement</span></span> | <span data-ttu-id="77779-128">Valor</span><span class="sxs-lookup"><span data-stu-id="77779-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="77779-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77779-129">Header</span></span><br/>  | <dl> <span data-ttu-id="77779-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="77779-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="77779-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77779-131">Library</span></span><br/> | <dl> <span data-ttu-id="77779-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77779-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="77779-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="77779-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77779-134">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="77779-134">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> </dl>

 

 
