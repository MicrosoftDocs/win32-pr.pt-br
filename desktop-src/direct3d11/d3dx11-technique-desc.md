---
title: Estrutura de D3DX11_TECHNIQUE_DESC (D3dx11effect. h)
description: Descreve uma técnica de efeito.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- Estrutura D3DX11_TECHNIQUE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664049"
---
# <a name="d3dx11_technique_desc-structure"></a><span data-ttu-id="eac9e-104">\_Estrutura desc de técnica de D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="eac9e-104">D3DX11\_TECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="eac9e-105">Descreve uma técnica de efeito.</span><span class="sxs-lookup"><span data-stu-id="eac9e-105">Describes an effect technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="eac9e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eac9e-106">Syntax</span></span>


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="eac9e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="eac9e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="eac9e-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="eac9e-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="eac9e-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eac9e-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eac9e-110">Nome dessa técnica (nulo se não anônimo).</span><span class="sxs-lookup"><span data-stu-id="eac9e-110">Name of this technique (NULL if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="eac9e-111">**Passa**</span><span class="sxs-lookup"><span data-stu-id="eac9e-111">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="eac9e-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eac9e-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eac9e-113">Número de passagens contidas na técnica.</span><span class="sxs-lookup"><span data-stu-id="eac9e-113">Number of passes contained in the technique.</span></span>

</dd> <dt>

<span data-ttu-id="eac9e-114">**Anotações**</span><span class="sxs-lookup"><span data-stu-id="eac9e-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="eac9e-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eac9e-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="eac9e-116">Número de anotações nesta técnica.</span><span class="sxs-lookup"><span data-stu-id="eac9e-116">Number of annotations on this technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eac9e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="eac9e-117">Remarks</span></span>

<span data-ttu-id="eac9e-118">\_A técnica \_ de D3DX11 DESC é usada com [**ID3DX11EffectTechnique:: GetDesc**](id3dx11effecttechnique-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="eac9e-118">D3DX11\_TECHNIQUE\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eac9e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eac9e-119">Requirements</span></span>



| <span data-ttu-id="eac9e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="eac9e-120">Requirement</span></span> | <span data-ttu-id="eac9e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="eac9e-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="eac9e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eac9e-122">Header</span></span><br/> | <dl> <span data-ttu-id="eac9e-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="eac9e-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eac9e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="eac9e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac9e-125">Efeitos 11 estruturas</span><span class="sxs-lookup"><span data-stu-id="eac9e-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

