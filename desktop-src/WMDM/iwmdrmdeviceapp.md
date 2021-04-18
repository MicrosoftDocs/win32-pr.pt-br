---
title: Interface IWMDRMDeviceApp
description: A interface IWMDRMDeviceApp permite que um aplicativo seja medido, sincronize licenças e atualize os componentes DRM de um dispositivo.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos
- Interface IWMDRMDeviceApp Windows Media Gerenciador de Dispositivos, descrita
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105800182"
---
# <a name="iwmdrmdeviceapp-interface"></a><span data-ttu-id="c2b5a-105">Interface IWMDRMDeviceApp</span><span class="sxs-lookup"><span data-stu-id="c2b5a-105">IWMDRMDeviceApp interface</span></span>

<span data-ttu-id="c2b5a-106">\[O recurso DRM do Windows Media foi preterido e não deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-106">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="c2b5a-107">Em vez disso, use [o Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="c2b5a-107">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="c2b5a-108">A interface **IWMDRMDeviceApp** permite que um aplicativo seja medido, sincronize licenças e atualize os componentes DRM de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-108">The **IWMDRMDeviceApp** interface enables an application to meter, synchronize licenses, and update a device's DRM components.</span></span> <span data-ttu-id="c2b5a-109">Esta interface só funcionará com dispositivos que dão suporte ao Windows Media DRM 10 para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-109">This interface will only work with devices that support Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="c2b5a-110">Para obter essa interface, chame **CoCreateInstance**, passando em CLSID \_ WMDRMDeviceApp.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-110">To get this interface, call **CoCreateInstance**, passing in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="c2b5a-111">Essa interface é definida no arquivo de cabeçalho criado a partir de WMDRMDeviceApp. idl.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-111">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="c2b5a-112">Esse cabeçalho **\# inclui** os s "WMDM. h".</span><span class="sxs-lookup"><span data-stu-id="c2b5a-112">This header **\#include** s "wmdm.h".</span></span> <span data-ttu-id="c2b5a-113">Talvez seja necessário alterar esse nome de arquivo para corresponder ao cabeçalho criado a partir de WMDM. idl.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-113">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="c2b5a-114">Membros</span><span class="sxs-lookup"><span data-stu-id="c2b5a-114">Members</span></span>

<span data-ttu-id="c2b5a-115">A interface **IWMDRMDeviceApp** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c2b5a-115">The **IWMDRMDeviceApp** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c2b5a-116">**IWMDRMDeviceApp** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c2b5a-116">**IWMDRMDeviceApp** also has these types of members:</span></span>

-   [<span data-ttu-id="c2b5a-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2b5a-117">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c2b5a-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2b5a-118">Methods</span></span>

<span data-ttu-id="c2b5a-119">A interface **IWMDRMDeviceApp** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-119">The **IWMDRMDeviceApp** interface has these methods.</span></span>



| <span data-ttu-id="c2b5a-120">Método</span><span class="sxs-lookup"><span data-stu-id="c2b5a-120">Method</span></span>                                                                   | <span data-ttu-id="c2b5a-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2b5a-121">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2b5a-122">**AcquireDeviceData**</span><span class="sxs-lookup"><span data-stu-id="c2b5a-122">**AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)           | <span data-ttu-id="c2b5a-123">Inicializa ou redefine um relógio seguro do dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2b5a-123">Initializes or resets a device secure clock</span></span><br/>                                                                                     |
| [<span data-ttu-id="c2b5a-124">**GenerateMeterChallenge**</span><span class="sxs-lookup"><span data-stu-id="c2b5a-124">**GenerateMeterChallenge**</span></span>](iwmdrmdeviceapp-generatemeterchallenge.md) | <span data-ttu-id="c2b5a-125">Adquire dados de medição de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-125">Acquires metering data from a device.</span></span><br/>                                                                                           |
| [<span data-ttu-id="c2b5a-126">**ProcessMeterResponse**</span><span class="sxs-lookup"><span data-stu-id="c2b5a-126">**ProcessMeterResponse**</span></span>](iwmdrmdeviceapp-processmeterresponse.md)     | <span data-ttu-id="c2b5a-127">Redefine algumas ou todas as contagens de medição em um dispositivo, depois que os dados do dispositivo tiverem sido enviados e processados pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-127">Resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span><br/> |
| [<span data-ttu-id="c2b5a-128">**QueryDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="c2b5a-128">**QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)           | <span data-ttu-id="c2b5a-129">Consulta um dispositivo quanto ao seu status e recursos de DRM atuais.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-129">Queries a device for its current DRM status and capabilities.</span></span><br/>                                                                   |
| [<span data-ttu-id="c2b5a-130">**SynchronizeLicenses**</span><span class="sxs-lookup"><span data-stu-id="c2b5a-130">**SynchronizeLicenses**</span></span>](iwmdrmdeviceapp-synchronizelicenses.md)       | <span data-ttu-id="c2b5a-131">Atualiza licenças em um dispositivo quando elas estiverem próximas de expirar.</span><span class="sxs-lookup"><span data-stu-id="c2b5a-131">Updates licenses on a device when they are close to expiring.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="c2b5a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2b5a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b5a-133">**Lidando com conteúdo protegido no aplicativo**</span><span class="sxs-lookup"><span data-stu-id="c2b5a-133">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="c2b5a-134">**Interfaces para aplicativos**</span><span class="sxs-lookup"><span data-stu-id="c2b5a-134">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="c2b5a-135">**Uso de conteúdo de medição**</span><span class="sxs-lookup"><span data-stu-id="c2b5a-135">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

