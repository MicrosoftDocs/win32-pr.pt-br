---
title: Função D3DPERF_QueryRepeatFrame
description: Determine se um criador de perfil de desempenho está solicitando que o quadro atual seja reenviado ao Direct3D para análise de desempenho. Atualmente, essa função não tem suporte no PIX.
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
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "103640240"
---
# <a name="d3dperf_queryrepeatframe-function"></a><span data-ttu-id="9da92-104">Função D3DPERF_QueryRepeatFrame</span><span class="sxs-lookup"><span data-stu-id="9da92-104">D3DPERF_QueryRepeatFrame function</span></span>

<span data-ttu-id="9da92-105">Determine se um criador de perfil de desempenho está solicitando que o quadro atual seja reenviado ao Direct3D para análise de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9da92-105">Determine whether a performance profiler is requesting that the current frame be resubmitted to Direct3D for performance analysis.</span></span> <span data-ttu-id="9da92-106">Atualmente, essa função não tem suporte no PIX.</span><span class="sxs-lookup"><span data-stu-id="9da92-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="9da92-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9da92-107">Syntax</span></span>

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a><span data-ttu-id="9da92-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9da92-108">Return value</span></span>

<span data-ttu-id="9da92-109">Se o valor de retorno for TRUE, o chamador deverá repetir a mesma sequência de chamadas.</span><span class="sxs-lookup"><span data-stu-id="9da92-109">If the return value is TRUE, the caller should repeat the same sequence of calls.</span></span> <span data-ttu-id="9da92-110">Se for FALSE, o chamador deverá continuar.</span><span class="sxs-lookup"><span data-stu-id="9da92-110">If FALSE, the caller should continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="9da92-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9da92-111">Remarks</span></span>

<span data-ttu-id="9da92-112">A função deve ser chamada imediatamente após **IDirect3DDevice9::P reenviado** é chamado.</span><span class="sxs-lookup"><span data-stu-id="9da92-112">The function should be called immediately after **IDirect3DDevice9::Present** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="9da92-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9da92-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9da92-114">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="9da92-114">**Target Platform**</span></span> | <span data-ttu-id="9da92-115">Windows</span><span class="sxs-lookup"><span data-stu-id="9da92-115">Windows</span></span> |
| <span data-ttu-id="9da92-116">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="9da92-116">**Header**</span></span> | <span data-ttu-id="9da92-117">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="9da92-117">d3d9.h</span></span> |
| <span data-ttu-id="9da92-118">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="9da92-118">**Library**</span></span> | <span data-ttu-id="9da92-119">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="9da92-119">d3d9.lib</span></span> |
| <span data-ttu-id="9da92-120">**DLL**</span><span class="sxs-lookup"><span data-stu-id="9da92-120">**DLL**</span></span> | <span data-ttu-id="9da92-121">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="9da92-121">d3d9.dll</span></span> |