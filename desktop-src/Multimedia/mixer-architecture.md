---
title: Arquitetura do mixer
description: Arquitetura do mixer
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- áudio multimídia, arquitetura do mixer
- áudio, arquitetura do mixer
- mixers de áudio, arquitetura
- mixers de áudio, linhas de áudio
- linhas de áudio
- mixers de áudio, controles
- áudio de multimídia, controles de mixer
- áudio, controles de mixer
- mixers, linhas de áudio
- mixers, arquitetura
- mixers, controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292135"
---
# <a name="mixer-architecture"></a><span data-ttu-id="9b66b-114">Arquitetura do mixer</span><span class="sxs-lookup"><span data-stu-id="9b66b-114">Mixer Architecture</span></span>

<span data-ttu-id="9b66b-115">O elemento básico da arquitetura do mixer é uma *linha de áudio*.</span><span class="sxs-lookup"><span data-stu-id="9b66b-115">The basic element of the mixer architecture is an *audio line*.</span></span> <span data-ttu-id="9b66b-116">Uma linha de áudio consiste em um ou mais canais de dados provenientes de uma única fonte ou um recurso do sistema.</span><span class="sxs-lookup"><span data-stu-id="9b66b-116">An audio line consists of one or more channels of data originating from a single source or a system resource.</span></span> <span data-ttu-id="9b66b-117">Por exemplo, uma linha de áudio estéreo tem dois canais de dados, mas é considerada uma única linha de áudio porque ela se origina de uma única fonte.</span><span class="sxs-lookup"><span data-stu-id="9b66b-117">For example, a stereo audio line has two data channels, but it is considered a single audio line because it originates from a single source.</span></span>

<span data-ttu-id="9b66b-118">A arquitetura do mixer fornece serviços de roteamento para gerenciar linhas de áudio em um computador.</span><span class="sxs-lookup"><span data-stu-id="9b66b-118">The mixer architecture provides routing services to manage audio lines on a computer.</span></span> <span data-ttu-id="9b66b-119">Você pode usar os serviços de roteamento se tiver dispositivos de hardware e drivers de software adequados instalados.</span><span class="sxs-lookup"><span data-stu-id="9b66b-119">You can use the routing services if you have adequate hardware devices and software drivers installed.</span></span> <span data-ttu-id="9b66b-120">A arquitetura do mixer permite que várias linhas de origem de áudio sejam mapeadas para uma única linha de áudio de destino.</span><span class="sxs-lookup"><span data-stu-id="9b66b-120">The mixer architecture allows several audio source lines to map to a single destination audio line.</span></span>

<span data-ttu-id="9b66b-121">Cada linha de áudio pode ter controles de mixer associados a ela.</span><span class="sxs-lookup"><span data-stu-id="9b66b-121">Each audio line can have mixer controls associated with it.</span></span> <span data-ttu-id="9b66b-122">Um controle de mixer pode executar qualquer número de funções (como o volume de controle), dependendo das características da linha de áudio associada.</span><span class="sxs-lookup"><span data-stu-id="9b66b-122">A mixer control can perform any number of functions (such as control volume), depending on the characteristics of the associated audio line.</span></span>

 

 




