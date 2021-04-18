---
description: O \_ tipo de enumeração de transportes de dispositivos WPD \_ especifica a relação de herança para um serviço. Essa enumeração é usada pela propriedade de \_ transporte do dispositivo WPD \_ .
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: Enumeração de WPD_DEVICE_TRANSPORTS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789338"
---
# <a name="wpd_device_transports-enumeration"></a><span data-ttu-id="13353-104">Enumeração de transportes de \_ dispositivos WPD \_</span><span class="sxs-lookup"><span data-stu-id="13353-104">WPD\_DEVICE\_TRANSPORTS enumeration</span></span>

<span data-ttu-id="13353-105">O tipo de enumeração de [**\_ \_ transportes de dispositivos WPD**](/windows/desktop/wpd_sdk/wpd-device-transports) especifica a relação de herança para um serviço.</span><span class="sxs-lookup"><span data-stu-id="13353-105">The [**WPD\_DEVICE\_TRANSPORTS**](/windows/desktop/wpd_sdk/wpd-device-transports) enumeration type specifies the inheritance relationship for a service.</span></span> <span data-ttu-id="13353-106">Essa enumeração é usada pela propriedade **de \_ \_ transporte do dispositivo WPD** .</span><span class="sxs-lookup"><span data-stu-id="13353-106">This enumeration is used by the **WPD\_DEVICE\_TRANSPORT** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="13353-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="13353-107">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a><span data-ttu-id="13353-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="13353-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="13353-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**\_transporte de dispositivo WPD \_ \_ não especificado**</span><span class="sxs-lookup"><span data-stu-id="13353-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**WPD\_DEVICE\_TRANSPORT\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="13353-110">O tipo de transporte não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="13353-110">The transport type was not specified.</span></span>

</dd> <dt>

<span data-ttu-id="13353-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**\_USB de \_ transporte de dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="13353-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD\_DEVICE\_TRANSPORT\_USB**</span></span>
</dt> <dd>

<span data-ttu-id="13353-112">O dispositivo está conectado por meio de USB.</span><span class="sxs-lookup"><span data-stu-id="13353-112">The device is connected through USB.</span></span>

</dd> <dt>

<span data-ttu-id="13353-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**\_IP de \_ transporte do dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="13353-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD\_DEVICE\_TRANSPORT\_IP**</span></span>
</dt> <dd>

<span data-ttu-id="13353-114">O dispositivo está conectado por meio do protocolo Internet (IP).</span><span class="sxs-lookup"><span data-stu-id="13353-114">The device is connected through Internet Protocol (IP).</span></span>

</dd> <dt>

<span data-ttu-id="13353-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**\_Bluetooth de \_ transporte de dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="13353-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD\_DEVICE\_TRANSPORT\_BLUETOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="13353-116">O dispositivo está conectado por meio de Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="13353-116">The device is connected through Bluetooth.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13353-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13353-117">Requirements</span></span>



| <span data-ttu-id="13353-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="13353-118">Requirement</span></span> | <span data-ttu-id="13353-119">Valor</span><span class="sxs-lookup"><span data-stu-id="13353-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="13353-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13353-120">Header</span></span><br/> | <dl> <span data-ttu-id="13353-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="13353-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

