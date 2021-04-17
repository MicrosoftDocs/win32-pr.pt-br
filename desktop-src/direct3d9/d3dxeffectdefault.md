---
description: Parâmetros padrão de efeito.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: Estrutura D3DXEFFECTDEFAULT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811519"
---
# <a name="d3dxeffectdefault-structure"></a><span data-ttu-id="5a911-103">Estrutura D3DXEFFECTDEFAULT</span><span class="sxs-lookup"><span data-stu-id="5a911-103">D3DXEFFECTDEFAULT structure</span></span>

<span data-ttu-id="5a911-104">Parâmetros padrão de efeito.</span><span class="sxs-lookup"><span data-stu-id="5a911-104">Effect default parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a911-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a911-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a><span data-ttu-id="5a911-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5a911-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5a911-107">**pParamName**</span><span class="sxs-lookup"><span data-stu-id="5a911-107">**pParamName**</span></span>
</dt> <dd>

<span data-ttu-id="5a911-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="5a911-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="5a911-109">Nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5a911-109">Parameter name.</span></span>

</dd> <dt>

<span data-ttu-id="5a911-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5a911-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="5a911-111">Tipo: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span><span class="sxs-lookup"><span data-stu-id="5a911-111">Type: **[**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5a911-112">Tipo de dados de uma era.</span><span class="sxs-lookup"><span data-stu-id="5a911-112">Data type in pValue.</span></span> <span data-ttu-id="5a911-113">Para obter mais informações, consulte [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span><span class="sxs-lookup"><span data-stu-id="5a911-113">For more information, see [**D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)</span></span>

</dd> <dt>

<span data-ttu-id="5a911-114">**NumBytes**</span><span class="sxs-lookup"><span data-stu-id="5a911-114">**NumBytes**</span></span>
</dt> <dd>

<span data-ttu-id="5a911-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a911-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5a911-116">Tamanho, em bytes, dos dados apontados por valores de a.</span><span class="sxs-lookup"><span data-stu-id="5a911-116">Size, in bytes, of the data pointed to by pValue.</span></span>

</dd> <dt>

<span data-ttu-id="5a911-117">**Valores**</span><span class="sxs-lookup"><span data-stu-id="5a911-117">**pValue**</span></span>
</dt> <dd>

<span data-ttu-id="5a911-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a911-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5a911-119">Ponteiro para o local da memória que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="5a911-119">Pointer to the memory location that contains the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a911-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a911-120">Requirements</span></span>



| <span data-ttu-id="5a911-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a911-121">Requirement</span></span> | <span data-ttu-id="5a911-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5a911-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a911-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a911-123">Header</span></span><br/> | <dl> <span data-ttu-id="5a911-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a911-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a911-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a911-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a911-126">Estruturas de efeito</span><span class="sxs-lookup"><span data-stu-id="5a911-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
