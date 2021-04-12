---
title: Interface IWMDRMDevice
description: Essa interface não deve ser implementada por um provedor de serviços, mas é fornecida para fins de documentação completa. A interface IWMDRMDevice permite que um provedor de conteúdo seguro se comunique com dispositivos que usam o Windows Media DRM 10 para dispositivos portáteis.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, descrita
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294173"
---
# <a name="iwmdrmdevice-interface"></a><span data-ttu-id="560c1-105">Interface IWMDRMDevice</span><span class="sxs-lookup"><span data-stu-id="560c1-105">IWMDRMDevice interface</span></span>

<span data-ttu-id="560c1-106">Essa interface não deve ser implementada por um provedor de serviços, mas é fornecida para fins de documentação completa.</span><span class="sxs-lookup"><span data-stu-id="560c1-106">This interface is not intended to be implemented by a service provider, but is provided for purposes of complete documentation.</span></span>

<span data-ttu-id="560c1-107">A interface **IWMDRMDevice** permite que um provedor de conteúdo seguro se comunique com dispositivos que usam o Windows Media DRM 10 para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="560c1-107">The **IWMDRMDevice** interface enables a secure content provider to communicate with devices that use Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="members"></a><span data-ttu-id="560c1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="560c1-108">Members</span></span>

<span data-ttu-id="560c1-109">A interface **IWMDRMDevice** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="560c1-109">The **IWMDRMDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="560c1-110">**IWMDRMDevice** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="560c1-110">**IWMDRMDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="560c1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="560c1-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="560c1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="560c1-112">Methods</span></span>

<span data-ttu-id="560c1-113">A interface **IWMDRMDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="560c1-113">The **IWMDRMDevice** interface has these methods.</span></span>



| <span data-ttu-id="560c1-114">Método</span><span class="sxs-lookup"><span data-stu-id="560c1-114">Method</span></span>                                                                  | <span data-ttu-id="560c1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="560c1-115">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="560c1-116">**CleanDataStore**</span><span class="sxs-lookup"><span data-stu-id="560c1-116">**CleanDataStore**</span></span>](iwmdrmdevice-cleandatastore.md)                   | <span data-ttu-id="560c1-117">Inicia o processo de limpeza do armazenamento de dados DRM no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="560c1-117">Starts the process of cleaning the DRM data store on the device.</span></span><br/>                  |
| [<span data-ttu-id="560c1-118">**GetDeviceCertificate**</span><span class="sxs-lookup"><span data-stu-id="560c1-118">**GetDeviceCertificate**</span></span>](iwmdrmdevice-getdevicecertificate.md)       | <span data-ttu-id="560c1-119">Recupera o certificado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="560c1-119">Retrieves the device certificate.</span></span><br/>                                                 |
| [<span data-ttu-id="560c1-120">**GetMeterChallenge**</span><span class="sxs-lookup"><span data-stu-id="560c1-120">**GetMeterChallenge**</span></span>](iwmdrmdevice-getmeterchallenge.md)             | <span data-ttu-id="560c1-121">Recupera o desafio de medição.</span><span class="sxs-lookup"><span data-stu-id="560c1-121">Retrieves the metering challenge.</span></span><br/>                                                 |
| [<span data-ttu-id="560c1-122">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="560c1-122">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)                   | <span data-ttu-id="560c1-123">Recupera o relógio seguro.</span><span class="sxs-lookup"><span data-stu-id="560c1-123">Retrieves the secure clock.</span></span><br/>                                                       |
| [<span data-ttu-id="560c1-124">**GetSecureClockChallenge**</span><span class="sxs-lookup"><span data-stu-id="560c1-124">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md) | <span data-ttu-id="560c1-125">Recupera o desafio do clock seguro.</span><span class="sxs-lookup"><span data-stu-id="560c1-125">Retrieves the secure clock challenge.</span></span><br/>                                             |
| [<span data-ttu-id="560c1-126">**Getsincronizarlist**</span><span class="sxs-lookup"><span data-stu-id="560c1-126">**GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)                         | <span data-ttu-id="560c1-127">Recupera a lista de sincronização de licenças.</span><span class="sxs-lookup"><span data-stu-id="560c1-127">Retrieves the license synchronization list.</span></span><br/>                                       |
| [<span data-ttu-id="560c1-128">**IsWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="560c1-128">**IsWMDRMDevice**</span></span>](iwmdrmdevice-iswmdrmdevice.md)                     | <span data-ttu-id="560c1-129">Determina se o dispositivo dá suporte a Windows Media DRM 10 para dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="560c1-129">Determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span><br/> |
| [<span data-ttu-id="560c1-130">**SetLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="560c1-130">**SetLicenseResponse**</span></span>](iwmdrmdevice-setlicenseresponse.md)           | <span data-ttu-id="560c1-131">Define a resposta da licença.</span><span class="sxs-lookup"><span data-stu-id="560c1-131">Sets the license response.</span></span><br/>                                                        |
| [<span data-ttu-id="560c1-132">**SetMeterResponse**</span><span class="sxs-lookup"><span data-stu-id="560c1-132">**SetMeterResponse**</span></span>](iwmdrmdevice-setmeterresponse.md)               | <span data-ttu-id="560c1-133">Define a resposta de medição.</span><span class="sxs-lookup"><span data-stu-id="560c1-133">Sets the metering response.</span></span><br/>                                                       |
| [<span data-ttu-id="560c1-134">**SetSecureClockResponse**</span><span class="sxs-lookup"><span data-stu-id="560c1-134">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)   | <span data-ttu-id="560c1-135">Define a resposta de clock seguro.</span><span class="sxs-lookup"><span data-stu-id="560c1-135">Sets the secure clock response.</span></span><br/>                                                   |



 

## <a name="see-also"></a><span data-ttu-id="560c1-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="560c1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="560c1-137">**Interfaces para provedores de serviços**</span><span class="sxs-lookup"><span data-stu-id="560c1-137">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> </dl>

 

