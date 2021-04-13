---
title: OP_POLICY_PART
description: Definição de IDL de OP_POLICY_PART
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104366869"
---
# <a name="op_policy_part-structure"></a><span data-ttu-id="71dd2-103">Estrutura de OP_POLICY_PART</span><span class="sxs-lookup"><span data-stu-id="71dd2-103">OP_POLICY_PART structure</span></span>

<span data-ttu-id="71dd2-104">Contém uma matriz de estruturas de OP_POLICY_ELEMENT_LIST.</span><span class="sxs-lookup"><span data-stu-id="71dd2-104">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="71dd2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71dd2-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a><span data-ttu-id="71dd2-106">Membros</span><span class="sxs-lookup"><span data-stu-id="71dd2-106">Members</span></span>

### <a name="celementlists"></a><span data-ttu-id="71dd2-107">cElementLists</span><span class="sxs-lookup"><span data-stu-id="71dd2-107">cElementLists</span></span>

<span data-ttu-id="71dd2-108">Contém o número de elementos em pElementLists.</span><span class="sxs-lookup"><span data-stu-id="71dd2-108">Contains the number of elements in pElementLists.</span></span>

### <a name="pelementlists"></a><span data-ttu-id="71dd2-109">pElementLists</span><span class="sxs-lookup"><span data-stu-id="71dd2-109">pElementLists</span></span>

<span data-ttu-id="71dd2-110">Contém uma matriz de estruturas de OP_POLICY_ELEMENT_LIST.</span><span class="sxs-lookup"><span data-stu-id="71dd2-110">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

### <a name="extension"></a><span data-ttu-id="71dd2-111">Extensão</span><span class="sxs-lookup"><span data-stu-id="71dd2-111">Extension</span></span>

<span data-ttu-id="71dd2-112">Reservado para uso futuro e deve conter todos os zeros.</span><span class="sxs-lookup"><span data-stu-id="71dd2-112">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="71dd2-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="71dd2-113">See also</span></span>

[<span data-ttu-id="71dd2-114">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="71dd2-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="71dd2-115">**\_lista de \_ elementos de política op \_**</span><span class="sxs-lookup"><span data-stu-id="71dd2-115">**OP\_POLICY\_ELEMENT\_LIST**</span></span>](odj-op_policy_element_list.md)
