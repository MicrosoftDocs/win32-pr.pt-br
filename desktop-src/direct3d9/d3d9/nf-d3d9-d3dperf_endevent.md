---
title: Função D3DPERF_EndEvent
description: Marca o final de um evento definido pelo usuário. O PIX pode usar esse evento para disparar uma ação.
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104365699"
---
# <a name="d3dperf_endevent-function"></a><span data-ttu-id="6fb22-104">Função D3DPERF_EndEvent</span><span class="sxs-lookup"><span data-stu-id="6fb22-104">D3DPERF_EndEvent function</span></span>

<span data-ttu-id="6fb22-105">Marca o final de um evento definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6fb22-105">Marks the end of a user-defined event.</span></span> <span data-ttu-id="6fb22-106">O PIX pode usar esse evento para disparar uma ação.</span><span class="sxs-lookup"><span data-stu-id="6fb22-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb22-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fb22-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a><span data-ttu-id="6fb22-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fb22-108">Return value</span></span>

<span data-ttu-id="6fb22-109">O nível da hierarquia na qual o evento está terminando.</span><span class="sxs-lookup"><span data-stu-id="6fb22-109">The level of the hierarchy in which the event is ending.</span></span> <span data-ttu-id="6fb22-110">Se ocorrer um erro, esse valor será negativo.</span><span class="sxs-lookup"><span data-stu-id="6fb22-110">If an error occurs, this value is negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fb22-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fb22-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6fb22-112">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="6fb22-112">**Target Platform**</span></span> | <span data-ttu-id="6fb22-113">Windows</span><span class="sxs-lookup"><span data-stu-id="6fb22-113">Windows</span></span> |
| <span data-ttu-id="6fb22-114">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="6fb22-114">**Header**</span></span> | <span data-ttu-id="6fb22-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="6fb22-115">d3d9.h</span></span> |
| <span data-ttu-id="6fb22-116">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="6fb22-116">**Library**</span></span> | <span data-ttu-id="6fb22-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="6fb22-117">d3d9.lib</span></span> |
| <span data-ttu-id="6fb22-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="6fb22-118">**DLL**</span></span> | <span data-ttu-id="6fb22-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="6fb22-119">d3d9.dll</span></span> |