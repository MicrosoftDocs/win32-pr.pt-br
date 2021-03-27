---
title: Estrutura de D3DX11_EFFECT_SHADER_DESC (D3dx11effect. h)
description: Descreve um sombreador de efeito.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- Estrutura D3DX11_EFFECT_SHADER_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837971"
---
# <a name="d3dx11_effect_shader_desc-structure"></a><span data-ttu-id="fa178-104">\_ \_ Estrutura Desc do sombreador de efeito D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="fa178-104">D3DX11\_EFFECT\_SHADER\_DESC structure</span></span>

<span data-ttu-id="fa178-105">Descreve um sombreador de efeito.</span><span class="sxs-lookup"><span data-stu-id="fa178-105">Describes an effect shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa178-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa178-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="fa178-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fa178-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa178-108">**pInputSignature**</span><span class="sxs-lookup"><span data-stu-id="fa178-108">**pInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="fa178-109">Tipo: **[**byte**](/windows/desktop/WinProg/windows-data-types) \* const**</span><span class="sxs-lookup"><span data-stu-id="fa178-109">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="fa178-110">Passado para CreateInputLayout.</span><span class="sxs-lookup"><span data-stu-id="fa178-110">Passed into CreateInputLayout.</span></span> <span data-ttu-id="fa178-111">Válido somente em um sombreador de vértice ou sombreador de geometria.</span><span class="sxs-lookup"><span data-stu-id="fa178-111">Only valid on a vertex shader or geometry shader.</span></span> <span data-ttu-id="fa178-112">Consulte [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="fa178-112">See [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="fa178-113">**IsInline**</span><span class="sxs-lookup"><span data-stu-id="fa178-113">**IsInline**</span></span>
</dt> <dd>

<span data-ttu-id="fa178-114">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fa178-114">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="fa178-115">**True** é o sombreador definido como embutido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fa178-115">**TRUE** is the shader is defined inline; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fa178-116">**pBytecode**</span><span class="sxs-lookup"><span data-stu-id="fa178-116">**pBytecode**</span></span>
</dt> <dd>

<span data-ttu-id="fa178-117">Tipo: **[**byte**](/windows/desktop/WinProg/windows-data-types) \* const**</span><span class="sxs-lookup"><span data-stu-id="fa178-117">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="fa178-118">Código de bytes do sombreador.</span><span class="sxs-lookup"><span data-stu-id="fa178-118">Shader bytecode.</span></span>

</dd> <dt>

<span data-ttu-id="fa178-119">**BytecodeLength**</span><span class="sxs-lookup"><span data-stu-id="fa178-119">**BytecodeLength**</span></span>
</dt> <dd>

<span data-ttu-id="fa178-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fa178-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="fa178-121">O comprimento de pBytecode.</span><span class="sxs-lookup"><span data-stu-id="fa178-121">The length of pBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="fa178-122">**SODecls**</span><span class="sxs-lookup"><span data-stu-id="fa178-122">**SODecls**</span></span>
</dt> <dd>

<span data-ttu-id="fa178-123">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fa178-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="fa178-124">Transmita a cadeia de caracteres de declaração (para o sombreador Geometry com isso).</span><span class="sxs-lookup"><span data-stu-id="fa178-124">Stream out declaration string (for geometry shader with SO).</span></span>

</dd> <dt>

<span data-ttu-id="fa178-125">**RasterizedStream**</span><span class="sxs-lookup"><span data-stu-id="fa178-125">**RasterizedStream**</span></span>
</dt> <dd>

<span data-ttu-id="fa178-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fa178-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="fa178-127">Indica qual fluxo está rasterizado.</span><span class="sxs-lookup"><span data-stu-id="fa178-127">Indicates which stream is rasterized.</span></span> <span data-ttu-id="fa178-128">Os sombreadores de geometria D3D11 podem produzir até quatro fluxos de dados, um dos quais pode ser rasterizado.</span><span class="sxs-lookup"><span data-stu-id="fa178-128">D3D11 geometry shaders can output up to four streams of data, one of which can be rasterized.</span></span>

</dd> <dt>

<span data-ttu-id="fa178-129">**NumInputSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="fa178-129">**NumInputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="fa178-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fa178-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="fa178-131">Número de entradas na assinatura de entrada.</span><span class="sxs-lookup"><span data-stu-id="fa178-131">Number of entries in the input signature.</span></span>

</dd> <dt>

<span data-ttu-id="fa178-132">**NumOutputSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="fa178-132">**NumOutputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="fa178-133">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fa178-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="fa178-134">Número de entradas na assinatura de saída.</span><span class="sxs-lookup"><span data-stu-id="fa178-134">Number of entries in the output signature.</span></span>

</dd> <dt>

<span data-ttu-id="fa178-135">**NumPatchConstantSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="fa178-135">**NumPatchConstantSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="fa178-136">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fa178-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="fa178-137">Número de entradas na assinatura constante de patch.</span><span class="sxs-lookup"><span data-stu-id="fa178-137">Number of entries in the patch constant signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa178-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa178-138">Remarks</span></span>

<span data-ttu-id="fa178-139">O \_ \_ sombreador \_ de efeito D3DX11 DESC é usado com [**ID3DX11EffectShaderVariable:: GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span><span class="sxs-lookup"><span data-stu-id="fa178-139">D3DX11\_EFFECT\_SHADER\_DESC is used with [**ID3DX11EffectShaderVariable::GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa178-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa178-140">Requirements</span></span>



| <span data-ttu-id="fa178-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa178-141">Requirement</span></span> | <span data-ttu-id="fa178-142">Valor</span><span class="sxs-lookup"><span data-stu-id="fa178-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa178-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa178-143">Header</span></span><br/> | <dl> <span data-ttu-id="fa178-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa178-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa178-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa178-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa178-146">Efeitos 11 estruturas</span><span class="sxs-lookup"><span data-stu-id="fa178-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

