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
# <a name="wpdattributeform-enumeration"></a>Enumeração WpdAttributeForm

O tipo de enumeração **WpdAttributeForm** descreve como uma propriedade armazena seus valores.

## <a name="syntax"></a>Syntax


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**\_formulário de atributo de propriedade WPD \_ \_ \_ não especificado**
</dt> <dd>

A forma dos dados da propriedade não foi especificada.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**\_intervalo de \_ formulários de atributo de propriedade WPD \_ \_**
</dt> <dd>

O valor é expresso como um intervalo de valores, com um mínimo e um máximo.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_enumeração de \_ formulário de atributo de propriedade WPD \_ \_**
</dt> <dd>

A propriedade tem uma série de valores individuais.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ \_ expressão regular de formulário de atributo \_ de propriedade WPD \_**
</dt> <dd>

O valor da propriedade é uma expressão regular, não uma expressão literal.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**\_identificador de \_ OJBECT do formulário de atributo de propriedade WPD \_ \_ \_**
</dt> <dd>

O valor da propriedade representa um identificador de objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela propriedade [de \_ \_ \_ formulário de atributo de propriedade WPD](attributes.md) para descrever como os dados de uma propriedade são armazenados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




