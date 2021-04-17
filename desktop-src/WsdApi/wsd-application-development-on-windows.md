---
description: A API do Microsoft Web Services on Devices (WSDAPI) dá suporte à implementação de dispositivos e serviços controlados pelo cliente e aos hosts de dispositivo em conformidade com o perfil de dispositivos para serviços Web (DPWS).
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Desenvolvimento de aplicativos WSD no Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33976a1903c87ffb6c577cd5a451a3b772a67a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761600"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="90755-103">Desenvolvimento de aplicativos WSD no Windows</span><span class="sxs-lookup"><span data-stu-id="90755-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="90755-104">A API do Microsoft Web Services on Devices (WSDAPI) dá suporte à implementação de dispositivos e serviços controlados pelo cliente e aos hosts de dispositivo em conformidade com o [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="90755-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="90755-105">O WSDAPI pode ser usado para o desenvolvimento de implementações de cliente e de servidor (dispositivo).</span><span class="sxs-lookup"><span data-stu-id="90755-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="90755-106">Com muita frequência, o código WSDAPI para esses aplicativos é gerado usando [WsdCodeGen](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="90755-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="90755-107">Algumas funções e métodos WSDAPI devem ser chamados apenas pelo código gerado.</span><span class="sxs-lookup"><span data-stu-id="90755-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="90755-108">A documentação de referência de API indica quando uma função ou método deve ser usado ou implementado somente pelo código gerado.</span><span class="sxs-lookup"><span data-stu-id="90755-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="90755-109">O SDK do Windows inclui alguns arquivos WSDL de exemplo, arquivos de configuração WsdCodeGen e código gerado.</span><span class="sxs-lookup"><span data-stu-id="90755-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="90755-110">Para obter mais informações, consulte [exemplos de WSDAPI](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="90755-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="90755-111">Se você quiser enumerar dispositivos usando o protocolo WSD e consultar metadados de dispositivo WSD, poderá usar a API de [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="90755-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="90755-112">Se você quiser implementar um dispositivo WSD que não executa o Windows, consulte [desenvolvimento de dispositivo WSD](wsd-device-development.md).</span><span class="sxs-lookup"><span data-stu-id="90755-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
