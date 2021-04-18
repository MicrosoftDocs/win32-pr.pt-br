---
description: Descreve uma chave de retorno de chamada para uso na animação de quadro chave.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: Estrutura de D3DXKEY_CALLBACK (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 5c2c4dc90cbb95218268bf673204867f5b5d6636
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807285"
---
# <a name="d3dxkey_callback-structure"></a><span data-ttu-id="fb6d0-103">\_Estrutura de retorno de chamada D3DXKEY</span><span class="sxs-lookup"><span data-stu-id="fb6d0-103">D3DXKEY\_CALLBACK structure</span></span>

<span data-ttu-id="fb6d0-104">Descreve uma chave de retorno de chamada para uso na animação de quadro chave.</span><span class="sxs-lookup"><span data-stu-id="fb6d0-104">Describes a callback key for use in key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb6d0-105">Syntax</span></span>


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a><span data-ttu-id="fb6d0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fb6d0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fb6d0-107">**Hora**</span><span class="sxs-lookup"><span data-stu-id="fb6d0-107">**Time**</span></span>
</dt> <dd>

<span data-ttu-id="fb6d0-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb6d0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb6d0-109">Carimbo de data/hora do quadro principal.</span><span class="sxs-lookup"><span data-stu-id="fb6d0-109">Key frame time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="fb6d0-110">**pCallbackData**</span><span class="sxs-lookup"><span data-stu-id="fb6d0-110">**pCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="fb6d0-111">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb6d0-111">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fb6d0-112">Ponteiro para dados de retorno de chamada do usuário.</span><span class="sxs-lookup"><span data-stu-id="fb6d0-112">Pointer to user callback data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb6d0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb6d0-113">Requirements</span></span>



| <span data-ttu-id="fb6d0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb6d0-114">Requirement</span></span> | <span data-ttu-id="fb6d0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fb6d0-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6d0-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb6d0-116">Header</span></span><br/> | <dl> <span data-ttu-id="fb6d0-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb6d0-117"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb6d0-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb6d0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6d0-119">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="fb6d0-119">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
