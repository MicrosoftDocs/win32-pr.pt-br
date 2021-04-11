---
title: Função D3DPERF_GetStatus
description: Determine o estado atual do criador de perfil do programa de destino.
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
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104293836"
---
# <a name="d3dperf_getstatus-function"></a><span data-ttu-id="83fcd-103">Função D3DPERF_GetStatus</span><span class="sxs-lookup"><span data-stu-id="83fcd-103">D3DPERF_GetStatus function</span></span>

<span data-ttu-id="83fcd-104">Determine o estado atual do criador de perfil do programa de destino.</span><span class="sxs-lookup"><span data-stu-id="83fcd-104">Determine the current state of the profiler from the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="83fcd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83fcd-105">Syntax</span></span>

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a><span data-ttu-id="83fcd-106">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83fcd-106">Return value</span></span>

<span data-ttu-id="83fcd-107">Um valor diferente de zero quando o PIX está criando o perfil do programa de destino; caso contrário, zero.</span><span class="sxs-lookup"><span data-stu-id="83fcd-107">A non-zero value when PIX is profiling the target program; otherwise, zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="83fcd-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83fcd-108">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="83fcd-109">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="83fcd-109">**Target Platform**</span></span> | <span data-ttu-id="83fcd-110">Windows</span><span class="sxs-lookup"><span data-stu-id="83fcd-110">Windows</span></span> |
| <span data-ttu-id="83fcd-111">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="83fcd-111">**Header**</span></span> | <span data-ttu-id="83fcd-112">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="83fcd-112">d3d9.h</span></span> |
| <span data-ttu-id="83fcd-113">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="83fcd-113">**Library**</span></span> | <span data-ttu-id="83fcd-114">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="83fcd-114">d3d9.lib</span></span> |
| <span data-ttu-id="83fcd-115">**DLL**</span><span class="sxs-lookup"><span data-stu-id="83fcd-115">**DLL**</span></span> | <span data-ttu-id="83fcd-116">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="83fcd-116">d3d9.dll</span></span> |