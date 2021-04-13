---
description: Alterna o status literal de um parâmetro. Um parâmetro literal tem um valor que não é alterado durante o tempo de vida de um efeito.
ms.assetid: 09ebf666-8a50-4604-abef-aed0d92a6d49
title: 'Método ID3DXEffectCompiler:: setliteral (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.SetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a64426381876458b601b741050a01e5f35d084c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298520"
---
# <a name="id3dxeffectcompilersetliteral-method"></a><span data-ttu-id="5cdc3-104">Método ID3DXEffectCompiler:: setliteral</span><span class="sxs-lookup"><span data-stu-id="5cdc3-104">ID3DXEffectCompiler::SetLiteral method</span></span>

<span data-ttu-id="5cdc3-105">Alterna o status literal de um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5cdc3-105">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="5cdc3-106">Um parâmetro literal tem um valor que não é alterado durante o tempo de vida de um efeito.</span><span class="sxs-lookup"><span data-stu-id="5cdc3-106">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cdc3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5cdc3-107">Syntax</span></span>


```C++
HRESULT SetLiteral(
  [in] D3DXHANDLE hParameter,
  [in] BOOL       Literal
);
```



## <a name="parameters"></a><span data-ttu-id="5cdc3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cdc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cdc3-109">*hParameter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5cdc3-109">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cdc3-110">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5cdc3-110">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5cdc3-111">Identificador exclusivo para um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5cdc3-111">Unique identifier to a parameter.</span></span> <span data-ttu-id="5cdc3-112">Consulte [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="5cdc3-112">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="5cdc3-113">*Literal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5cdc3-113">*Literal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cdc3-114">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5cdc3-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5cdc3-115">Defina como **true** para tornar o parâmetro um literal e **false** se o parâmetro puder alterar o valor durante o tempo de vida do sombreador.</span><span class="sxs-lookup"><span data-stu-id="5cdc3-115">Set to **TRUE** to make the parameter a literal, and **FALSE** if the parameter can change value during the shader lifetime.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cdc3-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5cdc3-116">Return value</span></span>

<span data-ttu-id="5cdc3-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5cdc3-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5cdc3-118">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5cdc3-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5cdc3-119">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5cdc3-119">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cdc3-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cdc3-120">Remarks</span></span>

<span data-ttu-id="5cdc3-121">Esses métodos só alteram se o parâmetro é um literal ou não.</span><span class="sxs-lookup"><span data-stu-id="5cdc3-121">This methods only changes whether the parameter is a literal or not.</span></span> <span data-ttu-id="5cdc3-122">Para alterar o valor de um parâmetro, use um método como [**ID3DXBaseEffect:: setbool**](id3dxbaseeffect--setbool.md) ou [**ID3DXBaseEffect:: SetValue**](id3dxbaseeffect--setvalue.md).</span><span class="sxs-lookup"><span data-stu-id="5cdc3-122">To change the value of a parameter, use a method like [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) or [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).</span></span>

<span data-ttu-id="5cdc3-123">Essa função deve ser chamada antes de o efeito ser compilado.</span><span class="sxs-lookup"><span data-stu-id="5cdc3-123">This function must be called before the effect is compiled.</span></span> <span data-ttu-id="5cdc3-124">Aqui está um exemplo de como uma delas pode usar essa função:</span><span class="sxs-lookup"><span data-stu-id="5cdc3-124">Here is an example of how one might use this function:</span></span>


```
    LPD3DXEFFECTCOMPILER pEffectCompiler;
    char errors[1000];
    HRESULT hr;
    
    hr = D3DXCreateEffectCompilerFromFile("shader.fx",
                                          NULL, NULL, 0,
                                          &pEffectCompiler, 
                                          &errors);
    
    //In the fx file, literalInt is declared as an int.
    //By calling this function, the compiler will treat
    //it as a literal (i.e. #define)
    hr = pEffectCompiler->SetLiteral("literalInt", TRUE);
    
    //create ten different variations of the same effect
    LPD3DXBUFFER pEffects[10];
    LPD3DXBUFFER pErrors;
    for(int i = 0; i < 10; ++i)
    {
        hr = pEffectCompiler->SetInt("literalInt", i);
    
        hr = pEffectCompiler->CompileEffect(0, &pEffects[i], &pErrors);
    }
```



## <a name="requirements"></a><span data-ttu-id="5cdc3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cdc3-125">Requirements</span></span>



| <span data-ttu-id="5cdc3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cdc3-126">Requirement</span></span> | <span data-ttu-id="5cdc3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5cdc3-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cdc3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5cdc3-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5cdc3-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cdc3-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5cdc3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5cdc3-130">Library</span></span><br/> | <dl> <span data-ttu-id="5cdc3-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5cdc3-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5cdc3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cdc3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cdc3-133">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="5cdc3-133">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="5cdc3-134">Usos e literais (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5cdc3-134">Usages and Literals (Direct3D 9)</span></span>](usages-and-literals.md)
</dt> <dt>

[<span data-ttu-id="5cdc3-135">**ID3DXEffectCompiler:: getliteral**</span><span class="sxs-lookup"><span data-stu-id="5cdc3-135">**ID3DXEffectCompiler::GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)
</dt> </dl>

 

 
