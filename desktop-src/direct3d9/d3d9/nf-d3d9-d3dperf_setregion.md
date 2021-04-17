---
title: Função D3DPERF_SetRegion
description: Marque uma série de quadros com a cor e o nome especificados no arquivo PIXRun. Atualmente, essa função não tem suporte no PIX.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "105812137"
---
# <a name="d3dperf_setregion-function"></a><span data-ttu-id="3637d-104">Função D3DPERF_SetRegion</span><span class="sxs-lookup"><span data-stu-id="3637d-104">D3DPERF_SetRegion function</span></span>

<span data-ttu-id="3637d-105">Marque uma série de quadros com a cor e o nome especificados no arquivo PIXRun.</span><span class="sxs-lookup"><span data-stu-id="3637d-105">Mark a series of frames with the specified color and name in the PIXRun file.</span></span> <span data-ttu-id="3637d-106">Atualmente, essa função não tem suporte no PIX.</span><span class="sxs-lookup"><span data-stu-id="3637d-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="3637d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3637d-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="3637d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3637d-108">Parameters</span></span>

`col`

<span data-ttu-id="3637d-109">Cor do evento.</span><span class="sxs-lookup"><span data-stu-id="3637d-109">Event color.</span></span> <span data-ttu-id="3637d-110">Essa é a cor para exibir o evento no modo de exibição de evento.</span><span class="sxs-lookup"><span data-stu-id="3637d-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="3637d-111">Nome do evento.</span><span class="sxs-lookup"><span data-stu-id="3637d-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="3637d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3637d-112">Return value</span></span>

<span data-ttu-id="3637d-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3637d-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3637d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3637d-114">Remarks</span></span>

<span data-ttu-id="3637d-115">Para facilitar a análise, o programa de destino pode usar cores para marcar cada nível de um programa de destino.</span><span class="sxs-lookup"><span data-stu-id="3637d-115">To make analysis easier, the target program can use color to mark each level of a target program.</span></span>

## <a name="requirements"></a><span data-ttu-id="3637d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3637d-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3637d-117">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="3637d-117">**Target Platform**</span></span> | <span data-ttu-id="3637d-118">Windows</span><span class="sxs-lookup"><span data-stu-id="3637d-118">Windows</span></span> |
| <span data-ttu-id="3637d-119">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="3637d-119">**Header**</span></span> | <span data-ttu-id="3637d-120">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="3637d-120">d3d9.h</span></span> |
| <span data-ttu-id="3637d-121">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="3637d-121">**Library**</span></span> | <span data-ttu-id="3637d-122">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="3637d-122">d3d9.lib</span></span> |
| <span data-ttu-id="3637d-123">**DLL**</span><span class="sxs-lookup"><span data-stu-id="3637d-123">**DLL**</span></span> | <span data-ttu-id="3637d-124">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="3637d-124">d3d9.dll</span></span> |