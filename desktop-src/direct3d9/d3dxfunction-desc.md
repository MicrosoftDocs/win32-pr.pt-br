---
description: Descreve uma função usada por um efeito.
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: Estrutura de D3DXFUNCTION_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781544"
---
# <a name="d3dxfunction_desc-structure"></a><span data-ttu-id="f22af-103">\_Estrutura desc de D3DXFUNCTION</span><span class="sxs-lookup"><span data-stu-id="f22af-103">D3DXFUNCTION\_DESC structure</span></span>

<span data-ttu-id="f22af-104">Descreve uma função usada por um efeito.</span><span class="sxs-lookup"><span data-stu-id="f22af-104">Describes a function used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="f22af-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f22af-105">Syntax</span></span>


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a><span data-ttu-id="f22af-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f22af-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f22af-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f22af-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="f22af-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f22af-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f22af-109">Nome da função.</span><span class="sxs-lookup"><span data-stu-id="f22af-109">Function name.</span></span>

</dd> <dt>

<span data-ttu-id="f22af-110">**Anotações**</span><span class="sxs-lookup"><span data-stu-id="f22af-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="f22af-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f22af-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f22af-112">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="f22af-112">Unused.</span></span> <span data-ttu-id="f22af-113">Esse membro sempre será definido como zero por [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span><span class="sxs-lookup"><span data-stu-id="f22af-113">This member will always be set to zero by [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f22af-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f22af-114">Requirements</span></span>



| <span data-ttu-id="f22af-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f22af-115">Requirement</span></span> | <span data-ttu-id="f22af-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f22af-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f22af-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f22af-117">Header</span></span><br/> | <dl> <span data-ttu-id="f22af-118"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f22af-118"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f22af-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f22af-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f22af-120">Estruturas de efeito</span><span class="sxs-lookup"><span data-stu-id="f22af-120">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
