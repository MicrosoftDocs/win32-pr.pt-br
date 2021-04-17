---
description: O tipo de enumeração WpdAttributeForm descreve como uma propriedade armazena seus valores.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Enumeração WpdAttributeForm (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c70f68dc04adcb454fcc7c5ae301f0dabf60c28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751343"
---
# <a name="wpdattributeform-enumeration"></a><span data-ttu-id="68c28-103">Enumeração WpdAttributeForm</span><span class="sxs-lookup"><span data-stu-id="68c28-103">WpdAttributeForm enumeration</span></span>

<span data-ttu-id="68c28-104">O tipo de enumeração **WpdAttributeForm** descreve como uma propriedade armazena seus valores.</span><span class="sxs-lookup"><span data-stu-id="68c28-104">The **WpdAttributeForm** enumeration type describes how a property stores its values.</span></span>

## <a name="syntax"></a><span data-ttu-id="68c28-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68c28-105">Syntax</span></span>


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="68c28-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="68c28-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="68c28-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**\_formulário de atributo de propriedade WPD \_ \_ \_ não especificado**</span><span class="sxs-lookup"><span data-stu-id="68c28-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="68c28-108">A forma dos dados da propriedade não foi especificada.</span><span class="sxs-lookup"><span data-stu-id="68c28-108">The form of the property's data is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="68c28-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**\_intervalo de \_ formulários de atributo de propriedade WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="68c28-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="68c28-110">O valor é expresso como um intervalo de valores, com um mínimo e um máximo.</span><span class="sxs-lookup"><span data-stu-id="68c28-110">The value is expressed as a range of values, with a minimum and a maximum.</span></span>

</dd> <dt>

<span data-ttu-id="68c28-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_enumeração de \_ formulário de atributo de propriedade WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="68c28-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="68c28-112">A propriedade tem uma série de valores individuais.</span><span class="sxs-lookup"><span data-stu-id="68c28-112">The property has a series of individual values.</span></span>

</dd> <dt>

<span data-ttu-id="68c28-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ \_ expressão regular de formulário de atributo \_ de propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="68c28-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="68c28-114">O valor da propriedade é uma expressão regular, não uma expressão literal.</span><span class="sxs-lookup"><span data-stu-id="68c28-114">The property value is a regular expression, not a literal expression.</span></span>

</dd> <dt>

<span data-ttu-id="68c28-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**\_identificador de \_ OJBECT do formulário de atributo de propriedade WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="68c28-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_OJBECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="68c28-116">O valor da propriedade representa um identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="68c28-116">The property value represents an object identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68c28-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="68c28-117">Remarks</span></span>

<span data-ttu-id="68c28-118">Essa enumeração é usada pela propriedade [de \_ \_ \_ formulário de atributo de propriedade WPD](attributes.md) para descrever como os dados de uma propriedade são armazenados.</span><span class="sxs-lookup"><span data-stu-id="68c28-118">This enumeration is used by the [WPD\_PROPERTY\_ATTRIBUTE\_FORM](attributes.md) property to describe how a property's data is stored.</span></span>

## <a name="requirements"></a><span data-ttu-id="68c28-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68c28-119">Requirements</span></span>



| <span data-ttu-id="68c28-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68c28-120">Requirement</span></span> | <span data-ttu-id="68c28-121">Valor</span><span class="sxs-lookup"><span data-stu-id="68c28-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="68c28-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68c28-122">Header</span></span><br/> | <dl> <span data-ttu-id="68c28-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="68c28-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68c28-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="68c28-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c28-125">**Estruturas e tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="68c28-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




