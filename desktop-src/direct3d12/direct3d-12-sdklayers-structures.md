---
title: Estruturas da camada de depuração
description: As seguintes estruturas são declaradas em d3d12sdklayers. h.
ms.assetid: FE8796A7-98D1-4333-8755-2A47567560B3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573d49d34c4432796ebac68ce004f265259b9eb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105791638"
---
# <a name="debug-layer-structures"></a><span data-ttu-id="88943-103">Estruturas da camada de depuração</span><span class="sxs-lookup"><span data-stu-id="88943-103">Debug Layer Structures</span></span>

<span data-ttu-id="88943-104">As seguintes estruturas são declaradas em d3d12sdklayers. h.</span><span class="sxs-lookup"><span data-stu-id="88943-104">The following structures are declared in d3d12sdklayers.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="88943-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="88943-105">In this section</span></span>



| <span data-ttu-id="88943-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="88943-106">Topic</span></span>                                                                                                                                      | <span data-ttu-id="88943-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="88943-107">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88943-108">**\_Configurações de \_ \_ \_ \_ validação baseadas em GPU \_ da \_ lista de comandos de depuração do D3D12**</span><span class="sxs-lookup"><span data-stu-id="88943-108">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)<br/> | <span data-ttu-id="88943-109">Descreve as configurações de lista de comandos usadas pela validação de GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="88943-109">Describes per-command-list settings used by GPU-Based Validation.</span></span> <br/>                                                        |
| [<span data-ttu-id="88943-110">**\_Configurações de \_ \_ \_ validação baseadas em \_ GPU \_ do dispositivo de depuração D3D12**</span><span class="sxs-lookup"><span data-stu-id="88943-110">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)<br/>              | <span data-ttu-id="88943-111">Descreve as configurações usadas pela validação de GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="88943-111">Describes settings used by GPU-Based Validation.</span></span> <br/>                                                                         |
| [<span data-ttu-id="88943-112">**\_Fator de \_ \_ desempenho de lentidão da GPU do dispositivo \_ de \_ depuração D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="88943-112">**D3D12\_DEBUG\_DEVICE\_GPU\_SLOWDOWN\_PERFORMANCE\_FACTOR**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_slowdown_performance_factor)<br/>          | <span data-ttu-id="88943-113">Descreve a quantidade de lentidão artificial inserida pelo dispositivo de depuração para simular adaptadores gráficos de baixo desempenho.</span><span class="sxs-lookup"><span data-stu-id="88943-113">Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.</span></span><br/> |
| [<span data-ttu-id="88943-114">**\_Filtro de \_ fila de informações de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="88943-114">**D3D12\_INFO\_QUEUE\_FILTER**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)<br/>                                                                   | <span data-ttu-id="88943-115">Filtro de mensagem de depuração; contém uma lista de tipos de mensagem para permitir ou negar.</span><span class="sxs-lookup"><span data-stu-id="88943-115">Debug message filter; contains a lists of message types to allow or deny.</span></span><br/>                                                 |
| [<span data-ttu-id="88943-116">**D3D12 \_ de \_ filtro de fila de informações \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="88943-116">**D3D12\_INFO\_QUEUE\_FILTER\_DESC**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter_desc)<br/>                                                        | <span data-ttu-id="88943-117">Permitir ou negar que determinados tipos de mensagens passem por um filtro.</span><span class="sxs-lookup"><span data-stu-id="88943-117">Allow or deny certain types of messages to pass through a filter.</span></span><br/>                                                         |
| [<span data-ttu-id="88943-118">**\_Mensagem D3D12**</span><span class="sxs-lookup"><span data-stu-id="88943-118">**D3D12\_MESSAGE**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_message)<br/>                                                                                         | <span data-ttu-id="88943-119">Uma mensagem de depuração na fila de informações.</span><span class="sxs-lookup"><span data-stu-id="88943-119">A debug message in the Information Queue.</span></span><br/>                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="88943-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88943-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88943-121">Configuração do ambiente programação do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="88943-121">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="88943-122">Referência da camada de depuração</span><span class="sxs-lookup"><span data-stu-id="88943-122">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="88943-123">Referência do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="88943-123">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





