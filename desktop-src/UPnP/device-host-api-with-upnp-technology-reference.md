---
title: Referência da API do host do dispositivo
description: As interfaces a seguir fazem parte da API de host do dispositivo com tecnologia UPnP. O host do dispositivo com a tecnologia UPnP dá suporte ao Microsoft Visual Basic e ao C++.
ms.assetid: 48e20a09-7e78-4b8d-aa16-78751b6fb586
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f42b43efcc1d51eb5e5581770260238640469
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364248"
---
# <a name="device-host-api-reference"></a><span data-ttu-id="8a4b2-104">Referência da API do host do dispositivo</span><span class="sxs-lookup"><span data-stu-id="8a4b2-104">Device Host API Reference</span></span>

<span data-ttu-id="8a4b2-105">As interfaces a seguir fazem parte da API de host do dispositivo com tecnologia UPnP.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-105">The following interfaces are part of the Device Host API with UPnP technology.</span></span> <span data-ttu-id="8a4b2-106">O host do dispositivo com a tecnologia UPnP dá suporte ao Microsoft Visual Basic e ao C++.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-106">The Device Host with UPnP technology supports Microsoft Visual Basic and C++.</span></span>

<span data-ttu-id="8a4b2-107">Essa API não fornece suporte para o Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="8a4b2-107">This API does not provide support for Microsoft Visual Basic Scripting Edition (VBScript).</span></span>



| <span data-ttu-id="8a4b2-108">Interface</span><span class="sxs-lookup"><span data-stu-id="8a4b2-108">Interface</span></span>                                                  | <span data-ttu-id="8a4b2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a4b2-109">Description</span></span>                                                                                         |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a4b2-110">**IUPnPDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="8a4b2-110">**IUPnPDeviceControl**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdevicecontrol)           | <span data-ttu-id="8a4b2-111">Usado pelo host do dispositivo para gerenciar dispositivos e serviços relacionados.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-111">Used by the device host to manage devices and related services.</span></span>                                     |
| [<span data-ttu-id="8a4b2-112">**IUPnPDeviceProvider**</span><span class="sxs-lookup"><span data-stu-id="8a4b2-112">**IUPnPDeviceProvider**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider)         | <span data-ttu-id="8a4b2-113">Usado pelo host do dispositivo para iniciar e parar provedores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-113">Used by the device host to start and stop device providers.</span></span>                                         |
| [<span data-ttu-id="8a4b2-114">**IUPnPEventSink**</span><span class="sxs-lookup"><span data-stu-id="8a4b2-114">**IUPnPEventSink**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink)                   | <span data-ttu-id="8a4b2-115">Usado por dispositivos para enviar notificações de eventos para o host do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-115">Used by devices to send event notifications to the device host.</span></span>                                     |
| [<span data-ttu-id="8a4b2-116">**IUPnPEventSource**</span><span class="sxs-lookup"><span data-stu-id="8a4b2-116">**IUPnPEventSource**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource)               | <span data-ttu-id="8a4b2-117">Usado pelo host do dispositivo para assinar ou cancelar a assinatura de eventos fornecidos pelo serviço hospedado.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-117">Used by the device host to subscribe or unsubscribe to events provided by the hosted service.</span></span>       |
| [<span data-ttu-id="8a4b2-118">**IUPnPRegistrar**</span><span class="sxs-lookup"><span data-stu-id="8a4b2-118">**IUPnPRegistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar)                   | <span data-ttu-id="8a4b2-119">Usado por dispositivos para registrar com o host do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-119">Used by devices to register with the device host.</span></span>                                                   |
| [<span data-ttu-id="8a4b2-120">**IUPnPRemoteEndpointInfo**</span><span class="sxs-lookup"><span data-stu-id="8a4b2-120">**IUPnPRemoteEndpointInfo**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) | <span data-ttu-id="8a4b2-121">Usado por dispositivos para obter informações sobre um solicitante (isto é, um ponto de controle) e a solicitação.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-121">Used by devices to obtain information about a requester (that is, a control point) and the request.</span></span> |
| [<span data-ttu-id="8a4b2-122">**IUPnPReregistrar**</span><span class="sxs-lookup"><span data-stu-id="8a4b2-122">**IUPnPReregistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)               | <span data-ttu-id="8a4b2-123">Usado pelos dispositivos para registrar novamente no host do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8a4b2-123">Used by devices to re-register with the device host.</span></span>                                                |



 

 

 




