---
description: O Winsock fornece uma interface de provedor de serviços para a criação de serviços de Winsock, comumente chamados de SPI do Winsock.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: Sobre o SPI do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090412"
---
# <a name="about-the-winsock-spi"></a><span data-ttu-id="7e0c0-103">Sobre o SPI do Winsock</span><span class="sxs-lookup"><span data-stu-id="7e0c0-103">About the Winsock SPI</span></span>

<span data-ttu-id="7e0c0-104">O Winsock fornece uma interface de provedor de serviços para a criação de serviços de Winsock, comumente chamados de SPI do Winsock.</span><span class="sxs-lookup"><span data-stu-id="7e0c0-104">Winsock provides a Service Provider Interface for creating Winsock services, commonly referred to as the Winsock SPI.</span></span> <span data-ttu-id="7e0c0-105">Existem dois tipos de provedores de serviços: provedores de transporte e provedores de namespace.</span><span class="sxs-lookup"><span data-stu-id="7e0c0-105">Two types of service providers exist: transport providers and namespace providers.</span></span> <span data-ttu-id="7e0c0-106">Exemplos de provedores de transporte incluem pilhas de protocolo, como TCP/IP ou IPX/SPX, enquanto um exemplo de um provedor de namespace seria uma interface para o DNS (sistema de cadastramento de domínio) da Internet.</span><span class="sxs-lookup"><span data-stu-id="7e0c0-106">Examples of transport providers include protocol stacks such as TCP/IP or IPX/SPX, while an example of a namespace provider would be an interface to the Internet's Domain Naming System (DNS).</span></span> <span data-ttu-id="7e0c0-107">Seções separadas da especificação da interface do provedor de serviços se aplicam a cada tipo de provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="7e0c0-107">Separate sections of the service provider interface specification apply to each type of service provider.</span></span>

<span data-ttu-id="7e0c0-108">Os provedores de serviço de [namespace](name-space-service-providers-2.md) e [transporte](transport-service-providers-2.md) devem ser registrados com o \_32.dll Ws2 no momento em que são instalados.</span><span class="sxs-lookup"><span data-stu-id="7e0c0-108">[Transport](transport-service-providers-2.md) and [namespace](name-space-service-providers-2.md) service providers must be registered with the Ws2\_32.dll at the time they are installed.</span></span> <span data-ttu-id="7e0c0-109">Esse registro só precisa ser feito uma vez para cada provedor, pois as informações necessárias são mantidas no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="7e0c0-109">This registration need only be done once for each provider as the necessary information is retained in persistent storage.</span></span>

 

 



