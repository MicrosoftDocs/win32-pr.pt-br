---
description: Compila um sombreador de um efeito que contém uma ou mais funções.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: Método ID3DXEffectCompiler::CompileShader (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3e8d1d72fccd5c4ad47d21d05ee46013860a7743
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343621"
---
# <a name="id3dxeffectcompilercompileshader-method"></a><span data-ttu-id="7058c-103">Método ID3DXEffectCompiler::CompileShader</span><span class="sxs-lookup"><span data-stu-id="7058c-103">ID3DXEffectCompiler::CompileShader method</span></span>

<span data-ttu-id="7058c-104">Compila um sombreador de um efeito que contém uma ou mais funções.</span><span class="sxs-lookup"><span data-stu-id="7058c-104">Compiles a shader from an effect that contains one or more functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7058c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7058c-105">Syntax</span></span>


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="7058c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7058c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7058c-107">*hFunction* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="7058c-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7058c-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7058c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7058c-109">Identificador exclusivo para a função a ser compilada.</span><span class="sxs-lookup"><span data-stu-id="7058c-109">Unique identifier to the function to be compiled.</span></span> <span data-ttu-id="7058c-110">Esse valor não deve ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7058c-110">This value must not be **NULL**.</span></span> <span data-ttu-id="7058c-111">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7058c-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="7058c-112">*pTarget* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="7058c-112">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7058c-113">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7058c-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7058c-114">Ponteiro para um perfil de sombreador que determina o conjunto de instruções do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7058c-114">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="7058c-115">Consulte [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) ou [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) para ver uma lista dos perfis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7058c-115">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="7058c-116">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="7058c-116">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7058c-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7058c-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7058c-118">Compile opções identificadas por vários sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="7058c-118">Compile options identified by various flags.</span></span> <span data-ttu-id="7058c-119">O compilador HLSL do Direct3D 10 agora é o padrão.</span><span class="sxs-lookup"><span data-stu-id="7058c-119">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="7058c-120">Consulte [Sinalizadores D3DXSHADER](d3dxshader-flags.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="7058c-120">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="7058c-121">*ppShader* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7058c-121">*ppShader* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7058c-122">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7058c-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7058c-123">Buffer que contém o sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="7058c-123">Buffer containing the compiled shader.</span></span> <span data-ttu-id="7058c-124">O sombreador do compilador é uma matriz de DWORDs.</span><span class="sxs-lookup"><span data-stu-id="7058c-124">The compiler shader is an array of DWORDs.</span></span> <span data-ttu-id="7058c-125">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="7058c-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="7058c-126">*ppErrorMsgs* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7058c-126">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7058c-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7058c-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7058c-128">Buffer que contém pelo menos a primeira mensagem de erro de compilação que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="7058c-128">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="7058c-129">Isso inclui efeitos de erros de compilador e erros de compilação de linguagem de alto nível.</span><span class="sxs-lookup"><span data-stu-id="7058c-129">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="7058c-130">Para obter mais informações sobre como acessar o buffer, consulte [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="7058c-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="7058c-131">*ppConstantTable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7058c-131">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7058c-132">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="7058c-132">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="7058c-133">Retorna uma interface [**ID3DXConstantTable**](id3dxconstanttable.md) , que pode ser usada para acessar constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7058c-133">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="7058c-134">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7058c-134">This value can be **NULL**.</span></span> <span data-ttu-id="7058c-135">Se você compilar seu aplicativo como grande reconhecimento de endereço (ou seja, usar a opção de vinculador/LARGEADDRESSAWARE para tratar endereços maiores que 2 GB), não poderá usar esse parâmetro e deve defini-lo como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7058c-135">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="7058c-136">Em vez disso, você deve usar a função [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) para recuperar a tabela de constante de sombreador que está inserida dentro do sombreador.</span><span class="sxs-lookup"><span data-stu-id="7058c-136">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="7058c-137">Nesta chamada **D3DXGetShaderConstantTableEx** , você deve passar o sinalizador **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** para o parâmetro *flags* para especificar o acesso a até 4 GB de espaço de endereço virtual.</span><span class="sxs-lookup"><span data-stu-id="7058c-137">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7058c-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7058c-138">Return value</span></span>

<span data-ttu-id="7058c-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7058c-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7058c-140">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7058c-140">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="7058c-141">Se os argumentos forem inválidos, o método retornará D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7058c-141">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="7058c-142">Se o método falhar, o valor de retorno será E \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="7058c-142">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7058c-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="7058c-143">Remarks</span></span>

<span data-ttu-id="7058c-144">Os destinos podem ser especificados para sombreadores de vértice, sombreadores de pixel e funções de preenchimento de textura.</span><span class="sxs-lookup"><span data-stu-id="7058c-144">Targets can be specified for vertex shaders, pixel shaders, and texture fill functions.</span></span>



| <span data-ttu-id="7058c-145">Destinos</span><span class="sxs-lookup"><span data-stu-id="7058c-145">Targets</span></span>                      | <span data-ttu-id="7058c-146">Funções</span><span class="sxs-lookup"><span data-stu-id="7058c-146">Functions</span></span>                                                                      |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="7058c-147">Destinos do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="7058c-147">Vertex shader targets</span></span> | <span data-ttu-id="7058c-148">vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ sw, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7058c-148">vs\_1\_1, vs\_2\_0, vs\_2\_sw, vs\_3\_0</span></span>                               |
| <span data-ttu-id="7058c-149">Destinos do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="7058c-149">Pixel shader targets</span></span>  | <span data-ttu-id="7058c-150">ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ \_ 1 3, ps \_ 1 \_ 4, ps \_ 2 \_ 0, ps \_ 2 \_ sw, ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7058c-150">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4, ps\_2\_0, ps\_2\_sw, ps\_3\_0</span></span> |
| <span data-ttu-id="7058c-151">Destinos de preenchimento de textura</span><span class="sxs-lookup"><span data-stu-id="7058c-151">Texture fill targets</span></span>  | <span data-ttu-id="7058c-152">tx \_ 0, tx \_ 1</span><span class="sxs-lookup"><span data-stu-id="7058c-152">tx\_0, tx\_1</span></span>                                                          |



 

<span data-ttu-id="7058c-153">Esse método compila um sombreador de uma função que é escrita em uma linguagem semelhante a C.</span><span class="sxs-lookup"><span data-stu-id="7058c-153">This method compiles a shader from a function that is written in a C-like language.</span></span> <span data-ttu-id="7058c-154">Para obter mais informações, consulte [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="7058c-154">For more information, see [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7058c-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7058c-155">Requirements</span></span>



| <span data-ttu-id="7058c-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="7058c-156">Requirement</span></span> | <span data-ttu-id="7058c-157">Valor</span><span class="sxs-lookup"><span data-stu-id="7058c-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7058c-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7058c-158">Header</span></span><br/>  | <dl> <span data-ttu-id="7058c-159"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="7058c-159"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7058c-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7058c-160">Library</span></span><br/> | <dl> <span data-ttu-id="7058c-161"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7058c-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7058c-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="7058c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7058c-163">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="7058c-163">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="7058c-164">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="7058c-164">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
