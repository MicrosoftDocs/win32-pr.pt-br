---
description: A QoS (qualidade de serviço) é implementada no Windows por meio de vários componentes de QoS com suporte no Windows Server 2003, Windows XP e Windows 2000.
ms.assetid: e55b085f-6f72-4aa4-a8b0-b7609b9010dc
title: Qualidade de serviço no SPI do Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87d37f2e30e0a4fb296fc340353e2f4d85b5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813731"
---
# <a name="quality-of-service-in-the-windows-sockets-2-spi"></a><span data-ttu-id="da1f3-103">Qualidade de serviço no SPI do Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="da1f3-103">Quality of Service in the Windows Sockets 2 SPI</span></span>

<span data-ttu-id="da1f3-104">A QoS (qualidade de serviço) é implementada no Windows por meio de vários componentes de QoS com suporte no Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="da1f3-104">Quality of Service (QoS) is implemented in Windows through various QoS components supported on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="da1f3-105">Uma explicação detalhada da QoS e de seus componentes está localizada em uma seção dedicada à qualidade do serviço, localizada no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="da1f3-105">A detailed explanation of QoS and its components is located in a section dedicated to Quality of Service, located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="da1f3-106">Cada componente de QoS e a função que ele desempenha na implementação de QoS são explicados nesta seção de QoS, com diretrizes adicionais fornecidas para a implementação de aplicativos e serviços habilitados para QoS.</span><span class="sxs-lookup"><span data-stu-id="da1f3-106">Each QoS component, and the role it plays in the QoS implementation, is explained in this QoS section, with additional guidance provided for the implementation of QoS-enabled applications and services.</span></span> <span data-ttu-id="da1f3-107">Consulte a seção [qualidade de serviço (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) do SDK do Windows para obter informações mais detalhadas.</span><span class="sxs-lookup"><span data-stu-id="da1f3-107">Please see the [Quality of Service (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) section of the Windows SDK for more detailed information.</span></span>

<span data-ttu-id="da1f3-108">Esta seção descreve a qualidade dos recursos de serviço disponíveis para desenvolvedores de Winsock.</span><span class="sxs-lookup"><span data-stu-id="da1f3-108">This section describes Quality of Service capabilities available to Winsock developers.</span></span> <span data-ttu-id="da1f3-109">A lista a seguir descreve os tópicos nesta seção:</span><span class="sxs-lookup"><span data-stu-id="da1f3-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="da1f3-110">Modelo de uso</span><span class="sxs-lookup"><span data-stu-id="da1f3-110">Usage Model</span></span>](usage-model-2.md)
-   [<span data-ttu-id="da1f3-111">Atualizações de QoS</span><span class="sxs-lookup"><span data-stu-id="da1f3-111">QoS Updates</span></span>](qos-updates-2.md)
-   [<span data-ttu-id="da1f3-112">Valores padrão no SPI</span><span class="sxs-lookup"><span data-stu-id="da1f3-112">Default Values in the SPI</span></span>](default-values-in-the-spi-2.md)
-   [<span data-ttu-id="da1f3-113">Modelos de QoS no SPI</span><span class="sxs-lookup"><span data-stu-id="da1f3-113">QoS Templates in the SPI</span></span>](qos-templates-in-the-spi-2.md)

## <a name="related-topics"></a><span data-ttu-id="da1f3-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da1f3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da1f3-115">Quality of Service (QoS)</span><span class="sxs-lookup"><span data-stu-id="da1f3-115">Quality of Service (QoS)</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> <dt>

<span data-ttu-id="da1f3-116">[O que é QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="da1f3-116">[What Is QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="da1f3-117">Extensão de QoS de ATM do Winsock</span><span class="sxs-lookup"><span data-stu-id="da1f3-117">Winsock ATM QoS Extension</span></span>](winsock-atm-qos-extension.md)
</dt> <dt>

[<span data-ttu-id="da1f3-118">**Winsock IOCTLs**</span><span class="sxs-lookup"><span data-stu-id="da1f3-118">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
