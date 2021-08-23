---
description: Descreve como um parâmetro (método ou evento) armazena seu valor.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: Enumeração WpdParameterAttributeForm (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f50665768d62d8155bd0ac9001f4ae5029766d7d5b27a942941f8f41b9492e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026744"
---
# <a name="wpdparameterattributeform-enumeration"></a>Enumeração WpdParameterAttributeForm

O tipo de enumeração [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) descreve como um parâmetro (método ou evento) armazena seu valor.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**FORMULÁRIO DE ATRIBUTO DE PARÂMETRO WPD \_ \_ NÃO \_ \_ ESPECIFICADO**
</dt> <dd>

A forma do parâmetro não é especificada.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**INTERVALO DE FORMULÁRIO \_ DE \_ ATRIBUTO DE PARÂMETRO \_ WPD \_**
</dt> <dd>

O parâmetro especifica um intervalo.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**ENUMERAÇÃO DE \_ FORMULÁRIO DE ATRIBUTO DE \_ \_ PARÂMETRO \_ WPD**
</dt> <dd>

O parâmetro é uma enumeração.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**EXPRESSÃO REGULAR \_ DE FORMULÁRIO DE ATRIBUTO \_ \_ DE \_ \_ PARÂMETRO WPD**
</dt> <dd>

O parâmetro é uma expressão regular.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**IDENTIFICADOR DE \_ OBJETO DE ATRIBUTO DE PARÂMETRO \_ \_ \_ WPD**
</dt> <dd>

O parâmetro é um identificador de objeto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

