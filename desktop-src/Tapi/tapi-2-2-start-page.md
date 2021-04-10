---
description: A TAPI (interface de programação de aplicativos de telefonia) da Microsoft versão 2,2 (TAPI/C) permite a implementação de aplicativos de comunicação que vão desde o controle de modem básico até centros de chamadas com vários agentes e comutadores.
ms.assetid: 02bfe923-9915-439e-ac7c-a570416d054a
title: Interface de programação de aplicativo de telefonia versão 2,2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0dc158210350979105d765dc939f600f61d8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169818"
---
# <a name="telephony-application-programming-interface-version-22"></a><span data-ttu-id="7c6ce-103">Interface de programação de aplicativo de telefonia versão 2,2</span><span class="sxs-lookup"><span data-stu-id="7c6ce-103">Telephony Application Programming Interface Version 2.2</span></span>

## <a name="purpose"></a><span data-ttu-id="7c6ce-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="7c6ce-104">Purpose</span></span>

<span data-ttu-id="7c6ce-105">A TAPI (interface de programação de aplicativos de telefonia) da Microsoft versão 2,2 (TAPI/C) permite a implementação de aplicativos de comunicação que vão desde o controle de modem básico até centros de chamadas com vários agentes e comutadores.</span><span class="sxs-lookup"><span data-stu-id="7c6ce-105">The Microsoft Telephony Application Programming Interface (TAPI) version 2.2 (TAPI/C) enables implementation of communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="7c6ce-106">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="7c6ce-106">Where applicable</span></span>

<span data-ttu-id="7c6ce-107">Os aplicativos TAPI 2,2 possíveis incluem:</span><span class="sxs-lookup"><span data-stu-id="7c6ce-107">Possible TAPI 2.2 applications include:</span></span>

-   <span data-ttu-id="7c6ce-108">Chamadas de voz básicas na rede telefônica pública comutada (PSTN)</span><span class="sxs-lookup"><span data-stu-id="7c6ce-108">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="7c6ce-109">Aplicativos de Call Center para acompanhamento de vários agentes</span><span class="sxs-lookup"><span data-stu-id="7c6ce-109">Call center applications for tracking multiple agents</span></span>
-   <span data-ttu-id="7c6ce-110">Controle de modem</span><span class="sxs-lookup"><span data-stu-id="7c6ce-110">Modem control</span></span>
-   <span data-ttu-id="7c6ce-111">Controle de PBX</span><span class="sxs-lookup"><span data-stu-id="7c6ce-111">PBX control</span></span>
-   <span data-ttu-id="7c6ce-112">Sistemas de reação a voz interativa (IVR)</span><span class="sxs-lookup"><span data-stu-id="7c6ce-112">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="7c6ce-113">Mensagem de voz</span><span class="sxs-lookup"><span data-stu-id="7c6ce-113">Voice mail</span></span>
-   <span data-ttu-id="7c6ce-114">Controle de dispositivo de telefone detalhado</span><span class="sxs-lookup"><span data-stu-id="7c6ce-114">Detailed phone device control</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7c6ce-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="7c6ce-115">Developer audience</span></span>

<span data-ttu-id="7c6ce-116">A TAPI/C foi projetada para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="7c6ce-116">TAPI/C is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="7c6ce-117">A experiência de desenvolvimento com telecomunicações ou outros aplicativos de telefonia é útil, mas não é necessária.</span><span class="sxs-lookup"><span data-stu-id="7c6ce-117">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7c6ce-118">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="7c6ce-118">Run-time requirements</span></span>

<span data-ttu-id="7c6ce-119">A TAPI versão 2,2 permite o desenvolvimento de aplicativos de comunicação para os sistemas operacionais Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98 e Windows 95.</span><span class="sxs-lookup"><span data-stu-id="7c6ce-119">TAPI version 2.2 enables development of communications applications for the Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, and Windows 95.</span></span> <span data-ttu-id="7c6ce-120">Para obter mais informações sobre quais sistemas operacionais dão suporte a uma função específica, consulte a seção requisitos da documentação para essa função.</span><span class="sxs-lookup"><span data-stu-id="7c6ce-120">For more information about which operating systems support a particular function, see the Requirements section of the documentation for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7c6ce-121">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7c6ce-121">In this section</span></span>



| <span data-ttu-id="7c6ce-122">Tópico</span><span class="sxs-lookup"><span data-stu-id="7c6ce-122">Topic</span></span>                                          | <span data-ttu-id="7c6ce-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="7c6ce-123">Description</span></span>                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c6ce-124">Visão geral</span><span class="sxs-lookup"><span data-stu-id="7c6ce-124">Overview</span></span>](tapi-2-2-overview.md)<br/>   | <span data-ttu-id="7c6ce-125">Informações gerais sobre arquitetura e componentes TAPI.</span><span class="sxs-lookup"><span data-stu-id="7c6ce-125">General information about TAPI architecture and components.</span></span><br/>                                            |
| [<span data-ttu-id="7c6ce-126">Referência</span><span class="sxs-lookup"><span data-stu-id="7c6ce-126">Reference</span></span>](tapi-2-2-reference.md)<br/> | <span data-ttu-id="7c6ce-127">Documentação de funções, estruturas, mensagens, constantes e classes de dispositivo disponíveis no TAPI 2,2.</span><span class="sxs-lookup"><span data-stu-id="7c6ce-127">Documentation of functions, structures, messages, constants, and device classes available in TAPI 2.2.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7c6ce-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c6ce-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c6ce-129">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7c6ce-129">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="7c6ce-130">Provedores de serviços TAPI</span><span class="sxs-lookup"><span data-stu-id="7c6ce-130">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

