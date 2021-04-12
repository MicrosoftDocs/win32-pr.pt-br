---
title: Função D3DPERF_BeginEvent
description: Marca o início de um evento definido pelo usuário. O PIX pode usar esse evento para disparar uma ação.
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: f6732d4ce969cbd26cdb32f4750654c7baacd324
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/08/2020
ms.locfileid: "104365697"
---
# <a name="d3dperf_beginevent-function"></a><span data-ttu-id="8afca-104">Função D3DPERF_BeginEvent</span><span class="sxs-lookup"><span data-stu-id="8afca-104">D3DPERF_BeginEvent function</span></span>

<span data-ttu-id="8afca-105">Marca o início de um evento definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8afca-105">Marks the beginning of a user-defined event.</span></span> <span data-ttu-id="8afca-106">O PIX pode usar esse evento para disparar uma ação.</span><span class="sxs-lookup"><span data-stu-id="8afca-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8afca-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_BeginEvent(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="8afca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8afca-108">Parameters</span></span>

`col`

<span data-ttu-id="8afca-109">Cor do evento.</span><span class="sxs-lookup"><span data-stu-id="8afca-109">Event color.</span></span> <span data-ttu-id="8afca-110">Essa é a cor para exibir o evento no modo de exibição de evento.</span><span class="sxs-lookup"><span data-stu-id="8afca-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="8afca-111">Nome do evento.</span><span class="sxs-lookup"><span data-stu-id="8afca-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="8afca-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8afca-112">Return value</span></span>

<span data-ttu-id="8afca-113">O nível de base zero da hierarquia em que esse evento está sendo iniciado.</span><span class="sxs-lookup"><span data-stu-id="8afca-113">The zero-based level of the hierarchy that this event is starting in.</span></span> <span data-ttu-id="8afca-114">Se ocorrer um erro, o valor de retorno será negativo.</span><span class="sxs-lookup"><span data-stu-id="8afca-114">If an error occurs, the return value will be negative.</span></span>

## <a name="remarks"></a><span data-ttu-id="8afca-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8afca-115">Remarks</span></span>

<span data-ttu-id="8afca-116">Os eventos definidos pelo usuário agrupam outros eventos de forma que sejam significativos ao programa de destino para que possam ser melhor representados em ferramentas de criação de perfil de desempenho.</span><span class="sxs-lookup"><span data-stu-id="8afca-116">User-defined events group together other events in a way that is meaningful to the target program so that they can be better represented in performance profiling tools.</span></span> <span data-ttu-id="8afca-117">Por exemplo, um evento *desenhar espaçamento* pode ser um número de chamadas Direct3D que lidam com o desenho de uma área de controle em um jogo.</span><span class="sxs-lookup"><span data-stu-id="8afca-117">For example, a *Draw Spaceship* event might bracket a number of Direct3D calls that handle drawing a spaceship in a game.</span></span> <span data-ttu-id="8afca-118">Os eventos podem ser aninhados.</span><span class="sxs-lookup"><span data-stu-id="8afca-118">Events can be nested.</span></span>

<span data-ttu-id="8afca-119">Cada chamada de **D3DPERF_BeginEvent** deve ter uma chamada de **D3DPERF_EndEvent** correspondente.</span><span class="sxs-lookup"><span data-stu-id="8afca-119">Each **D3DPERF_BeginEvent** call should have a matching **D3DPERF_EndEvent** call.</span></span> <span data-ttu-id="8afca-120">Os eventos instantâneos (que não têm outros eventos) devem ser rotulados usando **D3DPERF_SetMarker** em vez de **D3DPERF_BeginEvent** e **D3DPERF_EndEvent**.</span><span class="sxs-lookup"><span data-stu-id="8afca-120">Instantaneous events (which do not bracket other events) should be labeled by using **D3DPERF_SetMarker** rather than by **D3DPERF_BeginEvent** and **D3DPERF_EndEvent**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8afca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8afca-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8afca-122">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="8afca-122">**Target Platform**</span></span> | <span data-ttu-id="8afca-123">Windows</span><span class="sxs-lookup"><span data-stu-id="8afca-123">Windows</span></span> |
| <span data-ttu-id="8afca-124">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="8afca-124">**Header**</span></span> | <span data-ttu-id="8afca-125">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="8afca-125">d3d9.h</span></span> |
| <span data-ttu-id="8afca-126">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="8afca-126">**Library**</span></span> | <span data-ttu-id="8afca-127">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="8afca-127">d3d9.lib</span></span> |
| <span data-ttu-id="8afca-128">**DLL**</span><span class="sxs-lookup"><span data-stu-id="8afca-128">**DLL**</span></span> | <span data-ttu-id="8afca-129">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="8afca-129">d3d9.dll</span></span> |