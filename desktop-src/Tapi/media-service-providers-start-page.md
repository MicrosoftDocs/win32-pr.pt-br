---
description: Um MSP (provedor de serviços de mídia) permite que um aplicativo controle a mídia de um mecanismo de transporte específico.
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: Provedores de serviços de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105810458"
---
# <a name="media-service-providers"></a><span data-ttu-id="7afde-103">Provedores de serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="7afde-103">Media Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="7afde-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="7afde-104">Purpose</span></span>

<span data-ttu-id="7afde-105">Um MSP (provedor de serviços de mídia) permite que um aplicativo controle a mídia de um mecanismo de transporte específico.</span><span class="sxs-lookup"><span data-stu-id="7afde-105">A media service provider (MSP) enables an application to control media for a particular transport mechanism.</span></span> <span data-ttu-id="7afde-106">Um MSP é sempre emparelhado com um provedor de serviços de telefonia (TSP).</span><span class="sxs-lookup"><span data-stu-id="7afde-106">An MSP is always paired with a Telephony Service Provider (TSP).</span></span>

<span data-ttu-id="7afde-107">A MSPI (interface do provedor de serviços de mídia) é um conjunto de interfaces e métodos implementados por um MSP para permitir um controle de aplicativo sobre o transporte de mídia durante uma sessão de comunicações.</span><span class="sxs-lookup"><span data-stu-id="7afde-107">The Media Service Provider Interface (MSPI) is a set of interfaces and methods implemented by an MSP to allow an application control over media transport during a communications session.</span></span> <span data-ttu-id="7afde-108">Um MSP manipula os mecanismos específicos do dispositivo e do protocolo, necessários para aplicar esses controles e se comunica com seu TSP ou aplicativo emparelhado por meio do uso dos métodos fornecidos no MSPI.</span><span class="sxs-lookup"><span data-stu-id="7afde-108">An MSP handles the device-specific and protocol-specific mechanisms required to enact these controls, and communicates with its paired TSP or an application through use of the methods provided in the MSPI.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7afde-109">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="7afde-109">Developer audience</span></span>

<span data-ttu-id="7afde-110">É necessário ter familiaridade com com.</span><span class="sxs-lookup"><span data-stu-id="7afde-110">Familiarity with COM is required.</span></span> <span data-ttu-id="7afde-111">A experiência de desenvolvimento com telecomunicações ou outros aplicativos de telefonia é útil, mas não é necessária.</span><span class="sxs-lookup"><span data-stu-id="7afde-111">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7afde-112">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="7afde-112">Run-time requirements</span></span>

<span data-ttu-id="7afde-113">O MSPI permite o desenvolvimento de provedores de serviço de mídia para determinados protocolos ou dispositivos em execução em sistemas operacionais Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7afde-113">MSPI enables development of media service providers for particular protocols or devices running on Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7afde-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7afde-114">In this section</span></span>



| <span data-ttu-id="7afde-115">Tópico</span><span class="sxs-lookup"><span data-stu-id="7afde-115">Topic</span></span>                                                                       | <span data-ttu-id="7afde-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="7afde-116">Description</span></span>                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="7afde-117">Visão geral</span><span class="sxs-lookup"><span data-stu-id="7afde-117">Overview</span></span>](about-the-media-service-provider-msp-.md)<br/>            | <span data-ttu-id="7afde-118">Informações gerais sobre a arquitetura e os componentes do MSP.</span><span class="sxs-lookup"><span data-stu-id="7afde-118">General information about MSP architecture and components.</span></span><br/> |
| [<span data-ttu-id="7afde-119">Referência</span><span class="sxs-lookup"><span data-stu-id="7afde-119">Reference</span></span>](media-service-provider-interface-mspi-reference.md)<br/> | <span data-ttu-id="7afde-120">Documentação para as interfaces MSPI.</span><span class="sxs-lookup"><span data-stu-id="7afde-120">Documentation for the MSPI interfaces.</span></span><br/>                     |



 

## <a name="related-topics"></a><span data-ttu-id="7afde-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7afde-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7afde-122">Visão geral de telefonia da Microsoft</span><span class="sxs-lookup"><span data-stu-id="7afde-122">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="7afde-123">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7afde-123">TAPI 3.1</span></span>](tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="7afde-124">Provedores de serviços de telefonia</span><span class="sxs-lookup"><span data-stu-id="7afde-124">Telephony Service Providers</span></span>](./telephony-service-providers-start-page.md)
</dt> </dl>

 

