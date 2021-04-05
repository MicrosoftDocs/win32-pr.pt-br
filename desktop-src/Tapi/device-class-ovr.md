---
description: As classes de dispositivo simplificam o desenvolvimento, permitindo que os programadores tratem os dispositivos que têm propriedades semelhantes de maneira semelhante.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Classe de dispositivo (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921700"
---
# <a name="device-class"></a><span data-ttu-id="998ed-103">Classe de dispositivo</span><span class="sxs-lookup"><span data-stu-id="998ed-103">Device Class</span></span>

<span data-ttu-id="998ed-104">As classes de dispositivo simplificam o desenvolvimento, permitindo que os programadores tratem os dispositivos que têm propriedades semelhantes de maneira semelhante.</span><span class="sxs-lookup"><span data-stu-id="998ed-104">Device classes simplify development by letting programmers treat devices that have similar properties in a similar manner.</span></span> <span data-ttu-id="998ed-105">Por exemplo, um telefone digital em um escritório normalmente tem mais recursos do que um monofone padrão em casa, mas ambos respondem praticamente da mesma forma a um conjunto básico de funções e ambos pertencem a uma classe de dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="998ed-105">For example, a digital phone in an office typically has more capabilities than a standard handset in a home, but both respond in much the same way to a basic set of functions, and both belong to a phone device class.</span></span> <span data-ttu-id="998ed-106">As classes de dispositivo ajudam a tornar a TAPI extensível fornecendo uma estrutura da qual classificar e dar suporte a novos equipamentos.</span><span class="sxs-lookup"><span data-stu-id="998ed-106">Device classes help make TAPI extensible by providing a framework from which to classify and support new equipment.</span></span>

<span data-ttu-id="998ed-107">Consulte [classes de dispositivo TAPI](./tapi-device-classes.md) para classes que a TAPI predefiniu.</span><span class="sxs-lookup"><span data-stu-id="998ed-107">See [TAPI Device Classes](./tapi-device-classes.md) for classes that TAPI has predefined.</span></span> <span data-ttu-id="998ed-108">Um provedor de serviços pode implementar e definir classes de dispositivo adicionais para o equipamento que ele suporta.</span><span class="sxs-lookup"><span data-stu-id="998ed-108">A service provider may implement and define additional device classes for the equipment it supports.</span></span> <span data-ttu-id="998ed-109">Um aplicativo nunca precisa saber qual provedor de serviços controla qual dispositivo, mas pode exigir informações sobre o controle de novas classes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="998ed-109">An application never needs to know which service provider controls which device, but may require information on the control of new device classes.</span></span>

<span data-ttu-id="998ed-110">Um provedor de serviços implementa uma classe de dispositivo mapeando solicitações em comandos de dispositivo reais.</span><span class="sxs-lookup"><span data-stu-id="998ed-110">A service provider implements a device class by mapping requests into actual device commands.</span></span> <span data-ttu-id="998ed-111">Por exemplo, quando o provedor de serviços para um modem compatível com Hayes recebe um comando passado pelo TAPISVR para fazer uma chamada, ele envia comandos clássicos AT para o modem.</span><span class="sxs-lookup"><span data-stu-id="998ed-111">For example, when the service provider for a Hayes-compatible modem receives a command passed through TAPISVR to make a call, it sends classic AT commands to the modem.</span></span>

<span data-ttu-id="998ed-112">A interface do provedor de serviços pode ser mapeada para uma ampla variedade de ambientes, incluindo aqueles que não são tradicionalmente considerados como pertencentes a telefonia.</span><span class="sxs-lookup"><span data-stu-id="998ed-112">The service provider interface can be mapped to a wide range of environments, including those not traditionally thought of as belonging to telephony.</span></span> <span data-ttu-id="998ed-113">Um exemplo é a conferência de multimídia em uma rede baseada em IP, como a Internet.</span><span class="sxs-lookup"><span data-stu-id="998ed-113">An example is multimedia conferencing over an IP-based network such as the Internet.</span></span>

<span data-ttu-id="998ed-114">Os desenvolvedores de aplicativos devem ter em mente a existência de outros aplicativos que podem compartilhar serviços de telefonia.</span><span class="sxs-lookup"><span data-stu-id="998ed-114">Application developers should keep in mind the existence of other applications that may share telephony services.</span></span>

 

 
