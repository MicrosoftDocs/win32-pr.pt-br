---
title: Como registrar um dispositivo no host do dispositivo
description: Você pode registrar um dispositivo em execução ou um dispositivo que não esteja em execução.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005557"
---
# <a name="how-to-register-a-device-with-the-device-host"></a><span data-ttu-id="aeaf9-103">Como registrar um dispositivo no host do dispositivo</span><span class="sxs-lookup"><span data-stu-id="aeaf9-103">How to Register a Device with the Device Host</span></span>

<span data-ttu-id="aeaf9-104">Você pode registrar um dispositivo em execução ou um dispositivo que não esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-104">You can register either a running device or a non-running device.</span></span>

## <a name="registering-a-running-device"></a><span data-ttu-id="aeaf9-105">Registrando um dispositivo em execução</span><span class="sxs-lookup"><span data-stu-id="aeaf9-105">Registering a Running Device</span></span>

<span data-ttu-id="aeaf9-106">Os dispositivos são registrados usando a interface [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) .</span><span class="sxs-lookup"><span data-stu-id="aeaf9-106">Devices are registered using the [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) interface.</span></span> <span data-ttu-id="aeaf9-107">Somente administradores têm permissão para registrar dispositivos em execução.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-107">Only administrators are allowed to register running devices.</span></span> <span data-ttu-id="aeaf9-108">Para registrar um dispositivo que tem um objeto de controle de dispositivo em execução, um aplicativo deve invocar [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passando o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aeaf9-108">To register a device that has a running device control object, an application must invoke [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passing the following:</span></span>

-   <span data-ttu-id="aeaf9-109">O texto da descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-109">The text of the device's description.</span></span>
-   <span data-ttu-id="aeaf9-110">Um ponteiro **IUnknown** para o objeto de controle de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-110">An **IUnknown** pointer to the device control object.</span></span>
-   <span data-ttu-id="aeaf9-111">Uma cadeia de inicialização que é passada para o método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) do objeto de controle de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-111">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="aeaf9-112">O local do diretório de recursos.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-112">The location of the resource directory.</span></span>
-   <span data-ttu-id="aeaf9-113">O tempo de vida do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-113">The lifetime of the device.</span></span>
-   <span data-ttu-id="aeaf9-114">O parâmetro de ID do dispositivo (um parâmetro OUT), que é o valor de retorno dessa chamada; um ponteiro para a ID do dispositivo é retornado em C++.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-114">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

## <a name="registering-a-non-running-device"></a><span data-ttu-id="aeaf9-115">Registrando um dispositivo que não está em execução</span><span class="sxs-lookup"><span data-stu-id="aeaf9-115">Registering a Non-Running Device</span></span>

<span data-ttu-id="aeaf9-116">Por padrão, somente administradores e usuários interativos têm permissão para registrar dispositivos que não estão em execução.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-116">By default, only administrators and interactive users are allowed to register non-running devices.</span></span> <span data-ttu-id="aeaf9-117">Para registrar um dispositivo com um objeto de controle de dispositivo que não está em execução, o aplicativo usa o método [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) .</span><span class="sxs-lookup"><span data-stu-id="aeaf9-117">To register a device with a device control object that is not running, the application uses the [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) method.</span></span>

<span data-ttu-id="aeaf9-118">Para registrar um dispositivo de forma programática com um objeto de controle de dispositivo que não está em execução, o aplicativo deve invocar [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) e passá-lo para os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="aeaf9-118">To programmatically register a device with a non-running device control object, the application must invoke [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) and pass it the following parameters:</span></span>

-   <span data-ttu-id="aeaf9-119">O texto da descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-119">The text of the device's description.</span></span>
-   <span data-ttu-id="aeaf9-120">O ProgID do objeto de controle de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-120">The ProgID of the device control object.</span></span>
-   <span data-ttu-id="aeaf9-121">Uma cadeia de inicialização que é passada para o método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) do objeto de controle de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-121">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="aeaf9-122">Uma ID de contêiner.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-122">A container ID.</span></span>
-   <span data-ttu-id="aeaf9-123">O local do diretório de recursos.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-123">The location of the resource directory.</span></span>
-   <span data-ttu-id="aeaf9-124">O tempo de vida do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-124">The lifetime of the device.</span></span>
-   <span data-ttu-id="aeaf9-125">O parâmetro de ID do dispositivo (um parâmetro OUT), que é o valor de retorno dessa chamada; um ponteiro para a ID do dispositivo é retornado em C++.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-125">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

<span data-ttu-id="aeaf9-126">Os registros de dispositivos que não estão em execução podem ser configurados para persistir nas inicializações do sistema (os dispositivos não são publicados durante a fase de desligamento).</span><span class="sxs-lookup"><span data-stu-id="aeaf9-126">The registrations of non-running devices can be configured to persist across system boots (the devices are unpublished during the shutdown phase).</span></span> <span data-ttu-id="aeaf9-127">Portanto, se eles estiverem configurados dessa forma, os dispositivos serão publicados e anunciados toda vez que o computador for inicializado.</span><span class="sxs-lookup"><span data-stu-id="aeaf9-127">Therefore, if they are configured this way, devices are published and announced every time the computer is booted.</span></span>

 

 




