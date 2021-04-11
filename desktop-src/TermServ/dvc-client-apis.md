---
title: APIs de cliente do DVC
description: As APIs de cliente de canal virtual dinâmico (DVC) são implementadas especificamente para o cliente de Conexão de Área de Trabalho Remota (RDC) da conexão.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292060"
---
# <a name="dvc-client-apis"></a><span data-ttu-id="6270e-103">APIs de cliente do DVC</span><span class="sxs-lookup"><span data-stu-id="6270e-103">DVC Client APIs</span></span>

<span data-ttu-id="6270e-104">As APIs de cliente de canal virtual dinâmico (DVC) são implementadas especificamente para o cliente de Conexão de Área de Trabalho Remota (RDC) da conexão.</span><span class="sxs-lookup"><span data-stu-id="6270e-104">The dynamic virtual channel (DVC) client APIs are implemented specifically for the Remote Desktop Connection (RDC) client of the connection.</span></span> <span data-ttu-id="6270e-105">Algumas das APIs são implementadas pela estrutura DVC e algumas são implementadas pelo desenvolvedor de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="6270e-105">Some of the APIs are implemented by the DVC framework, and some are implemented by the plug-in developer.</span></span> <span data-ttu-id="6270e-106">Algumas das APIs são usadas para dar suporte ao plug-in de cliente Conexão de Área de Trabalho Remota (RDC) e não estão diretamente relacionadas ao transporte de dados.</span><span class="sxs-lookup"><span data-stu-id="6270e-106">Some of the APIs are used to support the Remote Desktop Connection (RDC) client plug-in, and are not directly related to data transport.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6270e-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6270e-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="6270e-108">**IWTSPlugin**</span><span class="sxs-lookup"><span data-stu-id="6270e-108">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

<span data-ttu-id="6270e-109">Permite que o plug-in do cliente Conexão de Área de Trabalho Remota (RDC) seja carregado pelo cliente Conexão de Área de Trabalho Remota (RDC).</span><span class="sxs-lookup"><span data-stu-id="6270e-109">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="6270e-110">**IWTSListener**</span><span class="sxs-lookup"><span data-stu-id="6270e-110">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

<span data-ttu-id="6270e-111">Gerencia definições de configuração para cada ouvinte para a conexão de canal virtual dinâmico (DVC).</span><span class="sxs-lookup"><span data-stu-id="6270e-111">Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6270e-112">**IWTSListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="6270e-112">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

<span data-ttu-id="6270e-113">Usado para notificar o plug-in do cliente Conexão de Área de Trabalho Remota (RDC) sobre solicitações de entrada em um ouvinte específico.</span><span class="sxs-lookup"><span data-stu-id="6270e-113">Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span>

</dd> <dt>

[<span data-ttu-id="6270e-114">**IWTSVirtualChannelManager**</span><span class="sxs-lookup"><span data-stu-id="6270e-114">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

<span data-ttu-id="6270e-115">Gerencia todos os plug-ins de cliente Conexão de Área de Trabalho Remota (RDC) e ouvintes de canal virtual dinâmico (DVC).</span><span class="sxs-lookup"><span data-stu-id="6270e-115">Manages all Remote Desktop Connection (RDC) client plug-ins and dynamic virtual channel (DVC) listeners.</span></span>

</dd> <dt>

[<span data-ttu-id="6270e-116">**IWTSVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="6270e-116">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

<span data-ttu-id="6270e-117">Usado para controlar o estado do canal e grava no canal.</span><span class="sxs-lookup"><span data-stu-id="6270e-117">Used to control the channel state, and writes on the channel.</span></span>

</dd> <dt>

[<span data-ttu-id="6270e-118">**IWTSVirtualChannelCallback**</span><span class="sxs-lookup"><span data-stu-id="6270e-118">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

<span data-ttu-id="6270e-119">Recebe notificações sobre alterações de estado de canal ou dados recebidos.</span><span class="sxs-lookup"><span data-stu-id="6270e-119">Receives notifications about channel state changes or data received.</span></span>

</dd> <dt>

[<span data-ttu-id="6270e-120">**IWTSVirtualChannelCallback2**</span><span class="sxs-lookup"><span data-stu-id="6270e-120">**IWTSVirtualChannelCallback2**</span></span>](iwtsvirtualchannelcallback2.md)
</dt> <dd>

<span data-ttu-id="6270e-121">Não há suporte para essa interface.</span><span class="sxs-lookup"><span data-stu-id="6270e-121">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="6270e-122">**VirtualChannelGetInstance**</span><span class="sxs-lookup"><span data-stu-id="6270e-122">**VirtualChannelGetInstance**</span></span>](virtualchannelgetinstance.md)
</dt> <dd>

<span data-ttu-id="6270e-123">Chamado para que o plug-in crie uma instância da interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos os plug-ins implementados pela dll.</span><span class="sxs-lookup"><span data-stu-id="6270e-123">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

</dd> </dl>

 

 




