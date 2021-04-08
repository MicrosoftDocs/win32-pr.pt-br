---
description: Um monitor é uma DLL (biblioteca de vínculo dinâmico) que examina as capturas em tempo real do tráfego de rede.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920997"
---
# <a name="monitors"></a><span data-ttu-id="62d37-103">Monitores</span><span class="sxs-lookup"><span data-stu-id="62d37-103">Monitors</span></span>

<span data-ttu-id="62d37-104">Um monitor é uma DLL (biblioteca de vínculo dinâmico) que examina as capturas em tempo real do tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="62d37-104">A monitor is a dynamic-link library (DLL) that examines real-time captures of network traffic.</span></span> <span data-ttu-id="62d37-105">Ele procura condições predefinidas e gera eventos quando essas condições são detectadas.</span><span class="sxs-lookup"><span data-stu-id="62d37-105">It searches for pre-defined conditions and then generates events when those conditions are detected.</span></span> <span data-ttu-id="62d37-106">Por exemplo, um evento pode ser acionado quando uma interrupção de rede é tentada, quando uma estação de trabalho não autorizada está distribuindo endereços IP ou quando um roteador falha.</span><span class="sxs-lookup"><span data-stu-id="62d37-106">For example, an event may be fired when a network break-in is attempted, when a rogue workstation is handing out IP addresses, or when a router fails.</span></span>

> [!Note]  
> <span data-ttu-id="62d37-107">Se você precisar executar análises detalhadas em dados de rede que exijam uma análise após a captura, você deverá usar aplicativos de [*especialista*](e.md) e [*analisador*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="62d37-107">If you need to perform detailed analyses on network data that requires a post-capture analysis, you must use [*expert*](e.md) and [*parser*](p.md) applications.</span></span>

 

<span data-ttu-id="62d37-108">O [*serviço de controle de monitor*](m.md) (MCSVC) fornece a estrutura para gerenciar seus monitores.</span><span class="sxs-lookup"><span data-stu-id="62d37-108">The [*Monitor Control Service*](m.md) (MCSVC) provides the framework for managing your monitors.</span></span> <span data-ttu-id="62d37-109">Ele fornece funções para carregar as DLLs de monitor e uma interface de comunicação para a ferramenta de controle de monitor para que você possa criar, configurar, iniciar, parar e desabilitar várias instâncias de seus monitores.</span><span class="sxs-lookup"><span data-stu-id="62d37-109">It provides functions to load the monitor DLLs, and a communications interface to the Monitor Control Tool so that you can create, configure, start, stop, and disable multiple instances of your monitors.</span></span>

<span data-ttu-id="62d37-110">Os monitores são executados em dois threads de execução.</span><span class="sxs-lookup"><span data-stu-id="62d37-110">Monitors run in two threads of execution.</span></span> <span data-ttu-id="62d37-111">O MCSVC fornece o primeiro thread, que fornece controle direto do monitor.</span><span class="sxs-lookup"><span data-stu-id="62d37-111">The MCSVC provides the first thread, which provides direct control of the monitor.</span></span> <span data-ttu-id="62d37-112">O segundo thread é fornecido pelo NPP ( [*provedor de pacotes de rede*](n.md) ), que fornece uma maneira de passar os dados de rede capturados, as estatísticas e o status da captura do NPP de volta para o monitor.</span><span class="sxs-lookup"><span data-stu-id="62d37-112">The second thread is provided by the [*network packet provider*](n.md) (NPP), which provides a way to pass the captured network data, statistics, and the status of the capture from the NPP back to the monitor.</span></span>

<span data-ttu-id="62d37-113">Mais de uma instância do mesmo monitor pode existir para cada interface NPP de tempo de execução usada para capturar dados.</span><span class="sxs-lookup"><span data-stu-id="62d37-113">More than one instance of the same monitor can exist for each run-time NPP interface used to capture data.</span></span>

 

 



