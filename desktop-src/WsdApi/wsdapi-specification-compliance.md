---
description: Os serviços Web na API de dispositivos (WSDAPI) fornecem suporte para o perfil de dispositivos para serviços Web (DPWS) no Windows Vista, que habilita a comunicação de serviços Web (WS) entre PCs baseados no Windows e dispositivos conectados à rede.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Conformidade de especificação do WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169642"
---
# <a name="wsdapi-specification-compliance"></a><span data-ttu-id="4edc6-103">Conformidade de especificação do WSDAPI</span><span class="sxs-lookup"><span data-stu-id="4edc6-103">WSDAPI Specification Compliance</span></span>

<span data-ttu-id="4edc6-104">Os serviços Web na API de dispositivos (WSDAPI) fornecem suporte para o [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) no Windows Vista, que habilita a comunicação de serviços Web (WS) entre PCs baseados no Windows e dispositivos conectados à rede.</span><span class="sxs-lookup"><span data-stu-id="4edc6-104">Web Services on Devices API (WSDAPI) provides support for the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) on Windows Vista, which enables Web Services (WS) communication between Windows-based PCs and network connected devices.</span></span> <span data-ttu-id="4edc6-105">O DPWS monta especificações básicas do WS, como [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)e [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), além de aprimorar ou restringir a capacidade de fornecer um conjunto de linha de base de recursos para dispositivos com restrição de recursos.</span><span class="sxs-lookup"><span data-stu-id="4edc6-105">DPWS assembles basic WS specifications, such as [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), and [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), and enhances or constrains them to provide a baseline set of capabilities for resource-constrained devices.</span></span> <span data-ttu-id="4edc6-106">Essa especificação de linha de base contém a funcionalidade necessária, como a capacidade de descrever as propriedades do dispositivo por meio de metadados e funcionalidade opcional, como a capacidade de rejeitar mensagens específicas por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="4edc6-106">This baseline specification contains required functionality, such as the ability to describe properties of the device through metadata, and optional functionality, such as the ability to reject specific messages for security reasons.</span></span>

<span data-ttu-id="4edc6-107">A implementação de WSDAPI no Windows Vista é a primeira versão do suporte explícito para o DPWS e é uma implementação não gerenciada de DPWS que é separada e distinta de outras implementações de serviços da Web (como o [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) ou o [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span><span class="sxs-lookup"><span data-stu-id="4edc6-107">The WSDAPI implementation in Windows Vista is the first release of explicit support for the DPWS, and is an unmanaged implementation of DPWS that is separate and distinct from other Web Services implementations (such as the [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) or [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span></span>

<span data-ttu-id="4edc6-108">Os tópicos a seguir são de interesse dos fabricantes de dispositivos e outros implementadores de dispositivos que criam dispositivos que interoperam com clientes e hosts WSDAPI baseados no Windows sem usar o WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="4edc6-108">The following topics are of interest to device manufacturers and other device implementers that create devices that interoperate with Windows-based WSDAPI clients and hosts without using WSDAPI.</span></span> <span data-ttu-id="4edc6-109">Estes tópicos descrevem a implementação de WSDAPI em relação às especificações subjacentes.</span><span class="sxs-lookup"><span data-stu-id="4edc6-109">These topics describe the implementation of WSDAPI relative to the underlying specifications.</span></span> <span data-ttu-id="4edc6-110">Eles abordam a implementação de funcionalidade necessária, funcionalidade opcional e funcionalidade adicional não definida na especificação.</span><span class="sxs-lookup"><span data-stu-id="4edc6-110">They cover the implementation of required functionality, optional functionality, and additional functionality not defined in the specification.</span></span>

-   [<span data-ttu-id="4edc6-111">Conformidade de especificação do DPWS</span><span class="sxs-lookup"><span data-stu-id="4edc6-111">DPWS Specification Compliance</span></span>](dpws-specification-compliance.md)
-   [<span data-ttu-id="4edc6-112">Conformidade de especificação do WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="4edc6-112">WS-Discovery Specification Compliance</span></span>](ws-discovery-specification-compliance.md)
-   [<span data-ttu-id="4edc6-113">Conformidade de especificação WS-MetadataExchange e WS-Transfer</span><span class="sxs-lookup"><span data-stu-id="4edc6-113">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [<span data-ttu-id="4edc6-114">Funcionalidade adicional de WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="4edc6-114">Additional WS-Discovery Functionality</span></span>](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="4edc6-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4edc6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4edc6-116">Desenvolvimento de dispositivo WSD</span><span class="sxs-lookup"><span data-stu-id="4edc6-116">WSD Device Development</span></span>](wsd-device-development.md)
</dt> <dt>

[<span data-ttu-id="4edc6-117">Recomendações de implementação de dispositivo WSD</span><span class="sxs-lookup"><span data-stu-id="4edc6-117">WSD Device Implementation Recommendations</span></span>](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
