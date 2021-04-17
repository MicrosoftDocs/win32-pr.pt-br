---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de dados da seção.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Propriedades de atributo de seção (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105808233"
---
# <a name="section-attribute-properties"></a><span data-ttu-id="53091-103">Propriedades de atributo de seção</span><span class="sxs-lookup"><span data-stu-id="53091-103">Section Attribute Properties</span></span>

<span data-ttu-id="53091-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de dados da seção.</span><span class="sxs-lookup"><span data-stu-id="53091-104">Windows Portable Devices supports the following section data properties.</span></span>



| <span data-ttu-id="53091-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="53091-105">Property</span></span>                                             | <span data-ttu-id="53091-106">VarType</span><span class="sxs-lookup"><span data-stu-id="53091-106">VarType</span></span>         | <span data-ttu-id="53091-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="53091-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53091-108">**\_comprimento de \_ dados da seção WPD \_**</span><span class="sxs-lookup"><span data-stu-id="53091-108">**WPD\_SECTION\_DATA\_LENGTH**</span></span>                       | <span data-ttu-id="53091-109">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="53091-109">**VT\_UI8**</span></span>     | <span data-ttu-id="53091-110">Especifica o comprimento do objeto referenciado.</span><span class="sxs-lookup"><span data-stu-id="53091-110">Specifies the length of the referenced object.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="53091-111">**\_deslocamento de \_ dados da seção WPD \_**</span><span class="sxs-lookup"><span data-stu-id="53091-111">**WPD\_SECTION\_DATA\_OFFSET**</span></span>                       | <span data-ttu-id="53091-112">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="53091-112">**VT\_UI8**</span></span>     | <span data-ttu-id="53091-113">Especifica o deslocamento de base zero dos dados para o objeto referenciado.</span><span class="sxs-lookup"><span data-stu-id="53091-113">Specifies the zero-based offset of the data for the referenced object.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="53091-114">**\_recurso de \_ \_ objeto referenciado de dados da \_ seção WPD \_**</span><span class="sxs-lookup"><span data-stu-id="53091-114">**WPD\_SECTION\_DATA\_REFERENCED\_OBJECT\_RESOURCE**</span></span> | <span data-ttu-id="53091-115">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="53091-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="53091-116">Um [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que contém um único valor que especifica a chave para um determinado recurso. Esse recurso é o objeto referenciado por \_ um \_ deslocamento de dados da seção WPD \_ e \_ comprimento de dados da seção WPD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="53091-116">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value that specifies the key for a given resource.This resource is the object referenced by WPD\_SECTION\_DATA\_OFFSET and WPD\_SECTION\_DATA\_LENGTH.</span></span><br/> <span data-ttu-id="53091-117">Se essa propriedade não existir, o \_ padrão de recursos WPD \_ será assumido.</span><span class="sxs-lookup"><span data-stu-id="53091-117">If this property doesn't exist, WPD\_RESOURCE\_DEFAULT is assumed.</span></span><br/> |
| <span data-ttu-id="53091-118">**\_unidades de \_ dados da seção WPD \_**</span><span class="sxs-lookup"><span data-stu-id="53091-118">**WPD\_SECTION\_DATA\_UNITS**</span></span>                        | <span data-ttu-id="53091-119">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="53091-119">**VT\_UI4**</span></span>     | <span data-ttu-id="53091-120">Especifica as unidades usadas para esse deslocamento, por exemplo, bytes, milissegundos e assim por diante. Os valores possíveis para essa propriedade são definidos na enumeração **de \_ \_ valores das \_ unidades \_ de dados da seção WPD** no arquivo PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="53091-120">Specifies the units used for this offset, for example, bytes, milliseconds, and so on.The possible values for this property are defined in the **WPD\_SECTION\_DATA\_UNITS\_VALUES** enumeration in the file PortableDevice.h.</span></span><br/> <span data-ttu-id="53091-121">Se nenhuma unidade for especificada, serão assumidos bytes.</span><span class="sxs-lookup"><span data-stu-id="53091-121">If no units are specified, bytes are assumed.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="53091-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53091-122">Requirements</span></span>



| <span data-ttu-id="53091-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="53091-123">Requirement</span></span> | <span data-ttu-id="53091-124">Valor</span><span class="sxs-lookup"><span data-stu-id="53091-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="53091-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53091-125">Header</span></span><br/> | <dl> <span data-ttu-id="53091-126"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="53091-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53091-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="53091-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53091-128">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="53091-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




