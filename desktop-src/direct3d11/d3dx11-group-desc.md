---
title: Estrutura de D3DX11_GROUP_DESC (D3dx11effect. h)
description: Descreve um grupo de efeitos.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- Estrutura D3DX11_GROUP_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012178"
---
# <a name="d3dx11_group_desc-structure"></a><span data-ttu-id="95c1f-104">\_Estrutura desc de grupo D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="95c1f-104">D3DX11\_GROUP\_DESC structure</span></span>

<span data-ttu-id="95c1f-105">Descreve um grupo de efeitos.</span><span class="sxs-lookup"><span data-stu-id="95c1f-105">Describes an effect group.</span></span>

## <a name="syntax"></a><span data-ttu-id="95c1f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95c1f-106">Syntax</span></span>


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a><span data-ttu-id="95c1f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="95c1f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="95c1f-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="95c1f-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="95c1f-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95c1f-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="95c1f-110">Nome deste grupo ( **nulo** somente se global).</span><span class="sxs-lookup"><span data-stu-id="95c1f-110">Name of this group (only **NULL** if global).</span></span>

</dd> <dt>

<span data-ttu-id="95c1f-111">**Técnicas**</span><span class="sxs-lookup"><span data-stu-id="95c1f-111">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="95c1f-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95c1f-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="95c1f-113">Número de técnicas contidas no grupo.</span><span class="sxs-lookup"><span data-stu-id="95c1f-113">Number of techniques contained in group.</span></span>

</dd> <dt>

<span data-ttu-id="95c1f-114">**Anotações**</span><span class="sxs-lookup"><span data-stu-id="95c1f-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="95c1f-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95c1f-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="95c1f-116">Número de anotações neste grupo.</span><span class="sxs-lookup"><span data-stu-id="95c1f-116">Number of annotations on this group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95c1f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="95c1f-117">Remarks</span></span>

<span data-ttu-id="95c1f-118">O \_ grupo \_ de D3DX11 DESC é usado com [**ID3DX11EffectTechnique:: GetDesc**](id3dx11effecttechnique-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="95c1f-118">D3DX11\_GROUP\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95c1f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95c1f-119">Requirements</span></span>



| <span data-ttu-id="95c1f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="95c1f-120">Requirement</span></span> | <span data-ttu-id="95c1f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="95c1f-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="95c1f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95c1f-122">Header</span></span><br/> | <dl> <span data-ttu-id="95c1f-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="95c1f-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95c1f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="95c1f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c1f-125">Efeitos 11 estruturas</span><span class="sxs-lookup"><span data-stu-id="95c1f-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

