---
title: Função D3DPERF_SetMarker
description: Marque um evento instantâneo. O PIX pode usar esse evento para disparar uma ação.
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104365698"
---
# <a name="d3dperf_setmarker-function"></a><span data-ttu-id="a6e90-104">Função D3DPERF_SetMarker</span><span class="sxs-lookup"><span data-stu-id="a6e90-104">D3DPERF_SetMarker function</span></span>

<span data-ttu-id="a6e90-105">Marque um evento instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a6e90-105">Mark an instantaneous event.</span></span> <span data-ttu-id="a6e90-106">O PIX pode usar esse evento para disparar uma ação.</span><span class="sxs-lookup"><span data-stu-id="a6e90-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6e90-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6e90-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetMarker(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="a6e90-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6e90-108">Parameters</span></span>

`col`

<span data-ttu-id="a6e90-109">Cor do evento.</span><span class="sxs-lookup"><span data-stu-id="a6e90-109">Event color.</span></span> <span data-ttu-id="a6e90-110">Essa é a cor para exibir o evento no modo de exibição de evento.</span><span class="sxs-lookup"><span data-stu-id="a6e90-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="a6e90-111">Nome do evento.</span><span class="sxs-lookup"><span data-stu-id="a6e90-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6e90-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6e90-112">Return value</span></span>

<span data-ttu-id="a6e90-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a6e90-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6e90-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6e90-114">Remarks</span></span>

<span data-ttu-id="a6e90-115">Os eventos de usuário instantâneos não têm nenhum colchete ou outro evento de grupo.</span><span class="sxs-lookup"><span data-stu-id="a6e90-115">Instantaneous user events do not bracket or group other events.</span></span> <span data-ttu-id="a6e90-116">Por exemplo, quando o usuário aciona uma arma em um jogo, um evento *acionado por captura* pode ser criado por uma chamada **D3DPERF_SetMarker** .</span><span class="sxs-lookup"><span data-stu-id="a6e90-116">For example, when the user fires a weapon in a game, a *Shot Fired* event could be created by a **D3DPERF_SetMarker** call.</span></span> <span data-ttu-id="a6e90-117">Para agrupar vários eventos em um único nome definido pelo usuário, use **D3DPERF_BeginEvent** e **D3DPERF_EndEvent** em vez de **D3DPERF_SetMarker**.</span><span class="sxs-lookup"><span data-stu-id="a6e90-117">To group together multiple events under a single, user-defined name, use **D3DPERF_BeginEvent** and **D3DPERF_EndEvent** rather than **D3DPERF_SetMarker**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6e90-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6e90-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a6e90-119">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="a6e90-119">**Target Platform**</span></span> | <span data-ttu-id="a6e90-120">Windows</span><span class="sxs-lookup"><span data-stu-id="a6e90-120">Windows</span></span> |
| <span data-ttu-id="a6e90-121">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="a6e90-121">**Header**</span></span> | <span data-ttu-id="a6e90-122">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="a6e90-122">d3d9.h</span></span> |
| <span data-ttu-id="a6e90-123">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="a6e90-123">**Library**</span></span> | <span data-ttu-id="a6e90-124">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="a6e90-124">d3d9.lib</span></span> |
| <span data-ttu-id="a6e90-125">**DLL**</span><span class="sxs-lookup"><span data-stu-id="a6e90-125">**DLL**</span></span> | <span data-ttu-id="a6e90-126">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="a6e90-126">d3d9.dll</span></span> |