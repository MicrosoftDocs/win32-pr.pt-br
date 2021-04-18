---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de atributo de recurso.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Propriedades do atributo de recurso (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814517"
---
# <a name="resource-attribute-properties"></a><span data-ttu-id="eef1a-103">Propriedades do atributo de recurso</span><span class="sxs-lookup"><span data-stu-id="eef1a-103">Resource Attribute Properties</span></span>

<span data-ttu-id="eef1a-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de atributo de recurso.</span><span class="sxs-lookup"><span data-stu-id="eef1a-104">Windows Portable Devices supports the following resource attribute properties.</span></span>



| <span data-ttu-id="eef1a-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="eef1a-105">Property</span></span>                                    | <span data-ttu-id="eef1a-106">VarType</span><span class="sxs-lookup"><span data-stu-id="eef1a-106">VarType</span></span>         | <span data-ttu-id="eef1a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="eef1a-107">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef1a-108">**\_chave de \_ recurso de atributo de recurso WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eef1a-108">**WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY**</span></span> | <span data-ttu-id="eef1a-109">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="eef1a-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="eef1a-110">Isso é um [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contém um único valor, que é a chave que identifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="eef1a-110">This is an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value, which is the key identifying the resource.</span></span>                     |
| <span data-ttu-id="eef1a-111">**\_formato de \_ atributo de recurso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="eef1a-111">**WPD\_RESOURCE\_ATTRIBUTE\_FORMAT**</span></span>        | <span data-ttu-id="eef1a-112">**CLSID do VT \_**</span><span class="sxs-lookup"><span data-stu-id="eef1a-112">**VT\_CLSID**</span></span>   | <span data-ttu-id="eef1a-113">Um valor de GUID que especifica o formato do recurso.</span><span class="sxs-lookup"><span data-stu-id="eef1a-113">A GUID value that specifies the format of the resource.</span></span> <span data-ttu-id="eef1a-114">Consulte [formatos de objeto](object-format-guids.md) para obter uma lista de formatos que são definidos por dispositivos portáteis do Windows.</span><span class="sxs-lookup"><span data-stu-id="eef1a-114">See [Object Formats](object-format-guids.md) for a list of formats that are defined by Windows Portable Devices.</span></span> |
| <span data-ttu-id="eef1a-115">**\_ \_ Tamanho total do atributo de recurso WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eef1a-115">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>   | <span data-ttu-id="eef1a-116">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="eef1a-116">**VT\_UI8**</span></span>     | <span data-ttu-id="eef1a-117">O tamanho total dos dados do recurso, em bytes.</span><span class="sxs-lookup"><span data-stu-id="eef1a-117">The total size of the resource data, in bytes.</span></span>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="eef1a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="eef1a-118">Remarks</span></span>

<span data-ttu-id="eef1a-119">Esses atributos são retornados pelo método [**IPortableDeviceResources:: Getresourceattributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="eef1a-119">These attributes are returned by the [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eef1a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eef1a-120">Requirements</span></span>



| <span data-ttu-id="eef1a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="eef1a-121">Requirement</span></span> | <span data-ttu-id="eef1a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="eef1a-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef1a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eef1a-123">Header</span></span><br/> | <dl> <span data-ttu-id="eef1a-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="eef1a-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef1a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="eef1a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef1a-126">**IPortableDeviceResources:: getresourceattributes**</span><span class="sxs-lookup"><span data-stu-id="eef1a-126">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[<span data-ttu-id="eef1a-127">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="eef1a-127">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




