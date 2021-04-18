---
description: A interface do dispositivo pode ser descrita por um valor de GUID. Os dispositivos portáteis do Windows definem a seguinte interface de dispositivo.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: GUIDs da interface do dispositivo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c2f97e050f839a268048aaaabac46b9e7698ee9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814114"
---
# <a name="device-interface-guids"></a><span data-ttu-id="6df91-104">GUIDs da interface do dispositivo</span><span class="sxs-lookup"><span data-stu-id="6df91-104">Device Interface GUIDs</span></span>

<span data-ttu-id="6df91-105">A interface do dispositivo pode ser descrita por um valor de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="6df91-105">The device interface can be described by a **GUID** value.</span></span> <span data-ttu-id="6df91-106">Os dispositivos portáteis do Windows definem a seguinte interface de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6df91-106">Windows Portable Devices defines the following device interface.</span></span>



| <span data-ttu-id="6df91-107">Constante</span><span class="sxs-lookup"><span data-stu-id="6df91-107">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="6df91-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6df91-108">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <span data-ttu-id="6df91-109"><dt>**GUID \_ DEVINTERFACE \_ WPD**</dt></span><span class="sxs-lookup"><span data-stu-id="6df91-109"><dt>**GUID\_DEVINTERFACE\_WPD**</dt></span></span> </dl>                          | <span data-ttu-id="6df91-110">Identifica os dispositivos que aparecem em uma enumeração WPD normal.</span><span class="sxs-lookup"><span data-stu-id="6df91-110">Identifies devices that appear in a normal WPD enumeration.</span></span> <span data-ttu-id="6df91-111">Qualquer dispositivo que registra esse GUID de interface será enumerado quando um aplicativo chamar o método [**IPortableDeviceManager:: Devices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .</span><span class="sxs-lookup"><span data-stu-id="6df91-111">Any device that registers this interface GUID will be enumerated when an application calls the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.</span></span><br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <span data-ttu-id="6df91-112"><dt>**GUID \_ DEVINTERFACE \_ WPD \_ particular**</dt></span><span class="sxs-lookup"><span data-stu-id="6df91-112"><dt>**GUID\_DEVINTERFACE\_WPD\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="6df91-113">Identifica os dispositivos que não serão exibidos durante uma enumeração WPD normal.</span><span class="sxs-lookup"><span data-stu-id="6df91-113">Identifies devices that will not appear during a normal WPD enumeration.</span></span> <span data-ttu-id="6df91-114">Qualquer dispositivo que registra esse GUID de interface será enumerado somente quando um aplicativo chamar o método [**IPortableDeviceManager:: GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) .</span><span class="sxs-lookup"><span data-stu-id="6df91-114">Any device that registers this interface GUID will be enumerated only when an application calls the [**IPortableDeviceManager::GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) method.</span></span><br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <span data-ttu-id="6df91-115"><dt>**\_serviço GUID DEVINTERFACE \_ WPD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6df91-115"><dt>**GUID\_DEVINTERFACE\_WPD\_SERVICE**</dt></span></span> </dl> | <span data-ttu-id="6df91-116">No Windows 7, os aplicativos podem enumerar todos os serviços de dispositivos WPD chamando [**IPortableDeviceServiceManager:: Getdeviceservices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) e usando essa classe de interface como o GUID do tipo de serviço.</span><span class="sxs-lookup"><span data-stu-id="6df91-116">In Windows 7, applications can enumerate all WPD device services by calling [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) and using this interface class as the service-type GUID.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="6df91-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6df91-117">Requirements</span></span>



| <span data-ttu-id="6df91-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6df91-118">Requirement</span></span> | <span data-ttu-id="6df91-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6df91-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df91-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6df91-120">Header</span></span><br/> | <dl> <span data-ttu-id="6df91-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="6df91-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df91-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="6df91-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df91-123">Referência de programação</span><span class="sxs-lookup"><span data-stu-id="6df91-123">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




