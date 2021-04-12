---
title: Sobre a API de host do dispositivo
description: A API de host de dispositivo com tecnologia UPnP é uma estrutura para implementar a funcionalidade de dispositivo baseada em UPnP na plataforma Windows.
ms.assetid: fa716c59-d3f0-4cd4-b92d-939b258b0102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c751328696d6524208dc95a0b7961829f8ee231c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364336"
---
# <a name="about-the-device-host-api"></a><span data-ttu-id="c547a-103">Sobre a API de host do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c547a-103">About the Device Host API</span></span>

<span data-ttu-id="c547a-104">A API de host de dispositivo com tecnologia UPnP é uma estrutura para implementar a funcionalidade de dispositivo baseada em UPnP na plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="c547a-104">The Device Host API with UPnP technology is a framework for implementing UPnP-based device functionality on the Windows platform.</span></span> <span data-ttu-id="c547a-105">Os desenvolvedores que estão criando dispositivos usando a API de host do dispositivo com a tecnologia UPnP (conhecida como [*dispositivos hospedados*](h-gly.md)) só precisam implementar a funcionalidade principal do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c547a-105">Developers who are creating devices by using the Device Host API with UPnP technology (referred to as [*hosted devices*](h-gly.md)) need only implement the device's core functionality.</span></span> <span data-ttu-id="c547a-106">Os desenvolvedores podem contar com o host do dispositivo para lidar com os detalhes específicos do UPnP de descoberta, descrição, controle, eventos e apresentações.</span><span class="sxs-lookup"><span data-stu-id="c547a-106">Developers can rely on the device host to handle the UPnP-specific details of discovery, description, control, eventing, and presentation.</span></span> <span data-ttu-id="c547a-107">O host do dispositivo valida os dados de entrada de clientes baseados em UPnP e formata todos os dados de saída de dispositivos hospedados de acordo com a arquitetura do dispositivo UPnP.</span><span class="sxs-lookup"><span data-stu-id="c547a-107">The device host validates incoming data from UPnP-based clients and formats all outgoing data from hosted devices according to the UPnP device architecture.</span></span>

<span data-ttu-id="c547a-108">As seções a seguir explicam, em geral, como o host do dispositivo UPnP funciona:</span><span class="sxs-lookup"><span data-stu-id="c547a-108">The following sections explain, in general, how the UPnP device host works:</span></span>

-   [<span data-ttu-id="c547a-109">Implementando um dispositivo hospedado</span><span class="sxs-lookup"><span data-stu-id="c547a-109">Implementing a Hosted Device</span></span>](implementing-a-hosted-device.md)
-   [<span data-ttu-id="c547a-110">Registrando um dispositivo hospedado no host do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c547a-110">Registering a Hosted Device with the Device Host</span></span>](registering-a-hosted-device-with-the-device-host.md)
-   [<span data-ttu-id="c547a-111">Provedores de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c547a-111">Device Providers</span></span>](device-providers.md)
-   [<span data-ttu-id="c547a-112">Eventos</span><span class="sxs-lookup"><span data-stu-id="c547a-112">Eventing</span></span>](eventing.md)
-   [<span data-ttu-id="c547a-113">Apresentação</span><span class="sxs-lookup"><span data-stu-id="c547a-113">Presentation</span></span>](presentation.md)

 

 




