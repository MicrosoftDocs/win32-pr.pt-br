---
title: Interfaces do provedor de protocolo RDP
description: Interfaces com suporte da API do provedor de protocolo RDP.
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915860"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a><span data-ttu-id="2c669-103">Interfaces do provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="2c669-103">Remote Desktop Protocol Provider Interfaces</span></span>

<span data-ttu-id="2c669-104">As interfaces a seguir têm suporte da API do provedor de protocolo RDP.</span><span class="sxs-lookup"><span data-stu-id="2c669-104">The following interfaces are supported by the Remote Desktop Protocol Provider API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2c669-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2c669-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="2c669-106">**IWRdsProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="2c669-106">**IWRdsProtocolConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

<span data-ttu-id="2c669-107">Expõe métodos chamados pelo serviço de Serviços de Área de Trabalho Remota para configurar uma conexão de cliente.</span><span class="sxs-lookup"><span data-stu-id="2c669-107">Exposes methods called by the Remote Desktop Services service to configure a client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-108">**IWRdsProtocolConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="2c669-108">**IWRdsProtocolConnectionCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

<span data-ttu-id="2c669-109">Expõe métodos que fornecem informações sobre o status de uma conexão de cliente e que executam ações para o cliente.</span><span class="sxs-lookup"><span data-stu-id="2c669-109">Exposes methods that provide information about the status of a client connection and that perform actions for the client.</span></span> <span data-ttu-id="2c669-110">Essa interface é implementada pelo serviço de Serviços de Área de Trabalho Remota e chamada pelo protocolo.</span><span class="sxs-lookup"><span data-stu-id="2c669-110">This interface is implemented by the Remote Desktop Services service and called by the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-111">**IWRdsProtocolLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="2c669-111">**IWRdsProtocolLicenseConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

<span data-ttu-id="2c669-112">Expõe métodos usados pelo serviço de Serviços de Área de Trabalho Remota para executar o handshake de licenciamento durante uma sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="2c669-112">Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-113">**IWRdsProtocolListener**</span><span class="sxs-lookup"><span data-stu-id="2c669-113">**IWRdsProtocolListener**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

<span data-ttu-id="2c669-114">Expõe métodos que solicitam que o protocolo inicie e pare de escutar solicitações de conexão de cliente.</span><span class="sxs-lookup"><span data-stu-id="2c669-114">Exposes methods that request that the protocol start and stop listening for client connection requests.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-115">**IWRdsProtocolListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="2c669-115">**IWRdsProtocolListenerCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

<span data-ttu-id="2c669-116">Expõe métodos que notificam o serviço de Serviços de Área de Trabalho Remota que um cliente conectou.</span><span class="sxs-lookup"><span data-stu-id="2c669-116">Exposes methods that notify the Remote Desktop Services service that a client has connected.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-117">**IWRdsProtocolLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="2c669-117">**IWRdsProtocolLogonErrorRedirector**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

<span data-ttu-id="2c669-118">Expõe métodos chamados pelo serviço de Serviços de Área de Trabalho Remota para atualizar o status de logon e determinar como direcionar mensagens de erro de logon.</span><span class="sxs-lookup"><span data-stu-id="2c669-118">Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-119">**IWRdsProtocolManager**</span><span class="sxs-lookup"><span data-stu-id="2c669-119">**IWRdsProtocolManager**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

<span data-ttu-id="2c669-120">Expõe métodos que o serviço Serviços de Área de Trabalho Remota usa para se comunicar com o provedor de protocolo.</span><span class="sxs-lookup"><span data-stu-id="2c669-120">Exposes methods that the Remote Desktop Services service uses to communicate with the protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-121">**IWRdsProtocolSettings**</span><span class="sxs-lookup"><span data-stu-id="2c669-121">**IWRdsProtocolSettings**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

<span data-ttu-id="2c669-122">Expõe métodos para recuperar e adicionar configurações relacionadas à política.</span><span class="sxs-lookup"><span data-stu-id="2c669-122">Exposes methods for retrieving and adding policy-related settings.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-123">**IWRdsProtocolShadowCallback**</span><span class="sxs-lookup"><span data-stu-id="2c669-123">**IWRdsProtocolShadowCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

<span data-ttu-id="2c669-124">Expõe métodos chamados pelo protocolo para notificar o serviço de Serviços de Área de Trabalho Remota para iniciar ou parar o lado de destino de uma sombra.</span><span class="sxs-lookup"><span data-stu-id="2c669-124">Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-125">**IWRdsProtocolShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="2c669-125">**IWRdsProtocolShadowConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

<span data-ttu-id="2c669-126">Expõe métodos que notificam o provedor de protocolo sobre o status de sombra da sessão.</span><span class="sxs-lookup"><span data-stu-id="2c669-126">Exposes methods that notify the protocol provider about the status of session shadowing.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-127">**IWRdsRemoteFXGraphicsConnection**</span><span class="sxs-lookup"><span data-stu-id="2c669-127">**IWRdsRemoteFXGraphicsConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

<span data-ttu-id="2c669-128">Expõe métodos relacionados à manipulação e à compreensão de elementos gráficos na conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="2c669-128">Exposes methods relating to the manipulation and understanding of graphics on the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="2c669-129">Interfaces do provedor de protocolo de desktop preteridas</span><span class="sxs-lookup"><span data-stu-id="2c669-129">Deprecated Desktop Protocol Provider Interfaces</span></span>](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

<span data-ttu-id="2c669-130">As interfaces a seguir foram preteridas e não devem mais ser usadas.</span><span class="sxs-lookup"><span data-stu-id="2c669-130">The following interfaces have been deprecated and should no longer be used.</span></span> <span data-ttu-id="2c669-131">Para novos projetos, use as interfaces de interfaces de provedor de protocolo RDP em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2c669-131">For new projects, use the Remote Desktop Protocol Provider Interfaces interfaces instead.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="2c669-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c669-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c669-133">Referência do provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="2c669-133">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="2c669-134">Enumerações de provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="2c669-134">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="2c669-135">Estruturas de provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="2c669-135">Remote Desktop Protocol Provider Structures</span></span>](custom-remote-protocol-structures.md)
</dt> <dt>

[<span data-ttu-id="2c669-136">Uniões de provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="2c669-136">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




