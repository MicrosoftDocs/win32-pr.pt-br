---
title: Método ID3DX11EffectShaderVariable GetGeometryShader (D3dx11effect. h)
description: Obter um sombreador de geometria.
ms.assetid: 395d5c92-a941-4fbf-9bb9-b43634c1810b
keywords:
- Método GetGeometryShader Direct3D 11
- Método GetGeometryShader Direct3D 11, interface ID3DX11EffectShaderVariable
- Interface ID3DX11EffectShaderVariable Direct3D 11, método GetGeometryShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetGeometryShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe30478d84e0048ff7a56e5bd8faee8d50548417
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298796"
---
# <a name="id3dx11effectshadervariablegetgeometryshader-method"></a><span data-ttu-id="767dd-106">Método ID3DX11EffectShaderVariable:: GetGeometryShader</span><span class="sxs-lookup"><span data-stu-id="767dd-106">ID3DX11EffectShaderVariable::GetGeometryShader method</span></span>

<span data-ttu-id="767dd-107">Obter um sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="767dd-107">Get a geometry shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="767dd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="767dd-108">Syntax</span></span>


```C++
HRESULT GetGeometryShader(
   UINT                 ShaderIndex,
   ID3D11GeometryShader **ppGS
);
```



## <a name="parameters"></a><span data-ttu-id="767dd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="767dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="767dd-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="767dd-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="767dd-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="767dd-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="767dd-112">Um índice de base zero.</span><span class="sxs-lookup"><span data-stu-id="767dd-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="767dd-113">*ppGS*</span><span class="sxs-lookup"><span data-stu-id="767dd-113">*ppGS*</span></span> 
</dt> <dd>

<span data-ttu-id="767dd-114">Tipo: **[ **ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="767dd-114">Type: **[**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)\*\***</span></span>

<span data-ttu-id="767dd-115">Um ponteiro para um ponteiro [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader) que será definido como o sombreador Geometry no retorno.</span><span class="sxs-lookup"><span data-stu-id="767dd-115">A pointer to an [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader) pointer that will be set to the geometry shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="767dd-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="767dd-116">Return value</span></span>

<span data-ttu-id="767dd-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="767dd-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="767dd-118">Retorna um dos seguintes [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="767dd-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="767dd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="767dd-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="767dd-120">O SDK do DirectX não fornece nenhum binário compilado para efeitos.</span><span class="sxs-lookup"><span data-stu-id="767dd-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="767dd-121">Você deve usar a fonte Effects 11 para criar seu aplicativo de tipo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="767dd-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="767dd-122">Para obter mais informações sobre como usar a fonte Effects 11, consulte [diferenças entre os efeitos 10 e os efeitos 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="767dd-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="767dd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="767dd-123">Requirements</span></span>



| <span data-ttu-id="767dd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="767dd-124">Requirement</span></span> | <span data-ttu-id="767dd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="767dd-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="767dd-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="767dd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="767dd-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="767dd-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="767dd-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="767dd-128">Library</span></span><br/> | <dl> <span data-ttu-id="767dd-129"><dt>N/A (uma biblioteca Effects 11 está disponível online como fonte compartilhada.)</dt></span><span class="sxs-lookup"><span data-stu-id="767dd-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="767dd-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="767dd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="767dd-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="767dd-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

