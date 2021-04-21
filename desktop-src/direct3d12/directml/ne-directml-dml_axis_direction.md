---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: Define constantes que especificam a direção de uma operação ao longo do eixo especificado para o operador (por exemplo, somatório, selecionando os elementos de Top-k, selecionando o elemento mínimo).
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_AXIS_DIRECTION
ms.openlocfilehash: e54d2abed3843ea9b2a22cb3c385f9edd1541ba5
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803778"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a><span data-ttu-id="64d71-103">Enumeração de DML_AXIS_DIRECTION (directml. h)</span><span class="sxs-lookup"><span data-stu-id="64d71-103">DML_AXIS_DIRECTION enumeration (directml.h)</span></span>

<span data-ttu-id="64d71-104">Define constantes que especificam a direção de uma operação ao longo do eixo especificado para o operador (por exemplo, somatório, selecionando os elementos de Top-k, selecionando o elemento mínimo).</span><span class="sxs-lookup"><span data-stu-id="64d71-104">Defines constants that specify the direction of an operation along the given axis for the operator (for example, summation, selecting the top-k elements, selecting the minimum element).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64d71-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="64d71-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="64d71-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="64d71-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="64d71-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64d71-107">Syntax</span></span>
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a><span data-ttu-id="64d71-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="64d71-108">Constants</span></span>

| <span data-ttu-id="64d71-109">Nome</span><span class="sxs-lookup"><span data-stu-id="64d71-109">Name</span></span> | <span data-ttu-id="64d71-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="64d71-110">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="64d71-111">DML_AXIS_DIRECTION_INCREASING</span><span class="sxs-lookup"><span data-stu-id="64d71-111">DML_AXIS_DIRECTION_INCREASING</span></span> | <span data-ttu-id="64d71-112">Especifica a ordem crescente (do índice baixo para o índice alto).</span><span class="sxs-lookup"><span data-stu-id="64d71-112">Specifies increasing order (from the low index to the high index).</span></span> |
| <span data-ttu-id="64d71-113">DML_AXIS_DIRECTION_DECREASING</span><span class="sxs-lookup"><span data-stu-id="64d71-113">DML_AXIS_DIRECTION_DECREASING</span></span> | <span data-ttu-id="64d71-114">Especifica a ordem decrescente (do índice alto para o índice baixo).</span><span class="sxs-lookup"><span data-stu-id="64d71-114">Specifies decreasing order (from the high index to the low index).</span></span> |


## <a name="requirements"></a><span data-ttu-id="64d71-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64d71-115">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="64d71-116">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="64d71-116">**Header**</span></span> | <span data-ttu-id="64d71-117">directml. h</span><span class="sxs-lookup"><span data-stu-id="64d71-117">directml.h</span></span> |