---
title: Interfaces da camada de depuração
description: As interfaces a seguir são declaradas em d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2020
ms.locfileid: "105752612"
---
# <a name="debug-layer-interfaces"></a><span data-ttu-id="1a588-103">Interfaces de camada de depuração</span><span class="sxs-lookup"><span data-stu-id="1a588-103">Debug Layer interfaces</span></span>

<span data-ttu-id="1a588-104">As interfaces a seguir são definidas em `d3d12sdklayers.h` .</span><span class="sxs-lookup"><span data-stu-id="1a588-104">The following interfaces are defined in `d3d12sdklayers.h`.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1a588-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1a588-105">In this section</span></span>

| <span data-ttu-id="1a588-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="1a588-106">Topic</span></span> | <span data-ttu-id="1a588-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a588-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="1a588-108">**ID3D12Debug**</span><span class="sxs-lookup"><span data-stu-id="1a588-108">**ID3D12Debug**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | <span data-ttu-id="1a588-109">Uma interface de depuração controla as configurações de depuração e valida o estado do pipeline.</span><span class="sxs-lookup"><span data-stu-id="1a588-109">A debug interface controls debug settings and validates pipeline state.</span></span> <span data-ttu-id="1a588-110">Ele só poderá ser usado se a camada de depuração estiver ativada.</span><span class="sxs-lookup"><span data-stu-id="1a588-110">It can only be used if the debug layer is turned on.</span></span> |
| [<span data-ttu-id="1a588-111">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="1a588-111">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | <span data-ttu-id="1a588-112">Adiciona a validação baseada em GPU e a sincronização de fila de comando dependente à camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="1a588-112">Adds GPU-based validation and Dependent Command Queue Synchronization to the debug layer.</span></span> |
| [<span data-ttu-id="1a588-113">**ID3D12Debug2**</span><span class="sxs-lookup"><span data-stu-id="1a588-113">**ID3D12Debug2**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | <span data-ttu-id="1a588-114">Adiciona níveis configuráveis de validação de GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="1a588-114">Adds configurable levels of GPU-Based Validation.</span></span> |
| [<span data-ttu-id="1a588-115">**ID3D12Debug3**</span><span class="sxs-lookup"><span data-stu-id="1a588-115">**ID3D12Debug3**</span></span>](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | <span data-ttu-id="1a588-116">Adiciona à validação baseada em GPU da camada de depuração, à sincronização da fila de comandos dependentes e aos níveis configuráveis da validação baseada em GPU.</span><span class="sxs-lookup"><span data-stu-id="1a588-116">Adds to the debug layer GPU-based validation, Dependent Command Queue Synchronization, and configurable levels of GPU-based validation.</span></span> |
| [<span data-ttu-id="1a588-117">**ID3D12DebugCommandList**</span><span class="sxs-lookup"><span data-stu-id="1a588-117">**ID3D12DebugCommandList**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | <span data-ttu-id="1a588-118">Fornece métodos para monitorar e depurar uma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="1a588-118">Provides methods to monitor and debug a command list.</span></span> |
| [<span data-ttu-id="1a588-119">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="1a588-119">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | <span data-ttu-id="1a588-120">Essa interface permite a modificação de configurações adicionais da camada de depuração da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="1a588-120">This interface enables modification of additional command list debug layer settings.</span></span> |
| [<span data-ttu-id="1a588-121">**ID3D12DebugCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="1a588-121">**ID3D12DebugCommandQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | <span data-ttu-id="1a588-122">Fornece métodos para monitorar e depurar uma fila de comando.</span><span class="sxs-lookup"><span data-stu-id="1a588-122">Provides methods to monitor and debug a command queue.</span></span> |
| [<span data-ttu-id="1a588-123">**ID3D12DebugDevice**</span><span class="sxs-lookup"><span data-stu-id="1a588-123">**ID3D12DebugDevice**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | <span data-ttu-id="1a588-124">Essa interface representa um dispositivo de gráficos para depuração.</span><span class="sxs-lookup"><span data-stu-id="1a588-124">This interface represents a graphics device for debugging.</span></span> |
| [<span data-ttu-id="1a588-125">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="1a588-125">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | <span data-ttu-id="1a588-126">Especifica as configurações da camada de depuração de todo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a588-126">Specifies device-wide debug layer settings.</span></span> |
| [<span data-ttu-id="1a588-127">**ID3D12InfoQueue**</span><span class="sxs-lookup"><span data-stu-id="1a588-127">**ID3D12InfoQueue**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | <span data-ttu-id="1a588-128">Uma interface de fila de informações armazena, recupera e filtra mensagens de depuração.</span><span class="sxs-lookup"><span data-stu-id="1a588-128">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="1a588-129">A fila consiste em uma fila de mensagens, uma pilha de filtro de armazenamento opcional e uma pilha de filtro de recuperação opcional.</span><span class="sxs-lookup"><span data-stu-id="1a588-129">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> |
| [<span data-ttu-id="1a588-130">**ID3D12SharingContract**</span><span class="sxs-lookup"><span data-stu-id="1a588-130">**ID3D12SharingContract**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | <span data-ttu-id="1a588-131">Parte de um contrato entre camadas de diagnóstico D3D11On12 e ferramentas de diagnóstico de gráficos.</span><span class="sxs-lookup"><span data-stu-id="1a588-131">Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="1a588-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a588-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a588-133">Configuração do ambiente programação do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1a588-133">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="1a588-134">Referência da camada de depuração</span><span class="sxs-lookup"><span data-stu-id="1a588-134">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="1a588-135">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="1a588-135">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>