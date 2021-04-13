---
description: Descreve uma passagem para um objeto de efeito.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: Estrutura de D3DXPASS_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298479"
---
# <a name="d3dxpass_desc-structure"></a><span data-ttu-id="4233e-103">\_Estrutura desc de D3DXPASS</span><span class="sxs-lookup"><span data-stu-id="4233e-103">D3DXPASS\_DESC structure</span></span>

<span data-ttu-id="4233e-104">Descreve uma passagem para um objeto de efeito.</span><span class="sxs-lookup"><span data-stu-id="4233e-104">Describes a pass for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4233e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4233e-105">Syntax</span></span>


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a><span data-ttu-id="4233e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4233e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4233e-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4233e-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="4233e-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4233e-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4233e-109">Valor de cadeia de caracteres usado para a passagem.</span><span class="sxs-lookup"><span data-stu-id="4233e-109">String value used for the pass.</span></span>

</dd> <dt>

<span data-ttu-id="4233e-110">**Anotações**</span><span class="sxs-lookup"><span data-stu-id="4233e-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="4233e-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4233e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4233e-112">As anotações são dados específicos do usuário que podem ser anexados a qualquer técnica, passagem ou parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4233e-112">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="4233e-113">Consulte [adicionar informações para parâmetros de efeito com \_ anotações](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="4233e-113">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> <dt>

<span data-ttu-id="4233e-114">**pVertexShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="4233e-114">**pVertexShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="4233e-115">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4233e-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="4233e-116">Ponteiro para a função de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="4233e-116">Pointer to the vertex shader function.</span></span> <span data-ttu-id="4233e-117">Se um efeito for criado com [D3DXFX \_ não \_ clonável](d3dxfx.md), essa estrutura retornará um ponteiro **nulo** quando for chamado por [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span><span class="sxs-lookup"><span data-stu-id="4233e-117">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> <dt>

<span data-ttu-id="4233e-118">**pPixelShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="4233e-118">**pPixelShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="4233e-119">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="4233e-119">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="4233e-120">Ponteiro para a função de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="4233e-120">Pointer to the pixel shader function.</span></span> <span data-ttu-id="4233e-121">Se um efeito for criado com [D3DXFX \_ não \_ clonável](d3dxfx.md), essa estrutura retornará um ponteiro **nulo** quando for chamado por [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span><span class="sxs-lookup"><span data-stu-id="4233e-121">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4233e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4233e-122">Requirements</span></span>



| <span data-ttu-id="4233e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4233e-123">Requirement</span></span> | <span data-ttu-id="4233e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4233e-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4233e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4233e-125">Header</span></span><br/> | <dl> <span data-ttu-id="4233e-126"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4233e-126"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4233e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4233e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4233e-128">Estruturas de efeito</span><span class="sxs-lookup"><span data-stu-id="4233e-128">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="4233e-129">**GetPassDesc**</span><span class="sxs-lookup"><span data-stu-id="4233e-129">**GetPassDesc**</span></span>](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
