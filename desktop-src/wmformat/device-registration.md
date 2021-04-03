---
title: Registro de dispositivo
description: Registro de dispositivo
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- SDK do Windows Media Format, registro de dispositivo
- SDK do Windows Media Format, registro de dispositivos
- ASF (Advanced Systems Format), registro de dispositivo
- ASF (formato de sistemas avançados), registro de dispositivo
- ASF (Advanced Systems Format), registro de dispositivos
- ASF (formato de sistemas avançados), registro de dispositivos
- DRM (gerenciamento de direitos digitais), registro de dispositivo
- DRM (gerenciamento de direitos digitais), registro de dispositivo
- DRM (gerenciamento de direitos digitais), registro de dispositivos
- DRM (gerenciamento de direitos digitais), registro de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007110"
---
# <a name="device-registration"></a><span data-ttu-id="a809d-113">Registro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a809d-113">Device Registration</span></span>

<span data-ttu-id="a809d-114">O SDK do Windows Media Format fornece acesso ao banco de dados de registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a809d-114">The Windows Media Format SDK provides access to the device registration database.</span></span> <span data-ttu-id="a809d-115">Esse banco de dados é protegido no computador cliente e é usado para registrar dispositivos que dão suporte ao Windows Media DRM 10 para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="a809d-115">This database is secured on the client computer and is used to register devices that support Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="a809d-116">Quando um dispositivo é adicionado a uma rede à qual o computador cliente está conectado, o dispositivo tenta contatar um aplicativo Windows Media DRM 10 para dispositivos de rede transmissor.</span><span class="sxs-lookup"><span data-stu-id="a809d-116">When a device is added to a network to which the client computer is connected, the device attempts to contact a Windows Media DRM 10 for Network Devices transmitter application.</span></span> <span data-ttu-id="a809d-117">Depois de estabelecer as comunicações, o dispositivo envia uma mensagem de solicitação de registro.</span><span class="sxs-lookup"><span data-stu-id="a809d-117">After establishing communications, the device sends a registration request message.</span></span>

<span data-ttu-id="a809d-118">Seu aplicativo deve executar as seguintes etapas ao receber uma mensagem de solicitação de registro:</span><span class="sxs-lookup"><span data-stu-id="a809d-118">Your application should perform the following steps when it receives a registration request message:</span></span>

1.  <span data-ttu-id="a809d-119">Analise a mensagem chamando o método [**IWMDRMMessageParser::P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) .</span><span class="sxs-lookup"><span data-stu-id="a809d-119">Parse the message by calling the [**IWMDRMMessageParser::ParseRegistrationReqMsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) method.</span></span> <span data-ttu-id="a809d-120">Esse método recupera o certificado do dispositivo e o número de série do dispositivo, ambos necessários para identificar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a809d-120">This method retrieves the device certificate and the device serial number, both of which are needed to identify the device.</span></span>
2.  <span data-ttu-id="a809d-121">Chame o método [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , passando o certificado e o número de série do dispositivo recuperado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="a809d-121">Call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method, passing in the certificate and device serial number retrieved in step 1.</span></span> <span data-ttu-id="a809d-122">Se o dispositivo for encontrado, ele já estará registrado e você poderá ignorar a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="a809d-122">If the device is found, it is already registered and you can skip the next step.</span></span>
3.  <span data-ttu-id="a809d-123">Chame o método [**IWMDeviceRegistration:: RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) para adicionar o dispositivo ao banco de dados de registro do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a809d-123">Call the [**IWMDeviceRegistration::RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) method to add the device to the device registration database.</span></span>

<span data-ttu-id="a809d-124">Você pode acessar informações sobre qualquer dispositivo no banco de dados de registro recuperando o objeto de dispositivo registrado associado a ele.</span><span class="sxs-lookup"><span data-stu-id="a809d-124">You can access information about any device in the registration database by retrieving the registered device object associated with it.</span></span> <span data-ttu-id="a809d-125">Há duas maneiras de obter um objeto de dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="a809d-125">There are two ways to get a registered device object.</span></span> <span data-ttu-id="a809d-126">Se você tiver o certificado e o número de série do dispositivo, poderá chamar o método [**IWMDeviceRegistration:: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) .</span><span class="sxs-lookup"><span data-stu-id="a809d-126">If you have the certificate and serial number of the device, you can call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method.</span></span> <span data-ttu-id="a809d-127">Se você não tiver o certificado e o número de série do dispositivo, poderá enumerar todos os dispositivos no banco de dados chamando [**IWMDeviceRegistration:: GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) seguido por chamadas repetidas para [**IWMDeviceRegistration:: GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) até que uma chamada retorne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="a809d-127">If you do not have the certificate and serial number of the device, you can enumerate all the devices in the database by calling [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) followed by repeated calls to [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) until a call returns S\_FALSE.</span></span>

<span data-ttu-id="a809d-128">Antes que o aplicativo possa enviar dados para um dispositivo, você deve garantir que o dispositivo seja aprovado, validado e aberto.</span><span class="sxs-lookup"><span data-stu-id="a809d-128">Before your application can send data to a device, you must ensure that the device is approved, validated, and open.</span></span>

<span data-ttu-id="a809d-129">A aprovação do dispositivo deve envolver a interação com o usuário.</span><span class="sxs-lookup"><span data-stu-id="a809d-129">Device approval should involve interaction with the user.</span></span> <span data-ttu-id="a809d-130">Quando um dispositivo envia uma mensagem de registro, seu aplicativo pode solicitar que o usuário decida se o dispositivo é aquele que deve receber os dados desse usuário.</span><span class="sxs-lookup"><span data-stu-id="a809d-130">When a device sends a registration message, your application can prompt the user to decide whether the device is one that should receive that user's data.</span></span> <span data-ttu-id="a809d-131">Em seguida, atualize o banco de dados de registro do dispositivo chamando o método [**IWMRegisteredDevice:: Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) , passando **true** ou **false** conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="a809d-131">Then update the device registration database by calling the [**IWMRegisteredDevice::Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) method, passing **TRUE** or **FALSE** as appropriate.</span></span>

<span data-ttu-id="a809d-132">A validação também é chamada de detecção de proximidade.</span><span class="sxs-lookup"><span data-stu-id="a809d-132">Validation is also called proximity detection.</span></span> <span data-ttu-id="a809d-133">Esse é um processo pelo qual os objetos DRM internos do Windows Media Format SDK determinam se o dispositivo é "próximo" o suficiente para o computador que está executando seu aplicativo para transmitir mídia com segurança.</span><span class="sxs-lookup"><span data-stu-id="a809d-133">This is a process by which the internal DRM objects of the Windows Media Format SDK determine whether the device is "near" enough to the computer running your application to securely transmit media.</span></span> <span data-ttu-id="a809d-134">A proximidade é determinada pelo tempo necessário para obter uma resposta a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="a809d-134">Nearness is determined by the time it takes to get a response to a message.</span></span> <span data-ttu-id="a809d-135">Esse recurso destina-se a impedir que usuários não autorizados acessem sua rede e obtenham sua mídia segura.</span><span class="sxs-lookup"><span data-stu-id="a809d-135">This feature is intended to prevent unauthorized users from accessing your network and obtaining your secured media.</span></span> <span data-ttu-id="a809d-136">Para obter mais informações, consulte [executando a detecção de proximidade](performing-proximity-detection.md).</span><span class="sxs-lookup"><span data-stu-id="a809d-136">For more information, see [Performing Proximity Detection](performing-proximity-detection.md).</span></span>

<span data-ttu-id="a809d-137">Para abrir um dispositivo, chame [**IWMRegisteredDevice:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span><span class="sxs-lookup"><span data-stu-id="a809d-137">To open a device, call [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span></span>

> [!Note]  
> <span data-ttu-id="a809d-138">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="a809d-138">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a809d-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a809d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a809d-140">**IWMRegisteredDevice**</span><span class="sxs-lookup"><span data-stu-id="a809d-140">**IWMRegisteredDevice**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[<span data-ttu-id="a809d-141">**Usando o protocolo Windows Media DRM 10 para dispositivos de rede**</span><span class="sxs-lookup"><span data-stu-id="a809d-141">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




