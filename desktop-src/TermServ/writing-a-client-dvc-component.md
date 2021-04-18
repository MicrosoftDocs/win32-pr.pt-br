---
title: Escrevendo um módulo de DVC de cliente
description: Para gravar um módulo de cliente de canal virtual dinâmico (DVC), você deve primeiro implementar e registrar um plug-in de cliente Conexão de Área de Trabalho Remota (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757921"
---
# <a name="writing-a-client-dvc-module"></a><span data-ttu-id="fd020-103">Escrevendo um módulo de DVC de cliente</span><span class="sxs-lookup"><span data-stu-id="fd020-103">Writing a Client DVC Module</span></span>

<span data-ttu-id="fd020-104">Para gravar um módulo de cliente de canal virtual dinâmico (DVC), você deve primeiro implementar e registrar um plug-in de cliente Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="fd020-104">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span> <span data-ttu-id="fd020-105">O plug-in DVC é uma implementação de [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registrada como um objeto Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="fd020-105">The DVC plug-in is an implementation of [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registered as a Component Object Model (COM) object.</span></span>

> [!Note]  
> <span data-ttu-id="fd020-106">O plug-in deve ser implementado em um modelo de Threading livre.</span><span class="sxs-lookup"><span data-stu-id="fd020-106">The plug-in must be implemented in a free-threading model.</span></span> <span data-ttu-id="fd020-107">Não há suporte para implementação de modelo de apartamento.</span><span class="sxs-lookup"><span data-stu-id="fd020-107">Apartment-model implementation is not supported.</span></span>

 

<span data-ttu-id="fd020-108">A seguir está uma lista de interfaces que são implementadas por objetos que são instanciados pelo plug-in do.</span><span class="sxs-lookup"><span data-stu-id="fd020-108">The following is a list of interfaces that are implemented by objects that are instantiated by the plug-in.</span></span>



| <span data-ttu-id="fd020-109">Interface</span><span class="sxs-lookup"><span data-stu-id="fd020-109">Interface</span></span>                                                        | <span data-ttu-id="fd020-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd020-110">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd020-111">**IWTSPlugin**</span><span class="sxs-lookup"><span data-stu-id="fd020-111">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | <span data-ttu-id="fd020-112">Permite que o plug-in do cliente Conexão de Área de Trabalho Remota (RDC) seja carregado pelo cliente Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="fd020-112">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span><br/>                                                                 |
| [<span data-ttu-id="fd020-113">**IWTSListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="fd020-113">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | <span data-ttu-id="fd020-114">Notifica o plug-in do cliente Conexão de Área de Trabalho Remota (RDC) sobre solicitações de entrada em um ouvinte específico.</span><span class="sxs-lookup"><span data-stu-id="fd020-114">Notifies the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span><br/>                                                                             |
| [<span data-ttu-id="fd020-115">**IWTSVirtualChannelCallback**</span><span class="sxs-lookup"><span data-stu-id="fd020-115">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | <span data-ttu-id="fd020-116">Recebe notificações sobre alterações de estado de canal ou dados recebidos.</span><span class="sxs-lookup"><span data-stu-id="fd020-116">Receives notifications about channel state changes or data received.</span></span> <span data-ttu-id="fd020-117">Cada instância dessa interface é associada a uma instância de [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span><span class="sxs-lookup"><span data-stu-id="fd020-117">Each instance of this interface is associated with one instance of [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span></span><br/> |



 

<span data-ttu-id="fd020-118">A seguir está uma lista de interfaces que são implementadas por objetos que são instanciados pelo cliente de Conexão de Área de Trabalho Remota (RDC) e fazem parte da estrutura.</span><span class="sxs-lookup"><span data-stu-id="fd020-118">The following is a list of interfaces that are implemented by objects that are instantiated by the Remote Desktop Connection (RDC) client, and are part of the framework.</span></span>



| <span data-ttu-id="fd020-119">Interface</span><span class="sxs-lookup"><span data-stu-id="fd020-119">Interface</span></span>                                                      | <span data-ttu-id="fd020-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd020-120">Description</span></span>                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd020-121">**IWTSVirtualChannelManager**</span><span class="sxs-lookup"><span data-stu-id="fd020-121">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | <span data-ttu-id="fd020-122">Gerencia todos os plug-ins de cliente Conexão de Área de Trabalho Remota (RDC), ouvintes DVC ou canais virtuais estáticos.</span><span class="sxs-lookup"><span data-stu-id="fd020-122">Manages all Remote Desktop Connection (RDC) client plug-ins, DVC listeners, or static virtual channels.</span></span><br/> |
| [<span data-ttu-id="fd020-123">**IWTSListener**</span><span class="sxs-lookup"><span data-stu-id="fd020-123">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | <span data-ttu-id="fd020-124">Gerencia as definições de configuração de cada ouvinte para a conexão DVC.</span><span class="sxs-lookup"><span data-stu-id="fd020-124">Manages configuration settings for each listener for the DVC connection.</span></span><br/>                                |
| [<span data-ttu-id="fd020-125">**IWTSVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="fd020-125">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | <span data-ttu-id="fd020-126">Controla o estado do canal, bem como gravações no canal.</span><span class="sxs-lookup"><span data-stu-id="fd020-126">Controls the channel state, as well as writes on the channel.</span></span><br/>                                           |



 

<span data-ttu-id="fd020-127">A ilustração a seguir mostra a relação entre o cliente de Conexão de Área de Trabalho Remota (RDC) e o plug-in cliente Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="fd020-127">The following illustration shows the relationship between the Remote Desktop Connection (RDC) client and the Remote Desktop Connection (RDC) client plug-in.</span></span>

![relação entre cliente e plug-in](images/tsclient.png)

 

 





