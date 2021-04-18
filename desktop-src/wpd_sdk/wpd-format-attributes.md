---
description: 'Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos para formatos em um serviço de dispositivo. Esses atributos são retornados pelo método IPortableDeviceServiceCapabilities:: getformable.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Atributos de formato (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771778"
---
# <a name="format-attributes"></a><span data-ttu-id="f92b7-104">Atributos de formato</span><span class="sxs-lookup"><span data-stu-id="f92b7-104">Format Attributes</span></span>

<span data-ttu-id="f92b7-105">Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos para formatos em um serviço de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f92b7-105">For Windows 7, Windows Portable Devices supports the following attributes for formats on a device service.</span></span> <span data-ttu-id="f92b7-106">Esses atributos são retornados pelo método [**IPortableDeviceServiceCapabilities:: Getformable**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) .</span><span class="sxs-lookup"><span data-stu-id="f92b7-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method.</span></span>




| <span data-ttu-id="f92b7-107">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f92b7-107">**Attribute**</span></span>                        | <span data-ttu-id="f92b7-108">**VarType**</span><span class="sxs-lookup"><span data-stu-id="f92b7-108">**VarType**</span></span>    | <span data-ttu-id="f92b7-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f92b7-109">**Description**</span></span>                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f92b7-110">**\_MIME de \_ atributo de formato WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f92b7-110">**WPD\_FORMAT\_ATTRIBUTE\_MIMETYPE**</span></span> | <span data-ttu-id="f92b7-111">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="f92b7-111">**VT\_LPWSTR**</span></span> | <span data-ttu-id="f92b7-112">O tipo MIME de formato.</span><span class="sxs-lookup"><span data-stu-id="f92b7-112">The format MIME type.</span></span>                                                                                                     |
| <span data-ttu-id="f92b7-113">**\_nome do \_ atributo de formato WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f92b7-113">**WPD\_FORMAT\_ATTRIBUTE\_NAME**</span></span>     | <span data-ttu-id="f92b7-114">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="f92b7-114">**VT\_LPWSTR**</span></span> | <span data-ttu-id="f92b7-115">Uma cadeia de caracteres que especifica o nome amigável do formato do script.</span><span class="sxs-lookup"><span data-stu-id="f92b7-115">A string that specifies the script-friendly name of the format.</span></span> <span data-ttu-id="f92b7-116">Os caracteres válidos são alfanuméricos \[ a-zA-Z0-9 \] e ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="f92b7-116">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f92b7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f92b7-117">Requirements</span></span>



| <span data-ttu-id="f92b7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f92b7-118">Requirement</span></span> | <span data-ttu-id="f92b7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f92b7-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f92b7-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f92b7-120">Header</span></span><br/> | <dl> <span data-ttu-id="f92b7-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f92b7-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f92b7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f92b7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f92b7-123">**Propriedades e atributos**</span><span class="sxs-lookup"><span data-stu-id="f92b7-123">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




