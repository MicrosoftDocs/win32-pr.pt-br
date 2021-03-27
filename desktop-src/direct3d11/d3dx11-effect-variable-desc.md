---
title: Estrutura de D3DX11_EFFECT_VARIABLE_DESC (D3dx11effect. h)
description: Descreve uma variável de efeito.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- Estrutura D3DX11_EFFECT_VARIABLE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989397"
---
# <a name="d3dx11_effect_variable_desc-structure"></a><span data-ttu-id="e1247-104">\_ \_ Estrutura desc da variável de efeito D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="e1247-104">D3DX11\_EFFECT\_VARIABLE\_DESC structure</span></span>

<span data-ttu-id="e1247-105">Descreve uma variável de efeito.</span><span class="sxs-lookup"><span data-stu-id="e1247-105">Describes an effect variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1247-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1247-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="e1247-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e1247-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e1247-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e1247-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="e1247-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1247-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e1247-110">Nome desta variável, anotação ou membro de estrutura.</span><span class="sxs-lookup"><span data-stu-id="e1247-110">Name of this variable, annotation, or structure member.</span></span>

</dd> <dt>

<span data-ttu-id="e1247-111">**Semântico**</span><span class="sxs-lookup"><span data-stu-id="e1247-111">**Semantic**</span></span>
</dt> <dd>

<span data-ttu-id="e1247-112">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1247-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e1247-113">Cadeia de caracteres semântica dessa variável ou membro de estrutura (NULL para anotações ou se não estiver presente).</span><span class="sxs-lookup"><span data-stu-id="e1247-113">Semantic string of this variable or structure member (NULL for annotations or if not present).</span></span>

</dd> <dt>

<span data-ttu-id="e1247-114">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="e1247-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="e1247-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1247-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e1247-116">Sinalizadores opcionais para variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="e1247-116">Optional flags for effect variables.</span></span>

</dd> <dt>

<span data-ttu-id="e1247-117">**Anotações**</span><span class="sxs-lookup"><span data-stu-id="e1247-117">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="e1247-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1247-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e1247-119">Número de anotações nessa variável (sempre 0 para anotações).</span><span class="sxs-lookup"><span data-stu-id="e1247-119">Number of annotations on this variable (always 0 for annotations).</span></span>

</dd> <dt>

<span data-ttu-id="e1247-120">**BufferOffset**</span><span class="sxs-lookup"><span data-stu-id="e1247-120">**BufferOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e1247-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1247-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e1247-122">Offset em contendo CBuffer ou tbuffers (sempre 0 para anotações ou variáveis que não estão em buffers constantes).</span><span class="sxs-lookup"><span data-stu-id="e1247-122">Offset into containing cbuffer or tbuffer (always 0 for annotations or variables not in constant buffers).</span></span>

</dd> <dt>

<span data-ttu-id="e1247-123">**ExplicitBindPoint**</span><span class="sxs-lookup"><span data-stu-id="e1247-123">**ExplicitBindPoint**</span></span>
</dt> <dd>

<span data-ttu-id="e1247-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1247-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="e1247-125">Usado se a variável tiver sido explicitamente associada usando a palavra-chave Register.</span><span class="sxs-lookup"><span data-stu-id="e1247-125">Used if the variable has been explicitly bound using the register keyword.</span></span> <span data-ttu-id="e1247-126">Verifique os sinalizadores para \_ o \_ \_ ponto de ligação explícito da variável de efeito D3DX11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e1247-126">Check Flags for D3DX11\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1247-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1247-127">Remarks</span></span>

<span data-ttu-id="e1247-128">\_ \_ A variável de efeito D3DX11 \_ DESC é usada com [**ID3DX11EffectVariable:: GetDesc**](id3dx11effectvariable-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="e1247-128">D3DX11\_EFFECT\_VARIABLE\_DESC is used with [**ID3DX11EffectVariable::GetDesc**](id3dx11effectvariable-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1247-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1247-129">Requirements</span></span>



| <span data-ttu-id="e1247-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1247-130">Requirement</span></span> | <span data-ttu-id="e1247-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e1247-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1247-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1247-132">Header</span></span><br/> | <dl> <span data-ttu-id="e1247-133"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1247-133"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1247-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1247-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1247-135">Efeitos 11 estruturas</span><span class="sxs-lookup"><span data-stu-id="e1247-135">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

