---
description: Os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos de recurso.
ms.assetid: 0cbf8777-5cea-4839-a4c3-366bb9e18488
title: Atributos de recurso (PortableDevice. h)
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
ms.openlocfilehash: 300add64d332dbc509bef6ec5bb2ad124f7a6b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791417"
---
# <a name="resource-attributes"></a><span data-ttu-id="94ac6-103">Atributos de recurso</span><span class="sxs-lookup"><span data-stu-id="94ac6-103">Resource Attributes</span></span>

<span data-ttu-id="94ac6-104">Os dispositivos portáteis do Windows oferecem suporte aos seguintes atributos de recurso.</span><span class="sxs-lookup"><span data-stu-id="94ac6-104">Windows Portable Devices supports the following resource attributes.</span></span> <span data-ttu-id="94ac6-105">Esses atributos são retornados pelos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="94ac6-105">These attributes are returned by the following methods:</span></span>

-   [<span data-ttu-id="94ac6-106">**IPortableDeviceResources:: getresourceattributes**</span><span class="sxs-lookup"><span data-stu-id="94ac6-106">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfixedpropertyattributes)



| <span data-ttu-id="94ac6-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="94ac6-107">Attribute</span></span>                                                  | <span data-ttu-id="94ac6-108">VarType</span><span class="sxs-lookup"><span data-stu-id="94ac6-108">VarType</span></span>      | <span data-ttu-id="94ac6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="94ac6-109">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ac6-110">**o \_ atributo de recurso WPD \_ \_ pode \_ excluir**</span><span class="sxs-lookup"><span data-stu-id="94ac6-110">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE**</span></span>                  | <span data-ttu-id="94ac6-111">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="94ac6-111">**VT\_BOOL**</span></span> | <span data-ttu-id="94ac6-112">Um valor booliano que especifica se um cliente tem permissão para excluir o recurso.</span><span class="sxs-lookup"><span data-stu-id="94ac6-112">A Boolean value that specifies whether a client has permission to delete the resource.</span></span> <span data-ttu-id="94ac6-113">Se estiver ausente, presume-se que seja falso.</span><span class="sxs-lookup"><span data-stu-id="94ac6-113">If absent, it is assumed to be false.</span></span>                |
| <span data-ttu-id="94ac6-114">**o \_ atributo de recurso WPD \_ \_ pode \_ ler**</span><span class="sxs-lookup"><span data-stu-id="94ac6-114">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ**</span></span>                    | <span data-ttu-id="94ac6-115">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="94ac6-115">**VT\_BOOL**</span></span> | <span data-ttu-id="94ac6-116">Um valor booliano que especifica se um cliente tem permissão para abrir o recurso para acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="94ac6-116">A Boolean value that specifies whether a client has permission to open the resource for Read access.</span></span> <span data-ttu-id="94ac6-117">Se estiver ausente, presume-se que seja falso.</span><span class="sxs-lookup"><span data-stu-id="94ac6-117">If absent, it is assumed to be False.</span></span>  |
| <span data-ttu-id="94ac6-118">**o \_ atributo de recurso WPD \_ \_ pode \_ gravar**</span><span class="sxs-lookup"><span data-stu-id="94ac6-118">**WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE**</span></span>                   | <span data-ttu-id="94ac6-119">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="94ac6-119">**VT\_BOOL**</span></span> | <span data-ttu-id="94ac6-120">Um valor booliano que especifica se um cliente tem permissão para abrir o recurso para acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="94ac6-120">A Boolean value that specifies whether a client has permission to open the resource for Write access.</span></span> <span data-ttu-id="94ac6-121">Se estiver ausente, presume-se que seja falso.</span><span class="sxs-lookup"><span data-stu-id="94ac6-121">If absent, it is assumed to be false.</span></span> |
| <span data-ttu-id="94ac6-122">**\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_**</span><span class="sxs-lookup"><span data-stu-id="94ac6-122">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE**</span></span>  | <span data-ttu-id="94ac6-123">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="94ac6-123">**VT\_UI4**</span></span>  | <span data-ttu-id="94ac6-124">O tamanho de buffer recomendado que um chamador deve usar para leituras em buffer do recurso.</span><span class="sxs-lookup"><span data-stu-id="94ac6-124">The recommended buffer size that a caller should use for buffered reads from the resource.</span></span>                                                  |
| <span data-ttu-id="94ac6-125">**\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de gravação \_ \_**</span><span class="sxs-lookup"><span data-stu-id="94ac6-125">**WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE**</span></span> | <span data-ttu-id="94ac6-126">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="94ac6-126">**VT\_UI4**</span></span>  | <span data-ttu-id="94ac6-127">O tamanho de buffer recomendado que um chamador deve usar para gravações em buffer no recurso.</span><span class="sxs-lookup"><span data-stu-id="94ac6-127">The recommended buffer size that a caller should use for buffered writes on the resource.</span></span>                                                   |
| <span data-ttu-id="94ac6-128">**\_ \_ Tamanho total do atributo de recurso WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="94ac6-128">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>                  | <span data-ttu-id="94ac6-129">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="94ac6-129">**VT\_UI8**</span></span>  | <span data-ttu-id="94ac6-130">O tamanho total dos dados do recurso, em bytes.</span><span class="sxs-lookup"><span data-stu-id="94ac6-130">The total size of the resource data, in bytes.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="94ac6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94ac6-131">Requirements</span></span>



| <span data-ttu-id="94ac6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="94ac6-132">Requirement</span></span> | <span data-ttu-id="94ac6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="94ac6-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ac6-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94ac6-134">Header</span></span><br/> | <dl> <span data-ttu-id="94ac6-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="94ac6-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94ac6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="94ac6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ac6-137">**Propriedades**</span><span class="sxs-lookup"><span data-stu-id="94ac6-137">**Properties**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




