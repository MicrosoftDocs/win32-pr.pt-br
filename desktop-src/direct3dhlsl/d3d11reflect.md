---
title: Função D3D11Reflect
description: Obtém um ponteiro para uma interface de reflexão.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- HLSL da função D3D11Reflect
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091995"
---
# <a name="d3d11reflect-function"></a><span data-ttu-id="c08bb-104">Função D3D11Reflect</span><span class="sxs-lookup"><span data-stu-id="c08bb-104">D3D11Reflect function</span></span>

<span data-ttu-id="c08bb-105">Obtém um ponteiro para uma interface de reflexão.</span><span class="sxs-lookup"><span data-stu-id="c08bb-105">Gets a pointer to a reflection interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c08bb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c08bb-106">Syntax</span></span>

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a><span data-ttu-id="c08bb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c08bb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c08bb-108">*pSrcData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c08bb-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c08bb-109">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c08bb-109">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c08bb-110">Um ponteiro para dados de origem como código HLSL compilado.</span><span class="sxs-lookup"><span data-stu-id="c08bb-110">A pointer to source data as compiled HLSL code.</span></span>

</dd> <dt>

<span data-ttu-id="c08bb-111">*SrcDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c08bb-111">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c08bb-112">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c08bb-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c08bb-113">Comprimento de *pSrcData*.</span><span class="sxs-lookup"><span data-stu-id="c08bb-113">Length of *pSrcData*.</span></span>

</dd> <dt>

<span data-ttu-id="c08bb-114">*ppReflector* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c08bb-114">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c08bb-115">Tipo: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span><span class="sxs-lookup"><span data-stu-id="c08bb-115">Type: **[**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span></span>

<span data-ttu-id="c08bb-116">O endereço de um ponteiro para a interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) .</span><span class="sxs-lookup"><span data-stu-id="c08bb-116">The address of a pointer to the [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c08bb-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c08bb-117">Return value</span></span>

<span data-ttu-id="c08bb-118">Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c08bb-118">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c08bb-119">Retorna um dos códigos de retorno descritos no tópico [códigos de retorno do Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span><span class="sxs-lookup"><span data-stu-id="c08bb-119">Returns one of the return codes described in the topic [Direct3D 11 Return Codes](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span></span>

## <a name="remarks"></a><span data-ttu-id="c08bb-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c08bb-120">Remarks</span></span>

<span data-ttu-id="c08bb-121">A função de compilador **D3D11Reflect** embutida é um wrapper para a função de compilador [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .</span><span class="sxs-lookup"><span data-stu-id="c08bb-121">The inline **D3D11Reflect** compiler function is a wrapper for the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) compiler function.</span></span> <span data-ttu-id="c08bb-122">**D3D11Reflect** pode recuperar apenas uma interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="c08bb-122">**D3D11Reflect** can retrieve only a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span> <span data-ttu-id="c08bb-123">O **D3DReflect** pode recuperar uma interface **ID3D11ShaderReflection** ou uma interface de reflexão direct3d 10 ou Direct3D 10,1, por exemplo, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span><span class="sxs-lookup"><span data-stu-id="c08bb-123">**D3DReflect** can retrieve a **ID3D11ShaderReflection** interface or a Direct3D 10 or Direct3D 10.1 reflection interface, for example, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span></span>

<span data-ttu-id="c08bb-124">O código do sombreador contém metadados que podem ser inspecionados usando as APIs de reflexão.</span><span class="sxs-lookup"><span data-stu-id="c08bb-124">Shader code contains metadata that can be inspected using the reflection APIs.</span></span>

<span data-ttu-id="c08bb-125">O código a seguir mostra como recuperar uma interface [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="c08bb-125">The following code shows how to retrieve a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span>


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a><span data-ttu-id="c08bb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c08bb-126">Requirements</span></span>



| <span data-ttu-id="c08bb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c08bb-127">Requirement</span></span> | <span data-ttu-id="c08bb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c08bb-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c08bb-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c08bb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c08bb-130"><dt>D3DCompiler. inl</dt></span><span class="sxs-lookup"><span data-stu-id="c08bb-130"><dt>D3DCompiler.inl</dt></span></span> </dl>     |
| <span data-ttu-id="c08bb-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c08bb-131">Library</span></span><br/> | <dl> <span data-ttu-id="c08bb-132"><dt>D3dcompiler \_ 47. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c08bb-132"><dt>D3dcompiler\_47.lib</dt></span></span> </dl> |
| <span data-ttu-id="c08bb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c08bb-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="c08bb-134"><dt>\_47.dllD3dcompiler</dt></span><span class="sxs-lookup"><span data-stu-id="c08bb-134"><dt>D3dcompiler\_47.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c08bb-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c08bb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c08bb-136">Funções</span><span class="sxs-lookup"><span data-stu-id="c08bb-136">Functions</span></span>](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

