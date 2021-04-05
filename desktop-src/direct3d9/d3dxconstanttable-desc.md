---
description: Uma descrição da tabela de constantes.
ms.assetid: 848b328a-95a4-4fd0-a7d4-4fb0e5d14f64
title: Estrutura de D3DXCONSTANTTABLE_DESC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANTTABLE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7c53023952518182f68cf4a671ec47c6056a92a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664021"
---
# <a name="d3dxconstanttable_desc-structure"></a><span data-ttu-id="e255c-103">\_Estrutura desc de D3DXCONSTANTTABLE</span><span class="sxs-lookup"><span data-stu-id="e255c-103">D3DXCONSTANTTABLE\_DESC structure</span></span>

<span data-ttu-id="e255c-104">Uma descrição da tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="e255c-104">A description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="e255c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e255c-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANTTABLE_DESC {
  LPCSTR Creator;
  DWORD  Version;
  UINT   Constants;
} D3DXCONSTANTTABLE_DESC, *LPD3DXCONSTANTTABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="e255c-106">Membros</span><span class="sxs-lookup"><span data-stu-id="e255c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e255c-107">**Criador**</span><span class="sxs-lookup"><span data-stu-id="e255c-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="e255c-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e255c-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e255c-109">Nome do criador da tabela constante.</span><span class="sxs-lookup"><span data-stu-id="e255c-109">Name of the constant table creator.</span></span>

</dd> <dt>

<span data-ttu-id="e255c-110">**Versão**</span><span class="sxs-lookup"><span data-stu-id="e255c-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="e255c-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e255c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e255c-112">Versão do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e255c-112">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="e255c-113">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="e255c-113">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="e255c-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e255c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e255c-115">Número de constantes na tabela de constantes.</span><span class="sxs-lookup"><span data-stu-id="e255c-115">Number of constants in the constant table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e255c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e255c-116">Requirements</span></span>



| <span data-ttu-id="e255c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e255c-117">Requirement</span></span> | <span data-ttu-id="e255c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e255c-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e255c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e255c-119">Header</span></span><br/> | <dl> <span data-ttu-id="e255c-120"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e255c-120"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e255c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e255c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e255c-122">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="e255c-122">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="e255c-123">**D3DXCONSTANT \_ desc**</span><span class="sxs-lookup"><span data-stu-id="e255c-123">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 
