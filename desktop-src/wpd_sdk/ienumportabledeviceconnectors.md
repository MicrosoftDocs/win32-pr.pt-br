---
description: Dá suporte à enumeração de interfaces IPortableDeviceConnector, representando dispositivos MTP/Bluetooth que foram emparelhados com o PC.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Interface IEnumPortableDeviceConnectors (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169559"
---
# <a name="ienumportabledeviceconnectors-interface"></a><span data-ttu-id="58364-103">Interface IEnumPortableDeviceConnectors</span><span class="sxs-lookup"><span data-stu-id="58364-103">IEnumPortableDeviceConnectors interface</span></span>

<span data-ttu-id="58364-104">A interface **IEnumPortableDeviceConnectors** dá suporte à enumeração de interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , representando dispositivos MTP/Bluetooth que foram emparelhados com o PC.</span><span class="sxs-lookup"><span data-stu-id="58364-104">The **IEnumPortableDeviceConnectors** interface supports the enumeration of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces, representing MTP/Bluetooth devices that were paired with the PC.</span></span> <span data-ttu-id="58364-105">Observe que isso recuperará todos os dispositivos emparelhados anteriormente, incluindo os dispositivos emparelhados, mas desconectados.</span><span class="sxs-lookup"><span data-stu-id="58364-105">Note that this will retrieve all previously-paired devices, including devices that are paired but disconnected.</span></span> <span data-ttu-id="58364-106">Para determinar se um dispositivo ainda está conectado, consulte a propriedade **DEVPKEY \_ MTPBTH \_ IsConnected** para esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58364-106">To determine if a device is still connected, query the **DEVPKEY\_MTPBTH\_IsConnected** property for that device.</span></span>

## <a name="members"></a><span data-ttu-id="58364-107">Membros</span><span class="sxs-lookup"><span data-stu-id="58364-107">Members</span></span>

<span data-ttu-id="58364-108">A interface **IEnumPortableDeviceConnectors** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="58364-108">The **IEnumPortableDeviceConnectors** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="58364-109">**IEnumPortableDeviceConnectors** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="58364-109">**IEnumPortableDeviceConnectors** also has these types of members:</span></span>

-   [<span data-ttu-id="58364-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="58364-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="58364-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="58364-111">Methods</span></span>

<span data-ttu-id="58364-112">A interface **IEnumPortableDeviceConnectors** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="58364-112">The **IEnumPortableDeviceConnectors** interface has these methods.</span></span>



| <span data-ttu-id="58364-113">Método</span><span class="sxs-lookup"><span data-stu-id="58364-113">Method</span></span>                                               | <span data-ttu-id="58364-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="58364-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58364-115">**8i**</span><span class="sxs-lookup"><span data-stu-id="58364-115">**Clone**</span></span>](ienumportabledeviceconnectors-clone.md) | <span data-ttu-id="58364-116">Cria uma cópia da interface **IEnumPortableDeviceConnectors** atual.</span><span class="sxs-lookup"><span data-stu-id="58364-116">Creates a copy of the current **IEnumPortableDeviceConnectors** interface.</span></span><br/>                                                       |
| [<span data-ttu-id="58364-117">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="58364-117">**Next**</span></span>](ienumportabledeviceconnectors-next.md)   | <span data-ttu-id="58364-118">Recupera o próximo um ou mais objetos [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="58364-118">Retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="58364-119">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="58364-119">**Reset**</span></span>](ienumportabledeviceconnectors-reset.md) | <span data-ttu-id="58364-120">Redefine a sequência de enumeração para o início.</span><span class="sxs-lookup"><span data-stu-id="58364-120">Resets the enumeration sequence to the beginning.</span></span><br/>                                                                                |
| [<span data-ttu-id="58364-121">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="58364-121">**Skip**</span></span>](ienumportabledeviceconnectors-skip.md)   | <span data-ttu-id="58364-122">Ignora o número especificado de dispositivos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="58364-122">Skips the specified number of devices in the enumeration sequence.</span></span><br/>                                                               |



 

## <a name="requirements"></a><span data-ttu-id="58364-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58364-123">Requirements</span></span>



| <span data-ttu-id="58364-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="58364-124">Requirement</span></span> | <span data-ttu-id="58364-125">Valor</span><span class="sxs-lookup"><span data-stu-id="58364-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58364-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58364-126">Minimum supported client</span></span><br/> | <span data-ttu-id="58364-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="58364-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="58364-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58364-128">Minimum supported server</span></span><br/> | <span data-ttu-id="58364-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="58364-129">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="58364-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58364-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="58364-131"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="58364-131"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="58364-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="58364-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="58364-133"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="58364-133"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="58364-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58364-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="58364-135"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58364-135"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 

