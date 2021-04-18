---
title: Objeto de registro de dispositivo
description: Objeto de registro de dispositivo
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- SDK do Windows Media Format, objetos de registro do dispositivo
- ASF (Advanced Systems Format), objetos de registro de dispositivo
- ASF (formato de sistemas avançados), objetos de registro de dispositivo
- objetos, objetos de registro de dispositivo
- objetos de registro de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105783779"
---
# <a name="device-registration-object"></a><span data-ttu-id="12977-108">Objeto de registro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="12977-108">Device Registration Object</span></span>

<span data-ttu-id="12977-109">O objeto de registro de dispositivo gerencia o banco de dados de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12977-109">The device registration object manages the device registration database.</span></span> <span data-ttu-id="12977-110">Esse banco de dados armazena informações sobre dispositivos de rede, como players de vídeo de conjunto superior, que estão conectados ao computador cliente.</span><span class="sxs-lookup"><span data-stu-id="12977-110">This database stores information about network devices, such as set-top video players, that are connected to the client computer.</span></span> <span data-ttu-id="12977-111">A principal finalidade do banco de dados de registro de dispositivos é gerenciar dispositivos que usam o protocolo Windows Media DRM 10 para dispositivos de rede para receber fluxos de dados protegidos.</span><span class="sxs-lookup"><span data-stu-id="12977-111">The primary purpose of the device registration database is to manage devices that use the Windows Media DRM 10 for Network Devices protocol to receive secured data streams.</span></span>

<span data-ttu-id="12977-112">Se seu aplicativo der suporte ao Windows Media DRM 10 para dispositivos de rede, você deverá usar as interfaces desse objeto para registrar dispositivos de rede e para validar esses dispositivos.</span><span class="sxs-lookup"><span data-stu-id="12977-112">If your application supports Windows Media DRM 10 for Network Devices, you must use the interfaces of this object to register network devices, and to validate those devices.</span></span> <span data-ttu-id="12977-113">Você também pode usar o banco de dados de registro de dispositivo para armazenar informações sobre dispositivos de rede que não usam o Windows Media DRM 10 para dispositivos de rede, embora nem todas as informações no banco de dados sejam aplicadas a tais dispositivos.</span><span class="sxs-lookup"><span data-stu-id="12977-113">You can also use the device registration database to store information about network devices that do not use Windows Media DRM 10 for Network Devices, although not all of the information in the database will apply to such devices.</span></span>

<span data-ttu-id="12977-114">O objeto de registro de dispositivo é criado pela função [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) , que define um ponteiro para uma interface **IWMDeviceRegistration** .</span><span class="sxs-lookup"><span data-stu-id="12977-114">The device registration object is created by the [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) function, which sets a pointer to an **IWMDeviceRegistration** interface.</span></span> <span data-ttu-id="12977-115">Os outros métodos do objeto de registro de dispositivo podem ser obtidos chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="12977-115">The other methods of the device registration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="12977-116">As interfaces a seguir têm suporte do objeto de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12977-116">The following interfaces are supported by the device registration object.</span></span>



| <span data-ttu-id="12977-117">Interface</span><span class="sxs-lookup"><span data-stu-id="12977-117">Interface</span></span>                                              | <span data-ttu-id="12977-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="12977-118">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="12977-119">**IWMDeviceRegistration**</span><span class="sxs-lookup"><span data-stu-id="12977-119">**IWMDeviceRegistration**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | <span data-ttu-id="12977-120">Gerencia o banco de dados de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12977-120">Manages the device registration database.</span></span> |
| [<span data-ttu-id="12977-121">**IWMDRMMessageParser**</span><span class="sxs-lookup"><span data-stu-id="12977-121">**IWMDRMMessageParser**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | <span data-ttu-id="12977-122">Analisa as mensagens enviadas por dispositivos.</span><span class="sxs-lookup"><span data-stu-id="12977-122">Parses messages sent by devices.</span></span>          |
| [<span data-ttu-id="12977-123">**IWMProximityDetection**</span><span class="sxs-lookup"><span data-stu-id="12977-123">**IWMProximityDetection**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | <span data-ttu-id="12977-124">Gerencia a validação de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="12977-124">Manages device validation.</span></span>                |



 

<span data-ttu-id="12977-125">A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para usar os métodos da interface **IWMProximityDetection** .</span><span class="sxs-lookup"><span data-stu-id="12977-125">The following callback interface must be implemented by the application in order to use the methods of the **IWMProximityDetection** interface.</span></span>



| <span data-ttu-id="12977-126">Interface</span><span class="sxs-lookup"><span data-stu-id="12977-126">Interface</span></span>                                      | <span data-ttu-id="12977-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="12977-127">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="12977-128">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="12977-128">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="12977-129">Recebe mensagens de status de processos que são executados em um thread separado.</span><span class="sxs-lookup"><span data-stu-id="12977-129">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="12977-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12977-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12977-131">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="12977-131">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




