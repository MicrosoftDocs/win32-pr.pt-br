---
title: Estrutura de D3DX11_PASS_DESC (D3dx11effect. h)
description: Descreve um efeito aprovado, que contém o estado do pipeline.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- Estrutura D3DX11_PASS_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968691"
---
# <a name="d3dx11_pass_desc-structure"></a><span data-ttu-id="31fd6-104">\_Estrutura desc de Pass D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="31fd6-104">D3DX11\_PASS\_DESC structure</span></span>

<span data-ttu-id="31fd6-105">Descreve um efeito aprovado, que contém o estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="31fd6-105">Describes an effect pass, which contains pipeline state.</span></span>

## <a name="syntax"></a><span data-ttu-id="31fd6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31fd6-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a><span data-ttu-id="31fd6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="31fd6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="31fd6-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="31fd6-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="31fd6-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="31fd6-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="31fd6-110">Nome dessa passagem (**NULL** se não anônimo).</span><span class="sxs-lookup"><span data-stu-id="31fd6-110">Name of this pass (**NULL** if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="31fd6-111">**Anotações**</span><span class="sxs-lookup"><span data-stu-id="31fd6-111">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="31fd6-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="31fd6-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="31fd6-113">Número de anotações nesta passagem.</span><span class="sxs-lookup"><span data-stu-id="31fd6-113">Number of annotations on this pass.</span></span>

</dd> <dt>

<span data-ttu-id="31fd6-114">**pIAInputSignature**</span><span class="sxs-lookup"><span data-stu-id="31fd6-114">**pIAInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="31fd6-115">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="31fd6-115">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="31fd6-116">Assinatura do sombreador de vértice ou do sombreador de geometria (se não houver nenhum sombreador de vértice) ou **NULL** se não houver nenhum.</span><span class="sxs-lookup"><span data-stu-id="31fd6-116">Signature from the vertex shader or geometry shader (if there is no vertex shader) or **NULL** if neither exists.</span></span>

</dd> <dt>

<span data-ttu-id="31fd6-117">**IAInputSignatureSize**</span><span class="sxs-lookup"><span data-stu-id="31fd6-117">**IAInputSignatureSize**</span></span>
</dt> <dd>

<span data-ttu-id="31fd6-118">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="31fd6-118">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="31fd6-119">Tamanho de Singature em bytes.</span><span class="sxs-lookup"><span data-stu-id="31fd6-119">Singature size in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="31fd6-120">**StencilRef**</span><span class="sxs-lookup"><span data-stu-id="31fd6-120">**StencilRef**</span></span>
</dt> <dd>

<span data-ttu-id="31fd6-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="31fd6-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="31fd6-122">O valor de referência de estêncil usado no estado de estêncil de profundidade.</span><span class="sxs-lookup"><span data-stu-id="31fd6-122">The stencil-reference value used in the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="31fd6-123">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="31fd6-123">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="31fd6-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="31fd6-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="31fd6-125">A máscara de exemplo para o estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="31fd6-125">The sample mask for the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="31fd6-126">**BlendFactor**</span><span class="sxs-lookup"><span data-stu-id="31fd6-126">**BlendFactor**</span></span>
</dt> <dd>

<span data-ttu-id="31fd6-127">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="31fd6-127">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="31fd6-128">Os fatores de combinação por componente (RGBA) para o estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="31fd6-128">The per-component blend factors (RGBA) for the blend state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31fd6-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="31fd6-129">Remarks</span></span>

<span data-ttu-id="31fd6-130">D3DX11 \_ Pass \_ DESC é usado com [**ID3DX11EffectPass:: GetDesc**](id3dx11effectpass-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="31fd6-130">D3DX11\_PASS\_DESC is used with [**ID3DX11EffectPass::GetDesc**](id3dx11effectpass-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31fd6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31fd6-131">Requirements</span></span>



| <span data-ttu-id="31fd6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="31fd6-132">Requirement</span></span> | <span data-ttu-id="31fd6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="31fd6-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="31fd6-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31fd6-134">Header</span></span><br/> | <dl> <span data-ttu-id="31fd6-135"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="31fd6-135"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31fd6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="31fd6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31fd6-137">Efeitos 11 estruturas</span><span class="sxs-lookup"><span data-stu-id="31fd6-137">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

