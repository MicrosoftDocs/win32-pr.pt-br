---
description: O Gerenciador de sincronização fornece uma tecnologia padrão centralizada para sincronizar arquivos para uso offline em um computador móvel ou um computador conectado a uma rede de área local.
title: gerenciador de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989009"
---
# <a name="synchronization-manager"></a><span data-ttu-id="7026a-103">gerenciador de sincronização</span><span class="sxs-lookup"><span data-stu-id="7026a-103">Synchronization Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="7026a-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="7026a-104">Purpose</span></span>

<span data-ttu-id="7026a-105">O Gerenciador de sincronização fornece uma tecnologia padrão centralizada para sincronizar arquivos para uso offline em um computador móvel ou um computador conectado a uma rede de área local.</span><span class="sxs-lookup"><span data-stu-id="7026a-105">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a mobile computer or a computer connected to a local area network.</span></span> <span data-ttu-id="7026a-106">Junto com as funções de conectividade, as notificações (serviço de notificação de eventos do sistema) e o cache do lado do cliente, o Gerenciador de sincronização fornece uma infraestrutura para dar suporte à computação móvel.</span><span class="sxs-lookup"><span data-stu-id="7026a-106">Together with the connectivity functions, notifications (System Event Notification Service), and client side caching, the Synchronization Manager provides an infrastructure to support mobile computing.</span></span> <span data-ttu-id="7026a-107">Em vez de cada aplicativo que implementa sua própria tecnologia para armazenar em cache e sincronizar recursos de rede para uso local, o sistema operacional fornece um modelo integrado que todos os aplicativos podem usar.</span><span class="sxs-lookup"><span data-stu-id="7026a-107">Instead of each application implementing its own technology to cache and synchronize network resources for local use, the operating system provides an integrated model that all applications can use.</span></span> <span data-ttu-id="7026a-108">Os arquivos são sincronizados independentemente do protocolo.</span><span class="sxs-lookup"><span data-stu-id="7026a-108">Files are synchronized independent of the protocol.</span></span> <span data-ttu-id="7026a-109">Por exemplo, um programa de email pode transferir suas mensagens usando SMTP, NMTP ou POP3, enquanto um navegador pode usar HTTP e um banco de dados pode usar RPC (chamada de procedimento remoto).</span><span class="sxs-lookup"><span data-stu-id="7026a-109">For example, an email program can transfer its messages using SMTP, NMTP, or POP3, while a browser can use HTTP, and a database can use remote procedure call (RPC) (RPC).</span></span> <span data-ttu-id="7026a-110">Os desenvolvedores podem usar a interface comum para o Gerenciador de sincronização em seus aplicativos para sincronizar arquivos entre o computador local do usuário e o armazenamento de rede.</span><span class="sxs-lookup"><span data-stu-id="7026a-110">Developers can use the common interface to the Synchronization Manager in their applications to synchronize files between the user's local computer and network storage.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="7026a-111">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="7026a-111">Where applicable</span></span>

<span data-ttu-id="7026a-112">O Gerenciador de sincronização destina-se a aplicativos que são executados principalmente em computadores móveis.</span><span class="sxs-lookup"><span data-stu-id="7026a-112">The Synchronization Manager is intended for applications that run primarily on mobile computers.</span></span> <span data-ttu-id="7026a-113">Os aplicativos executados em computadores conectados a redes locais de alta latência também podem se beneficiar do uso do Gerenciador de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7026a-113">Applications that run on computers connected to high latency local area networks may also benefit from using the Synchronization Manager.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="7026a-114">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="7026a-114">Developer audience</span></span>

<span data-ttu-id="7026a-115">Este documento destina-se a desenvolvedores de software que desenvolvem aplicativos para computação móvel e redes locais de alta latência.</span><span class="sxs-lookup"><span data-stu-id="7026a-115">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="7026a-116">Este documento fornece uma referência completa de todas as partes do Gerenciador de sincronização, incluindo os métodos e as interfaces para o Gerenciador de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7026a-116">This document provides a complete reference of all parts of the Synchronization Manager including the methods and interfaces to the Synchronization Manager.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7026a-117">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="7026a-117">Run-time requirements</span></span>

<span data-ttu-id="7026a-118">Requer o Windows Server 2003, o Windows XP, o Windows 2000 ou o Windows Millennium Edition (Windows me).</span><span class="sxs-lookup"><span data-stu-id="7026a-118">Requires Windows Server 2003, Windows XP, Windows 2000, or Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="7026a-119">Também disponível como um pacote redistribuível para Microsoft Windows NT 4,0, Windows 98 e Windows 95.</span><span class="sxs-lookup"><span data-stu-id="7026a-119">Also available as a redistributable for Microsoft Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7026a-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7026a-120">In this section</span></span>



| <span data-ttu-id="7026a-121">Tópico</span><span class="sxs-lookup"><span data-stu-id="7026a-121">Topic</span></span>                                                                                       | <span data-ttu-id="7026a-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="7026a-122">Description</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7026a-123">Sobre o Gerenciador de sincronização</span><span class="sxs-lookup"><span data-stu-id="7026a-123">About Synchronization Manager</span></span>](syncmgr-about.md)<br/>                               | <span data-ttu-id="7026a-124">O Gerenciador de sincronização fornece uma tecnologia padrão centralizada para sincronizar arquivos para uso offline em um computador local.</span><span class="sxs-lookup"><span data-stu-id="7026a-124">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a local computer.</span></span><br/>     |
| [<span data-ttu-id="7026a-125">Configurações de computação móvel</span><span class="sxs-lookup"><span data-stu-id="7026a-125">Mobile Computing Configurations</span></span>](syncmgr-mobile-computing-configs.md)<br/>          | <span data-ttu-id="7026a-126">Os aplicativos podem usar o sincronização Manager para manter arquivos e recursos armazenados em cache localmente e sincronizados em computadores móveis e de desktop.</span><span class="sxs-lookup"><span data-stu-id="7026a-126">Applications can use Sychronization Manager to keep files and resources cached locally and synchronized on mobile and desktop computers.</span></span><br/> |
| [<span data-ttu-id="7026a-127">Cenários de aplicativos</span><span class="sxs-lookup"><span data-stu-id="7026a-127">Application Scenarios</span></span>](syncmgr-app-scenarios.md)<br/>                               | <span data-ttu-id="7026a-128">Aplicativos e serviços que podem usar o Synchronization Manager.</span><span class="sxs-lookup"><span data-stu-id="7026a-128">Applications and services that can use Synchronization Manager.</span></span><br/>                                                                          |
| [<span data-ttu-id="7026a-129">Arquitetura do Gerenciador de sincronização</span><span class="sxs-lookup"><span data-stu-id="7026a-129">Synchronization Manager Architecture</span></span>](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [<span data-ttu-id="7026a-130">Usando o Gerenciador de sincronização de um programa</span><span class="sxs-lookup"><span data-stu-id="7026a-130">Using Synchronization Manager from a Program</span></span>](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [<span data-ttu-id="7026a-131">Referência do Synchronization Manager</span><span class="sxs-lookup"><span data-stu-id="7026a-131">Synchronization Manager Reference</span></span>](syncmgr-reference.md)<br/>                       | <span data-ttu-id="7026a-132">Os seguintes elementos de programação compõem a API para o Gerenciador de sincronização.</span><span class="sxs-lookup"><span data-stu-id="7026a-132">The following programming elements make up the API for Synchronization Manager.</span></span><br/>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="7026a-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7026a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7026a-134">Sobre o serviço de notificação de eventos do sistema</span><span class="sxs-lookup"><span data-stu-id="7026a-134">About System Event Notification Service</span></span>](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
