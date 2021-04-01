---
description: Um TSP (provedor de serviços de telefonia) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Provedores de serviços de telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836952"
---
# <a name="telephony-service-providers"></a><span data-ttu-id="aa2e1-103">Provedores de serviços de telefonia</span><span class="sxs-lookup"><span data-stu-id="aa2e1-103">Telephony Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="aa2e1-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="aa2e1-104">Purpose</span></span>

<span data-ttu-id="aa2e1-105">Um TSP (provedor de serviços de telefonia) é uma DLL (biblioteca de vínculo dinâmico) que dá suporte ao controle de dispositivo de comunicação por meio de um conjunto de funções de serviço exportadas.</span><span class="sxs-lookup"><span data-stu-id="aa2e1-105">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="aa2e1-106">Um aplicativo TAPI usa comandos padronizados, a TAPI passa informações para o provedor de serviços de telefonia e o TSP lida com os comandos específicos que devem ser trocados pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa2e1-106">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="aa2e1-107">Um TSP deve estar em conformidade com a TSPI (interface do provedor de serviços de telefonia) para funcionar como um provedor de serviços no ambiente de telefonia da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aa2e1-107">A TSP must conform to the Telephony Service Provider Interface (TSPI) to function as a service provider within the Microsoft Telephony environment.</span></span> <span data-ttu-id="aa2e1-108">TSPI define as funções externas expostas por um provedor de serviços de telefonia fornecido com equipamentos de comunicação.</span><span class="sxs-lookup"><span data-stu-id="aa2e1-108">TSPI defines the external functions exposed by a telephony service provider supplied with communications equipment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="aa2e1-109">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="aa2e1-109">Developer audience</span></span>

<span data-ttu-id="aa2e1-110">Você pode gravar aplicativos habilitados para TAPI em várias linguagens, incluindo Java, Visual Basic e C/C++.</span><span class="sxs-lookup"><span data-stu-id="aa2e1-110">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="aa2e1-111">A experiência de desenvolvimento anterior com telecomunicações ou outros aplicativos de telefonia é útil, mas não é necessária.</span><span class="sxs-lookup"><span data-stu-id="aa2e1-111">Previous development experience with telecommunications or other telephony applications is helpful but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="aa2e1-112">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="aa2e1-112">Run-time requirements</span></span>

<span data-ttu-id="aa2e1-113">O TSPI permite o desenvolvimento de TSPs para todas as versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="aa2e1-113">TSPI enables development of TSPs for all versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aa2e1-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="aa2e1-114">In this section</span></span>



| <span data-ttu-id="aa2e1-115">Tópico</span><span class="sxs-lookup"><span data-stu-id="aa2e1-115">Topic</span></span>                                                                | <span data-ttu-id="aa2e1-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa2e1-116">Description</span></span>                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="aa2e1-117">Visão geral</span><span class="sxs-lookup"><span data-stu-id="aa2e1-117">Overview</span></span>](about-the-telephony-service-provider-tsp-.md)<br/> | <span data-ttu-id="aa2e1-118">Informações gerais sobre a arquitetura e os componentes do TSPI.</span><span class="sxs-lookup"><span data-stu-id="aa2e1-118">General information about TSPI's architecture and components.</span></span><br/> |
| [<span data-ttu-id="aa2e1-119">Referência</span><span class="sxs-lookup"><span data-stu-id="aa2e1-119">Reference</span></span>](tspi-reference.md)<br/>                           | <span data-ttu-id="aa2e1-120">Documentação para as interfaces TSPI.</span><span class="sxs-lookup"><span data-stu-id="aa2e1-120">Documentation for the TSPI interfaces.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="aa2e1-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa2e1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa2e1-122">Visão geral de telefonia da Microsoft</span><span class="sxs-lookup"><span data-stu-id="aa2e1-122">Microsoft Telephony Overview</span></span>](./microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="aa2e1-123">Provedores de serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="aa2e1-123">Media Service Providers</span></span>](./media-service-providers-start-page.md)
</dt> <dt>

[<span data-ttu-id="aa2e1-124">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="aa2e1-124">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="aa2e1-125">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="aa2e1-125">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> </dl>

 

