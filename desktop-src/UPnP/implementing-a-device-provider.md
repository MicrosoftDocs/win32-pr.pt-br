---
title: Implementando um provedor de dispositivo
description: Para implementar um provedor de dispositivo, crie um objeto que expõe a interface IUPnPDeviceProvider.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453717"
---
# <a name="implementing-a-device-provider"></a><span data-ttu-id="29190-103">Implementando um provedor de dispositivo</span><span class="sxs-lookup"><span data-stu-id="29190-103">Implementing a Device Provider</span></span>

<span data-ttu-id="29190-104">Para implementar um provedor de dispositivo, crie um objeto que expõe a interface [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) .</span><span class="sxs-lookup"><span data-stu-id="29190-104">To implement a device provider, create an object that exposes the [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) interface.</span></span> <span data-ttu-id="29190-105">Esse objeto deve ser registrado com o host do dispositivo usando o método [**IUPnPRegistrar:: RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) .</span><span class="sxs-lookup"><span data-stu-id="29190-105">This object must be registered with the device host using the [**IUPnPRegistrar::RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) method.</span></span> <span data-ttu-id="29190-106">Esse método usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="29190-106">This method takes the following parameters:</span></span>

-   <span data-ttu-id="29190-107">O nome do provedor, que deve ser exclusivo no computador.</span><span class="sxs-lookup"><span data-stu-id="29190-107">The name of the provider, which must be unique on the computer.</span></span>
-   <span data-ttu-id="29190-108">O ProgID da classe que implementa o provedor do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29190-108">The ProgID of the class that implements the device provider.</span></span>
-   <span data-ttu-id="29190-109">Uma cadeia de inicialização que é passada para o provedor do dispositivo quando ele é iniciado.</span><span class="sxs-lookup"><span data-stu-id="29190-109">An initialization string that is passed to the device provider when it is started.</span></span>
-   <span data-ttu-id="29190-110">Uma ID de contêiner.</span><span class="sxs-lookup"><span data-stu-id="29190-110">A container ID.</span></span> <span data-ttu-id="29190-111">Uma ID de contêiner é uma cadeia de caracteres que identifica o grupo ao qual o dispositivo pertence.</span><span class="sxs-lookup"><span data-stu-id="29190-111">A container ID is a string that identifies the group to which the device belongs.</span></span> <span data-ttu-id="29190-112">Todos os dispositivos com o mesmo identificador de contêiner são hospedados no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="29190-112">All devices with the same container identifier are hosted in the same process.</span></span>

 

 




