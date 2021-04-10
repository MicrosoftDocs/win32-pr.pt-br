---
description: Descreve uma técnica usada por um efeito.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: Estrutura de D3DXTECHNIQUE_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012086"
---
# <a name="d3dxtechnique_desc-structure"></a><span data-ttu-id="eef2c-103">\_Estrutura desc de D3DXTECHNIQUE</span><span class="sxs-lookup"><span data-stu-id="eef2c-103">D3DXTECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="eef2c-104">Descreve uma técnica usada por um efeito.</span><span class="sxs-lookup"><span data-stu-id="eef2c-104">Describes a technique used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef2c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eef2c-105">Syntax</span></span>


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="eef2c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="eef2c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="eef2c-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="eef2c-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="eef2c-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eef2c-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eef2c-109">Cadeia de caracteres que contém o nome da técnica.</span><span class="sxs-lookup"><span data-stu-id="eef2c-109">String that contains the technique name.</span></span>

</dd> <dt>

<span data-ttu-id="eef2c-110">**Passa**</span><span class="sxs-lookup"><span data-stu-id="eef2c-110">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="eef2c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eef2c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eef2c-112">O número de renderização que a técnica exige.</span><span class="sxs-lookup"><span data-stu-id="eef2c-112">Number of rendering passes the technique requires.</span></span> <span data-ttu-id="eef2c-113">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="eef2c-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="eef2c-114">**Anotações**</span><span class="sxs-lookup"><span data-stu-id="eef2c-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="eef2c-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eef2c-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eef2c-116">O número de anotações.</span><span class="sxs-lookup"><span data-stu-id="eef2c-116">The number of annotations.</span></span> <span data-ttu-id="eef2c-117">Consulte [adicionar informações para parâmetros de efeito com \_ anotações](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="eef2c-117">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eef2c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="eef2c-118">Remarks</span></span>

<span data-ttu-id="eef2c-119">Algumas placas de vídeo podem renderizar duas texturas em uma única passagem.</span><span class="sxs-lookup"><span data-stu-id="eef2c-119">Some video cards can render two textures in a single pass.</span></span> <span data-ttu-id="eef2c-120">No entanto, se um cartão não tiver esse recurso, geralmente é possível renderizar o mesmo efeito em duas passagens, usando uma textura para cada passagem.</span><span class="sxs-lookup"><span data-stu-id="eef2c-120">However, if a card does not have this capability, it is often possible to render the same effect in two passes, using one texture for each pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="eef2c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eef2c-121">Requirements</span></span>



| <span data-ttu-id="eef2c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eef2c-122">Requirement</span></span> | <span data-ttu-id="eef2c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="eef2c-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef2c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eef2c-124">Header</span></span><br/> | <dl> <span data-ttu-id="eef2c-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="eef2c-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef2c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="eef2c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef2c-127">Estruturas de efeito</span><span class="sxs-lookup"><span data-stu-id="eef2c-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
