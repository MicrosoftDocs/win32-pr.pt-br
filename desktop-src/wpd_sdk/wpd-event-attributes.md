---
description: 'Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos para eventos de um serviço de dispositivo. Esses atributos são retornados pelo método IPortableDeviceServiceCapabilities:: geteventattributes.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Atributos de evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788930"
---
# <a name="event-attributes-portabledeviceh"></a><span data-ttu-id="b0999-104">Atributos de evento (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="b0999-104">Event Attributes (PortableDevice.h)</span></span>

<span data-ttu-id="b0999-105">Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos para eventos de um serviço de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0999-105">For Windows 7, Windows Portable Devices supports the following attributes for events of a device service.</span></span> <span data-ttu-id="b0999-106">Esses atributos são retornados pelo método [**IPortableDeviceServiceCapabilities:: Geteventattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .</span><span class="sxs-lookup"><span data-stu-id="b0999-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method.</span></span>




| <span data-ttu-id="b0999-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="b0999-107">Attribute</span></span>                             | <span data-ttu-id="b0999-108">VarType</span><span class="sxs-lookup"><span data-stu-id="b0999-108">VarType</span></span>         | <span data-ttu-id="b0999-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0999-109">Description</span></span>                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0999-110">**\_nome do \_ atributo de evento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b0999-110">**WPD\_EVENT\_ATTRIBUTE\_NAME**</span></span>       | <span data-ttu-id="b0999-111">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="b0999-111">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="b0999-112">Uma cadeia de caracteres que especifica o nome amigável de script do evento.</span><span class="sxs-lookup"><span data-stu-id="b0999-112">A string that specifies the script-friendly name of the event.</span></span> <span data-ttu-id="b0999-113">Os caracteres válidos são alfanuméricos \[ a-zA-Z0-9 \] e ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="b0999-113">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="b0999-114">**\_Opções de \_ atributo de evento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b0999-114">**WPD\_EVENT\_ATTRIBUTE\_OPTIONS**</span></span>    | <span data-ttu-id="b0999-115">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="b0999-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="b0999-116">Um [**IPortableDeviceValues**](iportabledevicevalues.md) que contém as opções de evento.</span><span class="sxs-lookup"><span data-stu-id="b0999-116">An [**IPortableDeviceValues**](iportabledevicevalues.md) that contains the event options.</span></span>                               |
| <span data-ttu-id="b0999-117">**\_parâmetros de \_ atributo de evento WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b0999-117">**WPD\_EVENT\_ATTRIBUTE\_PARAMETERS**</span></span> | <span data-ttu-id="b0999-118">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="b0999-118">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="b0999-119">Um [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contém os parâmetros do evento.</span><span class="sxs-lookup"><span data-stu-id="b0999-119">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) that contains the event parameters.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="b0999-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0999-120">Requirements</span></span>



| <span data-ttu-id="b0999-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0999-121">Requirement</span></span> | <span data-ttu-id="b0999-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b0999-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0999-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0999-123">Header</span></span><br/> | <dl> <span data-ttu-id="b0999-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0999-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0999-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0999-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0999-126">**Propriedades e atributos**</span><span class="sxs-lookup"><span data-stu-id="b0999-126">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




