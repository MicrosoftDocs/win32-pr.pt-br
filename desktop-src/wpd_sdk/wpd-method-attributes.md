---
description: 'Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos para métodos de um serviço de dispositivo. Esses atributos são retornados pelo método IPortableDeviceServiceCapabilities:: getmethodattributes.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Atributos do método (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807139"
---
# <a name="method-attributes"></a><span data-ttu-id="2d343-104">Atributos de método</span><span class="sxs-lookup"><span data-stu-id="2d343-104">Method Attributes</span></span>

<span data-ttu-id="2d343-105">Para o Windows 7, os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos para métodos de um serviço de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d343-105">For Windows 7, Windows Portable Devices supports the following attributes for methods of a device service.</span></span> <span data-ttu-id="2d343-106">Esses atributos são retornados pelo método [**IPortableDeviceServiceCapabilities:: Getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) .</span><span class="sxs-lookup"><span data-stu-id="2d343-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method.</span></span>




| <span data-ttu-id="2d343-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="2d343-107">Attribute</span></span>                                      | <span data-ttu-id="2d343-108">VarType</span><span class="sxs-lookup"><span data-stu-id="2d343-108">VarType</span></span>         | <span data-ttu-id="2d343-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d343-109">Description</span></span>                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d343-110">**\_acesso de \_ atributo de método WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2d343-110">**WPD\_METHOD\_ATTRIBUTE\_ACCESS**</span></span>             | <span data-ttu-id="2d343-111">**CLSID do VT \_**</span><span class="sxs-lookup"><span data-stu-id="2d343-111">**VT\_CLSID**</span></span>   | <span data-ttu-id="2d343-112">O método necessário de acesso.</span><span class="sxs-lookup"><span data-stu-id="2d343-112">The required method access.</span></span>                                                                                               |
| <span data-ttu-id="2d343-113">**\_ \_ formato associado de atributo de método WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2d343-113">**WPD\_METHOD\_ATTRIBUTE\_ASSOCIATED\_FORMAT**</span></span> | <span data-ttu-id="2d343-114">**CLSID do VT \_**</span><span class="sxs-lookup"><span data-stu-id="2d343-114">**VT\_CLSID**</span></span>   | <span data-ttu-id="2d343-115">O formato associado ao método ou ao **GUID \_ NULL** se não houver nenhum formato associado.</span><span class="sxs-lookup"><span data-stu-id="2d343-115">The format associated with the method, or **GUID\_NULL** if there is no associated format.</span></span>                                |
| <span data-ttu-id="2d343-116">**\_nome do \_ atributo do método WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2d343-116">**WPD\_METHOD\_ATTRIBUTE\_NAME**</span></span>               | <span data-ttu-id="2d343-117">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="2d343-117">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="2d343-118">Uma cadeia de caracteres que especifica o nome amigável de script do método.</span><span class="sxs-lookup"><span data-stu-id="2d343-118">A string that specifies the script-friendly name of the method.</span></span> <span data-ttu-id="2d343-119">Os caracteres válidos são alfanuméricos \[ a-zA-Z0-9 \] e ' \_ '.</span><span class="sxs-lookup"><span data-stu-id="2d343-119">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="2d343-120">**\_parâmetros de \_ atributo do método WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2d343-120">**WPD\_METHOD\_ATTRIBUTE\_PARAMETERS**</span></span>         | <span data-ttu-id="2d343-121">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="2d343-121">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="2d343-122">Uma interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contém os parâmetros do método.</span><span class="sxs-lookup"><span data-stu-id="2d343-122">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that contains the method parameters.</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="2d343-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d343-123">Requirements</span></span>



| <span data-ttu-id="2d343-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d343-124">Requirement</span></span> | <span data-ttu-id="2d343-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2d343-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d343-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d343-126">Header</span></span><br/> | <dl> <span data-ttu-id="2d343-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d343-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d343-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d343-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d343-129">**Propriedades e atributos**</span><span class="sxs-lookup"><span data-stu-id="2d343-129">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




