---
description: O provedor WMI do coletor de eventos de inicialização fornece acesso a informações de conexão e configuração para o recurso de coleta de eventos de instalação e inicialização no Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Provedor WMI do coletor de eventos de inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826110"
---
# <a name="boot-event-collector-wmi-provider"></a><span data-ttu-id="641d7-103">Provedor WMI do coletor de eventos de inicialização</span><span class="sxs-lookup"><span data-stu-id="641d7-103">Boot Event Collector WMI Provider</span></span>

## <a name="purpose"></a><span data-ttu-id="641d7-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="641d7-104">Purpose</span></span>

<span data-ttu-id="641d7-105">O provedor WMI do coletor de eventos de inicialização fornece acesso a informações de conexão e configuração para o recurso de coleta de eventos de instalação e inicialização no Windows Server.</span><span class="sxs-lookup"><span data-stu-id="641d7-105">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span> <span data-ttu-id="641d7-106">Isso permite que você exiba uma lista das conexões atuais e o histórico de conexão entre um servidor de coletor e seus computadores de destino.</span><span class="sxs-lookup"><span data-stu-id="641d7-106">This allows you to view a list of the current connections and the connection history between a collector server and its target computers.</span></span> <span data-ttu-id="641d7-107">Além disso, esse provedor permite que você gerencie a configuração de um servidor coletor.</span><span class="sxs-lookup"><span data-stu-id="641d7-107">In addition, this provider allows you to manage the configuration of a collector server.</span></span>

> [!Note]  
> <span data-ttu-id="641d7-108">O provedor WMI do coletor de eventos de inicialização é implementado no BEvtCol.exe.</span><span class="sxs-lookup"><span data-stu-id="641d7-108">The Boot Event Collector WMI provider is implemented in BEvtCol.exe.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="641d7-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="641d7-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="641d7-110">**TargetForwarding**</span><span class="sxs-lookup"><span data-stu-id="641d7-110">**TargetForwarding**</span></span>](targetforwarding.md)
</dt> <dd>

<span data-ttu-id="641d7-111">Recupera os dados de encaminhamento de um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="641d7-111">Retrieves forwarding data from a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="641d7-112">**TargetForwardingDestination**</span><span class="sxs-lookup"><span data-stu-id="641d7-112">**TargetForwardingDestination**</span></span>](targetforwardingdestination.md)
</dt> <dd>

<span data-ttu-id="641d7-113">Os destinos conhecidos que contêm os dados coletados.</span><span class="sxs-lookup"><span data-stu-id="641d7-113">The known destinations containing the collected data.</span></span> <span data-ttu-id="641d7-114">Disponível somente se o coletor estiver em execução com o log de status habilitado.</span><span class="sxs-lookup"><span data-stu-id="641d7-114">Available only if the collector is running with the status log enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="641d7-115">**TargetForwardingHistory**</span><span class="sxs-lookup"><span data-stu-id="641d7-115">**TargetForwardingHistory**</span></span>](targetforwardinghistory.md)
</dt> <dd>

<span data-ttu-id="641d7-116">O histórico recente de alterações nos dados de encaminhamento de um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="641d7-116">The recent history of changes to the forwarding data for a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="641d7-117">**Control**</span><span class="sxs-lookup"><span data-stu-id="641d7-117">**Control**</span></span>](control.md)
</dt> <dd>

<span data-ttu-id="641d7-118">Controle da instância do coletor.</span><span class="sxs-lookup"><span data-stu-id="641d7-118">Control of the collector instance.</span></span> <span data-ttu-id="641d7-119">Requer os privilégios de administrador (BA).</span><span class="sxs-lookup"><span data-stu-id="641d7-119">Requires the Administrator (BA) privileges.</span></span>

</dd> </dl>

 

 



