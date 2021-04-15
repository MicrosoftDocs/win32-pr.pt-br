---
title: Função D3DPERF_SetOptions
description: Defina as opções do criador de perfil especificadas pelo programa de destino.
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104453869"
---
# <a name="d3dperf_setoptions-function"></a><span data-ttu-id="a46c0-103">Função D3DPERF_SetOptions</span><span class="sxs-lookup"><span data-stu-id="a46c0-103">D3DPERF_SetOptions function</span></span>

<span data-ttu-id="a46c0-104">Defina as opções do criador de perfil especificadas pelo programa de destino.</span><span class="sxs-lookup"><span data-stu-id="a46c0-104">Set profiler options specified by the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="a46c0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a46c0-105">Syntax</span></span>

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a><span data-ttu-id="a46c0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a46c0-106">Parameters</span></span>

`dwOptions`

<span data-ttu-id="a46c0-107">Opções de usuário reconhecíveis pelo PIX.</span><span class="sxs-lookup"><span data-stu-id="a46c0-107">User options recognizable by PIX.</span></span> <span data-ttu-id="a46c0-108">Defina isso como 1 para notificar o PIX de que o programa de destino não dá permissão para ser criado.</span><span class="sxs-lookup"><span data-stu-id="a46c0-108">Set this to 1 to notify PIX that the target program does not give permission to be profiled.</span></span>

## <a name="return-value"></a><span data-ttu-id="a46c0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a46c0-109">Return value</span></span>

<span data-ttu-id="a46c0-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a46c0-110">This function doesn't return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a46c0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a46c0-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a46c0-112">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="a46c0-112">**Target Platform**</span></span> | <span data-ttu-id="a46c0-113">Windows</span><span class="sxs-lookup"><span data-stu-id="a46c0-113">Windows</span></span> |
| <span data-ttu-id="a46c0-114">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="a46c0-114">**Header**</span></span> | <span data-ttu-id="a46c0-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="a46c0-115">d3d9.h</span></span> |
| <span data-ttu-id="a46c0-116">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="a46c0-116">**Library**</span></span> | <span data-ttu-id="a46c0-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="a46c0-117">d3d9.lib</span></span> |
| <span data-ttu-id="a46c0-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="a46c0-118">**DLL**</span></span> | <span data-ttu-id="a46c0-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="a46c0-119">d3d9.dll</span></span> |