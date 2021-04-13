---
description: Tipo de dados para gerenciar um conjunto de parâmetros de efeito padrão.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: Estrutura D3DXEFFECTINSTANCE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298626"
---
# <a name="d3dxeffectinstance-structure"></a><span data-ttu-id="577a3-103">Estrutura D3DXEFFECTINSTANCE</span><span class="sxs-lookup"><span data-stu-id="577a3-103">D3DXEFFECTINSTANCE structure</span></span>

<span data-ttu-id="577a3-104">Tipo de dados para gerenciar um conjunto de parâmetros de efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="577a3-104">Data type for managing a set of default effect parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="577a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="577a3-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a><span data-ttu-id="577a3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="577a3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="577a3-107">**pEffectFilename**</span><span class="sxs-lookup"><span data-stu-id="577a3-107">**pEffectFilename**</span></span>
</dt> <dd>

<span data-ttu-id="577a3-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="577a3-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="577a3-109">Nome do arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="577a3-109">Name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="577a3-110">**NumDefaults**</span><span class="sxs-lookup"><span data-stu-id="577a3-110">**NumDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="577a3-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="577a3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="577a3-112">Número de parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="577a3-112">Number of default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="577a3-113">**pDefaults**</span><span class="sxs-lookup"><span data-stu-id="577a3-113">**pDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="577a3-114">Tipo: **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span><span class="sxs-lookup"><span data-stu-id="577a3-114">Type: **[**LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span></span>

</dd> <dd>

<span data-ttu-id="577a3-115">Ponteiro para uma matriz de elementos [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) , cada um contendo um parâmetro de efeito.</span><span class="sxs-lookup"><span data-stu-id="577a3-115">Pointer to an array of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) elements, each of which contains an effect parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="577a3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="577a3-116">Requirements</span></span>



| <span data-ttu-id="577a3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="577a3-117">Requirement</span></span> | <span data-ttu-id="577a3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="577a3-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="577a3-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="577a3-119">Header</span></span><br/> | <dl> <span data-ttu-id="577a3-120"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="577a3-120"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="577a3-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="577a3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577a3-122">Estruturas de efeito</span><span class="sxs-lookup"><span data-stu-id="577a3-122">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
