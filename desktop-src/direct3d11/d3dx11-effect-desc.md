---
title: Estrutura de D3DX11_EFFECT_DESC (D3dx11effect. h)
description: Descreve um efeito.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- Estrutura D3DX11_EFFECT_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968700"
---
# <a name="d3dx11_effect_desc-structure"></a><span data-ttu-id="736ed-104">\_Estrutura desc de efeito de D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="736ed-104">D3DX11\_EFFECT\_DESC structure</span></span>

<span data-ttu-id="736ed-105">Descreve um efeito.</span><span class="sxs-lookup"><span data-stu-id="736ed-105">Describes an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="736ed-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="736ed-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="736ed-107">Membros</span><span class="sxs-lookup"><span data-stu-id="736ed-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="736ed-108">**ConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="736ed-108">**ConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="736ed-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="736ed-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="736ed-110">Número de buffers de constantes neste efeito.</span><span class="sxs-lookup"><span data-stu-id="736ed-110">Number of constant buffers in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="736ed-111">**GlobalVariables**</span><span class="sxs-lookup"><span data-stu-id="736ed-111">**GlobalVariables**</span></span>
</dt> <dd>

<span data-ttu-id="736ed-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="736ed-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="736ed-113">Número de variáveis globais neste efeito.</span><span class="sxs-lookup"><span data-stu-id="736ed-113">Number of global variables in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="736ed-114">**InterfaceVariables**</span><span class="sxs-lookup"><span data-stu-id="736ed-114">**InterfaceVariables**</span></span>
</dt> <dd>

<span data-ttu-id="736ed-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="736ed-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="736ed-116">Número de interfaces globais neste efeito.</span><span class="sxs-lookup"><span data-stu-id="736ed-116">Number of global interfaces in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="736ed-117">**Técnicas**</span><span class="sxs-lookup"><span data-stu-id="736ed-117">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="736ed-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="736ed-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="736ed-119">Número de técnicas neste efeito.</span><span class="sxs-lookup"><span data-stu-id="736ed-119">Number of techniques in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="736ed-120">**Grupos**</span><span class="sxs-lookup"><span data-stu-id="736ed-120">**Groups**</span></span>
</dt> <dd>

<span data-ttu-id="736ed-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="736ed-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="736ed-122">Número de grupos neste efeito.</span><span class="sxs-lookup"><span data-stu-id="736ed-122">Number of groups in this effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="736ed-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="736ed-123">Remarks</span></span>

<span data-ttu-id="736ed-124">O \_ efeito \_ desc de D3DX11 é usado com [**ID3DX11Effect:: GetDesc**](id3dx11effect-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="736ed-124">D3DX11\_EFFECT\_DESC is used with [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="736ed-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="736ed-125">Requirements</span></span>



| <span data-ttu-id="736ed-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="736ed-126">Requirement</span></span> | <span data-ttu-id="736ed-127">Valor</span><span class="sxs-lookup"><span data-stu-id="736ed-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="736ed-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="736ed-128">Header</span></span><br/> | <dl> <span data-ttu-id="736ed-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="736ed-129"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="736ed-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="736ed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="736ed-131">Efeitos 11 estruturas</span><span class="sxs-lookup"><span data-stu-id="736ed-131">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

