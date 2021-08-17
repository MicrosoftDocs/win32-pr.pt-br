---
description: O tipo de enumeração WpdAttributeForm descreve como uma propriedade armazena seus valores.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Enumeração WpdAttributeForm (PortableDevice.h)
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
ms.openlocfilehash: 8366f90fe41eaa92d826f4d761fe8cdf58304f54e1f57cb074ae94d6fd9f1ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696264"
---
# <a name="wpdattributeform-enumeration"></a>Enumeração WpdAttributeForm

O **tipo de enumeração WpdAttributeForm** descreve como uma propriedade armazena seus valores.

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

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**FORMULÁRIO DE ATRIBUTO DE PROPRIEDADE WPD \_ \_ NÃO \_ \_ ESPECIFICADO**
</dt> <dd>

A forma dos dados da propriedade não é especificada.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**INTERVALO DE FORMULÁRIO \_ DO \_ ATRIBUTO DE PROPRIEDADE \_ WPD \_**
</dt> <dd>

O valor é expresso como um intervalo de valores, com um mínimo e um máximo.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**ENUMERAÇÃO DE FORMULÁRIO \_ \_ DE ATRIBUTO DE \_ \_ PROPRIEDADE WPD**
</dt> <dd>

A propriedade tem uma série de valores individuais.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**EXPRESSÃO REGULAR \_ DE FORMULÁRIO DE ATRIBUTO DE \_ \_ PROPRIEDADE \_ \_ WPD**
</dt> <dd>

O valor da propriedade é uma expressão regular, não uma expressão literal.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**IDENTIFICADOR \_ \_ \_ \_ OJBECT DO ATRIBUTO DE \_ PROPRIEDADE WPD**
</dt> <dd>

O valor da propriedade representa um identificador de objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada pela [propriedade WPD \_ PROPERTY ATTRIBUTE \_ \_ FORM](attributes.md) para descrever como os dados de uma propriedade são armazenados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




