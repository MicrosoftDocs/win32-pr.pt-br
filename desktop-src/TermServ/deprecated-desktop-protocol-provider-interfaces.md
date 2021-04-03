---
title: Interfaces do provedor de protocolo de desktop preteridas
description: As interfaces a seguir foram preteridas e não devem mais ser usadas. Para novos projetos, use as interfaces de interfaces de provedor de protocolo RDP em vez disso.
ms.assetid: FD64A6B9-AE15-4311-BD69-4824CAF53544
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11a586084bc4938727e632ca196e97117f7b8a4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823390"
---
# <a name="deprecated-desktop-protocol-provider-interfaces"></a><span data-ttu-id="99d5f-104">Interfaces do provedor de protocolo de desktop preteridas</span><span class="sxs-lookup"><span data-stu-id="99d5f-104">Deprecated Desktop Protocol Provider Interfaces</span></span>

<span data-ttu-id="99d5f-105">As interfaces a seguir foram preteridas e não devem mais ser usadas.</span><span class="sxs-lookup"><span data-stu-id="99d5f-105">The following interfaces have been deprecated and should no longer be used.</span></span> <span data-ttu-id="99d5f-106">Para novos projetos, use as interfaces de [interfaces de provedor de protocolo RDP](custom-remote-protocol-interfaces.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="99d5f-106">For new projects, use the [Remote Desktop Protocol Provider Interfaces](custom-remote-protocol-interfaces.md) interfaces instead.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99d5f-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="99d5f-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="99d5f-108">**IWTSProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="99d5f-108">**IWTSProtocolConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection)
</dt> <dd>

<span data-ttu-id="99d5f-109">O [**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="99d5f-109">[**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) is no longer available.</span></span> <span data-ttu-id="99d5f-110">Em vez disso, use [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection).</span><span class="sxs-lookup"><span data-stu-id="99d5f-110">Instead, use [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection).</span></span>

</dd> <dt>

[<span data-ttu-id="99d5f-111">**IWTSProtocolConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="99d5f-111">**IWTSProtocolConnectionCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback)
</dt> <dd>

<span data-ttu-id="99d5f-112">O [**IWTSProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback) não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="99d5f-112">[**IWTSProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback) is no longer available.</span></span> <span data-ttu-id="99d5f-113">Em vez disso, use [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback).</span><span class="sxs-lookup"><span data-stu-id="99d5f-113">Instead, use [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback).</span></span>

</dd> <dt>

[<span data-ttu-id="99d5f-114">**IWTSProtocolLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="99d5f-114">**IWTSProtocolLicenseConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection)
</dt> <dd>

<span data-ttu-id="99d5f-115">O [**IWTSProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection) não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="99d5f-115">[**IWTSProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection) is no longer available.</span></span> <span data-ttu-id="99d5f-116">Em vez disso, use [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection).</span><span class="sxs-lookup"><span data-stu-id="99d5f-116">Instead, use [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection).</span></span>

</dd> <dt>

[<span data-ttu-id="99d5f-117">**IWTSProtocolListener**</span><span class="sxs-lookup"><span data-stu-id="99d5f-117">**IWTSProtocolListener**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener)
</dt> <dd>

<span data-ttu-id="99d5f-118">O [**IWTSProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener) não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="99d5f-118">[**IWTSProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener) is no longer available.</span></span> <span data-ttu-id="99d5f-119">Em vez disso, use [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener).</span><span class="sxs-lookup"><span data-stu-id="99d5f-119">Instead, use [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener).</span></span>

</dd> <dt>

[<span data-ttu-id="99d5f-120">**IWTSProtocolListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="99d5f-120">**IWTSProtocolListenerCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistenercallback)
</dt> <dd>

<span data-ttu-id="99d5f-121">O [**IWTSProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistenercallback) não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="99d5f-121">[**IWTSProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistenercallback) is no longer available.</span></span> <span data-ttu-id="99d5f-122">Em vez disso, use [**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback).</span><span class="sxs-lookup"><span data-stu-id="99d5f-122">Instead, use [**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback).</span></span>

</dd> <dt>

[<span data-ttu-id="99d5f-123">**IWTSProtocolLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="99d5f-123">**IWTSProtocolLogonErrorRedirector**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector)
</dt> <dd>

<span data-ttu-id="99d5f-124">O [**IWTSProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector) não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="99d5f-124">[**IWTSProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector) is no longer available.</span></span> <span data-ttu-id="99d5f-125">Em vez disso, use [**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector).</span><span class="sxs-lookup"><span data-stu-id="99d5f-125">Instead, use [**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector).</span></span>

</dd> <dt>

[<span data-ttu-id="99d5f-126">**IWTSProtocolManager**</span><span class="sxs-lookup"><span data-stu-id="99d5f-126">**IWTSProtocolManager**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager)
</dt> <dd>

<span data-ttu-id="99d5f-127">O [**IWTSProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager) não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="99d5f-127">[**IWTSProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager) is no longer available.</span></span> <span data-ttu-id="99d5f-128">Em vez disso, use [**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager).</span><span class="sxs-lookup"><span data-stu-id="99d5f-128">Instead, use [**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager).</span></span>

</dd> <dt>

[<span data-ttu-id="99d5f-129">**IWTSProtocolShadowCallback**</span><span class="sxs-lookup"><span data-stu-id="99d5f-129">**IWTSProtocolShadowCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback)
</dt> <dd>

<span data-ttu-id="99d5f-130">O [**IWTSProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback) não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="99d5f-130">[**IWTSProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback) is no longer available.</span></span> <span data-ttu-id="99d5f-131">Em vez disso, use [**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback).</span><span class="sxs-lookup"><span data-stu-id="99d5f-131">Instead, use [**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback).</span></span>

</dd> <dt>

[<span data-ttu-id="99d5f-132">**IWTSProtocolShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="99d5f-132">**IWTSProtocolShadowConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection)
</dt> <dd>

<span data-ttu-id="99d5f-133">O [**IWTSProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection) não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="99d5f-133">[**IWTSProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection) is no longer available.</span></span> <span data-ttu-id="99d5f-134">Em vez disso, use [**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection).</span><span class="sxs-lookup"><span data-stu-id="99d5f-134">Instead, use [**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection).</span></span>

</dd> </dl>

 

 




